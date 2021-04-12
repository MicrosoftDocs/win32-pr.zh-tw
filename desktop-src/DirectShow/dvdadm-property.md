---
description: DVDAdm 屬性可讓您存取 MSDVDAdm 物件，其中包含用來儲存應用程式和使用者資訊的方法和屬性。
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: DVDAdm 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109224"
---
# <a name="dvdadm-property"></a>DVDAdm 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

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



 

 



