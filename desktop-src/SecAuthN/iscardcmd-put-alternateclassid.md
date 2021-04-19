---
description: 在應用程式協定資料單位中指定新的替代類別識別碼 (APDU) 。
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: 'ISCardCmd：:p ut_AlternateClassId 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972047"
---
# <a name="iscardcmdput_alternateclassid-method"></a>ISCardCmd：:p 的 \_ AlternateClassId 方法

\[**Put \_ AlternateClassId** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Put \_ AlternateClassId** 方法會在 [*應用程式協定資料單位*](../secgloss/a-gly.md)中指定新的替代類別識別碼 (APDU) 。

## <a name="syntax"></a>語法


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byClass* \[在\]
</dt> <dd>

替代類別識別碼。 預設值為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                  | Description                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業順利完成。<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *ByClass* 參數無效。<br/> |



 

## <a name="remarks"></a>備註

使用 [*T = 0 通訊協定*](../secgloss/t-gly.md)進行通訊時，APDU 可以自動產生額外的智慧卡命令，並將 (TPDU) 傳送至傳輸通訊協定資料單位。 其他命令通常會使用與原始命令相同的類別識別碼;藉由這個方法指定新的類別識別碼，可讓自動產生的命令使用新的類別識別碼。

## <a name="examples"></a>範例

下列範例顯示如何在 [*應用程式協定資料單位*](../secgloss/a-gly.md) 中設定新的替代類別識別碼 (APDU) 。 此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
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

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**取得 \_ AlternateClassId**](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
