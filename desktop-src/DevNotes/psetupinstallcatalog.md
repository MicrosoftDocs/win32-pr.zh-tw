---
description: 安裝類別目錄檔案。
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: pSetupInstallCatalog 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996210"
---
# <a name="psetupinstallcatalog-function"></a>pSetupInstallCatalog 函式

\[Microsoft 不再支援此功能。 開發人員應使用 **CryptCATAdminAddCatalog**。\]

安裝類別目錄檔案。

## <a name="syntax"></a>語法


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CatalogFullPath* \[在\]
</dt> <dd>

要安裝在系統上之目錄的完整路徑。

</dd> <dt>

*NewBaseName* \[在\]
</dt> <dd>

將類別目錄檔案複製到目錄存放區時要使用的新基底名稱。

</dd> <dt>

*NewCatalogFullPath* \[out、optional\]
</dt> <dd>

（選擇性）在目錄存放區內接收目錄檔案的完整路徑。 此緩衝區應至少為 (ANSI 版本) 的 **最大 \_ 路徑** 位元組，或 Unicode 版本)  (的字元數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則不會傳回 **任何 \_ 錯誤**，否則會傳回 Win32 錯誤碼，指出失敗的原因。

## <a name="remarks"></a>備註

系統會將檔案複製到特殊目錄，並選擇性地重新命名。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CryptCATAdminAddCatalog**](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
