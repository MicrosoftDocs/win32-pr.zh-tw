---
description: 驗證已簽署檔案的簽章，並取得檔案的雜湊值和演算法識別碼。
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: WTHelperGetFileHash 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: a136aaf0b5c8bbf860fa27c9b439cae89a74e5149698e4841b38cdb8d9e4f6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970479"
---
# <a name="wthelpergetfilehash-function"></a>WTHelperGetFileHash 函式

\[**WTHelperGetFileHash** 函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

**WTHelperGetFileHash** 函式會驗證已簽署檔案的簽章，並取得檔案的雜湊值和演算法識別碼。

> [!Note]  
> 未在已發行的標頭檔中宣告此函式。 若要使用此函式，請使用所示的確切格式來宣告。 此函數也沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Wintrust.dll。

 

## <a name="syntax"></a>語法


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszFilename* \[在\]
</dt> <dd>

以 null 終止的 Unicode 字串指標，其中包含要取得雜湊之檔案的路徑和檔案名。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

未使用此參數，且應為零。

</dd> <dt>

*pvReserved* \[in、out、optional\]
</dt> <dd>

未使用此參數，且應為 **Null**。

</dd> <dt>

*pbFileHash* \[out、optional\]
</dt> <dd>

緩衝區的指標，用來接收檔案的雜湊值。 *PcbFileHash* 參數包含這個緩衝區的大小。

</dd> <dt>

*pcbFileHash* \[in、out、optional\]
</dt> <dd>

**DWORD** 變數的指標，該變數在輸入時會包含 *pbFileHash* 緩衝區的大小（以位元組為單位），而在輸出時則會接收雜湊值的大小（以位元組為單位）。

若要取得雜湊值所需的大小，請針對 *pbFileHash* 參數傳遞 **Null** 。 此函式會將所需的大小（以位元組為單位）放在此位置中的雜湊值。

如果 *pbFileHash* 參數不是 **Null**，而且大小不夠大，無法接收雜湊值，則此函式會將所需的大小（以位元組為單位）放在此位置，並傳回 **錯誤的 \_ \_ 資料**。

</dd> <dt>

*pHashAlgid* \[out、optional\]
</dt> <dd>

要接收用來建立雜湊值之演算法識別碼的 [**ALG \_**](alg-id.md) 識別碼變數指標。 如果不需要這項資訊，則此參數可以是 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回表示函式成功或失敗的狀態碼。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼                                                                                               | 描述                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 成功**</dt> </dl>             | 檔案已簽署，並已驗證簽章。<br/>                                                                                        |
| <dl> <dt>**錯誤 \_ 的 \_ 資料**</dt> </dl>          | *PbFileHash* 參數不是 **Null**，而且 *pcbFileHash* 參數所指定的大小不夠大，無法接收雜湊。<br/> |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl> | 發生記憶體配置失敗。<br/>                                                                                                      |
| <dl> <dt>**信任 \_ 電子 \_ 不良 \_ 摘要**</dt> </dl>      | 未驗證檔案的簽章。<br/>                                                                                                |
| <dl> <dt>**信任 \_ 電子 \_ NOSIGNATURE**</dt> </dl>      | 檔案未簽署或簽章無效。<br/>                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
