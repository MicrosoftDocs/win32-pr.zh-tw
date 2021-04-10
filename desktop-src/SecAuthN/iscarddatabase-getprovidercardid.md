---
description: GetProviderCardId 方法會為指定的智慧卡抓取主要服務提供者的識別碼 (GUID) 。
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: 'ISCardDatabase：： GetProviderCardId 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f361e83431fa7c6e0a0c2c0ea363bef7e487738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694524"
---
# <a name="iscarddatabasegetprovidercardid-method"></a>ISCardDatabase：： GetProviderCardId 方法

\[**GetProviderCardId** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**GetProviderCardId** 方法會為指定的 [*智慧卡*](../secgloss/s-gly.md)抓取 [*主要服務提供者*](../secgloss/p-gly.md)的識別碼 (GUID) 。

## <a name="syntax"></a>語法


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrCardName* \[在\]
</dt> <dd>

智慧卡的名稱。

</dd> <dt>

*ppguidProviderId* \[擴展\]
</dt> <dd>

如果成功，則為主要服務提供者識別碼 (GUID) 的指標;如果作業失敗，則 **為 Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                              |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *ppguidProviderId* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                                  |



 

## <a name="remarks"></a>備註

若要列出智慧卡的介面，請呼叫 [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)。

為了取得所有已知的 [*智慧卡*](../secgloss/s-gly.md)， [*讀取器*](../secgloss/r-gly.md) 和 [*讀取器群組*](../secgloss/r-gly.md) 會分別呼叫 [**ListCards**](iscarddatabase-listcards.md)、 [**ListReaders**](iscarddatabase-listreaders.md)和 [**ListReaderGroups**](iscarddatabase-listreadergroups.md) 。

如需此介面所提供的所有方法清單，請參閱 [**ISCardDatabase**](iscarddatabase.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例示範如何為指定的智慧卡取得主要服務提供者的識別碼。


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
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

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
