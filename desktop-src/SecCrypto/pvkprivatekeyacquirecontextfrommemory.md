---
description: 在密碼編譯服務提供者 (CSP) 中建立暫存容器，並將私密金鑰從記憶體載入至容器。
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: PvkPrivateKeyAcquireCoNtextFromMemory 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320371"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a>PvkPrivateKeyAcquireCoNtextFromMemory 函式

> [!IMPORTANT]
> 此 API 即將淘汰。 Microsoft 可能會在未來的版本中移除此 API。

 

**PvkPrivateKeyAcquireCoNtextFromMemory** 函式會在 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 中建立暫存容器，並將 [*私密金鑰*](../secgloss/p-gly.md)從記憶體載入至容器。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszProvName* \[在\]
</dt> <dd>

以 null 結束的字串指標，其中包含在 *dwProvType* 中要求其類型的 CSP 名稱。

</dd> <dt>

*dwProvType* \[在\]
</dt> <dd>

CSP 類型的 **DWORD** 值。 如需 CSP 類型的詳細資訊，請參閱 [密碼編譯提供者類型](cryptographic-provider-types.md)。

</dd> <dt>

*>pbdata* \[在\]
</dt> <dd>

接收內容資料之緩衝區的指標。 呼叫端必須提供此資源。

</dd> <dt>

*cbData* \[在\]
</dt> <dd>

**DWORD** 值，指定 *>pbdata* 緩衝區的大小（以位元組為單位）。 呼叫端必須提供此值。

</dd> <dt>

*hwndOwner* \[在\]
</dt> <dd>

如果需要密碼來解密 *>pbdata* 參數所指向的內容資料，這個參數就是對話方塊父系的控制碼;否則，它會是 **Null**。

</dd> <dt>

*pwszKeyName* \[在\]
</dt> <dd>

以 null 結束的字串指標，其中包含要取出的索引鍵名稱。

</dd> <dt>

*pdwKeySpec* \[in、out、optional\]
</dt> <dd>

**DWORD** 值的指標，指定索引鍵的類型。 可能的值包括 **在 \_ KEYEXCHANGE** **或簽 \_** 章。

</dd> <dt>

*phCryptProv* \[擴展\]
</dt> <dd>

CSP 的控制碼指標。

</dd> <dt>

*ppwszTmpContainer* \[擴展\]
</dt> <dd>

暫存容器名稱之以 null 結束的字串指標的位址。 **PvkPrivateKeyAcquireCoNtextFromMemory** 函式會提供這個字串的緩衝區，並將其初始化。 呼叫 **PvkPrivateKeyAcquireCoNtextFromMemory** 時，位址應該指向 **Null** 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，此函數會傳回 **TRUE**。 如果失敗， **PvkPrivateKeyAcquireCoNtextFromMemory** 函數會傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
