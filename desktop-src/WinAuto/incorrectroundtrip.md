---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183876"
---
# <a name="incorrectroundtrip"></a><span data-ttu-id="7c643-103">IncorrectRoundTrip</span><span class="sxs-lookup"><span data-stu-id="7c643-103">IncorrectRoundTrip</span></span>

## <a name="text"></a><span data-ttu-id="7c643-104">Text</span><span class="sxs-lookup"><span data-stu-id="7c643-104">Text</span></span>

<span data-ttu-id="7c643-105">呼叫 accNavigate ( (按一下 [延遲]，以在下列內容中再次提醒： ) 、1、NAVDIR \_ 下一) ，然後 accNavigate ( (開啟) ，2，NAVDIR 上一個) ，則應該會傳回 click 延遲，以便在下列情況下提醒： \_ (ChildId = 1) </span><span class="sxs-lookup"><span data-stu-id="7c643-105">Call to accNavigate((Click Snooze to be reminded again in:), 1, NAVDIR\_NEXT), then accNavigate((Open), 2, NAVDIR\_PREVIOUS), should have returned Click Snooze to be reminded again in:(ChildId=1), but returned Click Snooze to be reminded again in:</span></span>

## <a name="type"></a><span data-ttu-id="7c643-106">類型</span><span class="sxs-lookup"><span data-stu-id="7c643-106">Type</span></span>

<span data-ttu-id="7c643-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="7c643-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="7c643-108">描述</span><span class="sxs-lookup"><span data-stu-id="7c643-108">Description</span></span>

<span data-ttu-id="7c643-109">當往返方向反轉時，使用 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) 來跨越驗證目標的專案樹狀結構並不會傳回相同的起始元素。</span><span class="sxs-lookup"><span data-stu-id="7c643-109">using [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to traverse the element tree of the verification target does not return the same starting element when the direction of traversal is reversed.</span></span>

![導致不正確的往返流覽的無效 msaa 執行範例](images/accchecker-invalid-round-trip.png)

<span data-ttu-id="7c643-111">此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。</span><span class="sxs-lookup"><span data-stu-id="7c643-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="7c643-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="7c643-112">Possible causes</span></span>

<span data-ttu-id="7c643-113">不正確或不正確 MSAA 執行。</span><span class="sxs-lookup"><span data-stu-id="7c643-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c643-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c643-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c643-115">**IAccessible：： accNavigate**</span><span class="sxs-lookup"><span data-stu-id="7c643-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




