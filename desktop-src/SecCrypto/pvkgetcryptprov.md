---
description: 根據私密金鑰檔案或金鑰容器名稱，取得密碼編譯服務提供者 (CSP) 的控制碼。
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: PvkGetCryptProv 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852884"
---
# <a name="pvkgetcryptprov-function"></a>PvkGetCryptProv 函式

> [!IMPORTANT]
> 此 API 即將淘汰。 Microsoft 可能會在未來的版本中移除此 API。

 

**PvkGetCryptProv** 函式會根據 [*私密金鑰*](../secgloss/p-gly.md)檔案或金鑰容器名稱，取得 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的控制碼。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* \[在\]
</dt> <dd>

如果需要密碼來解密私密金鑰檔案，此參數是密碼對話方塊父系的控制碼;否則，它會是 **Null**。

</dd> <dt>

*pwszCaption* \[在\]
</dt> <dd>

對話方塊標題之以 null 結束的字串指標。

</dd> <dt>

*pwszCapiProvider* \[在\]
</dt> <dd>

CSP 名稱之以 null 結束的字串指標。

</dd> <dt>

*dwProviderType* \[在\]
</dt> <dd>

代表密碼編譯提供者類型的 **DWORD** 值。 如需詳細資訊，請參閱 [密碼編譯提供者類型](cryptographic-provider-types.md)。

</dd> <dt>

*pwszPvkFile* \[在\]
</dt> <dd>

以 null 結束的字串指標，其中包含私密金鑰檔案的名稱。

</dd> <dt>

*pwszKeyContainerName* \[在\]
</dt> <dd>

私密金鑰容器名稱之以 null 結束的字串指標。

</dd> <dt>

*pdwKeySpec* \[擴展\]
</dt> <dd>

*PhCryptProv* 和 *ppwszTmpContainer* 所傳回之容器的索引鍵類型的 **DWORD** 值指標。

</dd> <dt>

*ppwszTmpContainer* \[out、optional\]
</dt> <dd>

暫存金鑰容器名稱之以 null 結束的字串指標的位址。 **PvkGetCryptProv** 函式會提供並初始化暫存容器。 呼叫 **PvkGetCryptProv** 時，位址應該指向 **Null** 值。

</dd> <dt>

*phCryptProv* \[擴展\]
</dt> <dd>

CSP 的控制碼指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 **S \_ OK**。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

## <a name="remarks"></a>備註

**PvkGetCryptProv** 函式會先嘗試從 *pwszKeyContainerName* 參數所指定的金鑰容器名稱取得提供者控制碼。 如果您傳遞 **Null** 給 *PwszKeyContainerName* 參數， **PvkGetCryptProv** 會嘗試從 *pwszPvkFile* 參數中指定的私密金鑰檔案取得提供者。

當您完成使用 CSP 之後，請呼叫 [**PvkFreeCryptProv**](pvkfreecryptprov.md) 函式來釋出提供者控制碼和暫存金鑰容器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
