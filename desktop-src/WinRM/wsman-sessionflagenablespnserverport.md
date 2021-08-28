---
title: 'SessionFlagEnableSPNServerPort 方法 (WSManDisp .h) '
description: 傳回驗證旗標 WSManFlagEnableSPNServerPort 的值，以便在 CreateSession 方法的 flags 參數中使用。
ms.assetid: a18a87e6-dcee-4e9f-8e8c-262fef36ab1a
ms.tgt_platform: multiple
keywords:
- SessionFlagEnableSPNServerPort 方法 Windows 遠端管理
- SessionFlagEnableSPNServerPort 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，SessionFlagEnableSPNServerPort 方法
topic_type:
- apiref
api_name:
- WSMan.SessionFlagEnableSPNServerPort
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb309f8fd9d6351ff34201ec409256bad5160ef2cd0224f5cdbf5263ae05214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758928"
---
# <a name="wsmansessionflagenablespnserverport-method"></a>WSMan. SessionFlagEnableSPNServerPort 方法

**SessionFlagEnableSPNServerPort** 方法會傳回 authentication 旗 *標* **WSManFlagEnableSPNServerPort** 的值，以用於 [**WSMan. CreateSession**](wsman-createsession.md)方法的 flags 參數。 這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。 如需如何呼叫這個方法的詳細資訊，請參閱 [會話常數](session-constants.md)。

**WSManFlagEnableSPNServerPort** 是 **\_ \_ WSManSessionFlags** 列舉中的常數。 如需詳細資訊，請參閱 [**其他會話常數**](other-session-constants.md)。

## <a name="syntax"></a>語法


```VB
WSMan.SessionFlagEnableSPNServerPort( _
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

 

 





