---
description: 清除目前開啟的會話或目前開啟的會話的狀態。
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: 'WFDDisplaySinkCloseSession 函式 (Wfdsink) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512768"
---
# <a name="wfddisplaysinkclosesession-function"></a>WFDDisplaySinkCloseSession 函式

清除目前開啟的會話或目前開啟的會話的狀態。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSessionHandle* \[在\]
</dt> <dd>

透過最新的 [**WFD \_ 顯示接收 \_ \_ 通知 \_ 回呼回呼**](wfd-display-sink-notification-callback.md) 的控制碼，其中包含一個。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

## <a name="remarks"></a>備註

基於任何原因，您的應用程式可以呼叫此函式來終止 Miracast 會話。 當您的應用程式在其回呼中收到 **DisconnectedNotification** 類型時，不需要呼叫它。

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

 

 




