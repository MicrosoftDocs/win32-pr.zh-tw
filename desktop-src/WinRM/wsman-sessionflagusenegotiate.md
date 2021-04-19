---
title: 'SessionFlagUseNegotiate 方法 (WSManDisp .h) '
description: 傳回 WSManFlagUseNegotiate authentication 旗標的值，以便在 CreateSession 方法的 flags 參數中使用。
ms.assetid: 86d8ed13-5eae-4a06-8ceb-b0ec067f4a4c
ms.tgt_platform: multiple
keywords:
- SessionFlagUseNegotiate 方法 Windows 遠端管理
- SessionFlagUseNegotiate 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，SessionFlagUseNegotiate 方法
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNegotiate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b57e463ccf71f22f12a964b1e1de72f426963c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966115"
---
# <a name="wsmansessionflagusenegotiate-method"></a>WSMan. SessionFlagUseNegotiate 方法

**SessionFlagUseNegotiate** 方法會傳回 **WSManFlagUseNegotiate** authentication 旗標的值，以便在 [**CreateSession**](wsman-createsession.md)方法的 *flags* 參數中使用。 這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。 如需如何呼叫這個方法的詳細資訊，請參閱 [會話常數](session-constants.md)。

**WSManFlagUseNegotiate** 是 **\_ \_ WSManSessionFlags** 列舉中的常數。 如需詳細資訊，請參閱 [驗證常數](authentication-constants.md)。

## <a name="syntax"></a>語法


```VB
WSMan.SessionFlagUseNegotiate( _
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

 

 





