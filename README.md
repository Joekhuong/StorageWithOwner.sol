# StorageWithOwner.sol
Remix - Deploy Contract On Base Network StorageWithOwner.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract StorageWithOwner {
    uint public value;
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    function setValue(uint _value) public {
        require(msg.sender == owner, "Not owner");
        value = _value;
    }
}
