---
description: InstallFinalize 動作會執行腳本，其中包含自安裝開始或執行 InstallExecute 或 InstallExecuteAgain 動作之後，動作順序中的所有作業。
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: InstallFinalize 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96296c2241f5769296b7192ce89ab9f44364bb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691436"
---
# <a name="installfinalize-action"></a><span data-ttu-id="7ccbe-103">InstallFinalize 動作</span><span class="sxs-lookup"><span data-stu-id="7ccbe-103">InstallFinalize Action</span></span>

<span data-ttu-id="7ccbe-104">InstallFinalize 動作會執行腳本，其中包含自安裝開始或執行 [InstallExecute](installexecute-action.md) 或 [InstallExecuteAgain](installexecuteagain-action.md) 動作之後，動作順序中的所有作業。</span><span class="sxs-lookup"><span data-stu-id="7ccbe-104">The InstallFinalize action runs a script that contains all operations in the action sequence since either the start of the installation or the execution of the [InstallExecute](installexecute-action.md) or [InstallExecuteAgain](installexecuteagain-action.md) actions.</span></span> <span data-ttu-id="7ccbe-105">此動作會標示以 [InstallInitialize](installinitialize-action.md) 動作開頭的交易結尾。</span><span class="sxs-lookup"><span data-stu-id="7ccbe-105">This action marks the end of a transaction that begins with the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7ccbe-106">順序限制</span><span class="sxs-lookup"><span data-stu-id="7ccbe-106">Sequence Restrictions</span></span>

<span data-ttu-id="7ccbe-107">[InstallInitialize](installinitialize-action.md)動作必須位於 InstallFinalize 動作之前。</span><span class="sxs-lookup"><span data-stu-id="7ccbe-107">The [InstallInitialize](installinitialize-action.md) action must come before the InstallFinalize action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7ccbe-108">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="7ccbe-108">ActionData Messages</span></span>

<span data-ttu-id="7ccbe-109">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="7ccbe-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ccbe-110">備註</span><span class="sxs-lookup"><span data-stu-id="7ccbe-110">Remarks</span></span>

<span data-ttu-id="7ccbe-111">如果偵測到產品已標示為要完成移除，則會自動將作業新增至腳本，以移除產品 **主控台** 資訊中的 [**新增/移除程式**]、取消註冊並解除發佈產品，以及從% WINDOWS% 移除快取的本機資料庫（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="7ccbe-111">If it is detected that the product is marked for complete removal, operations are automatically added to the script to remove the **Add/Remove Programs** in the **Control Panel** information for the product, to unregister and unpublish the product, and to remove the cached local database from %WINDOWS%, if it exists.</span></span>

<span data-ttu-id="7ccbe-112">執行 InstallFinalize 動作之後，在動作之前所做的系統變更可能不會還原。</span><span class="sxs-lookup"><span data-stu-id="7ccbe-112">System changes made before the action may not be restored after the InstallFinalize action is executed.</span></span> <span data-ttu-id="7ccbe-113">InstallFinalize 動作會將已判斷為該點的所有作業更新為系統，然後結束交易。</span><span class="sxs-lookup"><span data-stu-id="7ccbe-113">The InstallFinalize action updates the system with all operations determined to that point and then ends the transaction.</span></span>

 

 



