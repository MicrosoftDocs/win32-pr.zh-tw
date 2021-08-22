---
description: SubpictureOn 屬性會 (on 或 off) 來設定或抓取目前的子圖片狀態。
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: SubpictureOn 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692df6b69bc960562e9acd223a0e4e156fe00de2206146f609ba15d550b7a961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951767"
---
# <a name="subpictureon-property"></a>SubpictureOn 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`SubpictureOn`屬性會設定或抓取 (on 或 off) 的目前子圖片狀態。

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>傳回值

傳回布林值，指出是否顯示子圖片。

## <a name="remarks"></a>備註

這個屬性不會影響隱藏式輔助字幕的顯示。 隱藏式輔助字幕內嵌于影片資料流程中。 DVD subpictures 會在不同的串流上傳輸。

當使用 [**CurrentSubpictureStream**](currentsubpicturestream-property.md)變更子圖片資料流程時，屬性會 `SubpictureOn` 切換為 **True**。

這個屬性是讀取/寫入，預設值是 false。

 

 



