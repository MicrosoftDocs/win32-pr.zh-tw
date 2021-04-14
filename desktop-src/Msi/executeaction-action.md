---
description: ExecuteAction 動作會使用 EXECUTEACTION 屬性來起始執行順序，以判斷要執行哪一種類型的安裝。
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: ExecuteAction 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469280"
---
# <a name="executeaction-action"></a><span data-ttu-id="872f5-103">ExecuteAction 動作</span><span class="sxs-lookup"><span data-stu-id="872f5-103">ExecuteAction Action</span></span>

<span data-ttu-id="872f5-104">ExecuteAction 動作會使用 [**ExecuteAction**](executeaction.md) 屬性來起始執行順序，以判斷要執行哪一種類型的安裝。</span><span class="sxs-lookup"><span data-stu-id="872f5-104">The ExecuteAction action initiates the execution sequence using the [**EXECUTEACTION**](executeaction.md) property to determine which type of installation to perform.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="872f5-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="872f5-105">Sequence Restrictions</span></span>

<span data-ttu-id="872f5-106">在開始安裝所需的所有資訊收集完成之後，應該將這個動作排序。</span><span class="sxs-lookup"><span data-stu-id="872f5-106">This action should be sequenced after all information collection necessary to begin the installation is complete.</span></span> <span data-ttu-id="872f5-107">在 [InstallUISequence 資料表](installuisequence-table.md)和 [AdminUISequence 資料表](adminuisequence-table.md)中的 ExecuteAction 動作之後，可能會排序其他動作。</span><span class="sxs-lookup"><span data-stu-id="872f5-107">Additional actions may be sequenced after ExecuteAction action in the [InstallUISequence table](installuisequence-table.md), and [AdminUISequence table](adminuisequence-table.md).</span></span> <span data-ttu-id="872f5-108">順序通常會以 [*成本*](c-gly.md) 動作開頭，例如 [CostInitialize 動作](costinitialize-action.md)，後面接著使用者介面動作，再接著 ExecuteAction 動作。</span><span class="sxs-lookup"><span data-stu-id="872f5-108">A sequence will typically begin with [*costing*](c-gly.md) actions, such as the [CostInitialize action](costinitialize-action.md), followed by the user interface actions, and then the ExecuteAction action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="872f5-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="872f5-109">ActionData Messages</span></span>

<span data-ttu-id="872f5-110">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="872f5-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="872f5-111">備註</span><span class="sxs-lookup"><span data-stu-id="872f5-111">Remarks</span></span>

<span data-ttu-id="872f5-112">如果已啟用安裝程式服務，則會以系統許可權執行 ExecuteAction 動作。</span><span class="sxs-lookup"><span data-stu-id="872f5-112">The ExecuteAction action is run with system privileges if the installer service is enabled.</span></span> <span data-ttu-id="872f5-113">最上層的動作（例如 [ [安裝動作](install-action.md)]、[ [公告動作](advertise-action.md)] 和 [ [管理員] 動作](admin-action.md) ）包含判斷呼叫 ExecuteAction 動作是否需要執行執行順序或使用者介面順序的內部邏輯。</span><span class="sxs-lookup"><span data-stu-id="872f5-113">The top-level actions, such as the [INSTALL action](install-action.md), [ADVERTISE action](advertise-action.md), and [ADMIN action](admin-action.md) include internal logic that determines whether calling the ExecuteAction action requires either the execution sequence or the user interface sequence to run.</span></span>

## <a name="related-topics"></a><span data-ttu-id="872f5-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="872f5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="872f5-115">InstallUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="872f5-115">InstallUISequence table</span></span>](installuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="872f5-116">AdminUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="872f5-116">AdminUISequence table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="872f5-117">CostInitialize 動作</span><span class="sxs-lookup"><span data-stu-id="872f5-117">CostInitialize action</span></span>](costinitialize-action.md)
</dt> </dl>

 

 



