---
title: 'SessionFlagUseDigest 方法 (WSManDisp .h) '
description: 傳回 WSManFlagUseDigest authentication 旗標的值，以便在 CreateSession 方法的 flags 參數中使用。
ms.assetid: dba2448a-4f72-4000-8687-4c1be812fc3b
ms.tgt_platform: multiple
keywords:
- SessionFlagUseDigest 方法 Windows 遠端管理
- SessionFlagUseDigest 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，SessionFlagUseDigest 方法
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseDigest
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 888eec55e2c2ec4efc4613c9fa2bdda2713bcfd1761918f00d29816fb6bf43b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795108"
---
# <a name="wsmansessionflagusedigest-method"></a>WSMan. SessionFlagUseDigest 方法

**SessionFlagUseDigest** 方法會傳回 **WSManFlagUseDigest** authentication 旗標的值，以便在 [**CreateSession**](wsman-createsession.md)方法的 *flags* 參數中使用。 這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。 如需如何呼叫這個方法的詳細資訊，請參閱 [會話常數](session-constants.md)。

**WSManFlagUseDigest** 是 **\_ \_ WSManSessionFlags** 列舉中的值。 如需詳細資訊，請參閱 [驗證常數](authentication-constants.md)。

## <a name="syntax"></a>語法


```VB
WSMan.SessionFlagUseDigest( _
  ByRef flags _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[擴展\]
</dt> <dd>

常數的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**會話**](session.md)
</dt> </dl>

 

 





