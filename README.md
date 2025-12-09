# base225
Building a Simple On-Chain Wallet Monitor on Base (Python)  Today I experimented with building a lightweight wallet-monitoring tool that scans Base for incoming and outgoing transactions. The idea is to help new developers understand how easy it is to integrate Base RPC into a Python workflow.
from web3 import Web3

w3 = Web3(Web3.HTTPProvider("https://mainnet.base.org"))

address = Web3.to_checksum_address("0xYourWallet")

tx_count = w3.eth.get_transaction_count(address)
print("Transaction count:", tx_count)
This small piece of code is a gateway to building analytics dashboards, bots, or notifications.
