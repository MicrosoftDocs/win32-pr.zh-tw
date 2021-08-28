---
description: 從應用程式協定資料單位中，抓取第一個參數 (P1) 位元組 (APDU) 。
ms.assetid: a6648e70-96d8-4b7d-ae6d-8832e38d1c71
title: 'ISCardCmd：： get_P1 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 94fd7dbe7629ebc3137a6323515d401688dc489cf08c7bb3e6d4262527d4d0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014958"
---
# <a name="iscardcmdget_p1-method"></a>ISCardCmd：： get \_ P1 方法

\[**Get \_ P1** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Get \_ P1** 方法會從 [*應用程式協定資料單位*](../secgloss/a-gly.md)（ (APDU) ）抓取第一個參數 (P1) 位元組。

## <a name="syntax"></a>語法


```C++
HRESULT get_P1(
  [out] BYTE *pbyP1
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbyP1* \[擴展\]
</dt> <dd>

傳回之 APDU 中的 P1 位元組指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | 描述                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PbyP1* 參數無效。<br/>  |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *pbyP1* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                       |



 

## <a name="remarks"></a>備註

若要將 P1 參數設定為新的值，請呼叫 [**put \_ P1**](iscardcmd-put-p1.md)。

若要取得 P2 或 P3 參數，請呼叫 [**get \_ P2**](iscardcmd-get-p2.md) 並分別 [**取得 \_ p3**](iscardcmd-get-p3.md) 。

如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例示範如何從 [*應用程式協定資料單位*](../secgloss/a-gly.md) 取出第一個參數 (P1) 位元組 (APDU) 。 此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。


```C++
BYTE  byP1;
HRESULT  hr;

// Retrieve the P1 byte.
hr = pISCardCmd->get_P1(&byP1);
if (FAILED(hr))
{
  printf("Failed get_P1\n");
  // Take other error handling action as needed.
}
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

[**取得 \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**取得 \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ P1**](iscardcmd-put-p1.md)
</dt> </dl>

 

 
