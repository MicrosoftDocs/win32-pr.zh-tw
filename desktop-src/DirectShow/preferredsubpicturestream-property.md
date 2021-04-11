---
description: PreferredSubpictureStream 屬性會抓取目前觀賞會話的慣用子圖片資料流程。
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: PreferredSubpictureStream 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846288"
---
# <a name="preferredsubpicturestream-property"></a><span data-ttu-id="8b07f-103">PreferredSubpictureStream 屬性</span><span class="sxs-lookup"><span data-stu-id="8b07f-103">PreferredSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="8b07f-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="8b07f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8b07f-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="8b07f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8b07f-106">屬性會抓取 `PreferredSubpictureStream` 目前的觀看會話的慣用子圖片資料流程。</span><span class="sxs-lookup"><span data-stu-id="8b07f-106">The `PreferredSubpictureStream` property retrieves the preferred subpicture stream for the current viewing session.</span></span>

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="8b07f-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b07f-107">Return Value</span></span>

<span data-ttu-id="8b07f-108">傳回整數值，表示系統登錄中目前慣用的子圖片資料流程。</span><span class="sxs-lookup"><span data-stu-id="8b07f-108">Returns an Integer value representing the current preferred subpicture stream in the system registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b07f-109">備註</span><span class="sxs-lookup"><span data-stu-id="8b07f-109">Remarks</span></span>

<span data-ttu-id="8b07f-110">慣用的子圖片資料流程會以 [MSDVDAdm](msdvdadm-object.md) 物件的 [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)設定。</span><span class="sxs-lookup"><span data-stu-id="8b07f-110">The preferred subpicture stream is set with [MSDVDAdm](msdvdadm-object.md) object's [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md).</span></span>

 

 



