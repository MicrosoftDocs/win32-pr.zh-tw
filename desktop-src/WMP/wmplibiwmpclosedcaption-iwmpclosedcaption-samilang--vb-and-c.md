---
title: IWMPClosedCaption SAMILang 屬性
description: SAMILang 屬性會取得或設定針對隱藏式輔助字幕所顯示的語言。
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- SAMILang 屬性 Windows Media Player
- SAMILang 屬性 Windows Media Player，IWMPClosedCaption 介面
- IWMPClosedCaption 介面 Windows Media Player，SAMILang 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997030"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>IWMPClosedCaption：： SAMILang 屬性

**SAMILang** 屬性會取得或設定針對隱藏式輔助字幕所顯示的語言。

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>屬性值

**System.string** ，這是在薩米文檔案的語言識別項中所指定的名稱。

## <a name="remarks"></a>備註

薩米文檔案可以包含一或多個語言的文字。 隱藏式字幕的可用語言會定義于薩米文檔案的 <STYLE> 和 </STYLE> 標記之間。 語言識別項是使用唯一的英數位元字串所指定，該字串前面會加上句點 (。 ) 。 針對語言指定的名稱可以是任何字串。 例如，下列程式可用來定義美式英文：


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



如果未指定薩米文語言，預設會使用薩米文檔案中定義的第一種語言。

您使用 **SAMILang** 設定的字串必須符合語言規範中的 **Name** 屬性。

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

 

 





