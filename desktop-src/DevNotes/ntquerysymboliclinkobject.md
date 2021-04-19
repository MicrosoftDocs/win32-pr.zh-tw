---
description: 抓取符號連結的目標。
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: NtQuerySymbolicLinkObject 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994627"
---
# <a name="ntquerysymboliclinkobject-function"></a>NtQuerySymbolicLinkObject 函式

\[這項功能可能會在未來變更或無法使用。\]

抓取符號連結的目標。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*LinkHandle* \[在\]
</dt> <dd>

符號連結物件的控制碼。

</dd> <dt>

*LinkTarget* \[in、out\]
</dt> <dd>

已初始化的 Unicode 字串指標，該字串會接收符號連結的目標。 如果呼叫失敗，就必須設定 **MaximumLength** 和 **Buffer** 成員。

</dd> <dt>

*ReturnedLength* \[out、optional\]
</dt> <dd>

變數的指標，此變數會接收 *LinkTarget* 參數中所傳回之 Unicode 字串的長度。 如果函數傳回的 **狀態 \_ 緩衝區 \_ 太 \_ 小**，此變數會接收所需的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回 **狀態 \_ 成功** 或錯誤狀態。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NtOpenSymbolicLinkObject**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
