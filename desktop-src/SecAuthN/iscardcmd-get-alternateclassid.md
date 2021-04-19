---
description: 抓取替代類別識別碼的值。
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'ISCardCmd：： get_AlternateClassId 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987339"
---
# <a name="iscardcmdget_alternateclassid-method"></a>ISCardCmd：： get \_ AlternateClassId 方法

\[**Get \_ AlternateClassId** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Get \_ AlternateClassId** 方法會抓取替代類別識別碼的值。 除非先前呼叫 [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)來設定替代識別碼，否則這個方法將會失敗。

## <a name="syntax"></a>語法


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbyClass* \[擴展\]
</dt> <dd>

傳回時，包含替代類別識別碼值之位元組的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列可能的值。



| 傳回碼                                                                                    | Description                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>           | 作業已順利完成。<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *PbyClass* 參數無效。<br/>                                                                                           |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | 替代類別識別碼先前尚未藉由 [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)的呼叫來設定。<br/> |



 

## <a name="remarks"></a>備註

此方法適用于使用 [*T = 0 通訊協定*](../secgloss/t-gly.md)的通訊。 如需詳細資訊，請參閱 [**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)。

## <a name="examples"></a>範例

下列範例顯示如何取出替代類別識別碼。 此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
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

[**put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
