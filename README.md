// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

/**
 * @title Talent Token (TLNT)
 * @dev Talent projesi için özel olarak oluşturulmuş bir ERC-20 token.
 * Bu token, Talent doğrulama sisteminde kullanılmak üzere tasarlanmıştır.
 * Sahipler, doğrulama sürecine katkı sağlayan kullanıcılara token ödülleri verebilir.
 */
contract Talent is ERC20, Ownable {
    constructor(uint256 initialSupply) ERC20("Talent", "TLNT") {
        _mint(msg.sender, initialSupply * 10 ** decimals());
    }

    /**
     * @dev Belirli bir adrese ek token basma işlemi.
     * Yalnızca sözleşme sahibi tarafından çağrılabilir.
     * @param to Token gönderilecek adres
     * @param amount Gönderilecek miktar
     */
    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }
}

