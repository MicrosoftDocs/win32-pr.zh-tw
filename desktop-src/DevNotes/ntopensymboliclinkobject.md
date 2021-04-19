---
description: 開啟現有的符號連結。
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: NtOpenSymbolicLinkObject 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994742"
---
# <a name="ntopensymboliclinkobject-function"></a>NtOpenSymbolicLinkObject 函式

\[這項功能可能會在未來變更或無法使用。\]

開啟現有的符號連結。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*LinkHandle* \[擴展\]
</dt> <dd>

新開啟的符號連結物件的控制碼。

</dd> <dt>

*DesiredAccess* \[在\]
</dt> <dd>

[**存取 \_ 遮罩**](../secauthz/access-mask.md)，指定要求的目錄物件存取權。 一般會使用一般讀取， \_ 以便將控制碼傳遞至 [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) 函式。

</dd> <dt>

*ObjectAttributes* \[在\]
</dt> <dd>

目錄物件的屬性。 若要初始化 **物件 \_ 屬性** 結構，請使用 **InitializeObjectAttributes** 宏。 如果呼叫端不是在系統執行緒內容中執行，它必須在初始化結構時指定 **OBJ \_ 核心 \_ 控制碼** 旗標。 如需詳細資訊，請參閱 WDK 檔中的這些專案的說明文件。

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

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
