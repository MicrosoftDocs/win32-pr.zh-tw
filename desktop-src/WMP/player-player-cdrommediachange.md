---
title: CdromMediaChange 事件
description: 從 CD 或 DVD 光碟機插入或退出 CD 或 DVD 時，就會發生 CdromMediaChange 事件。 |CdromMediaChange 事件
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- CdromMediaChange 事件 Windows Media Player
- CdromMediaChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，CdromMediaChange 事件
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5e7301c1fb697f4dbbceea2d4dc46af1d884fe4b3e06166b5c24aa43502a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747384"
---
# <a name="playercdrommediachange-event"></a>CdromMediaChange 事件

從 CD 或 DVD 光碟機插入或退出 CD 或 DVD 時，就會發生 **CdromMediaChange** 事件。

## <a name="syntax"></a>語法


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*CdromNum* 
</dt> <dd>

指定 CD 或 DVD 光碟機索引的 (**長**) **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

CD 光碟機的索引會對應到 **CdromCollection** 中之 **Cdrom** 物件的索引。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Cdrom 物件**](cdrom-object.md)
</dt> <dt>

[**CdromCollection 物件**](cdromcollection-object.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





