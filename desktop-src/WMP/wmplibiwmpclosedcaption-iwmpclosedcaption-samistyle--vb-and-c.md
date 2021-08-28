---
title: IWMPClosedCaption SAMIStyle 屬性
description: SAMIStyle 屬性會取得或設定隱藏式輔助字幕樣式。
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- SAMIStyle 屬性 Windows Media Player
- SAMIStyle 屬性 Windows Media Player，IWMPClosedCaption 介面
- IWMPClosedCaption 介面 Windows Media Player，SAMIStyle 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e147b48ffb80e1114133b59018cef514eefd2ae7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885869"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a>IWMPClosedCaption：： SAMIStyle 屬性

**SAMIStyle** 屬性會取得或設定隱藏式輔助字幕樣式。

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a>屬性值

**System.string** ，此為薩米文檔案的樣式識別碼中所指定的名稱。

## <a name="remarks"></a>備註

薩米文檔案可以包含數個格式樣式定義。 薩米文的樣式定義在 &lt; 薩米文的樣式 &gt; 和標記之間 </STYLE> 。 樣式的定義是以文字字串前面加上 \# 字元。 例如：


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



這會指定產生特定字型的樣式。

如果未指定薩米體樣式，預設會使用薩米文檔案中所定義的第一個樣式。

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

 

 





