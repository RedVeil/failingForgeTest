# failingForgeTest

1. I had to run `npm install --force-legacy-deps` since normal `npm install` failed for me.
2. I ran `forge init --force` in the root of the project.
3. I navigated into `/lib` and ran `git clone --recursive https://github.com/brockelmore/forge-std` 
4. Back in the project root `forge build`

The build failed with:
```
Error: 
   0: Compiler run failed
      /home/leon/failingForgeTest/contracts/compound/strategies/BeefyERC4626.sol:2:1: ParserError: Source file requires different compiler version (current compiler is 0.7.6+commit.7338295f.Linux.g++) - note that nightly builds are considered to be strictly less than the released version
      pragma solidity 0.8.10;
      ^---------------------^
      

      /home/leon/failingForgeTest/contracts/utils/ERC4626.sol:2:1: ParserError: Source file requires different compiler version (current compiler is 0.7.6+commit.7338295f.Linux.g++) - note that nightly builds are considered to be strictly less than the released version
      pragma solidity >=0.8.0;
      ^----------------------^
      

      /home/leon/failingForgeTest/contracts/utils/FixedPointMathLib.sol:2:1: ParserError: Source file requires different compiler version (current compiler is 0.7.6+commit.7338295f.Linux.g++) - note that nightly builds are considered to be strictly less than the released version
      pragma solidity >=0.8.0;
      ^----------------------^
      

      /home/leon/failingForgeTest/contracts_forge/FusePoolDirectory.t.sol:9:1: ParserError: Source "/home/leon/failingForgeTest/contracts/FusePoolDirectory.sol" not found: File not found.
      import "../contracts/FusePoolDirectory.sol";
      ^------------------------------------------^
      

      /home/leon/failingForgeTest/node_modules/@rari-capital/solmate/src/test/utils/mocks/MockERC20.sol:2:1: ParserError: Source file requires different compiler version (current compiler is 0.7.6+commit.7338295f.Linux.g++) - note that nightly builds are considered to be strictly less than the released version
      pragma solidity >=0.8.0;
      ^----------------------^
      

      /home/leon/failingForgeTest/node_modules/@rari-capital/solmate/src/tokens/ERC20.sol:2:1: ParserError: Source file requires different compiler version (current compiler is 0.7.6+commit.7338295f.Linux.g++) - note that nightly builds are considered to be strictly less than the released version
      pragma solidity >=0.8.0;
      ^----------------------^
      

      /home/leon/failingForgeTest/node_modules/@rari-capital/solmate/src/utils/SafeTransferLib.sol:2:1: ParserError: Source file requires different compiler version (current compiler is 0.7.6+commit.7338295f.Linux.g++) - note that nightly builds are considered to be strictly less than the released version
      pragma solidity >=0.8.0;
      ^----------------------^
 ```

I used once node v14.19.0 and npm 8.4.1 and the other time node v16.13.2 with npm 8.1.2.
Running all on Linux Ubuntu 20.04

If you need any other informations please let me know :)
