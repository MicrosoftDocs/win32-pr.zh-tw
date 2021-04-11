---
description: 在第一次載入 DLL 時註冊通知。 這是在動態連結進行之前發生的通知。
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: LdrRegisterDllNotification 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025833"
---
# <a name="ldrregisterdllnotification-function"></a>LdrRegisterDllNotification 函式

\[您可以在不另行通知的情況下，從 Windows 變更或移除此功能。\]

在第一次載入 DLL 時註冊通知。 這是在動態連結進行之前發生的通知。

## <a name="syntax"></a>語法


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

此參數必須為零。

</dd> <dt>

*NotificationFunction* \[在\]
</dt> <dd>

載入 DLL 時要呼叫之 [*LdrDllNotification*](ldrdllnotification.md) 通知回呼函數的指標。

</dd> <dt>

*內容* \[在中，選擇性\]
</dt> <dd>

回呼函數的內容資料指標。

</dd> <dt>

*Cookie* \[擴展\]
</dt> <dd>

變數的指標，用來接收回呼函數的識別碼。 此識別碼是用來取消註冊通知回呼函式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回 **狀態 \_ 成功**。

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

[*LdrDllNotification*](ldrdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
