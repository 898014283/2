// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract AddressAuthorization {
    mapping(address => address) authorizedAddresses;

    function authorizeAddress(address originalAddress, address newAddress) public {
        authorizedAddresses[originalAddress] = newAddress;
    }

    function getAuthorizedAddress(address originalAddress) public view returns (address) {
        return authorizedAddresses[originalAddress];
    }
}