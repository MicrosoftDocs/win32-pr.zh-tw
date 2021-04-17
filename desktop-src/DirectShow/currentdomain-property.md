---
description: CurrentDomain 屬性會捕獲 MSWebDVD 物件所在的 DVD 網域。
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: CurrentDomain 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467727"
---
# <a name="currentdomain-property"></a><span data-ttu-id="c35f3-103">CurrentDomain 屬性</span><span class="sxs-lookup"><span data-stu-id="c35f3-103">CurrentDomain Property</span></span>

> [!Note]  
> <span data-ttu-id="c35f3-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="c35f3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c35f3-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c35f3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c35f3-106">`CurrentDomain`屬性會抓取 MSWebDVD 物件所在的 DVD 網域。</span><span class="sxs-lookup"><span data-stu-id="c35f3-106">The `CurrentDomain` property retrieves the DVD domain that the MSWebDVD object is in.</span></span>

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a><span data-ttu-id="c35f3-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="c35f3-107">Return Value</span></span>

<span data-ttu-id="c35f3-108">傳回代表目前網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="c35f3-108">Returns an integer value representing the current domain.</span></span>

## <a name="remarks"></a><span data-ttu-id="c35f3-109">備註</span><span class="sxs-lookup"><span data-stu-id="c35f3-109">Remarks</span></span>

<span data-ttu-id="c35f3-110">屬性的可能值為：</span><span class="sxs-lookup"><span data-stu-id="c35f3-110">The possible values of the property are:</span></span>



| <span data-ttu-id="c35f3-111">值</span><span class="sxs-lookup"><span data-stu-id="c35f3-111">Value</span></span> | <span data-ttu-id="c35f3-112">描述</span><span class="sxs-lookup"><span data-stu-id="c35f3-112">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="c35f3-113">1</span><span class="sxs-lookup"><span data-stu-id="c35f3-113">1</span></span>     | <span data-ttu-id="c35f3-114">初次播放</span><span class="sxs-lookup"><span data-stu-id="c35f3-114">First play</span></span>           |
| <span data-ttu-id="c35f3-115">2</span><span class="sxs-lookup"><span data-stu-id="c35f3-115">2</span></span>     | <span data-ttu-id="c35f3-116">影片管理員功能表</span><span class="sxs-lookup"><span data-stu-id="c35f3-116">Video Manager Menu</span></span>   |
| <span data-ttu-id="c35f3-117">3</span><span class="sxs-lookup"><span data-stu-id="c35f3-117">3</span></span>     | <span data-ttu-id="c35f3-118">影片標題設定功能表</span><span class="sxs-lookup"><span data-stu-id="c35f3-118">Video Title Set Menu</span></span> |
| <span data-ttu-id="c35f3-119">4</span><span class="sxs-lookup"><span data-stu-id="c35f3-119">4</span></span>     | <span data-ttu-id="c35f3-120">標題</span><span class="sxs-lookup"><span data-stu-id="c35f3-120">Title</span></span>                |
| <span data-ttu-id="c35f3-121">5</span><span class="sxs-lookup"><span data-stu-id="c35f3-121">5</span></span>     | <span data-ttu-id="c35f3-122">停止</span><span class="sxs-lookup"><span data-stu-id="c35f3-122">Stop</span></span>                 |



 

<span data-ttu-id="c35f3-123">呼叫這個方法，以確保 DVD 導覽器位於您要呼叫之方法的有效網域中。</span><span class="sxs-lookup"><span data-stu-id="c35f3-123">Call this method to ensure that the DVD Navigator is in a valid domain for the method you are about to call.</span></span> <span data-ttu-id="c35f3-124">例如，在呼叫 [**PlayTitle**](playtitle-method.md)之前，請檢查 `CurrentDomain` 屬性，以確定 DVD 導覽器不在「停止」或「第一個播放」網域中。</span><span class="sxs-lookup"><span data-stu-id="c35f3-124">For example, before calling [**PlayTitle**](playtitle-method.md), check the `CurrentDomain` property to make sure that the DVD Navigator is not in the Stop or First Play domain.</span></span>

 

 



