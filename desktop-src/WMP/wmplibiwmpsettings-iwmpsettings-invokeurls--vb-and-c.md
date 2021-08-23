---
title: IWMPSettings invokeURLs 屬性
description: InvokeURLs 屬性會取得或設定值，指出 URL 事件是否應該啟動網頁瀏覽器。
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- invokeURLs 屬性 Windows Media Player
- invokeURLs 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，invokeURLs 屬性
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba44af7e6ec700f9df810486acb57af24a14c9e5d4966fddbfe4b242d346a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053426"
---
# <a name="iwmpsettingsinvokeurls-property"></a>IWMPSettings：： invokeURLs 屬性

**InvokeURLs** 屬性會取得或設定值，指出 URL 事件是否應該啟動網頁瀏覽器。

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>屬性值

System.string **值，** 指出 URL 事件是否應啟動網頁瀏覽器。 預設值為 **True**。

## <a name="remarks"></a>備註

數位媒體檔案和資料流程可以包含 URL 指令碼命令。 將 URL 指令碼命令傳送給 Windows Media Player 控制項時，會先將它傳遞給 **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** 事件處理常式，而不論 **invokeURLs** 所抓取的值為何。 **\_ WMPOCXEvents \_ ScriptCommandEvent** 結束之後，Windows Media Player 會檢查 **invokeURLs** ，以判斷是否要使用 URL 啟動預設的網頁瀏覽器。 您可以選擇性地顯示 Url，方法是在 **\_ WMPOCXEvents \_ ScriptCommandEvent** 中進行檢查，並視需要設定 **invokeURLs** 。

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

 

 





