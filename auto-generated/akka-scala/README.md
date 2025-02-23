# swagger-client

BitMEX API
- API version: 1.2.0

## REST API for the BitMEX Trading Platform  [View Changelog](/app/apiChangelog)  -  #### Getting Started  Base URI: [https://www.bitmex.com/api/v1](/api/v1)  ##### Fetching Data  All REST endpoints are documented below. You can try out any query right from this interface.  Most table queries accept `count`, `start`, and `reverse` params. Set `reverse=true` to get rows newest-first.  Additional documentation regarding filters, timestamps, and authentication is available in [the main API documentation](/app/restAPI).  _All_ table data is available via the [Websocket](/app/wsAPI). We highly recommend using the socket if you want to have the quickest possible data without being subject to ratelimits.  ##### Return Types  By default, all data is returned as JSON. Send `?_format=csv` to get CSV data or `?_format=xml` to get XML data.  ##### Trade Data Queries  _This is only a small subset of what is available, to get you started._  Fill in the parameters and click the `Try it out!` button to try any of these queries.  - [Pricing Data](#!/Quote/Quote_get)  - [Trade Data](#!/Trade/Trade_get)  - [OrderBook Data](#!/OrderBook/OrderBook_getL2)  - [Settlement Data](#!/Settlement/Settlement_get)  - [Exchange Statistics](#!/Stats/Stats_history)  Every function of the BitMEX.com platform is exposed here and documented. Many more functions are available.  ##### Swagger Specification  [⇩ Download Swagger JSON](swagger.json)  -  ## All API Endpoints  Click to expand a section. 


*Automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen)*

## Requirements

Building the API client library requires:
1. Java 1.7+
2. Maven/Gradle/SBT

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>io.swagger</groupId>
  <artifactId>swagger-client</artifactId>
  <version>1.0.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "io.swagger:swagger-client:1.0.0"
```

### SBT users

```scala
libraryDependencies += "io.swagger" % "swagger-client" % "1.0.0"
```

## Getting Started

## Documentation for API Endpoints

All URIs are relative to *https://www.bitmex.com/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*APIKeyApi* | **aPIKey.get** | **GET** /apiKey | Get your API Keys.
*AnnouncementApi* | **announcement.get** | **GET** /announcement | Get site announcements.
*AnnouncementApi* | **announcement.getUrgent** | **GET** /announcement/urgent | Get urgent (banner) announcements.
*ChatApi* | **chat.get** | **GET** /chat | Get chat messages.
*ChatApi* | **chat.getChannels** | **GET** /chat/channels | Get available channels.
*ChatApi* | **chat.getConnected** | **GET** /chat/connected | Get connected users.
*ChatApi* | **chat.new** | **POST** /chat | Send a chat message.
*ExecutionApi* | **execution.get** | **GET** /execution | Get all raw executions for your account.
*ExecutionApi* | **execution.getTradeHistory** | **GET** /execution/tradeHistory | Get all balance-affecting executions. This includes each trade, insurance charge, and settlement.
*FundingApi* | **funding.get** | **GET** /funding | Get funding history.
*GlobalNotificationApi* | **globalNotification.get** | **GET** /globalNotification | Get your current GlobalNotifications.
*InstrumentApi* | **instrument.get** | **GET** /instrument | Get instruments.
*InstrumentApi* | **instrument.getActive** | **GET** /instrument/active | Get all active instruments and instruments that have expired in &lt;24hrs.
*InstrumentApi* | **instrument.getActiveAndIndices** | **GET** /instrument/activeAndIndices | Helper method. Gets all active instruments and all indices. This is a join of the result of /indices and /active.
*InstrumentApi* | **instrument.getActiveIntervals** | **GET** /instrument/activeIntervals | Return all active contract series and interval pairs.
*InstrumentApi* | **instrument.getCompositeIndex** | **GET** /instrument/compositeIndex | Show constituent parts of an index.
*InstrumentApi* | **instrument.getIndices** | **GET** /instrument/indices | Get all price indices.
*InsuranceApi* | **insurance.get** | **GET** /insurance | Get insurance fund history.
*LeaderboardApi* | **leaderboard.get** | **GET** /leaderboard | Get current leaderboard.
*LeaderboardApi* | **leaderboard.getName** | **GET** /leaderboard/name | Get your alias on the leaderboard.
*LiquidationApi* | **liquidation.get** | **GET** /liquidation | Get liquidation orders.
*OrderApi* | **order.amend** | **PUT** /order | Amend the quantity or price of an open order.
*OrderApi* | **order.cancel** | **DELETE** /order | Cancel order(s). Send multiple order IDs to cancel in bulk.
*OrderApi* | **order.cancelAll** | **DELETE** /order/all | Cancels all of your orders.
*OrderApi* | **order.cancelAllAfter** | **POST** /order/cancelAllAfter | Automatically cancel all your orders after a specified timeout.
*OrderApi* | **order.closePosition** | **POST** /order/closePosition | Close a position. [Deprecated, use POST /order with execInst: &#39;Close&#39;]
*OrderApi* | **order.getOrders** | **GET** /order | Get your orders.
*OrderApi* | **order.new** | **POST** /order | Create a new order.
*OrderBookApi* | **orderBook.getL2** | **GET** /orderBook/L2 | Get current orderbook in vertical format.
*PositionApi* | **position.get** | **GET** /position | Get your positions.
*PositionApi* | **position.isolateMargin** | **POST** /position/isolate | Enable isolated margin or cross margin per-position.
*PositionApi* | **position.transferIsolatedMargin** | **POST** /position/transferMargin | Transfer equity in or out of a position.
*PositionApi* | **position.updateLeverage** | **POST** /position/leverage | Choose leverage for a position.
*PositionApi* | **position.updateRiskLimit** | **POST** /position/riskLimit | Update your risk limit.
*QuoteApi* | **quote.get** | **GET** /quote | Get Quotes.
*QuoteApi* | **quote.getBucketed** | **GET** /quote/bucketed | Get previous quotes in time buckets.
*SchemaApi* | **schema.get** | **GET** /schema | Get model schemata for data objects returned by this API.
*SchemaApi* | **schema.websocketHelp** | **GET** /schema/websocketHelp | Returns help text &amp; subject list for websocket usage.
*SettlementApi* | **settlement.get** | **GET** /settlement | Get settlement history.
*StatsApi* | **stats.get** | **GET** /stats | Get exchange-wide and per-series turnover and volume statistics.
*StatsApi* | **stats.history** | **GET** /stats/history | Get historical exchange-wide and per-series turnover and volume statistics.
*StatsApi* | **stats.historyUSD** | **GET** /stats/historyUSD | Get a summary of exchange statistics in USD.
*TradeApi* | **trade.get** | **GET** /trade | Get Trades.
*TradeApi* | **trade.getBucketed** | **GET** /trade/bucketed | Get previous trades in time buckets.
*UserApi* | **user.cancelWithdrawal** | **POST** /user/cancelWithdrawal | Cancel a withdrawal.
*UserApi* | **user.checkReferralCode** | **GET** /user/checkReferralCode | Check if a referral code is valid.
*UserApi* | **user.communicationToken** | **POST** /user/communicationToken | Register your communication token for mobile clients
*UserApi* | **user.confirm** | **POST** /user/confirmEmail | Confirm your email address with a token.
*UserApi* | **user.confirmWithdrawal** | **POST** /user/confirmWithdrawal | Confirm a withdrawal.
*UserApi* | **user.get** | **GET** /user | Get your user model.
*UserApi* | **user.getAffiliateStatus** | **GET** /user/affiliateStatus | Get your current affiliate/referral status.
*UserApi* | **user.getCommission** | **GET** /user/commission | Get your account&#39;s commission status.
*UserApi* | **user.getDepositAddress** | **GET** /user/depositAddress | Get a deposit address.
*UserApi* | **user.getExecutionHistory** | **GET** /user/executionHistory | Get the execution history by day.
*UserApi* | **user.getMargin** | **GET** /user/margin | Get your account&#39;s margin status. Send a currency of \&quot;all\&quot; to receive an array of all supported currencies.
*UserApi* | **user.getQuoteFillRatio** | **GET** /user/quoteFillRatio | Get 7 days worth of Quote Fill Ratio statistics.
*UserApi* | **user.getWallet** | **GET** /user/wallet | Get your current wallet information.
*UserApi* | **user.getWalletHistory** | **GET** /user/walletHistory | Get a history of all of your wallet transactions (deposits, withdrawals, PNL).
*UserApi* | **user.getWalletSummary** | **GET** /user/walletSummary | Get a summary of all of your wallet transactions (deposits, withdrawals, PNL).
*UserApi* | **user.logout** | **POST** /user/logout | Log out of BitMEX.
*UserApi* | **user.minWithdrawalFee** | **GET** /user/minWithdrawalFee | Get the minimum withdrawal fee for a currency.
*UserApi* | **user.requestWithdrawal** | **POST** /user/requestWithdrawal | Request a withdrawal to an external wallet.
*UserApi* | **user.savePreferences** | **POST** /user/preferences | Save user preferences.
*UserEventApi* | **userEvent.get** | **GET** /userEvent | Get your user events


## Documentation for Models

 - [APIKey](APIKey.md)
 - [AccessToken](AccessToken.md)
 - [Affiliate](Affiliate.md)
 - [Announcement](Announcement.md)
 - [Chat](Chat.md)
 - [ChatChannel](ChatChannel.md)
 - [CommunicationToken](CommunicationToken.md)
 - [ConnectedUsers](ConnectedUsers.md)
 - [Error](Error.md)
 - [ErrorError](ErrorError.md)
 - [Execution](Execution.md)
 - [Funding](Funding.md)
 - [GlobalNotification](GlobalNotification.md)
 - [IndexComposite](IndexComposite.md)
 - [InlineResponse200](InlineResponse200.md)
 - [Instrument](Instrument.md)
 - [InstrumentInterval](InstrumentInterval.md)
 - [Insurance](Insurance.md)
 - [Leaderboard](Leaderboard.md)
 - [Liquidation](Liquidation.md)
 - [Margin](Margin.md)
 - [Order](Order.md)
 - [OrderBookL2](OrderBookL2.md)
 - [Position](Position.md)
 - [Quote](Quote.md)
 - [QuoteFillRatio](QuoteFillRatio.md)
 - [Settlement](Settlement.md)
 - [Stats](Stats.md)
 - [StatsHistory](StatsHistory.md)
 - [StatsUSD](StatsUSD.md)
 - [Trade](Trade.md)
 - [TradeBin](TradeBin.md)
 - [Transaction](Transaction.md)
 - [User](User.md)
 - [UserCommissionsBySymbol](UserCommissionsBySymbol.md)
 - [UserEvent](UserEvent.md)
 - [UserPreferences](UserPreferences.md)
 - [Wallet](Wallet.md)
 - [XAny](XAny.md)


## Documentation for Authorization

Authentication schemes defined for the API:
### apiExpires

- **Type**: API key
- **API key parameter name**: api-expires
- **Location**: HTTP header

### apiKey

- **Type**: API key
- **API key parameter name**: api-key
- **Location**: HTTP header

### apiSignature

- **Type**: API key
- **API key parameter name**: api-signature
- **Location**: HTTP header


## Author

support@bitmex.com
