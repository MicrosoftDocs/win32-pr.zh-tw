---
description: 驗證單一類別目錄檔案。
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: VerifyCatalogFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992381"
---
# <a name="verifycatalogfile-function"></a>VerifyCatalogFile 函式

\[這項功能不受支援，因此不應該使用。\]

驗證單一類別目錄檔案。

## <a name="syntax"></a>語法


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CatalogFullPath* 
</dt> <dd>

要驗證之類別目錄檔案的完整路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回 **錯誤 \_ 成功**; 否則，它會從 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)傳回錯誤。

如果目錄是 Authenticode 簽署的目錄，則此函式會在成功時傳回 **錯誤 \_ authenticode \_ 受信任 \_ 發行者** ; 否則，它會傳回 **錯誤 \_ authenticode \_ 信任 \_ 未 \_ 建立**。

如果函式無法判斷發行者是否受信任，則可能也會傳回 **錯誤 \_ 不明 \_ 錯誤**。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
