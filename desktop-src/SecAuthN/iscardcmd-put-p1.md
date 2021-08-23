---
description: 設定應用程式協定資料單位的第一個參數 (P1) 位元組 (APDU) 。
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: 'ISCardCmd：:p ut_P1 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7375a04928cf58dc9ef73b6463f2c7d2b19144649e21d7b3220f981584f4c63b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008141"
---
# <a name="iscardcmdput_p1-method"></a>ISCardCmd：:p 的 ui \_ P1 方法

\[**Put \_ P1** 方法可在 [需求] 區段中指定的作業系統中使用。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Put \_ P1** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md)的第一個參數 (P1) 位元組設定 (APDU) 。

## <a name="syntax"></a>語法


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byP1* \[在\]
</dt> <dd>

P1 欄位的位元組。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | 描述                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *ByP1* 參數無效。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                     |



 

## <a name="remarks"></a>備註

若要設定 APDU 的 P2 值，請呼叫 [**get \_ p2**](iscardcmd-get-p2.md)。

若要取出現有的 P1、P2 和 P3 值，請分別呼叫 [**get \_ p1**](iscardcmd-get-p1.md)、 [**取得 \_ P2**](iscardcmd-get-p2.md) 或 [**取得 \_ p3**](iscardcmd-get-p3.md) 。

如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例示範如何設定 [*應用程式協定資料單位*](../secgloss/a-gly.md) 的第一個參數 (P1) 位元組 (APDU) 。 此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。


```C++
HRESULT  hr;

// Set the P1 byte.
hr = pISCardCmd->put_P1(0x06);
if (FAILED(hr))
{
  printf("Failed put_P1\n");
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

[**取得 \_ P1**](iscardcmd-get-p1.md)
</dt> <dt>

[**取得 \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**取得 \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**put \_ P2**](iscardcmd-put-p2.md)
</dt> </dl>

 

 
