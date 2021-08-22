---
description: PreferredSubpictureStream 屬性會抓取目前觀賞會話的慣用子圖片資料流程。
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: PreferredSubpictureStream 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28b98163607e31a207bffb3974fee3b32505ff60ba3700b452b2dff2625f421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583538"
---
# <a name="preferredsubpicturestream-property"></a>PreferredSubpictureStream 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

屬性會抓取 `PreferredSubpictureStream` 目前的觀看會話的慣用子圖片資料流程。

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a>傳回值

傳回整數值，表示系統登錄中目前慣用的子圖片資料流程。

## <a name="remarks"></a>備註

慣用的子圖片資料流程會以 [MSDVDAdm](msdvdadm-object.md) 物件的 [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)設定。

 

 



