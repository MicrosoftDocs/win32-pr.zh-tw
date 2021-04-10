---
description: 抓取原始應用程式協定資料單位 (APDU) 。
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'ISCardCmd：： get_Apdu 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026238"
---
# <a name="iscardcmdget_apdu-method"></a>ISCardCmd：：取得 \_ Apdu 方法

\[「 **取得 \_ Apdu** 」方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

「 **取得 \_ apdu** 」方法會抓取原始的 [*應用程式協定資料單位*](../secgloss/a-gly.md) (Apdu) 。

## <a name="syntax"></a>語法


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppApdu* \[擴展\]
</dt> <dd>

透過包含傳回之 APDU 訊息的 **IStream** 物件對應的位元組緩衝區指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PpApdu* 參數無效。<br/>  |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *ppApdu* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                        |



 

## <a name="remarks"></a>備註

若要從 [**IByteBuffer**](ibytebuffer.md) 將 APDU 複製到包裝在此介面物件中的 Apdu (**IStream**) 物件，請呼叫 [**put \_ APDU**](iscardcmd-put-apdu.md)。

若要判斷 APDU 的長度，請呼叫 [**get \_ ApduLength**](iscardcmd-get-apdulength.md)。

如需 [**ISCardCmd**](iscardcmd.md) 介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需智慧卡錯誤碼的詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例示範如何 (APDU) 取得原始的 [*應用程式協定資料單位*](../secgloss/a-gly.md) 。 此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面的有效指標，而且 PIByteApdu 是 [**IByteBuffer**](ibytebuffer.md) 介面實例的有效指標。


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
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

[**取得 \_ ApduLength**](iscardcmd-get-apdulength.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ Apdu**](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
