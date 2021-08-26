---
description: ListCards 方法會將符合指定介面識別碼的所有智慧卡名稱， (Guid) 、指定的 ATR 字串或兩者。
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'ISCardDatabase：： ListCards 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c34d5d1449b2ef8f34fa87d3a70ecf37787d423a0d5df71ecd15e5f722d112ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014528"
---
# <a name="iscarddatabaselistcards-method"></a>ISCardDatabase：： ListCards 方法

\[**ListCards** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ListCards** 方法會將符合指定介面識別碼的所有智慧卡名稱， (guid) 、指定的 [*ATR 字串*](../secgloss/a-gly.md)或兩者。

## <a name="syntax"></a>語法


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAtr* \[在\]
</dt> <dd>

[*智慧卡*](../secgloss/s-gly.md)ATR 字串的指標。 ATR 字串必須封裝成 [**IByteBuffer**](ibytebuffer.md)。

</dd> <dt>

*pInterfaceGuids* \[在\]
</dt> <dd>

COM 介面識別碼之 SAFEARRAY 的指標， (Guid) BSTR 格式。

</dd> <dt>

*localeId* \[在\]
</dt> <dd>

語言當地語系化識別碼。

</dd> <dt>

*ppCardNames* \[擴展\]
</dt> <dd>

Bstr 之 SAFEARRAY 的指標，其中包含符合搜尋參數的智慧卡名稱（如果成功的話）;如果作業失敗，則 **為 Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | 描述                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入了錯誤指標。<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

若要取出所有已知的 [*讀取*](../secgloss/r-gly.md) 器或 [*讀取器*](../secgloss/r-gly.md)，請分別呼叫 [**ListReaders**](iscarddatabase-listreaders.md) 或 [**ListReaderGroups**](iscarddatabase-listreadergroups.md) 。

分別取出特定卡片 [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)或 [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)的 [*主要服務*](../secgloss/p-gly.md)或介面。

如需此介面所提供的所有方法清單，請參閱 [**ISCardDatabase**](iscarddatabase.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例顯示如何抓取符合指定 ATR 字串的智慧卡名稱。


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
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

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
