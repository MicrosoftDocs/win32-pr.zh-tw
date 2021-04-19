---
description: 取得對話方塊的控制碼，此控制碼會顯示錯誤訊息，並提供一或多個按鈕來繼續、取消或中止應用程式。
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'IWiaAppErrorHandler：： GetWindow 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979163"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a>IWiaAppErrorHandler：： GetWindow 方法

取得對話方塊的控制碼，此控制碼會顯示錯誤訊息，並提供一或多個按鈕來繼續、取消或中止應用程式。

## <a name="syntax"></a>語法


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phwnd* \[擴展\]
</dt> <dd>

類型： **HWND \** _

應用程式錯誤處理常式所使用的 HWND、驅動程式錯誤處理常式，以及裝置訊息對話方塊的預設錯誤處理常式 (錯誤和資訊性) 。 輸出值可能是 _ * Null * *。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

*phwnd* 指向 Windows 映像取得 (WIA) 2.0 Proxy 傳遞至 [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) 的視窗。 此視窗在資料傳輸期間必須保持有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 




