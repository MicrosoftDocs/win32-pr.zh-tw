---
title: 'SessionFlagSkipCACheck 方法 (WSManDisp .h) '
description: 傳回 WSManFlagSkipCACheck authentication 旗標的值，以便在 CreateSession 的 flags 參數中使用。
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- SessionFlagSkipCACheck 方法 Windows 遠端管理
- SessionFlagSkipCACheck 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，SessionFlagSkipCACheck 方法
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e536112b16ad8cbab3cebb2de582a2e0ea8aec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024604"
---
# <a name="wsmansessionflagskipcacheck-method"></a>WSMan. SessionFlagSkipCACheck 方法

**SessionFlagSkipCACheck** 方法會傳回 **WSManFlagSkipCACheck** authentication 旗標的值，以用於 [**WSMan. CreateSession**](wsman-createsession.md)的 *flags* 參數。 這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。 如需如何呼叫這個方法和程式碼範例的詳細資訊，請參閱 [會話常數](session-constants.md)。

**WSManFlagSkipCACheck** 是 **\_ \_ WSManSessionFlags** 列舉中的常數。 如需詳細資訊，請參閱 [**驗證常數**](authentication-constants.md)。

## <a name="syntax"></a>語法


```VB
WSMan.SessionFlagSkipCACheck( _
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
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**工作階段**](session.md)
</dt> </dl>

 

 





