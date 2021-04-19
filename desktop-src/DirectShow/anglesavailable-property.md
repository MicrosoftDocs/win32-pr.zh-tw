---
description: AnglesAvailable 屬性會抓取目前可用的角度數目。
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: AnglesAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971939"
---
# <a name="anglesavailable-property"></a><span data-ttu-id="c9357-103">AnglesAvailable 屬性</span><span class="sxs-lookup"><span data-stu-id="c9357-103">AnglesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="c9357-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="c9357-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c9357-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c9357-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c9357-106">屬性會抓取 `AnglesAvailable` 目前可用的角度數目。</span><span class="sxs-lookup"><span data-stu-id="c9357-106">The `AnglesAvailable` property retrieves the number of angles currently available.</span></span>

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a><span data-ttu-id="c9357-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9357-107">Return Value</span></span>

<span data-ttu-id="c9357-108">傳回從1到9的整數值，代表目前可用的角度數目。</span><span class="sxs-lookup"><span data-stu-id="c9357-108">Returns an integer value from 1 through 9 representing the number of angles currently available.</span></span> <span data-ttu-id="c9357-109">如果</span><span class="sxs-lookup"><span data-stu-id="c9357-109">If</span></span>


```
iAngles
```



<span data-ttu-id="c9357-110">= 1，目前位置沒有角區塊。</span><span class="sxs-lookup"><span data-stu-id="c9357-110">= 1, there is no angle block at the current location.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9357-111">備註</span><span class="sxs-lookup"><span data-stu-id="c9357-111">Remarks</span></span>

<span data-ttu-id="c9357-112">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="c9357-112">This property is read-only with no default value.</span></span> <span data-ttu-id="c9357-113">*角度區塊* 是從一個以上相機角度拍攝的影片區段。</span><span class="sxs-lookup"><span data-stu-id="c9357-113">An *angle block* is a video segment that was shot from more than one camera angle.</span></span> <span data-ttu-id="c9357-114">角度區塊中最多可以有九個角度，從1到9的編號。</span><span class="sxs-lookup"><span data-stu-id="c9357-114">There can be up to nine angles in an angle block, numbered from 1 through 9.</span></span> <span data-ttu-id="c9357-115">當 DVD 導覽器第一次進入角度區塊時，會以 \_ lParam1 中的角度數，將 EC DVD \_ 角度 \_ 可用事件通知傳送給您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c9357-115">When the DVD Navigator first enters an angle block, it sends your application an EC\_DVD\_ANGLES\_AVAILABLE event notification with the number of angles in *lParam1*.</span></span> <span data-ttu-id="c9357-116">您可以撰寫光碟來自動顯示可用角度的功能表（當其進入角度區塊時），但通常應用程式必須判斷可用的角度，並提供使用者一種方式來選取它。</span><span class="sxs-lookup"><span data-stu-id="c9357-116">A disc can be authored to automatically show a menu for available angles when it enters an angle block, but generally an application must determine the number of angles available and offer the user a way to select one.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9357-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9357-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9357-118">**CurrentAngle**</span><span class="sxs-lookup"><span data-stu-id="c9357-118">**CurrentAngle**</span></span>](currentangle-property.md)
</dt> </dl>

 

 



