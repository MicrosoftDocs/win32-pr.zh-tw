---
description: 抓取回復 APDU，將它放在特定的位元組緩衝區中。
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'ISCardCmd：： get_ApduReply 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027532"
---
# <a name="iscardcmdget_apdureply-method"></a>ISCardCmd：： get \_ ApduReply 方法

\[**Get \_ ApduReply** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Get \_ ApduReply** 方法會抓取 [*回復 APDU*](../secgloss/r-gly.md)，並將其放在特定的位元組緩衝區中。 如果未在命令 APDU 上執行任何 [*交易*](../secgloss/t-gly.md)，回復可能會是 **Null** 。

## <a name="syntax"></a>語法


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppReplyApdu* \[擴展\]
</dt> <dd>

位元組緩衝區的指標 (透過包含傳回之 APDU 回復訊息的 **IStream** 物件) 對應。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PpReplyApdu* 參數無效。<br/>  |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *ppReplyApdu* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                             |



 

## <a name="remarks"></a>備註

若要判斷 APDU 回復的長度，請呼叫 [**get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md)。

若要設定新的回復 APDU，請呼叫 [**put \_ ApduReply**](iscardcmd-put-apdureply.md)。

如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例示範如何取出回復資料。 此範例假設 lLe 是 **LONG** 類型的變數，其值是由先前的 [**ISCardCmd：： get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md) 方法呼叫所設定，該 pIByteReply 是 [**IByteBuffer**](ibytebuffer.md) 介面實例的有效指標，而且 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
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

[**取得 \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ ApduReply**](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
