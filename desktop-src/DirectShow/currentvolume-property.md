---
description: CurrentVolume 屬性會抓取目前根目錄的磁片區編號。
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: CurrentVolume 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972298"
---
# <a name="currentvolume-property"></a><span data-ttu-id="f6e58-103">CurrentVolume 屬性</span><span class="sxs-lookup"><span data-stu-id="f6e58-103">CurrentVolume Property</span></span>

> [!Note]  
> <span data-ttu-id="f6e58-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="f6e58-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f6e58-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f6e58-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f6e58-106">屬性會抓取 `CurrentVolume` 目前根目錄的磁片區編號。</span><span class="sxs-lookup"><span data-stu-id="f6e58-106">The `CurrentVolume` property retrieves the volume number for the current root directory.</span></span>

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a><span data-ttu-id="f6e58-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6e58-107">Return Value</span></span>

<span data-ttu-id="f6e58-108">傳回代表目前 DVD 磁片區的整數值。</span><span class="sxs-lookup"><span data-stu-id="f6e58-108">Returns an integer value representing the current DVD volume.</span></span> <span data-ttu-id="f6e58-109">如果光碟是多重磁片區集的一部分，則整數值應大於零。</span><span class="sxs-lookup"><span data-stu-id="f6e58-109">If a disc is part of a multi-volume set, then the integer value should be greater than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6e58-110">備註</span><span class="sxs-lookup"><span data-stu-id="f6e58-110">Remarks</span></span>

<span data-ttu-id="f6e58-111">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="f6e58-111">This property is read-only with no default value.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6e58-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6e58-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e58-113">**VolumesAvailable**</span><span class="sxs-lookup"><span data-stu-id="f6e58-113">**VolumesAvailable**</span></span>](volumesavailable-property.md)
</dt> </dl>

 

 



