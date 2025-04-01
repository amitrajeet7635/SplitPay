// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract PaymentSplitter {
    // Array of payable recipient addresses
    address payable[3] recipients = [
        payable(0x1111111111111111111111111111111111111111),
        payable(0x2222222222222222222222222222222222222222),
        payable(0x3333333333333333333333333333333333333333)
    ];
    
    // Corresponding percentage shares for each recipient
    uint256[3] shares = [40, 30, 30]; // Percentage-based split
    
    /**
     * @dev Function to distribute received Ether among the recipients
     * The distribution is based on the predefined shares
     * The function must be called with a payable transaction
     */
    function distribute() external payable {
        uint256 totalReceived = msg.value; // Get the total amount sent to the contract
        
        // Loop through recipients and transfer their respective share
        for (uint256 i = 0; i < recipients.length; i++) {
            uint256 payment = (totalReceived * shares[i]) / 100; // Calculate individual share
            recipients[i].transfer(payment); // Send payment to recipient
        }
    }
}
