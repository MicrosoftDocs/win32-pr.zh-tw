---
description: CCPSearch 動作會在執行升級安裝之前，使用檔案簽章來驗證是否已在系統上安裝合格產品。
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: CCPSearch 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977872"
---
# <a name="ccpsearch-action"></a><span data-ttu-id="689c0-103">CCPSearch 動作</span><span class="sxs-lookup"><span data-stu-id="689c0-103">CCPSearch Action</span></span>

<span data-ttu-id="689c0-104">CCPSearch 動作會在執行升級安裝之前，使用檔案簽章來驗證是否已在系統上安裝合格產品。</span><span class="sxs-lookup"><span data-stu-id="689c0-104">The CCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="689c0-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="689c0-105">Sequence Restrictions</span></span>

<span data-ttu-id="689c0-106">CCPSearch 動作應該撰寫到 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="689c0-106">CCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="689c0-107">如果動作已在 InstallUISequence 序列中執行，則安裝程式會防止在 InstallExecuteSequence 序列中執行 CCPSearch 動作。</span><span class="sxs-lookup"><span data-stu-id="689c0-107">The installer prevents the CCPSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span> <span data-ttu-id="689c0-108">CCPSearch 動作必須位於 [RMCCPSearch](rmccpsearch-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="689c0-108">The CCPSearch action must come before the [RMCCPSearch](rmccpsearch-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="689c0-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="689c0-109">ActionData Messages</span></span>

<span data-ttu-id="689c0-110">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="689c0-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="689c0-111">備註</span><span class="sxs-lookup"><span data-stu-id="689c0-111">Remarks</span></span>

<span data-ttu-id="689c0-112">CCPSearch 動作會使用下列資料表依序搜尋系統上 CCPSearch 資料表中所列的檔案簽章： Signature、CompLocator、RegLocator、IniLocator 和 DrLocator。</span><span class="sxs-lookup"><span data-stu-id="689c0-112">The CCPSearch action searches for file signatures listed in the CCPSearch table on the system using the following tables in order: Signature, CompLocator, RegLocator, IniLocator, and DrLocator.</span></span>

<span data-ttu-id="689c0-113">如果有任何簽章確定存在，則 **CCP \_ Success** 屬性會設定為1，而 CCPSearch 動作會終止。</span><span class="sxs-lookup"><span data-stu-id="689c0-113">If any signature is determined to exist, the **CCP\_Success** property is set to 1 and the CCPSearch action terminates.</span></span>

<span data-ttu-id="689c0-114">簽章資料表缺少簽章代表目錄。</span><span class="sxs-lookup"><span data-stu-id="689c0-114">The absence of the signature from the Signature table denotes a directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="689c0-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="689c0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="689c0-116">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="689c0-116">CCPSearch</span></span>](ccpsearch-table.md)
</dt> <dt>

[<span data-ttu-id="689c0-117">簽名</span><span class="sxs-lookup"><span data-stu-id="689c0-117">Signature</span></span>](signature-table.md)
</dt> <dt>

[<span data-ttu-id="689c0-118">CompLocator</span><span class="sxs-lookup"><span data-stu-id="689c0-118">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="689c0-119">RegLocator</span><span class="sxs-lookup"><span data-stu-id="689c0-119">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="689c0-120">IniLocator</span><span class="sxs-lookup"><span data-stu-id="689c0-120">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="689c0-121">DrLocator</span><span class="sxs-lookup"><span data-stu-id="689c0-121">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



