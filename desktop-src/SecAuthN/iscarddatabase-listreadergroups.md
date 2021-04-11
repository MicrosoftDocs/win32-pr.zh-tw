---
description: ListReaderGroups 方法會抓取智慧卡資料庫中註冊的讀者群組名稱。
ms.assetid: 81f6356a-92eb-4d27-abfe-e4a32de14d1c
title: 'ISCardDatabase：： ListReaderGroups 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaderGroups
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 00753b0ca3964dc5a35e26db0eec2aedda4d2511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113209"
---
# <a name="iscarddatabaselistreadergroups-method"></a>ISCardDatabase：： ListReaderGroups 方法

\[**ListReaderGroups** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ListReaderGroups** 方法會抓取智慧卡資料庫中註冊的 [*讀者群組*](../secgloss/r-gly.md)名稱。

## <a name="syntax"></a>語法


```C++
HRESULT ListReaderGroups(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaderGroups
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*localeId* \[在\]
</dt> <dd>

語言當地語系化識別碼。

</dd> <dt>

*ppReaderGroups* \[擴展\]
</dt> <dd>

Bstr 之 SAFEARRAY 的指標，其中包含符合搜尋參數的智慧卡讀取器群組名稱（如果成功）;如果作業失敗，則 **為 Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                            |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *ppReaderGroups* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                                |



 

## <a name="remarks"></a>備註

若要取出所有已知的 [*智慧卡*](../secgloss/s-gly.md) 或 [*讀取器*](../secgloss/r-gly.md)，請分別呼叫 [**ListCards**](iscarddatabase-listcards.md) 或 [**ListReaders**](iscarddatabase-listreaders.md) 。

分別取得 [*主要服務提供者*](../secgloss/p-gly.md) 或特定卡片 [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) 或 [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) 的介面。

如需此介面所提供的所有方法清單，請參閱 [**ISCardDatabase**](iscarddatabase.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例顯示如何抓取智慧卡資料庫中註冊的讀者群組名稱。


```C++
LPSAFEARRAY pGroups = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaderGroups(0x0409,  // English (US)
                                    &pGroups);
if (FAILED(hr))
{
   printf("Failed ListReaderGroups\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardmgr。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardmgr .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardDatabase 定義為1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetProviderCardId**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
