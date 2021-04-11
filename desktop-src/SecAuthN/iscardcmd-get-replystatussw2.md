---
description: 抓取回復 APDU SW2 狀態位元組。
ms.assetid: 24ad0164-84fc-4a99-b9dd-0f7d789dff92
title: 'ISCardCmd：： get_ReplyStatusSW2 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7ff503758a50437b4b7ff974fe4455d4b92ce978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113216"
---
# <a name="iscardcmdget_replystatussw2-method"></a>ISCardCmd：： get \_ ReplyStatusSW2 方法

\[**Get \_ ReplyStatusSW2** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Get \_ ReplyStatusSW2** 方法會抓取 [*回復 APDU*](../secgloss/r-gly.md) SW2 狀態位元組。

## <a name="syntax"></a>語法


```C++
HRESULT get_ReplyStatusSW2(
  [out] LPBYTE pbySW2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbySW2* \[擴展\]
</dt> <dd>

傳回時，包含 SW2 位元組值的位元組指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PbySW2* 無效。<br/>            |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *pbySW2* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                        |



 

## <a name="remarks"></a>備註

回復 APDU 的 SW2 狀態位元組是唯讀的。

若要取得回復 APDU 的 SW1 狀態位元組，請呼叫 [**get \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)。

如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例示範如何取出 [*回復 APDU*](../secgloss/r-gly.md)的 SW2 狀態位元組。 此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。


```C++
BYTE     bySW2;
HRESULT  hr;

// Retrieve the reply status SW2 byte.
hr = pISCardCmd->get_ReplyStatusSW2(&bySW2);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW2\n");
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
| 標頭<br/>                   | <dl> <dt>Scarddat。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scarddat .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**取得 \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)
</dt> <dt>

[**取得 \_ ReplyStatus**](iscardcmd-get-replystatus.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
