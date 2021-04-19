---
description: 當非同步呼叫傳回進行中之呼叫的狀態時，就會觸發 SWbemSink 的 OnProgress 事件。
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents：： OnProgress 事件 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980059"
---
# <a name="iswbemsinkeventsonprogress-event"></a>ISWbemSinkEvents：： OnProgress 事件

當非同步呼叫傳回進行中之呼叫的狀態時，就會觸發 [**SWbemSink**](swbemsink.md)的 **OnProgress** 事件。 如果從支援狀態更新的提供者產生事件、實例或類別，您可以將程式碼放在這個事件中，為使用者提供非同步作業狀態的相關意見反應。 如果您想要接收狀態更新，您必須將非同步呼叫的 *iFlags* 參數設定為 **wbemFlagSendStatus** (128/0x80) ，否則就不會觸發此事件。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iUpperBound* 
</dt> <dd>

描述要完成之工作總數的整數。

</dd> <dt>

*iCurrent* 
</dt> <dd>

目前正在處理的專案。

</dd> <dt>

*strMessage* 
</dt> <dd>

描述目前工作狀態的訊息。

</dd> <dt>

*objWbemAsyncCoNtext* 
</dt> <dd>

傳遞至原始非同步呼叫的 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件。 使用這個參數來識別非同步呼叫的來源，此呼叫會在使用這個物件接收進行多個非同步呼叫時觸發這個事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="error-codes"></a>錯誤碼

**OnProgress** 事件完成之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> <dt>

**wbemErrTransportFailure** -2147749909 (0x80041015) 
</dt> <dd>

發生網路錯誤，導致無法正常運作。

</dd> </dl>

## <a name="remarks"></a>備註

當非同步呼叫傳回正在進行之呼叫的狀態時，就會觸發 **OnProgress** 事件。 如果從支援狀態更新的提供者產生事件、實例或類別，您可以將程式碼放在這個事件中，以提供使用者有關非同步作業狀態的意見反應。

> [!Note]  
> 非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請使用半同步或同步通訊。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>wbemdisp.tlb .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSinkEvents<br/>                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

