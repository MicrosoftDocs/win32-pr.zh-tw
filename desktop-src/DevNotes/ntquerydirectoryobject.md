---
description: 抓取指定目錄物件的相關資訊。
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: NtQueryDirectoryObject 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000715"
---
# <a name="ntquerydirectoryobject-function"></a>NtQueryDirectoryObject 函式

\[這項功能可能會在未來變更或無法使用。\]

抓取指定目錄物件的相關資訊。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DirectoryHandle* \[在\]
</dt> <dd>

目錄物件的控制碼。

</dd> <dt>

*緩衝區* \[out、optional\]
</dt> <dd>

接收目錄資訊的緩衝區指標。 這個緩衝區會接收一或多個 **物件 \_ 目錄 \_ 資訊** 結構，最後一個是 **Null**，後面接著包含目錄專案名稱的字串。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

*長度* \[在\]
</dt> <dd>

使用者提供的輸出緩衝區大小（以位元組為單位）。

</dd> <dt>

*ReturnSingleEntry* \[在\]
</dt> <dd>

指出函數是否只傳回單一專案。

</dd> <dt>

*RestartScan* \[在\]
</dt> <dd>

指出是否要使用 *內容* 參數中傳遞的資訊，重新開機掃描或繼續列舉。

</dd> <dt>

*內容* \[in、out\]
</dt> <dd>

列舉內容。

</dd> <dt>

*ReturnLength* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收輸出緩衝區中傳回之目錄資訊的長度（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回 **狀態 \_ 成功** 或錯誤狀態。

## <a name="remarks"></a>備註

以下是 **物件 \_ 目錄 \_ 資訊** 結構的定義。

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NtOpenDirectoryObject**](ntopendirectoryobject.md)
</dt> </dl>

 

 
