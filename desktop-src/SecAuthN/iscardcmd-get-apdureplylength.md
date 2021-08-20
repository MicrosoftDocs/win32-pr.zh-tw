---
description: 判斷應用程式通訊協定資料單位) 的長度 (（以位元組為單位） (APDU) 。
ms.assetid: 25011db1-a037-4764-b700-8ad2200419da
title: 'ISCardCmd：： get_ApduReplyLength 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReplyLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bb08be6ad4e916a6dc7b1521dee7aac2dcac55c2bd0ac541278c9e00e34b6ed0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577688"
---
# <a name="iscardcmdget_apdureplylength-method"></a>ISCardCmd：： get \_ ApduReplyLength 方法

\[**Get \_ ApduReplyLength** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Get \_ ApduReplyLength** 方法會決定 [*應用程式協定資料單位*](../secgloss/a-gly.md)) 的長度 (（以位元組為單位）， (APDU) 。

## <a name="syntax"></a>語法


```C++
HRESULT get_ApduReplyLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*plSize* \[擴展\]
</dt> <dd>

回復 APDU 訊息大小的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | 描述                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PlSize* 參數無效。<br/>  |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *plSize* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                        |



 

## <a name="remarks"></a>備註

若要取得現有的回復 APDU，請呼叫 [**get \_ ApduReply**](iscardcmd-get-apdureply.md)。

如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例示範如何取出 [*回復 APDU*](../secgloss/r-gly.md)的長度。 此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU reply length.
hr = pISCardCmd->get_ApduReplyLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduReplyLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scarddat。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scarddat .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**取得 \_ ApduReply**](iscardcmd-get-apdureply.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ ApduReply**](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
