# FID-Notes

## 1. Preface

- Derivative & Subject Matter

  有基本变量派生的产品，价格可以依赖于**任何变量**

### 1.1 交易所市场 Exchange Market

- 交易所标准化之后的衍生品
  - 期货合约（将至合约 to-arrive contract）：直接交易合约的替代
  - 期权合约：外汇、期货合约、股票和股指
- 电子交易
  - 替代交易所的公开喊价系统（open-outcry system）
  - 算法交易

### 1.2 场外市场 Over-The-Counter Market OTC 

- participants：
  - 两家金融机构或金融机构P和其客户
  - 金融机构：流行产品的做市商market maker
    - 提供bid price和offer price
- 合约灵活但是存在对手信用风险
- 市场规模：OTC远大于交易所
  - OTC交易产品的面值和价值区分

### 1.3 远期合约 Forward Contract

- 简单衍生品

  在未来某一时刻以约定的价格买入或者卖出某一产品的合约

- 与即期合约Spot Contract对应

- Long Position and Short Position: Buyer and Seller

- 流行产品（标的物）：外汇

  - Future Price - Spot Price - Interest Rates of two currencies.
  - Hedge Foreign Currency Risk

#### 1.3.1 Payoffs from Forward Contracts

- Pay off for who holds ==Long Position==: 
  $$
  S_T - K
  $$

  - K: delivery price 合约规定的交割时的价格
  - $$S_T$$: 合约到期时的市场价格
  - LP必须以==价格K==买入==价值 (Worth)$$S_T$$==的asset

- Pay off for who holds ==Short Position==: 
  $$
  K - S_T
  $$
  
- 如果签订合约无需费用：Zero-Sum Game

  <img src="FID-Notes.assets/image-20201208181107071.png" alt="image-20201208181107071" style="zoom: 33%;" />

#### 1.3.2 Forward Prices and Spot Prices

考虑远期利息

### 1.4 期货合约 Futures Contract

与Forward Contract区别：trade on exchange

- Standardized
- 不知道交易对手
- Mechanism

### 1.5 期权 Options

- on exchange and OTC

- 期权合约往往是有费用的、持有者可以不行权

- Types:

  - Call Option 看涨期权/认购期权

    在VT能以特定价格==买入==资产 

  - Put Option 看跌期权/认沽期权

    在VT能以特定价格==卖出==资产 

  - 合约中的特定价格：Exercise Price / Strike Price

  - VT：到期日或者期限 （Expiration Date / Maturity）
  
- American Option:

  - 在Expiration Date之前的任何时间都可以行权
  - 居多

- European Option:

  - 只能在Expiration Date行权

- Properties
  - Exercise Price goes up; Call Option Price decreases;
  - Exercise Price goes up; Put Option Price increases;
- Participants:
  1. Buyers of Calls
  2. Sellers of Calls
  3. Buyers of Puts
  4. Sellers of Puts

## 1.6 交易员的类型 Traders

- Hedger 

  利用衍生平合约来减低自己面临的由于市场变化产生的风险

- Speculator

  利用衍生品对今后的市场变量走向下赌注

- Arbitrator

  在两个或者多个工具中进行相互抵消的交易来锁定收益

## 1.7 对冲交易员 Hedger 

### 1.7.1 远期对冲 Hedging Using Forward Contract

- Options帮助锁定收益/支出	
  - 不对冲时收益可能更好或更差
  - 对冲为了降低风险，实际结果并不能更好

### 1.7.2 期权对冲 Hedging Using Options

- 实际市场价格低于期权约定价格时，行权避免过高损失。

  ![image-20201221162808446](FID-Notes.assets/image-20201221162808446.png)

### 1.7.3 比较

- Forward: 通过设定买入和卖出的资产价格进行对冲
- Options: 提供价格保险

## 1.8 Speculators

建立postion，对资产的价格上涨或者下跌下注

### 1.8.1 Speculation Using Futures

- 期货市场可以使投机者取得杠杆，少量的保证金就能建立大的投机Position

### 1.8.2 Speculation Using Options

- 与即期市场比，放大收益，同时可能损失全部投资

  ![image-20201221170247618](FID-Notes.assets/image-20201221170247618.png)

### 1.8.3 比较

- 同为杠杆
  - 期货放大损失和收益
  - 期权最大损失为期权承约费用

## 1.9 套利者 ArbitraGEURS

- 通过同时进行两种或跟多的交易来锁定无风险盈利
  - 资产的futures价格和即期市场价格不协调时产生套利机会
- 套利行为会减少套利机会
- 由于套利者的存在，大多是金融市场中只会存在很小的套利机会
  - 大多数Futures, Forwards Contract, Options都是无套利机会的。

## 1.10 Dangers

- 衍生品的复杂性使得instrument目的的不确定性
  - trader有意无意或成为投机者
- 控制衍生品的交易机制
  - 用于指定目的
  - 建立风险额度
- "What can go wrong?"
- "If it does go wrong, how much will we lose?"



# 2. Futures Markets and Central  Counterparties <br> 期货市场和中央交易对手

## 2.1 Background  

- 期货价格也是买房和卖方的供求关系体现

### 2.1.1 Closing Out Positions 平仓

- Closing out a position means entering into the opposite trade to the original one.

  平仓就是承约一个与初始交易position相反的Position

