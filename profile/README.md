### What is 0slot?

Welcome to **0slot** – The Premium Solana Transaction Acceleration Service. Built by traders, for traders. As active Solana traders ourselves, we've experienced the frustration of transaction delays and execution failures firsthand. Our team doesn't just understand Solana transactions – we operate some of the top-performing arbitrage bots on the network. This hands-on expertise has allowed us to master the art and science of transaction execution, optimization, and timing.

We created **0slot** to address these pain points, not only to solve our own challenges but also to empower the entire trading community with the same advantages we've developed for our operations. Leveraging our specialized knowledge, we ensure your trades are executed with exceptional speed and reliability. Let us handle the technical complexities of transaction delivery so you can focus on what matters most – making better trading decisions. **From traders, for traders** (从交易者，为交易者) – that's the **0slot** promise.

---

### Pricing & Rate Limits

| **Plan**       | **Trial (first week)** | **Entry** | **Intermediate** | **Advanced** |
|-----------------|------------------------|-----------|-------------------|--------------|
| **Billed per month** | $0                     | $280      | $700              | $1400        |
| **Billed annually**  | $0                     | $3200     | $8100             | $16000       |
| **TPS**              | 5 TPS                  | 5 TPS     | 20 TPS            | 50 TPS       |
| **SWQoS**            | Dedicated SWQoS        | Dedicated SWQoS | Dedicated SWQoS | Dedicated SWQoS |
| **Transaction Tip**  | 0.001 SOL             | 0.001 SOL | 0.001 SOL        | 0.001 SOL   |

---

### Quickstart: `staked_conn`

The `staked_conn` interface is similar to the RPC interface, primarily providing the `sendTransaction` method, which directly connects to our validator node.

#### When calling the `sendTransaction` method of `staked_conn`, please note:
- A maximum of **5 calls per second** is allowed.
- You need to transfer an amount **greater than or equal to 0.001 SOL** to one of the following accounts:
  - `6fQaVhYZA4w3MBSXjJ81Vf6W1EDYeUPXpgVQ6UQyU1Av` (0slot_dot_trade.sol)
  - `4HiwLEP2Bzqj3hM2ENxJuzhcPCdsafwiet3oGkMkuQY4`(0slot_dot_trade_tip15.sol)
  - `7toBU3inhmrARGngC7z6SjyP85HgGMmCTEwGNRAcYnEK`(0slot_dot_trade_tip16.sol)
  - `8mR3wB1nh4D6J9RUCugxUpc6ya8w38LPxZ3ZjcBhgzws`(0slot_dot_trade_tip17.sol)
  - `6SiVU5WEwqfFapRuYCndomztEwDjvS5xgtEof3PLEGm9`(0slot_dot_trade_tip18.sol)
  - `TpdxgNJBWZRL8UXF5mrEsyWxDWx9HQexA9P1eTWQ42p`(0slot_dot_trade_tip19.sol)
  - `D8f3WkQu6dCF33cZxuAsrKHrGsqGP2yvAHf8mX6RXnwf`(0slot_dot_trade_tip20.sol)
  - `GQPFicsy3P3NXxB5piJohoxACqTvWE9fKpLgdsMduoHE`(0slot_dot_trade_tip21.sol)
  - `Ey2JEr8hDkgN8qKJGrLf2yFjRhW7rab99HVxwi5rcvJE`(0slot_dot_trade_tip22.sol)
  - `4iUgjMT8q2hNZnLuhpqZ1QtiV8deFPy2ajvvjEpKKgsS`(0slot_dot_trade_tip23.sol)
  - `3Rz8uD83QsU8wKvZbgWAPvCNDU6Fy8TSZTMcPm3RB6zt`(0slot_dot_trade_tip24.sol)

#### Example for `cmd: curl`:
```bash
curl -X POST 'https://ny.0slot.trade?api-key=$TOKEN' \
-d '{
    "jsonrpc": "2.0",
    "id": $UUID,
    "method": "sendTransaction",
    "params": [ 
        "<base64_encoded_tx>",
        { "encoding": "base64" }
    ] 
}'
```

#### For better performance and faster speeds, you can test and select the most suitable IP to use:
- **New York**: `ny.0slot.trade`
- **Frankfurt**: `de.0slot.trade`
- **Amsterdam**: `ams.0slot.trade`
- **Tokyo**: `jp.0slot.trade`
- **Los Angeles**: `la.0slot.trade`

---

### Special Error Codes

1. **API Key Expired**:
   ```json
   {"id":"1","jsonrpc":"2.0","error":{"code":403,"message":"API key has expired"}}
   ```

2. **Non-sendTransaction Method**:
   ```json
   {"id":"1","jsonrpc":"2.0","error":{"code":403,"message":"Invalid method"}}
   ```

3. **Rate Limit Exceeded**:
   ```json
   {"id":"1","jsonrpc":"2.0","error":{"code":419,"message":"Rate limit exceeded"}}
   ```

---

### Example

Add an instruction to the Transaction (preferably inserted at the beginning):
```javascript
transaction.addInstruction(SystemProgram.transfer(fromPublicKey, '6fQaVhYZA4w3MBSXjJ81Vf6W1EDYeUPXpgVQ6UQyU1Av', 1000000));
```

We hope the above information helps you better understand and use the `staked_conn` interface. If you have any questions, please feel free to contact our support team.

---

### Contact

If you want to create a free account, contact sales, or have any inquiries, please reach out to us via **Discord** or **X**:
- **Discord**: [https://discord.com/invite/r6VT48Zk](https://discord.com/invite/r6VT48Zk)  
  *(If this link has expired, please add me using the username `kurt0slot`)*
- **X**: [https://x.com/0slot_trade](https://x.com/0slot_trade)

---

### More Tip Accounts:
- `DiTmWENJsHQdawVUUKnUXkconcpW4Jv52TnMWhkncF6t`(0slot_dot_trade_tip1.sol)
- `HRyRhQ86t3H4aAtgvHVpUJmw64BDrb61gRiKcdKUXs5c`(0slot_dot_trade_tip2.sol)
- `7y4whZmw388w1ggjToDLSBLv47drw5SUXcLk6jtmwixd`(0slot_dot_trade_tip6.sol)
- `J9BMEWFbCBEjtQ1fG5Lo9kouX1HfrKQxeUxetwXrifBw`(0slot_dot_trade_tip7.sol)
- `8U1JPQh3mVQ4F5jwRdFTBzvNRQaYFQppHQYoH38DJGSQ`(0slot_dot_trade_tip8.sol)
- `Eb2KpSC8uMt9GmzyAEm5Eb1AAAgTjRaXWFjKyFXHZxF3`(0slot_dot_trade_tip3.sol)
- `FCjUJZ1qozm1e8romw216qyfQMaaWKxWsuySnumVCCNe`(0slot_dot_trade_tip5.sol)
- `ENxTEjSQ1YabmUpXAdCgevnHQ9MHdLv8tzFiuiYJqa13`(0slot_dot_trade_tip9.sol)
- `6rYLG55Q9RpsPGvqdPNJs4z5WTxJVatMB8zV3WJhs5EK`(0slot_dot_trade_tip10.sol)
- `Cix2bHfqPcKcM233mzxbLk14kSggUUiz2A87fJtGivXr`(0slot_dot_trade_tip12.sol)

---

We look forward to helping you optimize your Solana trading experience! 🚀
