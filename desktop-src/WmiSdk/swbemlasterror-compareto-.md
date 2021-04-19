---
description: '\_SWbemLastError 物件的 CompareTo 方法會比較兩個 SWbemObject 物件。 根據 iFlags 參數中指定的值，這項比較會受限於某些條件約束。'
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: 'SWbemLastError.CompareTo_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978877"
---
# <a name="swbemlasterrorcompareto_-method"></a>SWbemLastError. CompareTo \_ 方法

[**SWbemLastError**](swbemlasterror.md)物件的 **CompareTo \_** 方法會比較兩個 [**SWbemObject**](swbemobject.md)物件。 根據 *iFlags* 參數中指定的值，這項比較會受限於某些條件約束。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objwbemObject* \[在\]
</dt> <dd>

必要。 [**SWbemObject**](swbemobject.md)類別物件。 這個參數是用來比較第一個物件的物件。 物件必須是有效的 **SWbemObject** 實例。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

指定運算其他旗標的整數。 此參數會指定進行物件比較時要考慮的物件特性。 您可以使用 **wbemComparisonFlagIncludeAll** 將所有功能視為 (預設) 或下列值的任何組合。

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll * * * (0 (0x0) ) 


</dt> <dd>

造成所有屬性、限定詞和類別的比較。

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers * * * (1 (0x1) ) 


</dt> <dd>

使所有限定詞 (包括索引 **鍵** 和 **動態**) ，以進行比較。

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource * * * (2 (0x2) ) 


</dt> <dd>

使物件的來源（也就是伺服器及其來源的命名空間）與其他物件相比較，將會被忽略。

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues * * * (4 (0x4) ) 


</dt> <dd>

導致忽略屬性的預設值。 只有在比較類別時，此旗標才有意義。

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass * * * (8 (0x8) ) 


</dt> <dd>

指示系統假設要比較的物件是相同類別的實例。 因此，此旗標只會比較實例相關資訊。 使用這個旗標，將效能最佳化。 如果物件不屬於相同類別，則結果不會定義。

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase * * * (16 (0x10) ) 


</dt> <dd>

使字串值以不區分大小寫的方式進行比較。 這同時適用于字串和限定詞值。 不論這個旗標是否指定，屬性和限定詞名稱都是以區分大小寫的方式比較。

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor * * * (32 (0x20) ) 


</dt> <dd>

會忽略辨識符號的類別。 這個旗標仍然會考慮限定詞值，但是會忽略類型差異，例如傳用原則和覆寫限制。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

如果物件相符， **\_ CompareTo** 方法會傳回布林值 **TRUE** ; 否則會傳回 **FALSE**。

## <a name="error-codes"></a>錯誤碼

**CompareTo \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemLastError**](swbemlasterror.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

 




