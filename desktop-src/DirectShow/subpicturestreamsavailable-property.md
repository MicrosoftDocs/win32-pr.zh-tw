---
description: SubpictureStreamsAvailable 屬性會抓取目前標題中可用的子圖片資料流程數目。
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: SubpictureStreamsAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978145"
---
# <a name="subpicturestreamsavailable-property"></a><span data-ttu-id="b6a08-103">SubpictureStreamsAvailable 屬性</span><span class="sxs-lookup"><span data-stu-id="b6a08-103">SubpictureStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="b6a08-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="b6a08-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b6a08-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b6a08-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b6a08-106">屬性會抓取 `SubpictureStreamsAvailable` 目前標題中可用的子圖片資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="b6a08-106">The `SubpictureStreamsAvailable` property retrieves the number of subpicture streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="b6a08-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6a08-107">Return Value</span></span>

<span data-ttu-id="b6a08-108">以整數形式傳回可用資料流程的數目。</span><span class="sxs-lookup"><span data-stu-id="b6a08-108">Returns the number of available streams as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6a08-109">備註</span><span class="sxs-lookup"><span data-stu-id="b6a08-109">Remarks</span></span>

<span data-ttu-id="b6a08-110">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="b6a08-110">This property is read-only with no default value.</span></span> <span data-ttu-id="b6a08-111">若要查詢每個資料流程的語言屬性，請先呼叫這個方法來取得上限。</span><span class="sxs-lookup"><span data-stu-id="b6a08-111">To query each stream for its language attribute, first call this method to get the upper bound.</span></span>

<span data-ttu-id="b6a08-112">資料流程編號以零為基底。</span><span class="sxs-lookup"><span data-stu-id="b6a08-112">Stream numbering is zero-based.</span></span>

 

 



