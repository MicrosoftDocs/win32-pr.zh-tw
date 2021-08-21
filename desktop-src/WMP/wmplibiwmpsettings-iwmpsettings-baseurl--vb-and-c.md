---
title: IWMPSettings baseURL 屬性
description: BaseURL 屬性會取得或設定基底 URL，以用於以數位媒體內容內嵌之 URL 指令碼命令的相對路徑解析。
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- baseURL 屬性 Windows Media Player
- baseURL 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，baseURL 屬性
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3224a43a2689fd49dee2b2a66cc768250b1a829e61863d8cfbd029e3cdf783c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568415"
---
# <a name="iwmpsettingsbaseurl-property"></a>IWMPSettings：： baseURL 屬性

**BaseURL** 屬性會取得或設定基底 URL，以用於以數位媒體內容內嵌之 URL 指令碼命令的相對路徑解析。

## <a name="syntax"></a>Syntax


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a>屬性值

作為基底 URL 的 **system.string** 。

## <a name="remarks"></a>備註

這個屬性會指定 **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** 事件以命令參數形式傳遞的基底 HTTP URL。 基底 URL 會與相對 URL 串連，如下所示：

1.  尾端正斜線 (/) 會加入 **baseURL** 屬性所抓取的值中。
2.  前置句點、反斜線或正斜線字元 (.、 \\ 和/) 會從相對 URL 中刪除。
3.  相對 URL 會新增至基底 URL 的結尾。
4.  產生的完整 URL 中的所有斜線字元都會指向相同方向 (轉換成正斜線或反斜線) 根據新 URL 中遇到的第一個斜線字元的方向。

**注意**

Windows Media Player 控制項不支援使用兩個句號 (。在相對 URL 中 ) ，表示目前位置的父系。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer. ScriptCommand 事件 (VB 和 c # )**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





