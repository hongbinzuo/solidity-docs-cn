Solidity
========

.. image:: logo.svg
    :width: 120px
    :alt: Solidity logo
    :align: center

Solidity是一门面向合约的、为实现智能合约而生的高级编程语言。这门语言受C++，Python和Javascript语言的影响，设计的目的是能在以太坊虚拟机（EVM）上运行。

Solidity是静态类型语言，支持继承、库和复杂的用户定义类型等特性。

下面您将会看到，使用Solidity语言，可以为投票、众筹、秘密竞价（盲拍）、多重签名的钱包以及其他事务创建合约。

.. note::
    目前尝试Solidity编程的最好的方式是使用
    `Remix <https://remix.ethereum.org/>`_
    （需要一点时间加载，请耐心等待）。

.. warning::
    因为软件是人写的，就会有bug，所以，创建智能合约也应该遵循软件开发领域熟知的最佳实践。这些实践包括代码审查、测试、审计和正确性证明。

    同时也要注意：代码的用户有时比作者更有信心。
    最后，区块链本身有些东西需要留意，请参考 :ref:`security_considerations`.

翻译
------------

本文档被社区志愿者翻译成多种语言，但是英语版本作为主要参考。

* `Simplified Chinese <http://solidity-documentation-simplified-chinese.rtfd.io/>`_
* `Spanish <https://solidity-es.readthedocs.io>`_
* `Russian <https://github.com/ethereum/wiki/wiki/%5BRussian%5D-%D0%A0%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE-%D0%BF%D0%BE-Solidity>`_ (有点过时了)


有用的链接
------------

* `Ethereum <https://ethereum.org>`_

* `变更日志 <https://github.com/ethereum/solidity/blob/develop/Changelog.md>`_

* `故事需求列表 <https://www.pivotaltracker.com/n/projects/1189488>`_

* `源代码 <https://github.com/ethereum/solidity/>`_

* `Ethereum Stackexchange <https://ethereum.stackexchange.com/>`_

* `Gitter聊天 <https://gitter.im/ethereum/solidity/>`_

可用的Solidity集成
-------------------------------

* `Remix <https://remix.ethereum.org/>`_
    基于浏览器的IDE，集成了编译器和Solidity运行时环境，不需要服务端组件。

* `IntelliJ IDEA plugin <https://plugins.jetbrains.com/plugin/9475-intellij-solidity>`_
    IntelliJ IDEA的Solidity插件（以及其他所有的JetBrains IDEs）

* `Visual Studio Extension <https://visualstudiogallery.msdn.microsoft.com/96221853-33c4-4531-bdd5-d2ea5acc4799/>`_
    Microsoft Visual Studio的Solidity插件，包含Solidity编译器。

* `Package for SublimeText — Solidity language syntax <https://packagecontrol.io/packages/Ethereum/>`_
    SublimeText编辑器的语法高亮包。

* `Etheratom <https://github.com/0mkara/etheratom>`_
    Atom编辑器的插件，支持高亮、编译和运行时环境（后端节点，虚拟机兼容）。

* `Atom Solidity Linter <https://atom.io/packages/linter-solidity>`_
    Plugin for the Atom editor that provides Solidity linting.

* `Atom Solium Linter <https://atom.io/packages/linter-solium>`_
    Configurable Solidty linter for Atom using Solium as a base.

* `Solium <https://github.com/duaraghav8/Solium/>`_
    Linter to identify and fix style and security issues in Solidity.
    
* `Solhint <https://github.com/protofire/solhint>`_
    Solidity linter that provides security, style guide and best practice rules for smart contract validation.

* `Visual Studio Code extension <http://juan.blanco.ws/solidity-contracts-in-visual-studio-code/>`_
    Solidity plugin for Microsoft Visual Studio Code that includes syntax highlighting and the Solidity compiler.

* `Emacs Solidity <https://github.com/ethereum/emacs-solidity/>`_
    Plugin for the Emacs editor providing syntax highlighting and compilation error reporting.

* `Vim Solidity <https://github.com/tomlion/vim-solidity/>`_
    Plugin for the Vim editor providing syntax highlighting.

* `Vim Syntastic <https://github.com/scrooloose/syntastic>`_
    Plugin for the Vim editor providing compile checking.

Discontinued:

* `Mix IDE <https://github.com/ethereum/mix/>`_
    Qt based IDE for designing, debugging and testing solidity smart contracts.

* `Ethereum Studio <https://live.ether.camp/>`_		
    Specialized web IDE that also provides shell access to a complete Ethereum environment.

Solidity Tools
--------------

* `Dapp <https://dapp.readthedocs.io>`_
    Build tool, package manager, and deployment assistant for Solidity.

* `Solidity REPL <https://github.com/raineorshine/solidity-repl>`_
    Try Solidity instantly with a command-line Solidity console.

* `solgraph <https://github.com/raineorshine/solgraph>`_
    Visualize Solidity control flow and highlight potential security vulnerabilities.

* `evmdis <https://github.com/Arachnid/evmdis>`_
    EVM Disassembler that performs static analysis on the bytecode to provide a higher level of abstraction than raw EVM operations.

* `Doxity <https://github.com/DigixGlobal/doxity>`_
    Documentation Generator for Solidity.

Third-Party Solidity Parsers and Grammars
-----------------------------------------

* `solidity-parser <https://github.com/ConsenSys/solidity-parser>`_
    Solidity parser for JavaScript

* `Solidity Grammar for ANTLR 4 <https://github.com/federicobond/solidity-antlr4>`_
    Solidity grammar for the ANTLR 4 parser generator

Language Documentation
----------------------

On the next pages, we will first see a :ref:`simple smart contract <simple-smart-contract>` written
in Solidity followed by the basics about :ref:`blockchains <blockchain-basics>`
and the :ref:`Ethereum Virtual Machine <the-ethereum-virtual-machine>`.

The next section will explain several *features* of Solidity by giving
useful :ref:`example contracts <voting>`
Remember that you can always try out the contracts
`in your browser <https://remix.ethereum.org>`_!

The last and most extensive section will cover all aspects of Solidity in depth.

If you still have questions, you can try searching or asking on the
`Ethereum Stackexchange <https://ethereum.stackexchange.com/>`_
site, or come to our `gitter channel <https://gitter.im/ethereum/solidity/>`_.
Ideas for improving Solidity or this documentation are always welcome!

Contents
========

:ref:`Keyword Index <genindex>`, :ref:`Search Page <search>`

.. toctree::
   :maxdepth: 2

   introduction-to-smart-contracts.rst
   installing-solidity.rst
   solidity-by-example.rst
   solidity-in-depth.rst
   security-considerations.rst
   using-the-compiler.rst
   metadata.rst
   abi-spec.rst
   julia.rst
   style-guide.rst
   common-patterns.rst
   bugs.rst
   contributing.rst
   frequently-asked-questions.rst
