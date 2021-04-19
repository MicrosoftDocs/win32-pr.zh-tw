---
description: ResolveSource 動作會決定來源的位置，如果尚未解析來源，則會設定 SourceDir 屬性。
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: ResolveSource 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988368"
---
# <a name="resolvesource-action"></a><span data-ttu-id="acff5-103">ResolveSource 動作</span><span class="sxs-lookup"><span data-stu-id="acff5-103">ResolveSource Action</span></span>

<span data-ttu-id="acff5-104">ResolveSource 動作會決定來源的位置，如果尚未解析來源，則會設定 [**SourceDir**](sourcedir.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="acff5-104">The ResolveSource action determines the location of the source and sets the [**SourceDir**](sourcedir.md) property if the source has not been resolved yet.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="acff5-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="acff5-105">Sequence Restrictions</span></span>

<span data-ttu-id="acff5-106">ResolveSource 動作必須晚于 [CostInitialize 動作](costinitialize-action.md)。</span><span class="sxs-lookup"><span data-stu-id="acff5-106">The ResolveSource action must come after the [CostInitialize action](costinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="acff5-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="acff5-107">ActionData Messages</span></span>

<span data-ttu-id="acff5-108">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="acff5-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="acff5-109">備註</span><span class="sxs-lookup"><span data-stu-id="acff5-109">Remarks</span></span>

<span data-ttu-id="acff5-110">在任何運算式中使用 [**SourceDir**](sourcedir.md) 屬性之前，必須先呼叫 ResolveSource 動作。</span><span class="sxs-lookup"><span data-stu-id="acff5-110">The ResolveSource action must be called before using the [**SourceDir**](sourcedir.md) property in any expression.</span></span> <span data-ttu-id="acff5-111">您也必須先呼叫它，才能嘗試使用 [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)抓取 **SourceDir** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="acff5-111">It must also be called before attempting to retrieve the value of the **SourceDir** property using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="acff5-112">當來源無法使用時，不應執行 ResolveSource 動作，因為它可能會在卸載應用程式時執行。</span><span class="sxs-lookup"><span data-stu-id="acff5-112">The ResolveSource action should not be executed when the source is unavailable, as it may be when uninstalling the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acff5-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="acff5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acff5-114">來源復原</span><span class="sxs-lookup"><span data-stu-id="acff5-114">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



