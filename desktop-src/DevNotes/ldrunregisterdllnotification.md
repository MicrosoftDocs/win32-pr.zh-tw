---
description: 取消先前藉由呼叫 LdrRegisterDllNotification 函式註冊的 DLL 載入通知。
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: LdrUnregisterDllNotification 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385856"
---
# <a name="ldrunregisterdllnotification-function"></a>LdrUnregisterDllNotification 函式

\[您可以在不另行通知的情況下，從 Windows 變更或移除此功能。\]

取消先前藉由呼叫 [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) 函式註冊的 DLL 載入通知。

## <a name="syntax"></a>語法


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Cookie* \[在\]
</dt> <dd>

從註冊通知的 [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) 呼叫所接收到的回呼識別碼指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **NTSTATUS** 或錯誤碼。

如果函式成功，則會傳回 **狀態 \_ 成功**。

如果找不到回呼函式，函數會傳回 **\_ \_ \_ 找不到的狀態 DLL**。

在 WDK 中可用的 Ntstatus 標頭檔中，會列出 **ntstatus** 錯誤碼的表單和重要性，並會在 wdk 檔中說明。

## <a name="remarks"></a>備註

此函數沒有相關聯的標頭檔。 相關聯的匯入程式庫（Ntdll.dll）可在 WDK 中使用。 您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，動態連結至 Ntdll.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> </dl>

 

 
