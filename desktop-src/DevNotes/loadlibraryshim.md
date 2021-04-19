---
description: 載入指定版本的 .NET Framework 程式庫 DLL。
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: LoadLibraryShim 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982275"
---
# <a name="loadlibraryshim-function"></a>LoadLibraryShim 函式

載入指定版本的 .NET Framework 程式庫 DLL。

## <a name="syntax"></a>語法


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szDllName* \[在\]
</dt> <dd>

要從 .NET Framework 載入的 DLL 名稱。

</dd> <dt>

*szVersion* \[在\]
</dt> <dd>

要載入的 DLL 版本。 如果 *szVersion* 為 **Null**，則會載入指定 DLL 的最新版本。

</dd> <dt>

*pvReserved* 
</dt> <dd>

保留的。

</dd> <dt>

*phModDll* \[擴展\]
</dt> <dd>

模組的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個函式是用來載入 .NET Framework 可轉散發套件所包含的程式庫 Dll，而不是使用者產生的 Dll。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll</dt> </dl> |



 

 
