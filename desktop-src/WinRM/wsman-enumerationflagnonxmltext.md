---
title: 'EnumerationFlagNonXmlText 方法 (WSManDisp .h) '
description: 傳回列舉常數 WSManFlagNonXmlText 的值，以用於 Session 的 flags 參數。列舉方法。
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- EnumerationFlagNonXmlText 方法 Windows 遠端管理
- EnumerationFlagNonXmlText 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，EnumerationFlagNonXmlText 方法
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6606a20d0ab7f59b7521367243ccdc97fd90209f1791d8f1ded3e48c70e3f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742287"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a>WSMan. EnumerationFlagNonXmlText 方法

**EnumerationFlagNonXmlText** 會傳回列舉常數 **WSManFlagNonXmlText** 的值，以用於 Session 的 *flags* 參數。[**列舉**](session-enumerate.md)方法。 這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。 如需如何呼叫這個方法的詳細資訊，請參閱 [會話常數](session-constants.md)。

**WSManFlagNonXmlText** 是 **\_ \_ WSManEnumFlags** 列舉中的常數。 如需詳細資訊，請參閱 [**列舉常數**](enumeration-constants.md)。

## <a name="syntax"></a>語法


```VB
WSMan.EnumerationFlagNonXmlText( _
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

[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[**Iwsmansession.invoke**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





