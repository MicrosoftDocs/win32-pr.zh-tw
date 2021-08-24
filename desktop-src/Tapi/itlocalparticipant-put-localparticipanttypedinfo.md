---
description: Put \_ LocalParticipantTypedInfo 方法會設定參與者資訊。
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: 'ITLocalParticipant：:p ut_LocalParticipantTypedInfo 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acca83d7ad68ed0974aaa2e7d4fb4755c11939d0711473c406cb09d78451ac41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774898"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a>ITLocalParticipant：:p 的 \_ LocalParticipantTypedInfo 方法

**Put \_ LocalParticipantTypedInfo** 方法會設定參與者資訊。

## <a name="syntax"></a>語法


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*InfoType* \[在\]
</dt> <dd>

[**參與者 \_所 \_**](participant-typed-info.md) 需資訊類型的類型資訊識別碼。

</dd> <dt>

*ppInfo* \[在\]
</dt> <dd>

包含資訊的必要新值的 **BSTR** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

應用程式必須使用 [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *ppInfo* 參數配置記憶體，並在不再需要該變數時，使用 [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**參與者 \_ 輸入 \_ 資訊**](participant-typed-info.md)
</dt> </dl>

 

