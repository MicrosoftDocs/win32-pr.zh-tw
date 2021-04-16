---
description: 一般來說， (MSP 的媒體服務提供者) 會實行終端機建立。
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: 寫入可插入的終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511868"
---
# <a name="writing-a-pluggable-terminal"></a>寫入可插入的終端機

一般來說， (MSP 的媒體服務提供者) 會實行終端機建立。 從 Windows 2000 SP1 開始，TAPI 3 包含可插入的終端機，可讓應用程式執行終端機建立。 如需有關使用這些終端機的詳細資訊，請參閱瞭解如何實行可 [插入的終端](implementing-pluggable-terminals.md) 機。

您不應該定期使用插入式終端機，因為只有當 MSP 完全知道終端機的功能時，才能使用該終端機的完整功能。 此外，除非您已經熟悉撰寫媒體服務提供者，否則您不應該嘗試執行可插入的終端機。 相關的技術和潛在問題相當類似。

在需要將非 Windows 2000 SP1 或 nonmulticast H. 323 用戶端新增至 TAPI 3 多方 SDP/IP 多播會議的會議服務器的情況下，布建特殊的插即用終端機目前存在。

 

 



