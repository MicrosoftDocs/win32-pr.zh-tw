---
description: 在目錄中安裝目錄。
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: InstallCatalog 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995414"
---
# <a name="installcatalog-function"></a>InstallCatalog 函式

\[這項功能不受支援，因此不應該使用。\]

在目錄中安裝目錄。

## <a name="syntax"></a>語法


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CatalogFullPath* \[在\]
</dt> <dd>

字串的指標，表示安裝之前的目錄完整路徑。

</dd> <dt>

*NewBaseName* \[在中，選擇性\]
</dt> <dd>

新基底名稱的指標。

</dd> <dt>

*NewCatalogFullPath* \[out、optional\]
</dt> <dd>

字串的指標，代表安裝之後目錄的完整路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式目前未執行，因此不會傳回實際值。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
