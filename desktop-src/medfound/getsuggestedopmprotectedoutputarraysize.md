---
description: 取得在呼叫 CreateOPMProtectedOutputs 之前，應該配置的陣列大小。
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: GetSuggestedOPMProtectedOutputArraySize 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: c84738fe37661d2a593432b571c6022b0369e28ee3b2a3cb028b8eb84276a21a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879375"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a>GetSuggestedOPMProtectedOutputArraySize 函式

> [!IMPORTANT]
> [輸出保護管理員](output-protection-manager.md)會使用此函式 (OPM) 來存取顯示驅動程式中的功能。 應用程式不應該呼叫此函式。

 

取得在呼叫 [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)之前，應該配置的陣列大小。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pstrDeviceName* \[在\]
</dt> <dd>

[**UNICODE \_ 字串**](/windows/win32/api/subauth/ns-subauth-unicode_string)結構的指標，其中包含 [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)函式所傳回之顯示裝置的名稱。

</dd> <dt>

*pdwSuggestedOPMProtectedOutputArraySize* \[擴展\]
</dt> <dd>

接收應配置給陣列的大小，以陣列元素的數目為限。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **狀態 \_ 成功**。 否則，它會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫。 若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Gdi32.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[OPM 函式](opm-functions.md)
</dt> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> </dl>

 

 
