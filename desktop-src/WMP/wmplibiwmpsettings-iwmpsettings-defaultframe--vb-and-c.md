---
title: IWMPSettings defaultFrame 屬性
description: DefaultFrame 屬性會取得或設定用來顯示 AxWindowsMediaPlayer \_ WMPOCXEvents ScriptCommandEvent 事件中所接收之 URL 的框架名稱 \_ 。
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- defaultFrame 屬性 Windows Media Player
- defaultFrame 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，defaultFrame 屬性
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000712"
---
# <a name="iwmpsettingsdefaultframe-property"></a>IWMPSettings：:d efaultFrame 屬性

**DefaultFrame** 屬性會取得或設定用來顯示 **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** 事件中所接收之 URL 的框架名稱。

## <a name="syntax"></a>Syntax


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>屬性值

**System.string** ，此為目標 **框架** 專案的 name 屬性值。

## <a name="remarks"></a>備註

如果在 **\_ WMPOCXEvents \_ ScriptCommandEvent** 事件本身中指定了目標框架，則會忽略這個屬性。

使用 JAVA applet Netscape Navigator 時，會忽略這個屬性。 在 Netscape Navigator 中，每個收到的 URL 指令碼命令都會在新的瀏覽器視窗中顯示 URL，不論 **defaultFrame** 的值為何。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer ScriptCommand 事件 (VB 和 c # )**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





