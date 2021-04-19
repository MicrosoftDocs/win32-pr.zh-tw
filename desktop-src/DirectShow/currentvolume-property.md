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
# <a name="currentvolume-property"></a>CurrentVolume 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

屬性會抓取 `CurrentVolume` 目前根目錄的磁片區編號。

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>傳回值

傳回代表目前 DVD 磁片區的整數值。 如果光碟是多重磁片區集的一部分，則整數值應大於零。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VolumesAvailable**](volumesavailable-property.md)
</dt> </dl>

 

 



