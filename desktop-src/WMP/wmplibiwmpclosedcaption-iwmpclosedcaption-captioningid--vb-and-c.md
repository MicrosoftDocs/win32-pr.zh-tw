---
title: IWMPClosedCaption captioningId 屬性
description: IWMPClosedCaption 屬性會取得或設定顯示字幕的 HTML 元素名稱。
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- captioningId 屬性 Windows Media Player
- captioningId 屬性 Windows Media Player，IWMPClosedCaption 介面
- IWMPClosedCaption 介面 Windows Media Player，captioningId 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f6d4c10beb3f0fd94da0365d67b6c5ab480d36d5a3786021f538e9dcf4e90c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116054"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a>IWMPClosedCaption：： captioningId 屬性

**IWMPClosedCaption** 屬性會取得或設定顯示字幕的 HTML 元素名稱。

## <a name="syntax"></a>Syntax


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a>屬性值

表示 HTML 元素之識別碼的 **system.string** 。

## <a name="remarks"></a>備註

指定的元素名稱可以是網頁中的任何 HTML 專案，只要它支援 **innerHTML** 屬性即可。 如果網頁包含多個框架，元素名稱只能參考與 Windows Media Player 控制項相同框架中的元素。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**IWMPClosedCaption 介面 (VB 和 c # )**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2 介面 (VB 和 c # )**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





