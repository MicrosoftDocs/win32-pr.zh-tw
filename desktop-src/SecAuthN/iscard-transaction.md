---
description: " (應用程式協定資料單位) 物件，執行智慧卡命令的寫入和讀取作業。"
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'ISCard：： Transaction 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993034"
---
# <a name="iscardtransaction-method"></a>ISCard：： Transaction 方法

\[**交易** 方法可用於 [需求] 區段中指定的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**交易** 方法會在 [*智慧卡*](../secgloss/s-gly.md)命令 ([*應用程式協定資料單位*](../secgloss/a-gly.md)) 物件上執行寫入和讀取作業。 在此函式傳回之後，將可存取智慧卡中為傳送至智慧卡之卡片中所定義之命令字串的回復字串。

## <a name="syntax"></a>語法


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppCmd* \[in、out\]
</dt> <dd>

智慧卡命令物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業已成功完成。<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PpCmd* 參數無效。<br/>           |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *ppCmd* 中傳遞了錯誤指標。<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 無法取得滿足要求的記憶體。<br/> |



 

## <a name="remarks"></a>備註

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例顯示在智慧卡命令物件上執行寫入和讀取作業。


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
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
| IID<br/>                      | IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**中斷連結**](iscard-detach.md)
</dt> <dt>

[**取得 \_ Atr**](iscard-get-atr.md)
</dt> <dt>

[**取得 \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**取得 \_ 內容**](iscard-get-context.md)
</dt> <dt>

[**取得 \_ 通訊協定**](iscard-get-protocol.md)
</dt> <dt>

[**取得 \_ 狀態**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**LockSCard**](iscard-lockscard.md)
</dt> <dt>

[**附加**](iscard-reattach.md)
</dt> <dt>

[**UnlockSCard**](iscard-unlockscard.md)
</dt> </dl>

 

 
