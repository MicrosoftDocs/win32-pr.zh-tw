---
description: 下載 .cab 檔簽章、驗證與封裝相關聯的許可權，並根據驗證執行。
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: DownloadJAVAEX 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999359"
---
# <a name="downloadjavaex-function"></a>DownloadJAVAEX 函式

下載 .cab 檔簽章、驗證與封裝相關聯的許可權，並根據驗證執行。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*保留* \[在\]
</dt> <dd>

此參數已保留備用。

</dd> <dt>

*pProviderData* \[在\]
</dt> <dd>

包含憑證資料的 [**CRYPT \_ 提供者 \_ 資料**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) 結構，例如檔案和區域許可權。

</dd> <dt>

*pJAVA* \[在\]
</dt> <dd>

[**JAVA \_ 原則 \_ 提供者**](/previous-versions//bb432350(v=vs.85))結構，其中包含與原則提供者相關的資料。

</dd> <dt>

*pFunctions* \[在\]
</dt> <dd>

[**CRYPT \_ 提供者 \_**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions)函式結構，其中包含驗證憑證物件、簽章和最終原則的方法清單。

</dd> <dt>

*fCertificate* \[在\]
</dt> <dd>

如果有憑證存在，此參數為 **TRUE**。 否則為 **FALSE**。

</dd> <dt>

*pTrust* \[在\]
</dt> <dd>

[**JAVA \_ 信任**](/windows/desktop/api/Capi/ns-capi-java_trust)結構，包含信任資訊，例如編碼的許可權、編碼器簽章和真實的傳回原則代碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 **S \_ OK**。 否則，傳回值會是錯誤碼。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Javacypt.dll</dt> </dl> |



 

 
