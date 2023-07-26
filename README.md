## StreamPayments - Real-Time Money Streaming Protocol on Solana

StreamPayments is an innovative protocol and suite of Software Development Kits (SDKs) designed to enable real-time money streaming on the Solana blockchain. The protocol facilitates seamless and continuous money transfers from one user to another at customizable intervals, with a minimum resolution of up to one second. By leveraging the high-performance capabilities of the Solana blockchain, StreamPayments empowers developers and users to implement efficient and low-cost real-time payment solutions.


## Use Cases:

**Payroll**: StreamPayments can revolutionize traditional payroll systems by allowing employers to stream hourly wages to their employees in real-time. Instead of waiting for a fixed payday, employees can receive their earnings continuously throughout the workday, providing them with greater financial flexibility and access to their funds when they need them most.

**- Hourly Wages**: For gig economy workers, freelancers, or contractors who are compensated based on hourly rates, StreamPayments offers a convenient way to receive payments as they complete tasks or work on projects. This ensures that they can access their earnings in real-time and manage their cash flow efficiently.

**- RSU/ESOP/Token Distribution/Vesting**: In the realm of employee incentives and equity compensation, StreamPayments can facilitate the real-time distribution of Restricted Stock Units (RSUs), Employee Stock Ownership Plans (ESOPs), or tokens. Employees can receive their vested shares or tokens continuously based on predefined vesting schedules, aligning their interests with the company's long-term performance.

**- Subscriptions**: StreamPayments can be integrated into subscription-based services, allowing users to pay for their subscriptions in real-time at regular intervals. This ensures that users have uninterrupted access to the services they subscribe to and offers businesses a seamless alternative to traditional billing cycles.

**- SIPs (Systematic Investment Plans)**:
For investment platforms or wealth management applications, StreamPayments can enable users to set up SIPs, where a fixed amount of money is invested at regular intervals into various financial instruments. This automation of investments provides a disciplined approach to wealth creation and takes advantage of market volatility through rupee-cost averaging.

**- EMIs (Equated Monthly Installments):** In the context of loans and financing, StreamPayments can streamline EMI payments by allowing borrowers to make real-time installment payments at predefined intervals. This promotes timely repayments and reduces the chances of default, benefiting both borrowers and lenders.

**- Sponsorships:** For content creators, artists, or athletes who rely on sponsorships, StreamPayments can offer real-time sponsorship funding. Sponsors can continuously stream funds to their beneficiaries, supporting their ongoing projects, content creation, or sports activities.
In each of these use cases, StreamPayments brings several advantages, including:

**- Real-time access to funds**: Recipients can access their funds immediately, enhancing financial liquidity and flexibility.
Seamless integration: The protocol's SDKs make it easy for businesses to integrate real-time money streaming into their existing applications.

**- Cost-effectiveness**: StreamPayments leverages the efficiency of the Solana blockchain, resulting in low transaction costs for both senders and receivers.

**- Trust and security**: The protocol operates in a non-custodial manner, ensuring that users have complete control and ownership of their funds at all times.

**- Automation and convenience**: StreamPayments automates the payment process, reducing manual intervention and providing a hassle-free experience for users.

Overall, StreamPayments presents an innovative solution for various financial scenarios, transforming the way money is distributed and managed in real-time on the Solana blockchain.


### Features of StreamPayments Protocol and SDKs:

Some payment streams like ESOPs would need to be prepaid because employees would need assurance that some set of tokens are locked up in an escrow that will be given to them on the vesting schedule. Other streams like payroll and subscriptions will be unbounded - senders can top up the escrow to keep them running. Both these use cases are supported. Read more about these here.

1. **Prepaid and Unbounded Payment Streams**:

   - The protocol supports both prepaid and unbounded payment streams. Prepaid streams are suitable for cases like ESOPs where tokens are locked up in escrow and distributed on a vesting schedule.
   - Unbounded streams are used for scenarios like payroll and subscriptions, where senders can continuously top up the escrow to keep the payments running.

3. **Support for Cliffs**:
   - The protocol enables the vesting of RSUs, ESOPs, and tokens with cliffs. Cliffs are periods where no vesting occurs, and the protocol accommodates such conditions in the payment schedules.

4. **Cancellable Streams**:
   - Streams can be canceled based on configurable options. The protocol allows defining rules for who can cancel a stream and when they can do it.

5. **Pausable Streams**:
   - Streams can be paused and resumed as needed. This feature is particularly useful for payroll software that requires employees to check in and check out, allowing control over when payments are made.

6. **Unbounded Streams Solvency Detection**:
   - The protocol includes mechanisms to detect insolvency in unbounded streams where timely top-ups are essential. If a stream becomes insolvent due to insufficient funds, the sender can be penalized.

**Components of** **Stream**Payments:

1. **Stream**Payments **Program**:
   - The on-chain program maintains the state of all payment streams on the Solana blockchain. It serves as the core of the **Stream**Payments ecosystem and facilitates interaction with other on-chain programs through Cross-Program Invocation (CPI).

2. **Stream**Payments **Inspector**:
   - An off-chain software that monitors the on-chain program and identifies insolvent streams. When an insolvent stream is detected, the inspector cancels the stream, penalizing bad actors in the system. Users running the inspector can earn rewards for their contributions.

3. **Client SDKs - Typescript**:
   - The Typescript client SDK allows developers to interact with the on-chain StreamPayments program efficiently. Developers can use this SDK to build Typescript applications and integrate payment streams seamlessly. It is compatible with various environments, including browsers and native environments like React Native.

4. **Dashboard**:
   - The StreamPayments Dashboard is a web interface provided by StreamPayments, allowing users to create and manage their payment streams conveniently. Users can connect their wallets to the dashboard and initiate real-time money streaming for various use cases. It provides a user-friendly way to create, monitor, and control payment streams.

The **Stream**Payments protocol and SDKs offer a comprehensive solution for implementing real-time money streaming on the Solana blockchain, catering to various use cases, from employee compensation to subscriptions and sponsorships. With support for prepaid and unbounded streams, vesting cliffs, cancellation, and pause features, StreamPayments provides flexibility, security, and ease of use to both developers and users.


### Features

**Prepaid and unbounded payment streams**: Some payment streams like ESOPs would need to be prepaid because employees would need assurance that some set of tokens are locked up in an escrow that will be given to them on the vesting schedule. Other streams like payroll and subscriptions will be unbounded - senders can top up the escrow to keep them running. Both these use cases are supported. Read more about these here.

**Support for cliffs**: Vesting of RSUs/ESOPs/Tokens involving cliffs is supported.

**Cancellable streams**: Streams are cancellable. Various different options are available to configure who is allowed to cancel and when.

**Pausable streams**: Streams can be paused and resumed. This is useful for payroll software which requires employees to check in and check out. Options are available to configure who can pause and when.

**Unbounded streams solvency detection**: Unbounded streams may become insolvent if not topped up timely. There needs to be a way to identify them as quickly as possible and penalize the sender of that stream somehow. Read more about insolvency here.


## Protocol

#### **Stream**Payments program

A Solana on-chain program that maintains the state of all the streams on-chain. Other Solana on-chain programs can interact with it directly using Cross-Program Invocation (CPI for short).

#### **Stream**Payments program

An off-chain software that monitors the on-chain program and cancels streams when they become insolvent. Anyone can run this software and earn rewards for finding insolvent streams and penalizing bad actors in the ecosystem.

#### **Stream**Payments Inspector

An off-chain software that monitors the on-chain program and cancels streams when they become insolvent. Anyone can run this software and earn rewards for finding insolvent streams and penalizing bad actors in the ecosystem.


### **Stream**Payments Dashboard

Dashboard is a web interface maintained by StreamPayments where you can create and manage all of your payment streams. Just connect your wallet and start sending and receiving money real-time. The dashboard is built using the typescript client SDK.

You can create a StreamPayment on the dashboard to understand the various parameters needed when creating a stream.


### Client SDKs

**- Typescript client SDK**: A typescript SDK to interact with the on-chain StreamPayments program. Developers would use this typically when they want to create a typescript app and integrate streams into that. It's compatible with browsers and native environments (like React Native).


### License

Licensed under MIT license (LICENSE or opensource.org/licenses/MIT)
