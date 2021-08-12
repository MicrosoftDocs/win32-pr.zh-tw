---
description: CurrentVolume 屬性會抓取目前根目錄的磁片區編號。
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: CurrentVolume 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07f9d82facc243654bad2e16e9a028e8cf920a51f15dd92cc879b0ea1340d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654599"
---
# <a name="currentvolume-property"></a>CurrentVolume 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

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

 

 



