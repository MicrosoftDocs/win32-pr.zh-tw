---
description: CurrentSubpictureStream 屬性會設定或抓取目前的子圖片資料流程。
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: CurrentSubpictureStream 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510303"
---
# <a name="currentsubpicturestream-property"></a>CurrentSubpictureStream 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`CurrentSubpictureStream`屬性會設定或抓取目前的子圖片資料流程。

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a>傳回值

傳回代表資料流程的整數值。

## <a name="remarks"></a>備註

這個屬性的可能值為：



| 值   | 描述              |
|---------|--------------------------|
| 0到31 | 子圖片資料流程    |
| 63      | 靜音低位元速率串流 |



 

此屬性是讀取/寫入，沒有預設值。 在設定新的子圖片資料流程之前，請先呼叫 [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) 確認資料流程是否可用。

設定這個屬性會使 [**SubpictureOn**](subpictureon-property.md) 屬性切換為 **True**。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SubpictureOn**](subpictureon-property.md)
</dt> <dt>

[**SubpictureStreamsAvailable**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



