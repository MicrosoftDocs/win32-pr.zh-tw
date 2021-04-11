---
description: 傳回物件或實例的 XML 表示。 文字檔會以指定的 XML 格式格式化，如 WbemObjectTextFormatEnum 中所示。
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: 'SWbemObjectEx.GetText_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027435"
---
# <a name="swbemobjectexgettext_-method"></a>SWbemObjectEx. GetText \_ 方法

[**SWbemObjectEx**](swbemobjectex.md)物件的 **GetText \_** 方法會傳回物件或實例的 XML 標記法。 文字檔會以指定的 XML 格式格式化，如 [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)中所示。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iTextFormat* \[在\]
</dt> <dd>

必要。 [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)中的值，指定產生的 XML 格式。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

保留的作業旗標。 預設值是 0 (零)。

</dd> <dt>

*objWbemNamedValueSet* \[在中，選擇性\]
</dt> <dd>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，它會設定作業的內容。 預設值是 null。 如需所允許之名稱/值組的詳細資訊，請參閱下面的備註。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法沒有傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **GetText \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

找不到要求的格式。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

呼叫的其中一個參數不正確。

</dd> <dt>

**wbemErrCriticalError** -2147749898 (0x8004100A) 
</dt> <dd>

發生內部嚴重意外錯誤。 請向 Microsoft 技術支援反映這個錯誤。

</dd> </dl>

## <a name="remarks"></a>備註

當您建立 [**SWbemNamedValueSet**](swbemnamedvalueset.md)時，只允許下列名稱/值配對。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LocalOnly</td>
<td><strong>VT_BOOL</strong><br/> 若 <strong>為 TRUE</strong>，則產生的 XML 中只會出現本機定義的屬性和方法。 預設值為 <strong>FALSE</strong>。<br/></td>
</tr>
<tr class="even">
<td>IncludeQualifiers</td>
<td><strong>VT_BOOL</strong><br/> 若 <strong>為 TRUE</strong>，則會在產生的 XML 中包含類別、實例、屬性和方法的限定詞。 預設值為 <strong>FALSE</strong>。<br/></td>
</tr>
<tr class="odd">
<td>PathLevel</td>
<td><strong>VT-I4</strong><br/> 預設值為 0 (零) 。 可能的值包括：<br/>
<ul>
<li>0： <CLASS> <INSTANCE> 根據物件是否為類別或實例，建立或專案。</li>
<li>1： <VALUE.NAMEDOBJECT> 產生元素。</li>
<li>2： <VALUE.OBJECTWITHLOCALPATH> 產生元素。</li>
<li>3： <VALUE.OBJECTWITHPATH> 產生元素。</li>
</ul></td>
</tr>
<tr class="even">
<td>ExcludeSystemProperties</td>
<td><strong>VT-BOOL</strong><br/> 若 <strong>為 TRUE</strong>，系統屬性（例如 __NAMESPACE）會從輸出中排除。<br/></td>
</tr>
<tr class="odd">
<td>IncludeClassOrigin</td>
<td><strong>VT_BOOL</strong><br/> 若 <strong>為 TRUE</strong>，則會在和元素上設定類別來源屬性 <PROPERTY> <METHOD> 。 預設值為 <strong>FALSE</strong>。<br/></td>
</tr>
</tbody>
</table>



 

如需建立 [**SWbemNamedValueSet**](swbemnamedvalueset.md)的詳細資訊，請參閱 [**SWbemNamedValueSet。**](swbemnamedvalueset-add.md)

## <a name="examples"></a>範例

下列腳本顯示如何取得 [**Win32 \_ Bios**](/windows/desktop/CIMWin32Prov/win32-bios) 類別定義的 XML 標記法。 您可以藉由指定特定的 **Win32 \_ Bios** 實例，以 XML 取得該物件的資料。


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



 

