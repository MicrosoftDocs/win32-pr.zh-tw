---
title: 啟用延伸的錯誤資訊
description: 啟用遠端程序呼叫的延伸錯誤資訊 (RPC) 。
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183763"
---
# <a name="enabling-extended-error-information"></a><span data-ttu-id="2d7f5-103">啟用延伸的錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="2d7f5-103">Enabling Extended Error Information</span></span>

<span data-ttu-id="2d7f5-104">若要啟用延伸錯誤資訊，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="2d7f5-104">To enable extended error information, take the following steps:</span></span>

<span data-ttu-id="2d7f5-105">使用 gpedit.msc 介面開啟本機電腦原則。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-105">Open the local machine policy using the gpedit.msc interface.</span></span>

<span data-ttu-id="2d7f5-106">流覽至位於 [電腦設定]/[系統管理範本/系統/遠端程序呼叫/Rpc 疑難排解支援/傳播延伸錯誤資訊的原則</span><span class="sxs-lookup"><span data-stu-id="2d7f5-106">Navigate to the policy located at Computer Configuration/Administrative Templates/System/Remote Procedure Call/Rpc Troubleshooting Support/Propagation of extended error information</span></span>

<span data-ttu-id="2d7f5-107">啟用原則，並將 **擴充錯誤資訊** 的欄位傳播設定為 [開啟]。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-107">Enable the policy, and set the field **Propagation of extended error information** to "On".</span></span>

<span data-ttu-id="2d7f5-108">此程式會針對電腦上的所有處理常式，開啟的延伸錯誤資訊的傳播。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-108">This process turns the propagation of extended error information on for all processes on the machine.</span></span>

<span data-ttu-id="2d7f5-109">若只要在電腦上啟用特定處理常式的延伸錯誤資訊，或只針對電腦上的特定處理常式停用它，請使用 **Off with 例外** 狀況，或使用 **with 例外** 狀況選項。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-109">To enable extended error information for only certain processes on a computer, or to disable it for only certain processes on the computer, use the **Off with exceptions** or **On with exceptions** options.</span></span> <span data-ttu-id="2d7f5-110">這兩個選項都會使用「欄位 **延伸的錯誤資訊」例外** 狀況，來指定哪些處理常式具有預設設定，而哪些處理常式的預設值相反。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-110">Both options use the field **Extended Error Information Exceptions** to specify which processes have the default setting, and which processes have the opposite of the default setting.</span></span> <span data-ttu-id="2d7f5-111">**擴充的錯誤資訊例外** 狀況包含進程名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-111">**Extended Error Information Exceptions** contains a list of process names.</span></span>

<span data-ttu-id="2d7f5-112">如果處理常式的命令列是以 **延伸的錯誤資訊例外** 狀況中的字串開始，進程將會收到預設設定的相反設定。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-112">If the command line of a process starts with a string that is in the **Extended Error Information Exceptions**, the process will receive the opposite of the default setting.</span></span> <span data-ttu-id="2d7f5-113">例如，如果您想要讓電腦上的所有處理常式傳播延伸的錯誤資訊（lsass 和稱為 **Secure Server** 的程式除外），請將 **擴充錯誤資訊的傳播** 設為 **on，但有例外** 狀況，並在 [ **擴充錯誤資訊例外** ] 欄位中指定下列字串： lsass "Secure Server"。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-113">For example, if you want all the process on your computer to propagate extended error information, except for lsass and the process called **Secure Server**, set the **Propagation of extended error information** to **On with exceptions**, and specify in the **Extended Error Information Exceptions** field the following string: lsass "Secure Server".</span></span>

<span data-ttu-id="2d7f5-114">字串可以用雙引號括住，但如果字串中沒有空格，則可以選擇性地執行此動作。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-114">Strings can be enclosed with double quotes, but doing so is optional if there are no spaces in the string.</span></span> <span data-ttu-id="2d7f5-115">此外，也可以指定進程命令列的開頭。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-115">Also, the beginning of the process command line can be specified.</span></span> <span data-ttu-id="2d7f5-116">例如，如果在 [**擴充錯誤資訊**] 欄位的 [傳播] 中指定 **Off** ，而且在 [**擴充錯誤資訊例外** 狀況] 欄位中指定了下列內容： win。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-116">For example, if **Off with exceptions** is specified in the **Propagation of extended error information** field, and in the **Extended Error Information Exceptions** field the following is specified: win.</span></span>

<span data-ttu-id="2d7f5-117">開頭為 "win" 的每個進程都會傳播擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-117">Each process that begins with "win" propagates extended error information.</span></span> <span data-ttu-id="2d7f5-118">例如，在許多電腦上，這些處理常式會 winlogon.exe 並 WINWORD.EXE。</span><span class="sxs-lookup"><span data-stu-id="2d7f5-118">On many computers, for example, those processes would be winlogon.exe and WINWORD.EXE.</span></span>

 

 




