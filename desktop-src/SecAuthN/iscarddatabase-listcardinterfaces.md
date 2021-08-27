---
description: ListCardInterfaces 方法會抓取指定智慧卡支援的所有介面 (Guid) 識別碼。
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'ISCardDatabase：： ListCardInterfaces 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b97569f967c76c985eb05099a21ed10e90456563a871f3e5d9803c6a5875ebdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008106"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a>ISCardDatabase：： ListCardInterfaces 方法

\[**ListCardInterfaces** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**ListCardInterfaces** 方法會抓取指定 [*智慧卡*](../secgloss/s-gly.md)支援的所有介面 (guid) 識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrCardName* \[在\]
</dt> <dd>

智慧卡的名稱。

</dd> <dt>

*ppInterfaceGuids* \[擴展\]
</dt> <dd>

如果成功，則為介面 Guid 的指標;如果作業失敗，則 **為 Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | 描述                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                              |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *ppInterfaceGuids* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                                  |



 

## <a name="remarks"></a>備註

若要取出智慧卡的 [*主要服務提供者*](../secgloss/p-gly.md) ，請呼叫 [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)。

若要取出所有已知的 [*智慧卡*](../secgloss/s-gly.md)、 [*讀取器*](../secgloss/r-gly.md)和 [*讀取器群組*](../secgloss/r-gly.md) ，請分別呼叫 [**ListCards**](iscarddatabase-listcards.md)、 [**ListReaders**](iscarddatabase-listreaders.md)和 [**ListReaderGroups**](iscarddatabase-listreadergroups.md) 。

如需此介面所提供的所有方法清單，請參閱 [**ISCardDatabase**](iscarddatabase.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例將示範如何取得所指定智慧卡所支援之介面的識別碼。


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
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

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
