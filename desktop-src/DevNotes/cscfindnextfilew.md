---
description: 繼續進行檔案搜尋作業。
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: CSCFindNextFileW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindNextFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 50b387a1ff99a95fcbe0fae8fe8ad93d14c335b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995330"
---
# <a name="cscfindnextfilew-function"></a>CSCFindNextFileW 函式

\[這項功能不受支援，因此不應該使用。\]

繼續進行檔案搜尋作業。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CSCFindNextFileW(
  _In_  HANDLE           hFind,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _In_  FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFind* \[在\]
</dt> <dd>

[**CSCFindFirstFileW**](cscfindfirstfilew.md)函數所傳回的搜尋控制碼。

</dd> <dt>

*lpFind32* \[擴展\]
</dt> <dd>

[**WIN32 \_ 尋找 \_ 資料**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa)結構的指標，此結構會接收檔案或子目錄的相關資訊。

</dd> <dt>

*lpdwStatus* \[擴展\]
</dt> <dd>

表示撥號狀態的 NTSTATUS 程式碼。

</dd> <dt>

*lpdwPinCount* \[擴展\]
</dt> <dd>

如果檔案已離線提供，則此參數為非零，否則為0。

</dd> <dt>

*lpdwHintFlags* \[擴展\]
</dt> <dd>

此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                | 意義                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**旗 \_ 標CSC \_ 提示 \_ PIN \_ 使用者**</dt> <dt>0x01</dt> </dl>                                | 使用者使檔案可離線使用。<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**旗 \_ 標CSC \_ 提示 \_ PIN \_ 繼承 \_ 使用者**</dt> <dt>0x02</dt> </dl>       | 使用者已讓父代可離線使用，並標示父系，使其子系可供離線使用。<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**旗 \_ 標CSC \_ 提示 \_ PIN \_ 繼承 \_ 系統**</dt> <dt>0x04</dt> </dl> | 系統管理員或群組原則已讓父系可離線使用，並標示父系，使其子系可供離線使用。<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**旗 \_ 標CSC \_ 提示 \_ 針腳 \_ 系統**</dt> <dt>0x10</dt> </dl>                          | 系統管理員或群組原則已讓檔案可離線使用。<br/>                                                                      |



 

</dd> <dt>

*lpOrgFileTime* \[在\]
</dt> <dd>

要接收檔案或子目錄之日期和時間資訊的 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
