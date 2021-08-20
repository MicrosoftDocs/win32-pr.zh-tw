---
description: SWbemSink 物件的 Cancel 方法會取消與這個物件接收相關聯的所有未完成非同步作業。
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'ISWbemSink：： Cancel 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe2d8e8c0c5663adee0d6545e32f63cb5e8334269be99192122a2a66ac83159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107856"
---
# <a name="iswbemsinkcancel-method"></a>ISWbemSink：： Cancel 方法

[**SWbemSink**](swbemsink.md)物件的 **Cancel** 方法會取消與這個物件接收相關聯的所有未完成非同步作業。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **取消** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列其中一個錯誤碼。

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

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前或指定的使用者名稱和密碼無效或已獲授權，無法進行連接。

</dd> </dl>

## <a name="remarks"></a>備註

您無法只取消一個非同步呼叫。 如果有多個非同步呼叫暫止，而使用這個物件接收，則此方法會使用這個物件接收來取消所有的非同步呼叫。 與其他物件接收器相關聯的非同步呼叫會繼續受到影響。

您無法將此接收指派給 **任何** 專案，以取消非同步作業。 您必須呼叫 **Cancel** 方法，讓 WMI 中止作業並釋放相關聯的資源。 這對於冗長的非同步作業（例如查詢或永遠不會完成的作業，例如 [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)）非常重要。

> [!Note]  
> 非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請使用最半同步或同步通訊。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

下列範例說明如何取消非同步呼叫。


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>Wbemdisp.tlb .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSink<br/>                                                              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

