---
description: 執行必要的初始化，以允許呼叫的應用程式成為 Miracast 顯示接收。
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: 'WFDDisplaySinkStart 函式 (Wfdsink) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512765"
---
# <a name="wfddisplaysinkstart-function"></a>WFDDisplaySinkStart 函式

執行必要的初始化，以允許呼叫的應用程式成為 Miracast 顯示接收。 您的應用程式應該在啟動時呼叫此一次。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uDeviceCategory* \[在\]
</dt> <dd>

裝置類別。

</dd> <dt>

*uSubCategory* \[在\]
</dt> <dd>

裝置子類別。

</dd> <dt>

*pCallbackCoNtext* \[在中，選擇性\]
</dt> <dd>

選用的內容指標，會傳遞給 *pfnCallback* 參數中指定的回呼函數。

</dd> <dt>

*pfnCallback* \[在\]
</dt> <dd>

只要有應用程式的通知，就會呼叫回呼函式的指標。 可傳送的通知會在 [ [**WFD \_ 顯示 \_ 接收 \_ 通知 \_ 回呼**](wfd-display-sink-notification-callback.md)] 中描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值可能是下列其中一個傳回碼。



| 傳回碼                                                                                          | Description                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**\_不 \_ 支援的錯誤**</dt> </dl> | 此硬體不支援顯示接收。<br/> |



 

## <a name="remarks"></a>備註

此函式會執行下列工作：

-   讓電腦可供探索
-   設定 P2P 裝置資訊以反映指定的類別和子類別
-   將所有 Wi-Fi 直接畫面上的 Miracast 設定為接收的裝置類型
-   註冊要在有連入連線時叫用的指定回呼

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows 10<br/>                                                                      |
| 伺服器支援結束<br/>    | Windows Server 2016<br/>                                                             |
| 標頭<br/>                   | <dl> <dt>Wfdsink。h</dt> </dl>       |
| 程式庫<br/>                  | <dl> <dt>Wifidisplay .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WFD \_ 顯示 \_ 接收 \_ 通知 \_ 回呼**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




