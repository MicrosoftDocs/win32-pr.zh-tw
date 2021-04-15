---
title: IMsRdpClientNonScriptable2 UIParentWindowHandle 屬性
description: 設定或抓取視窗控制碼，使其成為控制項所顯示之任何對話方塊的父視窗。 如此一來，控制項所顯示的任何視窗都能針對父應用程式所顯示的任何視窗適當地進行模式回應。
ms.assetid: 5ecf1fc3-492e-4faf-89c5-7f7abb3778a0
ms.tgt_platform: multiple
keywords:
- UIParentWindowHandle 屬性遠端桌面服務
- UIParentWindowHandle 屬性遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，UIParentWindowHandle 屬性
- UIParentWindowHandle 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，UIParentWindowHandle 屬性
- UIParentWindowHandle 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，UIParentWindowHandle 屬性
- UIParentWindowHandle 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，UIParentWindowHandle 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2.UIParentWindowHandle
- IMsRdpClientNonScriptable2.get_UIParentWindowHandle
- IMsRdpClientNonScriptable2.put_UIParentWindowHandle
- IMsRdpClientNonScriptable3.UIParentWindowHandle
- IMsRdpClientNonScriptable3.get_UIParentWindowHandle
- IMsRdpClientNonScriptable3.put_UIParentWindowHandle
- IMsRdpClientNonScriptable4.UIParentWindowHandle
- IMsRdpClientNonScriptable4.get_UIParentWindowHandle
- IMsRdpClientNonScriptable4.put_UIParentWindowHandle
- IMsRdpClientNonScriptable5.UIParentWindowHandle
- IMsRdpClientNonScriptable5.get_UIParentWindowHandle
- IMsRdpClientNonScriptable5.put_UIParentWindowHandle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5526fd1a699c87e32c6acadd238c2144d00a10be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464313"
---
# <a name="imsrdpclientnonscriptable2uiparentwindowhandle-property"></a>IMsRdpClientNonScriptable2：： UIParentWindowHandle 屬性

設定或抓取視窗控制碼，使其成為控制項所顯示之任何對話方塊的父視窗。 如此一來，控制項所顯示的任何視窗都能針對父應用程式所顯示的任何視窗適當地進行模式回應。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UIParentWindowHandle(
  [in]  HWND hwndUIParentWindowHandle
);

HRESULT get_UIParentWindowHandle(
  [out] HWND *phwndUIParentWindowHandle
);
```



## <a name="property-value"></a>屬性值

新的視窗控制碼。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008、Windows Server 2008 SP1<br/>                                  |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable2 定義為17a5e535-4072-4fa4-af32-c8d0d47345e9<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> </dl>

 

 





