---
description: 在應用程式協定資料單位中設定新的類別識別碼 (APDU) 。
ms.assetid: 7e7d42f2-2858-4b37-a7d5-a919e3e005da
title: 'ISCardCmd：:p ut_ClassId 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ed4b1f273ebe9ea0a5e105ec3d88fc8446f7a831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943668"
---
# <a name="iscardcmdput_classid-method"></a>ISCardCmd：:p 的 ui \_ ClassId 方法

\[**Put \_ ClassId** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Put \_ ClassId** 方法會在 [*應用程式協定資料單位*](../secgloss/a-gly.md)中設定新的類別識別碼， (APDU) 。

## <a name="syntax"></a>語法


```C++
HRESULT put_ClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byClass* \[在\]
</dt> <dd>

表示類別識別碼的位元組。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *ByClass* 無效。<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

若要取得目前的類別識別碼，請呼叫 [**get \_ ClassId**](iscardcmd-get-classid.md)。

如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例顯示如何在 [*應用程式協定資料單位*](../secgloss/a-gly.md) 中設定新的類別識別碼， (APDU) 。 此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_ClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_ClassId\n");
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

[**取得 \_ ClassId**](iscardcmd-get-classid.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
