---
description: 使用標準作業系統程式碼簽署原則（例如驅動程式簽署）來驗證單一類別目錄檔案。
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: pSetupVerifyCatalogFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995618"
---
# <a name="psetupverifycatalogfile-function"></a>pSetupVerifyCatalogFile 函式

\[Microsoft 不再支援此功能。 若為 INF 檔案 (裝置安裝) ，開發人員應該使用 **SetupVerifyInfFile**。 若要驗證非 INF 型類別目錄，請使用 **WinVerifyTrust**。\]

使用標準作業系統程式碼簽署原則（例如驅動程式簽署）來驗證單一類別目錄檔案。

## <a name="syntax"></a>語法


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CatalogFullPath* \[在\]
</dt> <dd>

要驗證之類別目錄檔案的完整路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回 **錯誤 \_ 成功**; 否則，它會從 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)傳回錯誤。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SetupVerifyInfFile**](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
