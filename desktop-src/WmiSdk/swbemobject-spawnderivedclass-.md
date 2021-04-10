---
description: 使用 \_ SWbemObject 物件的 SpawnDerivedClass 方法，從目前的物件建立衍生類別物件。 物件必須是類別定義，才能成為衍生物件的父類別。
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: 'SWbemObject.SpawnDerivedClass_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192064"
---
# <a name="swbemobjectspawnderivedclass_-method"></a>SWbemObject. SpawnDerivedClass \_ 方法

使用 [**SWbemObject**](swbemobject.md)物件的 **SpawnDerivedClass \_** 方法，從目前的物件建立衍生類別物件。 物件必須是類別定義，才能成為衍生物件的父類別。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iFlags* \[選\]
</dt> <dd>

如果有指定，就會保留，且必須為 0 (零) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果呼叫成功， [**SWbemObject**](swbemobject.md) 物件就會包含新的類別定義物件。 發生錯誤時，不會傳回任何物件。

## <a name="error-codes"></a>錯誤碼

**SpawnDerivedClass \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101E) 
</dt> <dd>

使用者要求了不合法的操作，例如從實例產生類別。

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020) 
</dt> <dd>

來源類別未完整定義或向 WMI 註冊，因此不允許新的衍生類別。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="remarks"></a>備註

所傳回的物件會自動成為目前物件的子類別。 無法覆寫此行為。 沒有其他方法可讓您建立衍生類別。

您無法從您自己的用戶端進程的本機類別建立衍生類別。 使用這個方法建立衍生類別之前，您必須先建立基類。 若要建立基類，請呼叫 [**SWbemObject \_**](swbemobject-put-.md)，然後使用 [**SWbemServices 取得**](swbemservices-get.md)基類。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




