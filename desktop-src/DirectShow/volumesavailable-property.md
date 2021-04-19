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
# <a name="volumesavailable-property"></a>VolumesAvailable 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`VolumesAvailable`屬性會捕獲 multivolume 集中的磁片區數目。

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>傳回值

以整數形式傳回集合中的磁片區數目。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 某些 DVD 標題可能會以 multidisc 組或數列的形式發行。 使用這個方法來判斷目前光碟的磁片區編號。

 

 



