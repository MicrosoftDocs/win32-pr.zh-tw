---
title: IWMPSettings 餘額屬性
description: 餘額屬性會取得或設定目前的立體餘額。
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- 平衡屬性 Windows Media Player
- 平衡屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，餘額屬性
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d519d656be6b4974e2b4dd2707aafb2bb153f6b26bafe75de948d5e50c67b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861079"
---
# <a name="iwmpsettingsbalance-property"></a>IWMPSettings：：餘額屬性

**餘額** 屬性會取得或設定目前的立體餘額。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a>屬性值

表示餘額值的 **system.object** 。 此值的範圍可以從100到100。 預設值為零。

## <a name="remarks"></a>備註

值為零表示音訊在左右通道的相同磁片區上播放。 值為100表示音訊只會在左邊的頻道播放。 值為100表示音訊只會在右聲道上播放。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player  9  系列或更新的版本。<br/>                                                                     |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





