---
description: 將私密金鑰和其對應的公開金鑰儲存至指定的檔案。
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: PvkPrivateKeySave 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988896"
---
# <a name="pvkprivatekeysave-function"></a>PvkPrivateKeySave 函式

> [!IMPORTANT]
> 此 API 即將淘汰。 Microsoft 可能會在未來的版本中移除此 API。

 

**PvkPrivateKeySave** 函式會將 [*私密金鑰*](../secgloss/p-gly.md)和其對應的 [*公開金鑰*](../secgloss/p-gly.md)儲存至指定的檔案。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCryptProv* \[在\]
</dt> <dd>

[*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的控制碼。

</dd> <dt>

*hFile* \[在\]
</dt> <dd>

以初始讀取/寫入權限和後續唯讀許可權建立之檔案的控制碼。

</dd> <dt>

*dwKeySpec* \[在\]
</dt> <dd>

索引鍵類型的長整數。 可能的值包括 **在 \_ KEYEXCHANGE** **或簽 \_** 章。

</dd> <dt>

*hwndOwner* \[在\]
</dt> <dd>

如果需要密碼來加密私密金鑰，此參數是對話方塊父系的控制碼;否則，它會是 **Null**。

</dd> <dt>

*pwszKeyName* \[在\]
</dt> <dd>

要儲存的索引鍵名稱之以 null 結束的字串指標。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定函數其他選項的 **DWORD** 值。 如需詳細資訊，請參閱 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)中的 *dwFlags* 參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，此函數會傳回 **TRUE**。 如果失敗， **PvkPrivateKeySave** 函數會傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
