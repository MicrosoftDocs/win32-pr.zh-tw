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
# <a name="writing-a-pluggable-terminal"></a><span data-ttu-id="010fc-103">寫入可插入的終端機</span><span class="sxs-lookup"><span data-stu-id="010fc-103">Writing a Pluggable Terminal</span></span>

<span data-ttu-id="010fc-104">一般來說， (MSP 的媒體服務提供者) 會實行終端機建立。</span><span class="sxs-lookup"><span data-stu-id="010fc-104">Normally, a media service provider (MSP) implements terminal creation.</span></span> <span data-ttu-id="010fc-105">從 Windows 2000 SP1 開始，TAPI 3 包含可插入的終端機，可讓應用程式執行終端機建立。</span><span class="sxs-lookup"><span data-stu-id="010fc-105">Starting with Windows 2000 SP1, TAPI 3 includes pluggable terminals to allow an application to implement terminal creation.</span></span> <span data-ttu-id="010fc-106">如需有關使用這些終端機的詳細資訊，請參閱瞭解如何實行可 [插入的終端](implementing-pluggable-terminals.md) 機。</span><span class="sxs-lookup"><span data-stu-id="010fc-106">Please see the overview on [implementing pluggable terminals](implementing-pluggable-terminals.md) for additional information on using these terminals.</span></span>

<span data-ttu-id="010fc-107">您不應該定期使用插入式終端機，因為只有當 MSP 完全知道終端機的功能時，才能使用該終端機的完整功能。</span><span class="sxs-lookup"><span data-stu-id="010fc-107">You should not use pluggable terminals routinely because the full capabilities of a terminal will only be available when an MSP is fully aware of it.</span></span> <span data-ttu-id="010fc-108">此外，除非您已經熟悉撰寫媒體服務提供者，否則您不應該嘗試執行可插入的終端機。</span><span class="sxs-lookup"><span data-stu-id="010fc-108">Further, you should not attempt to implement pluggable terminals unless you are already familiar with writing media service providers.</span></span> <span data-ttu-id="010fc-109">相關的技術和潛在問題相當類似。</span><span class="sxs-lookup"><span data-stu-id="010fc-109">The techniques and potential problems involved are quite similar.</span></span>

<span data-ttu-id="010fc-110">在需要將非 Windows 2000 SP1 或 nonmulticast H. 323 用戶端新增至 TAPI 3 多方 SDP/IP 多播會議的會議服務器的情況下，布建特殊的插即用終端機目前存在。</span><span class="sxs-lookup"><span data-stu-id="010fc-110">Provision for a special case of pluggable terminal currently exists for the situation of a conferencing server that needs to add non-Windows 2000 SP1 or nonmulticast H.323 clients to TAPI 3 multiparty SDP/IP multicast conferences.</span></span>

 

 



