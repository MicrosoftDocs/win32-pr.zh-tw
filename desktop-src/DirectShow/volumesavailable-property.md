---
description: VolumesAvailable 屬性會捕獲 multivolume 集中的磁片區數目。
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: VolumesAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987232"
---
# <a name="volumesavailable-property"></a><span data-ttu-id="fc25c-103">VolumesAvailable 屬性</span><span class="sxs-lookup"><span data-stu-id="fc25c-103">VolumesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="fc25c-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="fc25c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fc25c-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="fc25c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fc25c-106">`VolumesAvailable`屬性會捕獲 multivolume 集中的磁片區數目。</span><span class="sxs-lookup"><span data-stu-id="fc25c-106">The `VolumesAvailable` property retrieves the number of volumes in a multivolume set.</span></span>

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a><span data-ttu-id="fc25c-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc25c-107">Return Value</span></span>

<span data-ttu-id="fc25c-108">以整數形式傳回集合中的磁片區數目。</span><span class="sxs-lookup"><span data-stu-id="fc25c-108">Returns the number of volumes in the set as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc25c-109">備註</span><span class="sxs-lookup"><span data-stu-id="fc25c-109">Remarks</span></span>

<span data-ttu-id="fc25c-110">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="fc25c-110">This property is read-only with no default value.</span></span> <span data-ttu-id="fc25c-111">某些 DVD 標題可能會以 multidisc 組或數列的形式發行。</span><span class="sxs-lookup"><span data-stu-id="fc25c-111">Some DVD titles might be released as a multidisc set or series.</span></span> <span data-ttu-id="fc25c-112">使用這個方法來判斷目前光碟的磁片區編號。</span><span class="sxs-lookup"><span data-stu-id="fc25c-112">Use this method to determine the volume number for the current disc.</span></span>

 

 



