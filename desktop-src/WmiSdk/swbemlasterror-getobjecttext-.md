---
description: SWbemLastError 物件的 GetObjectText 方法會傳回 \_ 受控物件格式 (MOF) 格式之物件的文字呈現。
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: 'SWbemLastError.GetObjectText_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944403"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a>SWbemLastError. GetObjectText \_ 方法

[**SWbemLastError**](swbemlasterror.md)物件的 **GetObjectText \_** 方法會傳回 [受控物件格式 (MOF)](managed-object-format--mof-.md)格式之物件的文字呈現。 這個 MOF 物件可以用來顯示物件的內容。 請注意，傳回的 MOF 文字未包含物件的所有資訊，但只有足夠的資訊可供 MOF 編譯器重新建立原始物件。 例如，您將找不到有關傳播的限定詞或父類別屬性的任何資訊。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

這個參數是保留的，而且必須是 0 (零) 如果有指定的話）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，這個方法會傳回包含輸出文字的字串。

## <a name="error-codes"></a>錯誤碼

**GetObjectText \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




