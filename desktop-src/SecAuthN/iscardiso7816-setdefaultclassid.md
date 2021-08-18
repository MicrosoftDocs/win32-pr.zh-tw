---
description: SetDefaultClassId 方法會指派標準類別識別碼位元組，以在建立 ISO 7816-4 命令應用程式協定資料單位 (APDU) 時用於所有作業。 標準類別識別碼的位元組預設為0x00。
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'ISCardISO7816：： SetDefaultClassId 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d242d83af00bb0d8e10d7da22d014a31deafaa66f49fb509cc91b65263239dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481109"
---
# <a name="iscardiso7816setdefaultclassid-method"></a>ISCardISO7816：： SetDefaultClassId 方法

\[**SetDefaultClassId** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**SetDefaultClassId** 方法會指派標準類別識別碼位元組，以在建立 ISO 7816-4 命令 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 時用於所有作業。 標準類別識別碼的位元組預設為0x00。

## <a name="syntax"></a>語法


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*byClass* \[在\]
</dt> <dd>

類別識別碼位元組。

</dd> </dl>

## <a name="return-value"></a>傳回值

可能的傳回值如下：



| 傳回碼                                                                          | 描述                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 作業順利完成。<br/> |



 

如需 [**ISCardISO7816**](iscardiso7816.md) 介面所提供的所有方法清單，請參閱 **ISCardISO7816**。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需智慧卡錯誤碼的詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardssp。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardsrv .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
