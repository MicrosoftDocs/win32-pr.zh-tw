---
description: DVDAdm 屬性可讓您存取 MSDVDAdm 物件，其中包含用來儲存應用程式和使用者資訊的方法和屬性。
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: DVDAdm 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adedea036393e68456cfd9f035882ae9c335063030518e808c57bced6d5b5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079158"
---
# <a name="dvdadm-property"></a>DVDAdm 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`DVDAdm`屬性可讓您存取[MSDVDAdm](msdvdadm-object.md)物件，其中包含用來儲存應用程式和使用者資訊的方法和屬性。

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 不需要建立 **MSDVDAdm** 物件的個別參考。 若要存取物件的方法和屬性，請使用 `DVDAdm` 屬性，如下列範例所示。

## <a name="examples"></a>範例


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



