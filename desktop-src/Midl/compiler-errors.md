---
title: 編譯器錯誤
description: MIDL 編譯期間產生的錯誤訊息清單。
ms.assetid: 492eacdd-6bd1-49df-9112-3765f6c05f34
keywords:
- 錯誤 MIDL，編譯器錯誤
topic_type:
- apiref
api_name:
- Compiler Errors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b4bb2189e824f82cc9247abc68844068d083b2f0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104093440"
---
# <a name="compiler-errors"></a>編譯器錯誤

在 MIDL 編譯期間，會產生下列錯誤訊息：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>傳回碼</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="MIDL2000"></span><span id="midl2000"></span><dl> <dt><strong>MIDL2000</strong></dt> </dl></td>
<td><dl> <dt><span id="must_specify__c_ext_for_abstract_declarators"></span><span id="MUST_SPECIFY__C_EXT_FOR_ABSTRACT_DECLARATORS"></span>必須為抽象宣告子指定/c_ext</dt> <dd> 抽象宣告子代表 Microsoft 對 RPC 的延伸模組，而且不會在 DCE RPC 中定義。 因此，如果您的檔案包含抽象宣告子，您就無法使用 <a href="-osf.md"><strong>/osf</strong></a> 參數進行編譯，這會強制執行嚴格的 DCE 相容性。 MIDL 3.0 版和更新版本會使用 <a href="-c-ext.md"><strong>/c_ext</strong></a> 參數作為預設值; <strong>/osf</strong> 參數會關閉 <strong>/c_ext</strong> 參數。 如需抽象宣告子的詳細資訊，請參閱 <a href="/windows/desktop/Rpc/the-acf-body">ACF 主體</a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2001"></span><span id="midl2001"></span><dl> <dt><strong>MIDL2001</strong></dt> </dl></td>
<td><dl> <dt><span id="instantiation_of_data_is_illegal__you_must_use__extern__or__static_"></span><span id="INSTANTIATION_OF_DATA_IS_ILLEGAL__YOU_MUST_USE__EXTERN__OR__STATIC_"></span>資料的具現化不合法;您必須使用 &quot; extern &quot; 或 &quot; static&quot;</dt> <dd> IDL 檔案中的宣告和初始化與 DCE RPC 不相容。 這項功能是 Microsoft 擴充功能，當您在 DCE 相容性 (<a href="-osf.md"><strong>/osf</strong></a>) 模式中進行編譯時無法使用。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2002"></span><span id="midl2002"></span><dl> <dt><strong>MIDL2002</strong></dt> </dl></td>
<td><dl> <dt><span id="compiler_stack_overflow"></span><span id="COMPILER_STACK_OVERFLOW"></span>編譯器堆疊溢位</dt> <dd> 編譯器在處理 IDL 檔案時，已用完堆疊空間。 當編譯器處理複雜的宣告或運算式時，就會發生這個問題。 若要解決此問題，請簡化複雜的宣告或運算式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2003"></span><span id="midl2003"></span><dl> <dt><strong>MIDL2003</strong></dt> </dl></td>
<td><dl> <dt><span id="redefinition"></span><span id="REDEFINITION"></span>定義</dt> <dd> 此錯誤訊息可能會出現在下列情況下：已重新定義類型;已重新定義程式原型;已經有相同名稱的結構或等位成員。原型中已經有相同名稱的參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2004"></span><span id="midl2004"></span><dl> <dt><strong>MIDL2004</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__binding_will_be_used"></span><span id="_AUTO_HANDLE__BINDING_WILL_BE_USED"></span>將使用 [auto_handle] 系結</dt> <dd> 未將控制碼類型定義為預設控制碼類型。 編譯器會假設自動控制碼將用作指定程式的系結控制碼。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2005"></span><span id="midl2005"></span><dl> <dt><strong>MIDL2005</strong></dt> </dl></td>
<td><dl> <dt><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>記憶體不足</dt> <dd> 編譯器在編譯期間已用盡記憶體。 減少 IDL 檔案的大小或複雜度，或配置更多記憶體給進程。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2006"></span><span id="midl2006"></span><dl> <dt><strong>MIDL2006</strong></dt> </dl></td>
<td><dl> <dt><span id="recursive_definition"></span><span id="RECURSIVE_DEFINITION"></span>遞迴定義</dt> <dd> 已遞迴定義結構或等位。 當遺漏嵌套結構定義中的指標規格時，就會發生這個錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2007"></span><span id="midl2007"></span><dl> <dt><strong>MIDL2007</strong></dt> </dl></td>
<td><dl> <dt><span id="import_ignored__file_already_imported"></span><span id="IMPORT_IGNORED__FILE_ALREADY_IMPORTED"></span>已忽略匯入;檔案已匯入</dt> <dd> 匯入 IDL 檔案是等冪作業。 包含超過一次沒有任何作用。 除了第一個匯入作業之外，所有作業都會被忽略。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2008"></span><span id="midl2008"></span><dl> <dt><strong>MIDL2008</strong></dt> </dl></td>
<td><dl> <dt><span id="sparse_enums_require__c_ext_or__ms_ext"></span><span id="SPARSE_ENUMS_REQUIRE__C_EXT_OR__MS_EXT"></span>稀疏列舉需要/c_ext 或/ms_ext</dt> <dd> 將值指派給列舉常數與 DCE RPC 不相容。 如果您想要使用允許將值指派給列舉常數的 MIDL 的 Microsoft 擴充功能，您無法使用 <a href="-osf.md"><strong>/osf</strong></a> 參數進行編譯，這會強制執行嚴格的 DCE 相容性。 MIDL 3.0 版和更新版本會使用 <a href="-c-ext.md"><strong>/c_ext</strong></a> 和 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 參數作為預設值; <strong>/osf</strong> 參數會關閉這些擴充功能參數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2009"></span><span id="midl2009"></span><dl> <dt><strong>MIDL2009</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined_symbol"></span><span id="UNDEFINED_SYMBOL"></span>未定義的符號</dt> <dd> 運算式中使用了未定義的符號。 當您使用未定義的列舉值時，就會發生這個錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2010"></span><span id="midl2010"></span><dl> <dt><strong>MIDL2010</strong></dt> </dl></td>
<td><dl> <dt><span id="type_used_in_ACF_file_not_defined_in_IDL_file"></span><span id="type_used_in_acf_file_not_defined_in_idl_file"></span><span id="TYPE_USED_IN_ACF_FILE_NOT_DEFINED_IN_IDL_FILE"></span>在 IDL 檔案中未定義的 ACF 檔案中使用的類型</dt> <dd> 使用的是未定義的類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2011"></span><span id="midl2011"></span><dl> <dt><strong>MIDL2011</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_type_declaration"></span><span id="UNRESOLVED_TYPE_DECLARATION"></span>未解析的類型宣告</dt> <dd> 在 [其他錯誤-資訊] 欄位中報告的類型尚未在 IDL 檔案中的其他地方定義。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2012"></span><span id="midl2012"></span><dl> <dt><strong>MIDL2012</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide-character_constants_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE-CHARACTER_CONSTANTS_REQUIRES__MS_EXT_OR__C_EXT"></span>使用寬字元常數需要/ms_ext 或/c_ext</dt> <dd> 寬字元常數是 DCE IDL 的 Microsoft 延伸模組。 若要使用資料類型 <a href="wchar-t.md"><strong>wchar_t</strong></a>，您無法使用 <a href="-osf.md"><strong>/osf</strong></a> 參數進行編譯，這會覆寫 MIDL 編譯器預設參數 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 和 <a href="-c-ext.md"><strong>/c_ext</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2013"></span><span id="midl2013"></span><dl> <dt><strong>MIDL2013</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide_character_strings_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE_CHARACTER_STRINGS_REQUIRES__MS_EXT_OR__C_EXT"></span>使用寬字元字串需要/ms_ext 或/c_ext</dt> <dd> 寬字元字串常數是 DCE IDL 的 Microsoft 延伸模組。 若要使用資料類型 <a href="wchar-t.md"><strong>wchar_t</strong></a>，您無法使用 <a href="-osf.md"><strong>/osf</strong></a> 參數進行編譯，這會覆寫 MIDL 編譯器預設參數 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 和 <a href="-c-ext.md"><strong>/c_ext</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2014"></span><span id="midl2014"></span><dl> <dt><strong>MIDL2014</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_wchar_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_WCHAR_T"></span>類型 wchar_t 的重新定義不一致</dt> <dd> 類型 <a href="wchar-t.md"><strong>wchar_t</strong></a> 已重新定義為不等於不帶正負號的短 DOS * 的類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2015"></span><span id="midl2015"></span><dl> <dt><strong>MIDL2015</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_not_found"></span><span id="IMPORTLIB_NOT_FOUND"></span>找不到 importlib</dt> <dd> 編譯器找不到 [ <a href="importlib.md"><strong>importlib</strong></a>] 指示詞所指定的類型程式庫。 請檢查以確定程式庫的路徑和名稱正確無誤。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2016"></span><span id="midl2016"></span><dl> <dt><strong>MIDL2016</strong></dt> </dl></td>
<td><dl> <dt><span id="two_library_blocks"></span><span id="TWO_LIBRARY_BLOCKS"></span>兩個程式庫區塊</dt> <dd> 即使在相同的原始檔中) 的不同名稱， (兩個程式庫區塊都不合法。 將所有元素合併成單一程式庫區塊。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2017"></span><span id="midl2017"></span><dl> <dt><strong>MIDL2017</strong></dt> </dl></td>
<td><dl> <dt><span id="the_dispinterface_statement_requires_a_definition_for_IDispatch"></span><span id="the_dispinterface_statement_requires_a_definition_for_idispatch"></span><span id="THE_DISPINTERFACE_STATEMENT_REQUIRES_A_DEFINITION_FOR_IDISPATCH"></span>介面介面語句需要 IDispatch 的定義</dt> <dd> 當未匯入 Stdole2 .tlb 或 Oaidl.idl 的檔案時，通常會發生這個錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2018"></span><span id="midl2018"></span><dl> <dt><strong>MIDL2018</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_library"></span><span id="ERROR_ACCESSING_TYPE_LIBRARY"></span>存取類型程式庫時發生錯誤</dt> <dd> 編譯器找不到指定的類型程式庫。 請檢查以確定您已正確指定路徑。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2019"></span><span id="midl2019"></span><dl> <dt><strong>MIDL2019</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_info"></span><span id="ERROR_ACCESSING_TYPE_INFO"></span>存取類型資訊時發生錯誤</dt> <dd> 匯入的類型程式庫已損毀、無效或僅部分構成。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2020"></span><span id="midl2020"></span><dl> <dt><strong>MIDL2020</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library"></span><span id="ERROR_GENERATING_TYPE_LIBRARY"></span>產生類型程式庫時發生錯誤</dt> <dd> 無法產生類型程式庫。 此錯誤的其中一個可能原因是指定的 IDL 檔案路徑超過126個字元。 Oleaut32.dll 不支援長度超過126個字元的路徑名稱。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2021"></span><span id="midl2021"></span><dl> <dt><strong>MIDL2021</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_id"></span><span id="DUPLICATE_ID"></span>重複的識別碼</dt> <dd> 應用程式會使用 IDL 檔案中的 <a href="id.md"><strong>id</strong></a> 語句來指定 DISPID 的成員函式。 成員函式可以是介面或分配介面的屬性或方法。 此錯誤表示 IDL 檔案為兩個方法或屬性指定相同的識別碼號碼。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2022"></span><span id="midl2022"></span><dl> <dt><strong>MIDL2022</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_or_missing_value_for_entry_attribute"></span><span id="ILLEGAL_OR_MISSING_VALUE_FOR_ENTRY_ATTRIBUTE"></span>專案屬性的值不合法或遺失</dt> <dd> 專案屬性的引數可以是指定命名進入點的字串，或是定義進入點的序號。 此引數可能遺失或包含不正確值。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2023"></span><span id="midl2023"></span><dl> <dt><strong>MIDL2023</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_assumes"></span><span id="ERROR_RECOVERY_ASSUMES"></span>錯誤修復假設</dt> <dd> MIDL 編譯器在 IDL 檔案中找到不合法的字元。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2024"></span><span id="midl2024"></span><dl> <dt><strong>MIDL2024</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_discards"></span><span id="ERROR_RECOVERY_DISCARDS"></span>錯誤修復捨棄</dt> <dd> MIDL 編譯器在 IDL 檔案中找到不合法的字元。 它會忽略不合法的字元。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2025"></span><span id="midl2025"></span><dl> <dt><strong>MIDL2025</strong></dt> </dl></td>
<td><dl> <dt><span id="syntax_error"></span><span id="SYNTAX_ERROR"></span>語法錯誤</dt> <dd> 編譯器偵測到指定的行有語法錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2026"></span><span id="midl2026"></span><dl> <dt><strong>MIDL2026</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_recover_from_earlier_syntax_errors__aborting_compilation"></span><span id="CANNOT_RECOVER_FROM_EARLIER_SYNTAX_ERRORS__ABORTING_COMPILATION"></span>無法從先前的語法錯誤復原;正在中止編譯</dt> <dd> MIDL 編譯器會自動嘗試透過新增或移除語法元素來從語法錯誤中復原。 這則訊息表示雖然這些嘗試復原，但編譯器偵測到太多錯誤。 更正指定的錯誤 (s) 並重新編譯。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2027"></span><span id="midl2027"></span><dl> <dt><strong>MIDL2027</strong></dt> </dl></td>
<td><dl> <dt><span id="unknown_pragma_option"></span><span id="UNKNOWN_PRAGMA_OPTION"></span>未知的 pragma 選項</dt> <dd> MIDL 中不支援指定的 C pragma。 從 IDL 檔案中移除 pragma。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2028"></span><span id="midl2028"></span><dl> <dt><strong>MIDL2028</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_not_implemented"></span><span id="FEATURE_NOT_IMPLEMENTED"></span>未執行功能</dt> <dd> MIDL 功能（雖然部分的語言定義）不會在 Microsoft RPC 中執行，而且 MIDL 編譯器不支援此功能。 例如，下列語言功能不會實作為： bitset、管道和國際字元類型。 未實現的語言功能會出現在錯誤訊息的 [其他錯誤資訊] 欄位中。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2029"></span><span id="midl2029"></span><dl> <dt><strong>MIDL2029</strong></dt> </dl></td>
<td><dl> <dt><span id="type_not_implemented"></span><span id="TYPE_NOT_IMPLEMENTED"></span>類型未實作為</dt> <dd> 雖然在 Microsoft RPC 中不會實作為合法 MIDL 關鍵字的指定資料類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2030"></span><span id="midl2030"></span><dl> <dt><strong>MIDL2030</strong></dt> </dl></td>
<td><dl> <dt><span id="non-pointer_used_in_a_dereference_operation"></span><span id="NON-POINTER_USED_IN_A_DEREFERENCE_OPERATION"></span>取值運算中使用的非指標</dt> <dd> 不是指標的資料類型已與指標作業相關聯。 您無法透過指定的非指標存取物件。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2031"></span><span id="midl2031"></span><dl> <dt><strong>MIDL2031</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_has_a_divide_by_zero"></span><span id="EXPRESSION_HAS_A_DIVIDE_BY_ZERO"></span>運算式的零除</dt> <dd> 常數運算式包含零除。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2032"></span><span id="midl2032"></span><dl> <dt><strong>MIDL2032</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_uses_incompatible_types"></span><span id="EXPRESSION_USES_INCOMPATIBLE_TYPES"></span>運算式使用不相容的類型</dt> <dd> 運算式中運算子的左邊和右邊都是不相容的類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2033"></span><span id="midl2033"></span><dl> <dt><strong>MIDL2033</strong></dt> </dl></td>
<td><dl> <dt><span id="nonarray_expression_uses_index_operator"></span><span id="NONARRAY_EXPRESSION_USES_INDEX_OPERATOR"></span>nonarray 運算式使用索引運算子</dt> <dd> 運算式在不屬於陣列類型的資料項目上使用陣列索引作業。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2034"></span><span id="midl2034"></span><dl> <dt><strong>MIDL2034</strong></dt> </dl></td>
<td><dl> <dt><span id="left-hand_side_of_expression_does_not_evaluate_to_struct_union_enum"></span><span id="LEFT-HAND_SIDE_OF_EXPRESSION_DOES_NOT_EVALUATE_TO_STRUCT_UNION_ENUM"></span>運算式的左邊不會評估為 struct/union/enum</dt> <dd> 直接或間接參考運算子， &quot; 或已套用 &quot; &quot; -> &quot; 至不是結構、等位或列舉的資料物件。 您無法使用指定的物件取得直接或間接參考。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2035"></span><span id="midl2035"></span><dl> <dt><strong>MIDL2035</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_expression_expected"></span><span id="CONSTANT_EXPRESSION_EXPECTED"></span>需要常數運算式</dt> <dd> 語法中必須要有常數運算式。 例如，陣列界限需要常數運算式。 當陣列系結定義了變數或未定義的符號時，編譯器會發出這個錯誤訊息。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2036"></span><span id="midl2036"></span><dl> <dt><strong>MIDL2036</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_cannot_be_evaluated_at_compile_time"></span><span id="EXPRESSION_CANNOT_BE_EVALUATED_AT_COMPILE_TIME"></span>無法在編譯時期評估運算式</dt> <dd> 編譯器無法在編譯時期評估運算式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2037"></span><span id="midl2037"></span><dl> <dt><strong>MIDL2037</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_not_implemented"></span><span id="EXPRESSION_NOT_IMPLEMENTED"></span>運算式未實作為</dt> <dd> 在 Microsoft RPC 提供的編譯器版本中不支援舊版 MIDL 編譯器所支援的功能。 移除指定的運算式。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2038"></span><span id="midl2038"></span><dl> <dt><strong>MIDL2038</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__unique__for_all_unattributed_pointers"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__UNIQUE__FOR_ALL_UNATTRIBUTED_POINTERS"></span>未指定 [pointer_default] 屬性，假設 [unique] 適用于所有未歸屬指標</dt> <dd> MIDL 編譯器針對沒有指標屬性的指標提供三種不同的預設案例。 最上層指標的函式參數預設為 [<a href="ref.md"><strong>ref</strong></a>] 指標。 內嵌在結構中的指標，以及指向其他指標 (不是最上層指標的指標) 預設為 [<a href="pointer-default.md"><strong>pointer_default</strong></a>] 屬性所指定的類型。 當未提供 [<strong>pointer_default</strong>] 屬性時，這些 nontop 層級指標會預設為唯一指標。 此錯誤訊息表示最後一個案例：未提供 [<strong>pointer_default</strong>] 屬性，而且至少有一個非最上層指標會被視為唯一指標。 如需詳細資訊，請參閱 <a href="/windows/desktop/Rpc/default-pointer-types">預設指標類型</a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2039"></span><span id="midl2039"></span><dl> <dt><strong>MIDL2039</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_is_not_automation_marshaling_conformant"></span><span id="INTERFACE_IS_NOT_AUTOMATION_MARSHALING_CONFORMANT"></span>介面不符合自動化封送處理</dt> <dd> 介面不符合 OLE Automation 介面的需求。 請檢查以確定介面衍生自 <strong>IUnknown</strong> 或 <strong>IDispatch</strong>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2040"></span><span id="midl2040"></span><dl> <dt><strong>MIDL2040</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_a_pointer_to_an_open_structure"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_A_POINTER_TO_AN_OPEN_STRUCTURE"></span>[out] 唯一的參數不能是開啟結構的指標</dt> <dd> 已使用 [<a href="out-idl.md"><strong>out</strong></a>]-唯一的參數做為結構的指標，稱為開放式結構，其傳輸的範圍和大小會在執行時間決定。 伺服器 stub 不知道要為開啟的結構配置多少空間。 使用指向開放式結構指標的指標，並確定伺服器應用程式為其配置足夠的空間。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2041"></span><span id="midl2041"></span><dl> <dt><strong>MIDL2041</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_an_unsized_string"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_AN_UNSIZED_STRING"></span>[out] 唯一的參數不能是可變大小字串</dt> <dd> 具有字串屬性的陣列已經宣告為 [<a href="out-idl.md"><strong>out</strong></a>] 參數，但沒有任何大小規格。 伺服器 stub 需要大小資訊，以配置字串的記憶體。 您可以移除字串屬性並新增 [<a href="size-is.md"><strong>size_is</strong></a>] 屬性，也可以將參數變更為 [<strong>in，out</strong>] 參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2042"></span><span id="midl2042"></span><dl> <dt><strong>MIDL2042</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameter_is_not_a_pointer"></span><span id="_OUT__PARAMETER_IS_NOT_A_POINTER"></span>[out] 參數不是指標</dt> <dd> 所有 [<a href="out-idl.md"><strong>out</strong></a>] 參數都必須是指標，以配合 C 程式設計語言的呼叫傳值慣例。 [<strong>Out</strong>] 方向參數表示伺服器將值傳送至用戶端。 使用以傳值慣例的慣例，只有當函式引數為指標時，伺服器才能將資料傳送至用戶端。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2043"></span><span id="midl2043"></span><dl> <dt><strong>MIDL2043</strong></dt> </dl></td>
<td><dl> <dt><span id="open_structure_cannot_be_a_parameter"></span><span id="OPEN_STRUCTURE_CANNOT_BE_A_PARAMETER"></span>開啟的結構不能是參數</dt> <dd> 開啟的結構包含符合的陣列做為最後一個元素。 當結構或等位的最後一個元素是符合標準的陣列時，就會截斷結構或等位。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2044"></span><span id="midl2044"></span><dl> <dt><strong>MIDL2044</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__context_handle_generic_handle_must_be_specified_as_a_pointer_to_that_handle_type"></span><span id="_OUT__CONTEXT_HANDLE_GENERIC_HANDLE_MUST_BE_SPECIFIED_AS_A_POINTER_TO_THAT_HANDLE_TYPE"></span>[out] 必須將內容控制碼/泛型控制碼指定為該控制碼類型的指標</dt> <dd> 具有 [<a href="out-idl.md"><strong>out</strong></a>] 方向屬性的內容控制碼或使用者定義控制碼參數必須是指向指標的指標。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2045"></span><span id="midl2045"></span><dl> <dt><strong>MIDL2045</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_must_not_derive_from_a_type_that_has_the__transmit_as__attribute"></span><span id="CONTEXT_HANDLE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS_THE__TRANSMIT_AS__ATTRIBUTE"></span>內容控制碼不能衍生自具有 [transmit_as] 屬性的類型</dt> <dd> 內容控制碼必須以內容控制碼類型的形式傳送。 它們無法以其他類型的形式傳輸，也無法衍生自 [transmit_is]、[<strong>represent_as</strong>]、[<strong>wire_marshal</strong>] 或 [<strong>user_marshal</strong>]。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2046"></span><span id="midl2046"></span><dl> <dt><strong>MIDL2046</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_a_variable_number_of_arguments_to_a_remote_procedure"></span><span id="CANNOT_SPECIFY_A_VARIABLE_NUMBER_OF_ARGUMENTS_TO_A_REMOTE_PROCEDURE"></span>無法為遠端程式指定變數數目的引數</dt> <dd> 在編譯時期指定可變數目引數的遠端程序呼叫，與 DCE RPC 定義不相容。 您無法在 Microsoft RPC 中使用不定數目的引數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2047"></span><span id="midl2047"></span><dl> <dt><strong>MIDL2047</strong></dt> </dl></td>
<td><dl> <dt><span id="named_parameter_cannot_be__void_"></span><span id="NAMED_PARAMETER_CANNOT_BE__VOID_"></span>具名引數不可為 &quot; void&quot;</dt> <dd> 以名稱指定基底類型為 <a href="void.md"><strong>void</strong></a> 的參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2048"></span><span id="midl2048"></span><dl> <dt><strong>MIDL2048</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_derives_from__coclass__or__module_"></span><span id="PARAMETER_DERIVES_FROM__COCLASS__OR__MODULE_"></span>參數衍生自 &quot; coclass &quot; 或 &quot; module&quot;</dt> <dd> <a href="coclass.md"><strong>Coclass</strong></a>指定包含介面和分配介面的最上層物件。 無法以參數形式傳遞。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2049"></span><span id="midl2049"></span><dl> <dt><strong>MIDL2049</strong></dt> </dl></td>
<td><dl> <dt><span id="only_the_first_parameter_can_be_a_binding_handle__you_must_specify_the__ms_ext_switch"></span><span id="ONLY_THE_FIRST_PARAMETER_CAN_BE_A_BINDING_HANDLE__YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>只有第一個參數可以是系結控制碼;您必須指定/ms_ext 參數</dt> <dd> DCE RPC 只允許第一個參數為系結控制碼。 使用 <a href="-osf.md"><strong>/osf</strong></a> 參數進行編譯時，會關閉支援多個控制碼參數的預設 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 參數，並在最左邊的位置處理參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2050"></span><span id="midl2050"></span><dl> <dt><strong>MIDL2050</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__comm_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__COMM_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>無法在參數和傳回類型上使用 [comm_status]</dt> <dd> 程式和其中一個參數都有 [<a href="comm-status.md"><strong>comm_status</strong></a>] 屬性。 [<strong>Comm_status</strong>] 屬性可指定一次只能有一個資料物件的類型為 <a href="error-status-t.md"><strong>error_status_t</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2051"></span><span id="midl2051"></span><dl> <dt><strong>MIDL2051</strong></dt> </dl></td>
<td><dl> <dt><span id="__local__attribute_on_a_procedure_requires__ms_ext"></span><span id="__LOCAL__ATTRIBUTE_ON_A_PROCEDURE_REQUIRES__MS_EXT"></span> 程式上的 [local] 屬性需要/ms_ext</dt> <dd> [<a href="local.md"><strong>Local</strong></a>] 屬性是 DCE IDL 的 Microsoft 延伸模組。 若要在函式上使用此屬性，您無法使用 <a href="-osf.md"><strong>/osf</strong></a> 參數進行編譯。 <strong>/Osf</strong>參數會覆寫 MIDL 編譯器預設參數<a href="-ms-ext.md"><strong>/ms_ext</strong></a>和<a href="-c-ext.md"><strong>/c_ext</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2052"></span><span id="midl2052"></span><dl> <dt><strong>MIDL2052</strong></dt> </dl></td>
<td><dl> <dt><span id="property_attributes_may_only_be_used_with_procedures"></span><span id="PROPERTY_ATTRIBUTES_MAY_ONLY_BE_USED_WITH_PROCEDURES"></span>屬性屬性只能搭配程式使用</dt> <dd> 不當使用 [<a href="propget.md"><strong>propget</strong></a>]、[<a href="propput.md"><strong>propput</strong></a>] 或 [<a href="propputref.md"><strong>propputref</strong></a>] 屬性。 請檢查以確定您已正確拼寫屬性的函式名稱，且屬性和函式具有相同的名稱。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2053"></span><span id="midl2053"></span><dl> <dt><strong>MIDL2053</strong></dt> </dl></td>
<td><dl> <dt><span id="a_procedure_may_not_have_more_than_one_property_attribute"></span><span id="A_PROCEDURE_MAY_NOT_HAVE_MORE_THAN_ONE_PROPERTY_ATTRIBUTE"></span>程式可能沒有一個以上的屬性屬性</dt> <dd> 最多隻能為函數指定一個 [<a href="propget.md"><strong>propget</strong></a>]、[<a href="propput.md"><strong>propput</strong></a>] 或 [<a href="propputref.md"><strong>propputref</strong></a>] 屬性。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2054"></span><span id="midl2054"></span><dl> <dt><strong>MIDL2054</strong></dt> </dl></td>
<td><dl> <dt><span id="the_procedure_has_an_illegal_combination_of_operation_attributes"></span><span id="THE_PROCEDURE_HAS_AN_ILLEGAL_COMBINATION_OF_OPERATION_ATTRIBUTES"></span>程式具有不合法的作業屬性組合</dt> <dd> 某些屬性無法用於與其他屬性的連接。 請檢查 MIDL 語言參考，以瞭解此程式中所使用之屬性的確切需求和語法。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2055"></span><span id="midl2055"></span><dl> <dt><strong>MIDL2055</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_a_conformant_array_must_be_the_last_member_of_the_structure"></span><span id="FIELD_DERIVING_FROM_A_CONFORMANT_ARRAY_MUST_BE_THE_LAST_MEMBER_OF_THE_STRUCTURE"></span>衍生自符合標準的陣列的欄位必須是結構的最後一個成員</dt> <dd> 結構包含符合標準的陣列，而該陣列不是結構中的最後一個元素。 符合標準的陣列必須顯示為最後一個結構元素。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2056"></span><span id="midl2056"></span><dl> <dt><strong>MIDL2056</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate__case__label"></span><span id="DUPLICATE__CASE__LABEL"></span>重複的 [案例] 標籤</dt> <dd> 已指定重複的 case 標籤。 會顯示重複的標籤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2057"></span><span id="midl2057"></span><dl> <dt><strong>MIDL2057</strong></dt> </dl></td>
<td><dl> <dt><span id="no__default__case_specified_for_discriminated_union"></span><span id="NO__DEFAULT__CASE_SPECIFIED_FOR_DISCRIMINATED_UNION"></span>未針對差異聯集指定 [default] 案例</dt> <dd> 已指定差異聯集，但沒有預設案例。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2058"></span><span id="midl2058"></span><dl> <dt><strong>MIDL2058</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_cannot_be_resolved"></span><span id="ATTRIBUTE_EXPRESSION_CANNOT_BE_RESOLVED"></span>無法解析屬性運算式</dt> <dd> 無法解析與屬性相關聯的運算式。 當運算式中出現的變數未定義時，通常會發生這個錯誤。 例如，當變數 <em>s</em> 未定義，而且屬性 [<a href="size-is.md"><strong>size_is</strong></a>] 使用時，就會發生此錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2059"></span><span id="midl2059"></span><dl> <dt><strong>MIDL2059</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_integral_type__no_support_for_64-bit_expressions"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_INTEGRAL_TYPE__NO_SUPPORT_FOR_64-BIT_EXPRESSIONS"></span>屬性運算式必須是整數類型，不支援64位運算式</dt> <dd> 指定的屬性變數或運算式必須是整數類資料類型。 當屬性運算式型別無法解析為整數時，就會發生這個錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2060"></span><span id="midl2060"></span><dl> <dt><strong>MIDL2060</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__requires__ms_ext"></span><span id="_BYTE_COUNT__REQUIRES__MS_EXT"></span>[byte_count] 需要/ms_ext</dt> <dd> [<a href="byte-count.md"><strong>Byte_count</strong></a>] 屬性是 DCE IDL 的 Microsoft 延伸模組。 若要使用這個屬性，您無法使用 <a href="-osf.md"><strong>/osf</strong></a> 參數進行編譯，這會覆寫 MIDL 編譯器預設參數 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 和 <a href="-c-ext.md"><strong>/c_ext</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2061"></span><span id="midl2061"></span><dl> <dt><strong>MIDL2061</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__can_be_applied_only_to_out_parameters_of_pointer_type"></span><span id="_BYTE_COUNT__CAN_BE_APPLIED_ONLY_TO_OUT_PARAMETERS_OF_POINTER_TYPE"></span>[byte_count] 只能套用至指標類型的 out 參數</dt> <dd> [<a href="byte-count.md"><strong>Byte_count</strong></a>] 屬性只能套用至 [<a href="out-idl.md"><strong>out</strong></a>] 參數，而所有 [<strong>out</strong>] 參數都必須是指標類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2062"></span><span id="midl2062"></span><dl> <dt><strong>MIDL2062</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_pointer_to_a_conformant_array_or_structure"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_POINTER_TO_A_CONFORMANT_ARRAY_OR_STRUCTURE"></span>無法在符合標準的陣列或結構的指標上指定 [byte_count]</dt> <dd> [<a href="byte-count.md"><strong>Byte_count</strong></a>] 屬性無法套用至符合標準的陣列或結構。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2063"></span><span id="midl2063"></span><dl> <dt><strong>MIDL2063</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not__in__only_or_byte_count_parameter_is_not__out__only"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT__IN__ONLY_OR_BYTE_COUNT_PARAMETER_IS_NOT__OUT__ONLY"></span>指定位元組計數的參數不是 [in]，或 byte count 參數不是 [out]</dt> <dd> 與 [<a href="byte-count.md"><strong>byte_count</strong></a>] 相關聯的值必須從用戶端傳送到伺服器;它必須是 [<a href="in.md"><strong>in</strong></a>] 參數。 [<strong>Byte_count</strong>] 參數不需要是 [<strong>in，out</strong>] 參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2064"></span><span id="midl2064"></span><dl> <dt><strong>MIDL2064</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not_an_integral_type"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT_AN_INTEGRAL_TYPE"></span>指定位元組計數的參數不是整數類資料類型</dt> <dd> 與位元組計數相關聯的值必須是整數類型 <a href="int.md"><strong>int</strong></a>、 <a href="small.md"><strong>small</strong></a>、 <a href="short.md"><strong>short</strong></a>或 <a href="long.md"><strong>long</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2065"></span><span id="midl2065"></span><dl> <dt><strong>MIDL2065</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_parameter_with_size_attributes"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_PARAMETER_WITH_SIZE_ATTRIBUTES"></span>無法在具有 size 屬性的參數上指定 [byte_count]</dt> <dd> [<a href="byte-count.md"><strong>Byte_count</strong></a>] 屬性不能與其他大小屬性（例如 [<a href="size-is.md"><strong>size_is</strong></a>] 或 [<a href="length-is.md"><strong>length_is</strong></a>]）一起使用。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2066"></span><span id="midl2066"></span><dl> <dt><strong>MIDL2066</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_constant"></span><span id="_CASE__EXPRESSION_IS_NOT_CONSTANT"></span>[case] 運算式不是常數</dt> <dd> 針對 case 標籤指定的運算式不是常數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2067"></span><span id="midl2067"></span><dl> <dt><strong>MIDL2067</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_of_integral_type"></span><span id="_CASE__EXPRESSION_IS_NOT_OF_INTEGRAL_TYPE"></span>[case] 運算式不是整數類資料類型</dt> <dd> 針對 case 標籤指定的運算式不是整數類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2068"></span><span id="midl2068"></span><dl> <dt><strong>MIDL2068</strong></dt> </dl></td>
<td><dl> <dt><span id="specifying__context_handle__on_a_type_other_than_void___requires__ms_ext"></span><span id="SPECIFYING__CONTEXT_HANDLE__ON_A_TYPE_OTHER_THAN_VOID___REQUIRES__MS_EXT"></span>在 void * 以外的類型上指定 [coNtext_handle] 需要/ms_ext</dt> <dd> 如果是 DCE RPC 相容性，內容控制碼必須是 <strong>void *</strong>類型的指標。 如果您希望內容控制碼與 <strong>void *</strong>以外的類型產生關聯，請不要使用 midl 編譯器參數 <a href="-osf.md"><strong>/osf</strong></a>，它會覆寫 midl 編譯器預設參數 <a href="-ms-ext.md"><strong>/ms_ext</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2069"></span><span id="midl2069"></span><dl> <dt><strong>MIDL2069</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_more_than_one_parameter_with_each_of_comm_status_fault_status"></span><span id="CANNOT_SPECIFY_MORE_THAN_ONE_PARAMETER_WITH_EACH_OF_COMM_STATUS_FAULT_STATUS"></span>無法指定多個參數，每一個 comm_status/fault_status</dt> <dd> 程式只能有一個具有 [<a href="comm-status.md"><strong>comm_status</strong></a>] 屬性的參數。 其中最多隻能有一個具有 [<a href="fault-status.md"><strong>fault_status</strong></a>] 屬性的參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2070"></span><span id="midl2070"></span><dl> <dt><strong>MIDL2070</strong></dt> </dl></td>
<td><dl> <dt><span id="comm_status_fault_status_parameter_must_be_an__out__only_pointer_parameter"></span><span id="COMM_STATUS_FAULT_STATUS_PARAMETER_MUST_BE_AN__OUT__ONLY_POINTER_PARAMETER"></span>comm_status/fault_status 參數必須是 [out] only 指標參數</dt> <dd> 錯誤程式碼類型 [<a href="comm-status.md"><strong>comm_status</strong></a>] 和 [<a href="fault-status.md"><strong>fault_status</strong></a>] 會從伺服器傳送到用戶端，因此必須指定為 [<a href="out-idl.md"><strong>out</strong></a>] 參數。 由於 C 程式設計語言中的條件約束，所有的 [<strong>out</strong>] 參數都必須是指標。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2071"></span><span id="midl2071"></span><dl> <dt><strong>MIDL2071</strong></dt> </dl></td>
<td><dl> <dt><span id="endpoint_syntax_error"></span><span id="ENDPOINT_SYNTAX_ERROR"></span>端點語法錯誤</dt> <dd> 端點語法不正確。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2072"></span><span id="midl2072"></span><dl> <dt><strong>MIDL2072</strong></dt> </dl></td>
<td><dl> <dt><span id="inapplicable_attribute"></span><span id="INAPPLICABLE_ATTRIBUTE"></span>不適用屬性</dt> <dd> 無法在此結構中套用指定的屬性。 例如，字串屬性會套用至 <a href="char-idl.md"><strong>char</strong></a> 陣列或 <strong>char</strong> 指標，且無法套用至包含兩個 <a href="short.md"><strong>小</strong></a> 整數的結構： <br/>
<pre class="syntax" data-space="preserve"><code>typedef [string] struct moo 
{
    short x;
    short y;
};</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2073"></span><span id="midl2073"></span><dl> <dt><strong>MIDL2073</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__requires__ms_ext"></span><span id="_ALLOCATE__REQUIRES__MS_EXT"></span>[配置] 需要/ms_ext</dt> <dd> <a href="allocate.md"><strong>配置</strong></a>屬性代表未定義為 DCE RPC 一部分的 Microsoft 擴充功能。 若要使用這個屬性，您無法使用 <a href="-osf.md"><strong>/osf</strong></a> 參數進行編譯，這會覆寫 MIDL 編譯器預設參數 <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2074"></span><span id="midl2074"></span><dl> <dt><strong>MIDL2074</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid__allocate__mode"></span><span id="INVALID__ALLOCATE__MODE"></span>不正確 [配置] 模式</dt> <dd> 已指定 [<a href="allocate.md"><strong>配置</strong></a>] 屬性結構的無效模式。 四種有效的模式是 single_node、all_nodes、on_null 和 always。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2075"></span><span id="midl2075"></span><dl> <dt><strong>MIDL2075</strong></dt> </dl></td>
<td><dl> <dt><span id="length_attributes_cannot_be_applied_with_string_attribute"></span><span id="LENGTH_ATTRIBUTES_CANNOT_BE_APPLIED_WITH_STRING_ATTRIBUTE"></span>長度屬性無法套用至字串屬性</dt> <dd> 使用字串屬性時，產生的存根檔案會呼叫 <strong>strlen</strong> 函數來判斷字串長度。 請勿使用相同變數的 length 屬性和 string 屬性。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2076"></span><span id="midl2076"></span><dl> <dt><strong>MIDL2076</strong></dt> </dl></td>
<td><dl> <dt><span id="_last_is__and__length_is__cannot_be_specified_at_the_same_time"></span><span id="_LAST_IS__AND__LENGTH_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>無法同時指定 [last_is] 和 [length_is]</dt> <dd> 已為相同的陣列指定 [<a href="last-is.md"><strong>last_is</strong></a>] 和 [<a href="length-is.md"><strong>length_is</strong></a>]。 這些屬性的關聯如下： length = last first + 1。 因為每個值都可以從另一個值衍生，所以請不要同時指定兩者。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2077"></span><span id="midl2077"></span><dl> <dt><strong>MIDL2077</strong></dt> </dl></td>
<td><dl> <dt><span id="_max_is__and__size_is__cannot_be_specified_at_the_same_time"></span><span id="_MAX_IS__AND__SIZE_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>無法同時指定 [max_is] 和 [size_is]</dt> <dd> 已為相同的陣列指定 [ <a href="max-is.md"><strong>max_is</strong></a>] 和 [ <a href="size-is.md"><strong>size_is</strong></a>]。 這些屬性的關聯如下： max = size + 1。 因為每個值都可以從另一個值衍生，所以請不要同時指定兩者。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2078"></span><span id="midl2078"></span><dl> <dt><strong>MIDL2078</strong></dt> </dl></td>
<td><dl> <dt><span id="no__switch_is__attribute_specified_at_use_of_union"></span><span id="NO__SWITCH_IS__ATTRIBUTE_SPECIFIED_AT_USE_OF_UNION"></span>使用 union 時未指定 [switch_is] 屬性</dt> <dd> 尚未為聯集指定判別。 [<a href="switch-is.md"><strong>Switch_is</strong></a>] 屬性工作表示用來在聯集欄位之間選取的判別。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2079"></span><span id="midl2079"></span><dl> <dt><strong>MIDL2079</strong></dt> </dl></td>
<td><dl> <dt><span id="no__uuid__specified"></span><span id="NO__UUID__SPECIFIED"></span>未指定 [uuid]</dt> <dd> 未指定介面的 UUID。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2080"></span><span id="midl2080"></span><dl> <dt><strong>MIDL2080</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__ignored_on__local__interface"></span><span id="_UUID__IGNORED_ON__LOCAL__INTERFACE"></span>[local] 介面上已忽略 [uuid]</dt> <dd> 使用物件介面上的 [<a href="local.md"><strong>local</strong></a>] 屬性會導致 MIDL 編譯器忽略 [<a href="uuid.md"><strong>uuid</strong></a>] 屬性。 您無法在 RPC 介面上使用這兩個屬性。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2081"></span><span id="midl2081"></span><dl> <dt><strong>MIDL2081</strong></dt> </dl></td>
<td><dl> <dt><span id="type_mismatch_between_length_and_size_attribute_expressions"></span><span id="TYPE_MISMATCH_BETWEEN_LENGTH_AND_SIZE_ATTRIBUTE_EXPRESSIONS"></span>長度和大小屬性運算式之間的類型不符</dt> <dd> Length 和 size 屬性運算式必須屬於相同的類型。 例如，當 [<a href="size-is.md"><strong>size_is</strong></a>] 運算式的屬性變數的類型不 <strong>帶正負</strong> 號，且 [<a href="length-is.md"><strong>length_is</strong></a>] 運算式的屬性變數為 <a href="long.md"><strong>long</strong></a>類型時，就會發出此警告。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2082"></span><span id="midl2082"></span><dl> <dt><strong>MIDL2082</strong></dt> </dl></td>
<td><dl> <dt><span id="_string__attribute_must_be_specified__byte____char___or__wchar_t__array_or_pointer"></span><span id="_STRING__ATTRIBUTE_MUST_BE_SPECIFIED__BYTE____CHAR___OR__WCHAR_T__ARRAY_OR_POINTER"></span>[string] 屬性必須指定 &quot; byte、 &quot; &quot; char &quot; 或 &quot; wchar_t &quot; 陣列或指標</dt> <dd> 字串屬性無法套用至其基底類型不是 <a href="byte.md"><strong>位元組</strong></a>、 <a href="char-idl.md"><strong>char</strong></a>或 <a href="struct.md"><strong>結構</strong></a> 的指標或陣列，其中的成員全部為 <strong>位元組</strong> 或 <strong>字元</strong> 類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2083"></span><span id="midl2083"></span><dl> <dt><strong>MIDL2083</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_between_the_type_of_the__switch_is__expression_and_the_switch_type_of_the_union"></span><span id="MISMATCH_BETWEEN_THE_TYPE_OF_THE__SWITCH_IS__EXPRESSION_AND_THE_SWITCH_TYPE_OF_THE_UNION"></span>[switch_is] 運算式的型別與 union 的 switch 型別不相符</dt> <dd> 如果未指定聯集 [<a href="switch-type.md"><strong>switch_type</strong></a>]，參數類型會與 [<a href="switch-is.md"><strong>switch_is</strong></a>] 欄位的類型相同。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2084"></span><span id="midl2084"></span><dl> <dt><strong>MIDL2084</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_that_derives_from_a_context_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_DERIVES_FROM_A_CONTEXT_HANDLE"></span>[transmit_as] 不得套用至衍生自內容控制碼的型別</dt> <dd> 內容控制碼無法以其他類型的形式傳送。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2085"></span><span id="midl2085"></span><dl> <dt><strong>MIDL2085</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_specify_a_transmissible_type"></span><span id="_TRANSMIT_AS__MUST_SPECIFY_A_TRANSMISSIBLE_TYPE"></span>[transmit_as] 必須指定 transmissible 類型</dt> <dd> 指定的 [<a href="transmit-as.md"><strong>transmit_as</strong></a>] 類型衍生自無法由 Microsoft RPC 傳送的類型，例如 <a href="void.md"><strong>void</strong></a>、 <strong>void *</strong>或 <a href="int.md"><strong>int</strong></a>。使用已定義的 RPC 基底類型;如果是 <strong>int</strong>，請新增大小規範（例如 <a href="small.md"><strong>small</strong></a>、 <a href="short.md"><strong>short</strong></a>或 <a href="long.md"><strong>long</strong></a> ）來限定 <strong>int</strong>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2086"></span><span id="midl2086"></span><dl> <dt><strong>MIDL2086</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_for__transmit_as__and__represent_as__must_not_be_a_pointer_or_derive_from_a_pointer"></span><span id="TRANSMITTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_BE_A_POINTER_OR_DERIVE_FROM_A_POINTER"></span>[transmit_as] 和 [represent_as] 的傳輸類型不得為指標或衍生自指標</dt> <dd> 傳送的型別不能是指標，也不能衍生自指標。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2087"></span><span id="midl2087"></span><dl> <dt><strong>MIDL2087</strong></dt> </dl></td>
<td><dl> <dt><span id="presented_type_for__transmit_as__and__represent_as__must_not_derive_from_a_conformant_varying_array__its_pointer_equivalent__or_a_conformant_varying_structure"></span><span id="PRESENTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY__ITS_POINTER_EQUIVALENT__OR_A_CONFORMANT_VARYING_STRUCTURE"></span>[transmit_as] 和 [represent_as] 的呈現類型不能衍生自符合/變化的陣列、其指標相等或符合/不同的結構</dt> <dd> [<a href="transmit-as.md"><strong>Transmit_as</strong></a>] 已套用的類型無法衍生自符合標準的陣列或結構， (在執行時間) 判斷其大小的陣列或結構。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2088"></span><span id="midl2088"></span><dl> <dt><strong>MIDL2088</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__format_is_incorrect"></span><span id="_UUID__FORMAT_IS_INCORRECT"></span>[uuid] 格式不正確</dt> <dd> UUID 格式不符合規格。 UUID 必須是由五個十六進位數位序列組成的字串，長度為8、4、4、4和12位數。 &quot;12345678-1234-ABCD-EF01-28A49C28F17D &quot; 是有效的 UUID。 使用函數 <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate"><strong>UuidCreate</strong></a> 或公用程式來產生有效的 UUID。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2089"></span><span id="midl2089"></span><dl> <dt><strong>MIDL2089</strong></dt> </dl></td>
<td><dl> <dt><span id="uuid_is_not_a_hexadecimal_number"></span><span id="UUID_IS_NOT_A_HEXADECIMAL_NUMBER"></span>uuid 不是十六進位數位</dt> <dd> 為介面指定的 UUID 包含在十六進位數位標記法中不正確字元。 字元0到9和 A 到 F 在十六進位標記法中是有效的。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2090"></span><span id="midl2090"></span><dl> <dt><strong>MIDL2090</strong></dt> </dl></td>
<td><dl> <dt><span id="optional_parameters_must_come_after_required_parameters"></span><span id="OPTIONAL_PARAMETERS_MUST_COME_AFTER_REQUIRED_PARAMETERS"></span>選擇性參數必須在必要參數之後</dt> <dd> 如需參數清單順序的描述，請參閱 MIDL 語言參考中的 [<a href="optional.md"><strong>選擇性</strong></a>]。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2091"></span><span id="midl2091"></span><dl> <dt><strong>MIDL2091</strong></dt> </dl></td>
<td><dl> <dt><span id="_dllname__required_when__entry__is_used"></span><span id="_DLLNAME__REQUIRED_WHEN__ENTRY__IS_USED"></span>當使用 [entry] 時，需要 [dllname]</dt> <dd> 如果您要在 DLL 中指定進入點，您也必須使用 [<a href="dllname-str-.md"><strong>dllname</strong></a>] 屬性來指定該 dll 的名稱。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2092"></span><span id="midl2092"></span><dl> <dt><strong>MIDL2092</strong></dt> </dl></td>
<td><dl> <dt><span id="_bindable__is_invalid_without__propget____propput___or__propputref_"></span><span id="_BINDABLE__IS_INVALID_WITHOUT__PROPGET____PROPPUT___OR__PROPPUTREF_"></span>[可系結] 無效，沒有 [propget]、[propput] 或 [propputref]</dt> <dd> <a href="bindable.md"><strong>[可</strong></a>系結] 屬性僅適用于屬性，因此您也必須指定其中一個屬性存取或屬性設定函數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2093"></span><span id="midl2093"></span><dl> <dt><strong>MIDL2093</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput__or__propputref__must_have_at_least_one_parameter"></span><span id="PROCEDURES_WITH__PROPPUT__OR__PROPPUTREF__MUST_HAVE_AT_LEAST_ONE_PARAMETER"></span>具有 [propput] 或 [propputref] 的程式必須至少有一個參數</dt> <dd> [<a href="propput.md"><strong>Propput</strong></a>] 或 [ <a href="propputref.md"><strong>propputref</strong></a>] 程式必須至少有一個具有要設定之屬性的 [<a href="in.md"><strong>in</strong></a>] 參數;[<a href="propget.md"><strong>propget</strong></a>] 程式必須至少有一個 [<a href="out-idl.md"><strong>out</strong></a>， <a href="retval.md"><strong>retval</strong></a>] 參數才能接收屬性或參考。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2094"></span><span id="midl2094"></span><dl> <dt><strong>MIDL2094</strong></dt> </dl></td>
<td><dl> <dt><span id="_id__attribute_is_required"></span><span id="_ID__ATTRIBUTE_IS_REQUIRED"></span>[識別碼] 屬性為必要項</dt> <dd> 這個成員函式的原因是，由於使用的是使用的分配 <a href="dispinterface.md"><strong>介面</strong></a> ，因此需要 DISPID，您可以使用 [ <a href="id.md"><strong>id</strong></a>] 屬性來指定此函數。 當您使用屬性和方法來指定分配 <strong>介面</strong> 時，您必須為每個屬性和方法指定 DISPID。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2095"></span><span id="midl2095"></span><dl> <dt><strong>MIDL2095</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_name_specified_in_the_ACF_does_not_match_that_specified_in_the_IDL_file"></span><span id="interface_name_specified_in_the_acf_does_not_match_that_specified_in_the_idl_file"></span><span id="INTERFACE_NAME_SPECIFIED_IN_THE_ACF_DOES_NOT_MATCH_THAT_SPECIFIED_IN_THE_IDL_FILE"></span>在 ACF 中指定的介面名稱與 IDL 檔案中指定的介面名稱不相符</dt> <dd> 在目前的編譯器模式中，ACF 中 interface 關鍵字後面的名稱必須與 IDL 檔案中 interface 關鍵字後面的名稱相同。 當您使用 MIDL 編譯器參數 <a href="-acf.md"><strong>/acf</strong></a>編譯時，IDL 和 ACF 檔案中的介面名稱可能會不同。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2096"></span><span id="midl2096"></span><dl> <dt><strong>MIDL2096</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicated_attribute"></span><span id="DUPLICATED_ATTRIBUTE"></span>重複的屬性</dt> <dd> 指定了重複或衝突的屬性。 當兩個屬性互斥時，通常會發生這個錯誤。 例如，不能同時使用屬性 [程式<a href="code.md"><strong>代碼</strong></a>] 和 [<a href="nocode.md"><strong>了 nocode</strong></a>]。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2097"></span><span id="midl2097"></span><dl> <dt><strong>MIDL2097</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_with__comm_status__or__fault_status__attribute_must_be_a_pointer_to_type_error_status_t"></span><span id="PARAMETER_WITH__COMM_STATUS__OR__FAULT_STATUS__ATTRIBUTE_MUST_BE_A_POINTER_TO_TYPE_ERROR_STATUS_T"></span>具有 [comm_status] 或 [fault_status] 屬性的參數必須是類型的指標 error_status_t</dt> <dd> 當 [<a href="fault-status.md"><strong>fault_status</strong></a>] 或 [<a href="comm-status.md"><strong>comm_status</strong></a>] 當做參數屬性使用時，參數必須是類型<a href="error-status-t.md"><strong>error_status_t</strong></a>的 [<a href="out-idl.md"><strong>out</strong></a>] 參數。 如果發生伺服器錯誤，參數會設定為錯誤碼。 當遠端呼叫順利完成時，程式會設定此值。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2098"></span><span id="midl2098"></span><dl> <dt><strong>MIDL2098</strong></dt> </dl></td>
<td><dl> <dt><span id="a__local__procedure_cannot_be_specified_in_ACF_file"></span><span id="a__local__procedure_cannot_be_specified_in_acf_file"></span><span id="A__LOCAL__PROCEDURE_CANNOT_BE_SPECIFIED_IN_ACF_FILE"></span>無法在 ACF 檔中指定 [local] 程式</dt> <dd> 已在 ACF 中指定本機程式。 本機程式只能在 IDL 檔案中指定。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2099"></span><span id="midl2099"></span><dl> <dt><strong>MIDL2099</strong></dt> </dl></td>
<td><dl> <dt><span id="specified_type_is_not_defined_as_a_handle"></span><span id="SPECIFIED_TYPE_IS_NOT_DEFINED_AS_A_HANDLE"></span>指定的類型未定義為控制碼</dt> <dd> 在 [<a href="implicit-handle.md"><strong>implicit_handle</strong></a>] 屬性中指定的型別未定義為控制碼類型。 變更類型定義或屬性所指定的類型名稱。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2100"></span><span id="midl2100"></span><dl> <dt><strong>MIDL2100</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_undefined"></span><span id="PROCEDURE_UNDEFINED"></span>未定義程式</dt> <dd> 屬性已套用至 ACF 中的程式，且該程式未定義于 IDL 檔案中。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2101"></span><span id="midl2101"></span><dl> <dt><strong>MIDL2101</strong></dt> </dl></td>
<td><dl> <dt><span id="this_parameter_does_not_exist_in_the_IDL_file"></span><span id="this_parameter_does_not_exist_in_the_idl_file"></span><span id="THIS_PARAMETER_DOES_NOT_EXIST_IN_THE_IDL_FILE"></span>此參數不存在於 IDL 檔案中</dt> <dd> 在 ACF 中指定的參數不存在於 IDL 檔案的定義中。 出現在 ACF 中的所有參數、函數和類型定義，都必須對應至 IDL 檔案中先前定義的參數、函式和類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2102"></span><span id="midl2102"></span><dl> <dt><strong>MIDL2102</strong></dt> </dl></td>
<td><dl> <dt><span id="this_array-bounds_construct_is_not_supported"></span><span id="THIS_ARRAY-BOUNDS_CONSTRUCT_IS_NOT_SUPPORTED"></span>不支援這個陣列界限結構</dt> <dd> MIDL 目前支援在表單陣列中表示陣列的上限和下限 [較低]。 Upper]，只有在指定陣列下限的常數解析為零值時才會。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2103"></span><span id="midl2103"></span><dl> <dt><strong>MIDL2103</strong></dt> </dl></td>
<td><dl> <dt><span id="array_bound_specification_is_illegal"></span><span id="ARRAY_BOUND_SPECIFICATION_IS_ILLEGAL"></span>陣列系結規格不合法</dt> <dd> 固定大小陣列的陣列界限使用者規格不合法。 例如： <br/>
<pre class="syntax" data-space="preserve"><code>typedef short Array[-1]</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2104"></span><span id="midl2104"></span><dl> <dt><strong>MIDL2104</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_conformant_array_or_an_array_that_contains_a_conformant_array_is_not_supported"></span><span id="POINTER_TO_A_CONFORMANT_ARRAY_OR_AN_ARRAY_THAT_CONTAINS_A_CONFORMANT_ARRAY_IS_NOT_SUPPORTED"></span>不支援符合標準陣列的指標或包含符合一致性陣列的陣列</dt> <dd> 符合標準的陣列使用方式。 如需管理符合規範之陣列的規則，請參閱 <a href="/windows/desktop/Rpc/arrays-and-rpc">陣列和 RPC</a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2105"></span><span id="midl2105"></span><dl> <dt><strong>MIDL2105</strong></dt> </dl></td>
<td><dl> <dt><span id="pointee_array_does_not_derive_any_size"></span><span id="POINTEE_ARRAY_DOES_NOT_DERIVE_ANY_SIZE"></span>pointee/陣列不會衍生任何大小</dt> <dd> 指定了一致的陣列，但沒有任何大小規格。 您可以使用 [<a href="max-is.md"><strong>max_is</strong></a>] 或 [<a href="size-is.md"><strong>size_is</strong></a>] 屬性來指定大小。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2106"></span><span id="midl2106"></span><dl> <dt><strong>MIDL2106</strong></dt> </dl></td>
<td><dl> <dt><span id="only_fixed_arrays_and_SAFEARRAYs_are_legal_in_a_type_library"></span><span id="only_fixed_arrays_and_safearrays_are_legal_in_a_type_library"></span><span id="ONLY_FIXED_ARRAYS_AND_SAFEARRAYS_ARE_LEGAL_IN_A_TYPE_LIBRARY"></span>只有固定的陣列和 Safearray 在類型程式庫中是合法的</dt> <dd> 您已在無法在類型程式庫中使用的程式庫語句內使用陣列類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2107"></span><span id="midl2107"></span><dl> <dt><strong>MIDL2107</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAYs_are_only_legal_inside_a_library_block"></span><span id="safearrays_are_only_legal_inside_a_library_block"></span><span id="SAFEARRAYS_ARE_ONLY_LEGAL_INSIDE_A_LIBRARY_BLOCK"></span>Safearray 在程式庫區塊內只有合法</dt> <dd> 除非在產生類型程式庫時，MIDL 編譯器無法將 SAFEARRAY 辨識為有效的資料類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2108"></span><span id="midl2108"></span><dl> <dt><strong>MIDL2108</strong></dt> </dl></td>
<td><dl> <dt><span id="badly_formed_character_constant"></span><span id="BADLY_FORMED_CHARACTER_CONSTANT"></span>格式不正確的字元常數</dt> <dd> 字元常數中不允許使用行尾字元。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2109"></span><span id="midl2109"></span><dl> <dt><strong>MIDL2109</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_comment"></span><span id="END_OF_FILE_FOUND_IN_COMMENT"></span>在批註中找到的檔案結尾</dt> <dd> 批註中遇到檔案結尾字元。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2110"></span><span id="midl2110"></span><dl> <dt><strong>MIDL2110</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_string"></span><span id="END_OF_FILE_FOUND_IN_STRING"></span>在字串中找到的檔案結尾</dt> <dd> 在字串中遇到檔案結尾字元。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2111"></span><span id="midl2111"></span><dl> <dt><strong>MIDL2111</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_length_exceeds_31_characters"></span><span id="IDENTIFIER_LENGTH_EXCEEDS_31_CHARACTERS"></span>識別碼長度超過31個字元</dt> <dd> 識別碼限制為31個英數位元。 長度超過31個字元的識別碼名稱會被截斷。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2112"></span><span id="midl2112"></span><dl> <dt><strong>MIDL2112</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_line_found_in_string"></span><span id="END_OF_LINE_FOUND_IN_STRING"></span>在字串中找到的行尾</dt> <dd> 在字串中遇到行結尾字元。 確認您已包含可結束字串的雙引號字元。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2113"></span><span id="midl2113"></span><dl> <dt><strong>MIDL2113</strong></dt> </dl></td>
<td><dl> <dt><span id="string_constant_exceeds_limit_of_255_characters"></span><span id="STRING_CONSTANT_EXCEEDS_LIMIT_OF_255_CHARACTERS"></span>字串常數超過255個字元的限制</dt> <dd> 字串超過允許的最大長度255個字元。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2114"></span><span id="midl2114"></span><dl> <dt><strong>MIDL2114</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_exceeds_limit_of_255_characters_and_has_been_truncated"></span><span id="IDENTIFIER_EXCEEDS_LIMIT_OF_255_CHARACTERS_AND_HAS_BEEN_TRUNCATED"></span>識別碼超過255個字元的限制，且已被截斷</dt> <dd> 識別碼超過最大允許長度255個字元。 識別碼中多餘的字元會被截斷。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2115"></span><span id="midl2115"></span><dl> <dt><strong>MIDL2115</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_too_big"></span><span id="CONSTANT_TOO_BIG"></span>常數太大</dt> <dd> 常數太大而無法在內部表示。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2116"></span><span id="midl2116"></span><dl> <dt><strong>MIDL2116</strong></dt> </dl></td>
<td><dl> <dt><span id="numerical_parsing_error"></span><span id="NUMERICAL_PARSING_ERROR"></span>數值剖析錯誤</dt> <dd> 編譯器無法剖析數值識別碼。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2117"></span><span id="midl2117"></span><dl> <dt><strong>MIDL2117</strong></dt> </dl></td>
<td><dl> <dt><span id="error_in_opening_file"></span><span id="ERROR_IN_OPENING_FILE"></span>開啟檔案時發生錯誤</dt> <dd> 作業系統在嘗試開啟輸出檔時回報了錯誤。 這個錯誤可能是因為名稱對檔案系統而言太長或檔案名重複所致。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2118"></span><span id="midl2118"></span><dl> <dt><strong>MIDL2118</strong></dt> </dl></td>
<td>函數系結時發生錯誤<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2119"></span><span id="midl2119"></span><dl> <dt><strong>MIDL2119</strong></dt> </dl></td>
<td>初始化 OLE 時發生錯誤<br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2120"></span><span id="midl2120"></span><dl> <dt><strong>MIDL2120</strong></dt> </dl></td>
<td>載入程式庫時發生錯誤<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2121"></span><span id="midl2121"></span><dl> <dt><strong>MIDL2121</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_must_not_derive_from_a_top-level__unique__or__ptr__pointer_array"></span><span id="_OUT__ONLY_PARAMETER_MUST_NOT_DERIVE_FROM_A_TOP-LEVEL__UNIQUE__OR__PTR__POINTER_ARRAY"></span>[out] 只有參數不能衍生自最上層 [unique] 或 [ptr] 指標/陣列</dt> <dd> 唯一的指標不能是 [<a href="out-idl.md"><strong>out</strong></a>]-唯一的參數。 根據定義，唯一的指標可以從 <strong>Null</strong> 變更為非<strong>null</strong>。 沒有 [<strong>out</strong>] 參數的相關資訊會從用戶端傳遞至伺服器。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2122"></span><span id="midl2122"></span><dl> <dt><strong>MIDL2122</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_is_not_applicable_to_this_non-rpcable_union"></span><span id="ATTRIBUTE_IS_NOT_APPLICABLE_TO_THIS_NON-RPCABLE_UNION"></span>屬性不適用於這個非 rpcable 聯集</dt> <dd> 只有 [<a href="switch-is.md"><strong>switch_is</strong></a>] 和 [<a href="switch-type.md"><strong>switch_type</strong></a>] 屬性會套用至做為遠端程序呼叫一部分傳送的聯集。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2123"></span><span id="midl2123"></span><dl> <dt><strong>MIDL2123</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_size_attribute_must_not_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_SIZE_ATTRIBUTE_MUST_NOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>用於 size 屬性的運算式不能衍生自 [out]-only 參數</dt> <dd> [<a href="out-idl.md"><strong>Out</strong></a>] 參數的值不會傳送到伺服器，也不能用來判斷 [<a href="in.md"><strong>in</strong></a>] 參數的長度或大小。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2124"></span><span id="midl2124"></span><dl> <dt><strong>MIDL2124</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_length_attribute_for_an__in__parameter_cannot_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_LENGTH_ATTRIBUTE_FOR_AN__IN__PARAMETER_CANNOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>用於 [in] 參數之 length 屬性的運算式不能衍生自 [out] 參數</dt> <dd> [<a href="out-idl.md"><strong>Out</strong></a>] 參數的值不會傳送到伺服器，也不能用來判斷 [<a href="in.md"><strong>in</strong></a>] 參數的長度或大小。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2125"></span><span id="midl2125"></span><dl> <dt><strong>MIDL2125</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__int__needs__c_ext"></span><span id="USE_OF__INT__NEEDS__C_EXT"></span>使用 &quot; int &quot; 需求/c_ext</dt> <dd> MIDL 是強型別語言。 透過網路傳輸的所有參數都必須衍生自其中一個 MIDL 基底類型。 類型 <a href="int.md"><strong>int</strong></a> 未定義為 MIDL 的一部分。 傳輸的資料必須包含大小規範： <a href="small.md"><strong>small</strong></a>、 <strong>short</strong>或 <strong>long</strong>。 未透過網路傳輸的資料可以包含在介面中;使用 <a href="-c-ext.md"><strong>/c_ext</strong></a> 參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2126"></span><span id="midl2126"></span><dl> <dt><strong>MIDL2126</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_be__void_"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_BE__VOID_"></span>結構/等位欄位不得為 &quot; void&quot;</dt> <dd> 結構或等位中的欄位，必須宣告為 MIDL 所支援的特定基底類型，或是衍生自基底類型的類型。 遠端作業中不允許 Void 類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2127"></span><span id="midl2127"></span><dl> <dt><strong>MIDL2127</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_void"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_VOID"></span>陣列元素不得為 void</dt> <dd> 陣列元素不可以是 void。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2128"></span><span id="midl2128"></span><dl> <dt><strong>MIDL2128</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_type_qualifiers_and_or_modifiers_needs__c_ext"></span><span id="USE_OF_TYPE_QUALIFIERS_AND_OR_MODIFIERS_NEEDS__C_EXT"></span>使用類型限定詞及/或修飾詞需要/c_ext</dt> <dd> 只有當您指定<a href="-c-ext.md"><strong>/c_ext</strong></a>參數時，才能編譯型別修飾詞，例如<strong>_cdecl</strong>和<strong>_far</strong> 。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2129"></span><span id="midl2129"></span><dl> <dt><strong>MIDL2129</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_a_function"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_A_FUNCTION"></span>結構/等位欄位不能衍生自函數</dt> <dd> 結構或等位的欄位必須是 MIDL 基底類型或衍生自這些基底類型的類型。 函數在結構或等位欄位中不合法。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2130"></span><span id="midl2130"></span><dl> <dt><strong>MIDL2130</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_a_function"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_A_FUNCTION"></span>陣列元素不得為函式</dt> <dd> 陣列元素不能是函數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2131"></span><span id="midl2131"></span><dl> <dt><strong>MIDL2131</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_be_a_function"></span><span id="PARAMETER_MUST_NOT_BE_A_FUNCTION"></span>參數不得為函式</dt> <dd> 遠端程式的參數必須是指定類型的變數。 函數不能是遠端程式的參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2132"></span><span id="midl2132"></span><dl> <dt><strong>MIDL2132</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_with_bit_fields_needs__c_ext"></span><span id="STRUCT_UNION_WITH_BIT_FIELDS_NEEDS__C_EXT"></span>具有位欄位的結構/等位需要/c_ext</dt> <dd> 您必須指定 MIDL 編譯器參數 <a href="-c-ext.md"><strong>/c_ext</strong></a> ，以允許在遠端程序呼叫中不會傳輸之結構中的位欄位。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2133"></span><span id="midl2133"></span><dl> <dt><strong>MIDL2133</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ANSI-compatible_extension"></span><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ansi-compatible_extension"></span><span id="BIT_FIELD_SPECIFICATION_ON_A_TYPE_OTHER_THAT__INT__IS_A_NON-ANSI-COMPATIBLE_EXTENSION"></span>int 類型的位欄位規格 &quot; &quot; 為非 ANSI 相容的延伸模組</dt> <dd> ANSI C 程式設計語言規格不允許將位欄位套用至非整數類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2134"></span><span id="midl2134"></span><dl> <dt><strong>MIDL2134</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_can_be_applied_only_to_simple__integral_types"></span><span id="BIT_FIELD_SPECIFICATION_CAN_BE_APPLIED_ONLY_TO_SIMPLE__INTEGRAL_TYPES"></span>位欄位規格只能套用至簡單、整數類型</dt> <dd> ANSI C 程式設計語言規格不允許將位欄位套用至非整數類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2135"></span><span id="midl2135"></span><dl> <dt><strong>MIDL2135</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_handle_t_or_a_context-handle"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT-HANDLE"></span>結構/等位欄位不能衍生自 handle_t 或內容控制碼</dt> <dd> 無法將內容控制碼傳輸為另一個結構的一部分。 它們必須以內容控制碼的形式傳送。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2136"></span><span id="midl2136"></span><dl> <dt><strong>MIDL2136</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_handle_t_or_a_context_handle"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT_HANDLE"></span>陣列元素不能衍生自 handle_t 或內容控制碼</dt> <dd> 內容控制碼無法做為陣列的一部分傳送。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2137"></span><span id="midl2137"></span><dl> <dt><strong>MIDL2137</strong></dt> </dl></td>
<td><dl> <dt><span id="this_specification_of_union_needs__c_ext"></span><span id="THIS_SPECIFICATION_OF_UNION_NEEDS__C_EXT"></span>這種 union 需求的規格/c_ext</dt> <dd> 出現在介面定義中的聯集必須與判別相關聯或宣告為 local。 當您使用 <a href="-c-ext.md"><strong>/c_ext</strong></a> 參數（即 MIDL 預設值）時，無法透過網路傳輸的資料可以隱含地宣告為本機。 您無法使用 <a href="-osf.md"><strong>/osf</strong></a> 參數編譯此 IDL。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2138"></span><span id="midl2138"></span><dl> <dt><strong>MIDL2138</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="PARAMETER_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>從 int 衍生的參數的 &quot; &quot; 大小規範必須是 &quot; small、 &quot; &quot; short &quot; 或 &quot; long （ &quot; &quot; 整數）&quot;</dt> <dd> 類型 <a href="int.md"><strong>int</strong></a> 只有在32位平臺上的有效 MIDL 類型，在16位系統上的 <strong>int</strong> 必須伴隨大小規格。 使用其中一個 <a href="small.md"><strong>小</strong></a>、 <a href="short.md"><strong>短</strong></a>或 <a href="long.md"><strong>長</strong></a>的大小規範。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2139"></span><span id="midl2139"></span><dl> <dt><strong>MIDL2139</strong></dt> </dl></td>
<td><dl> <dt><span id="type_of_the_parameter_cannot_derive_from_void_or_void_"></span><span id="TYPE_OF_THE_PARAMETER_CANNOT_DERIVE_FROM_VOID_OR_VOID_"></span>參數的類型不能衍生自 void 或 void *</dt> <dd> MIDL 是強型別語言。 透過網路傳輸的所有參數都必須衍生自其中一個 MIDL 基底類型。 MIDL 不支援 <a href="void.md"><strong>void</strong></a> 做為基底類型。 您必須將宣告變更為有效的 MIDL 型別。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2140"></span><span id="midl2140"></span><dl> <dt><strong>MIDL2140</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_a_struct_union_containing_bit_fields_is_not_supported"></span><span id="PARAMETER_DERIVING_FROM_A_STRUCT_UNION_CONTAINING_BIT_FIELDS_IS_NOT_SUPPORTED"></span>不支援衍生自包含位欄位之結構/等位的參數</dt> <dd> DCE RPC 未將位欄位定義為有效的資料類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2141"></span><span id="midl2141"></span><dl> <dt><strong>MIDL2141</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_a_parameter_deriving_from_a_type_containing_type-modifiers_type-qualifiers_needs__c_ext"></span><span id="USE_OF_A_PARAMETER_DERIVING_FROM_A_TYPE_CONTAINING_TYPE-MODIFIERS_TYPE-QUALIFIERS_NEEDS__C_EXT"></span>使用衍生自類型的參數，其中包含型別修飾詞/型別限定詞需求/c_ext</dt> <dd> 在 IDL 檔案中使用關鍵字（例如 <strong>遠</strong>、 <strong>near</strong>、 <a href="const.md"><strong>Const</strong></a>和 <strong>volatile</strong> ）是 MICROSOFT 擴充功能，可延伸至 DCE RPC。 當您使用 <a href="-osf.md"><strong>/osf</strong></a> 參數編譯時，無法使用這些關鍵字，這會關閉預設 <a href="-c-ext.md"><strong>/c_ext</strong></a> 擴充功能參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2142"></span><span id="midl2142"></span><dl> <dt><strong>MIDL2142</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_pointer_to_a_function"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>參數不能衍生自函式的指標</dt> <dd> RPC 執行時間程式庫會在用戶端與伺服器之間傳輸指標和其相關聯的資料。 無法以參數形式傳送函式的指標，因為無法透過網路傳送函式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2143"></span><span id="midl2143"></span><dl> <dt><strong>MIDL2143</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_nonrpccapable_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>參數不能衍生自 nonrpc 支援的聯集</dt> <dd> 聯集必須與判別相關聯。 使用 [<a href="switch-is.md"><strong>switch_is</strong></a>] 和 [<a href="switch-type.md"><strong>switch_type</strong></a>] 屬性。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2144"></span><span id="midl2144"></span><dl> <dt><strong>MIDL2144</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_derives_from_an__int.__You_must_use_size_specifiers_with_the__int_"></span><span id="return_type_derives_from_an__int.__you_must_use_size_specifiers_with_the__int_"></span><span id="RETURN_TYPE_DERIVES_FROM_AN__INT.__YOU_MUST_USE_SIZE_SPECIFIERS_WITH_THE__INT_"></span>傳回型別衍生自 &quot; int。 &quot; 您必須使用大小規範搭配 &quot; int&quot;</dt> <dd> 在16位系統上，型別 <a href="int.md"><strong>int</strong></a> 不是有效的 MIDL 型別，除非它伴隨著大小規格。 使用其中一個 <a href="small.md"><strong>小</strong></a>、 <a href="short.md"><strong>短</strong></a>或 <a href="long.md"><strong>長</strong></a>的大小規範。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2145"></span><span id="midl2145"></span><dl> <dt><strong>MIDL2145</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_void_pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_VOID_POINTER"></span>傳回類型不能衍生自 void 指標</dt> <dd> MIDL 是強型別語言。 透過網路傳輸的所有參數都必須衍生自其中一個 MIDL 基底類型。 Void 類型未定義為 MIDL 的一部分。 您必須將宣告變更為有效的 MIDL 型別。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2146"></span><span id="midl2146"></span><dl> <dt><strong>MIDL2146</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_structure_union_containing_bit-fields"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_STRUCTURE_UNION_CONTAINING_BIT-FIELDS"></span>傳回類型不能衍生自包含位欄位的結構/等位</dt> <dd> DCE RPC 未將位欄位定義為有效的資料類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2147"></span><span id="midl2147"></span><dl> <dt><strong>MIDL2147</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_nonrpccapable_union"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>傳回類型不能衍生自具有 nonrpc 功能的聯集</dt> <dd> 聯集必須與判別相關聯。 使用 [<a href="switch-is.md"><strong>switch_is</strong></a>] 和 [<a href="switch-type.md"><strong>switch_type</strong></a>] 屬性。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2148"></span><span id="midl2148"></span><dl> <dt><strong>MIDL2148</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_pointer_to_a_function"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>傳回類型不能衍生自函式的指標</dt> <dd> RPC 執行時間程式庫會在用戶端與伺服器之間傳輸指標和其相關聯的資料。 無法以參數形式傳送函式的指標，因為 RPC 並未定義方法來透過網路傳輸相關聯的函式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2149"></span><span id="midl2149"></span><dl> <dt><strong>MIDL2149</strong></dt> </dl></td>
<td><dl> <dt><span id="compound_initializers_are_not_supported"></span><span id="COMPOUND_INITIALIZERS_ARE_NOT_SUPPORTED"></span>不支援複合初始化運算式</dt> <dd> DCE RPC 僅支援簡單初始化。 無法在 IDL 檔案中初始化結構或陣列。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2150"></span><span id="midl2150"></span><dl> <dt><strong>MIDL2150</strong></dt> </dl></td>
<td><dl> <dt><span id="ACF_attributes_in_the_IDL_file_need_the__app_config_switch"></span><span id="acf_attributes_in_the_idl_file_need_the__app_config_switch"></span><span id="ACF_ATTRIBUTES_IN_THE_IDL_FILE_NEED_THE__APP_CONFIG_SWITCH"></span>IDL 檔案中的 ACF 屬性需要/app_config 參數</dt> <dd> Microsoft 擴充功能可讓您指定 IDL 檔案中的 ACF 屬性。 使用 <a href="-app-config.md"><strong>/app_config</strong></a> 參數來啟用此延伸模組。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2151"></span><span id="midl2151"></span><dl> <dt><strong>MIDL2151</strong></dt> </dl></td>
<td><dl> <dt><span id="single-line_comment_needs__ms_ext_or__c_ext"></span><span id="SINGLE-LINE_COMMENT_NEEDS__MS_EXT_OR__C_EXT"></span>單行批註需要/ms_ext 或/c_ext</dt> <dd> 使用兩個斜線字元的單行批註 (//) 代表 Microsoft 對 DCE RPC 的擴充功能。 如果您要使用 <a href="-osf.md"><strong>/osf</strong></a> 參數進行編譯，則無法使用單行批註。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2152"></span><span id="midl2152"></span><dl> <dt><strong>MIDL2152</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__format_is_incorrect"></span><span id="_VERSION__FORMAT_IS_INCORRECT"></span>[version] 格式不正確</dt> <dd> 介面標頭中的介面版本號碼必須以 <em>主要</em>格式來指定。<em>次要</em>，其中每個數位的範圍可以從0到65535。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2153"></span><span id="midl2153"></span><dl> <dt><strong>MIDL2153</strong></dt> </dl></td>
<td><dl> <dt><span id="_signed__needs__ms_ext_or__c_ext"></span><span id="_SIGNED__NEEDS__MS_EXT_OR__C_EXT"></span>&quot;簽署 &quot; 的需求/ms_ext 或/c_ext</dt> <dd> 使用 <a href="signed.md"><strong>帶正負</strong></a> 號的關鍵字是 Microsoft 擴充功能，可用於 DCE RPC。 如果您想要使用此功能，則無法使用 <a href="-osf.md"><strong>/osf</strong></a> 參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2154"></span><span id="midl2154"></span><dl> <dt><strong>MIDL2154</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_assignment_type"></span><span id="MISMATCH_IN_ASSIGNMENT_TYPE"></span>指派類型不符</dt> <dd> 變數的類型不符合指派給變數的數值型別。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2155"></span><span id="midl2155"></span><dl> <dt><strong>MIDL2155</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_be_of_the_form__const__type__declarator_____initializing_expression_"></span><span id="DECLARATION_MUST_BE_OF_THE_FORM__CONST__TYPE__DECLARATOR_____INITIALIZING_EXPRESSION_"></span>宣告的格式必須為： const <type><declarator> = <initializing expression></dt> <dd> 宣告與 DCE RPC 語法不相容。 使用 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 或 <a href="-c-ext.md"><strong>/c_ext</strong></a> MIDL 編譯器模式參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2156"></span><span id="midl2156"></span><dl> <dt><strong>MIDL2156</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_have__const_"></span><span id="DECLARATION_MUST_HAVE__CONST_"></span>宣告必須有 &quot; const&quot;</dt> <dd> IDL 檔案中的宣告必須是使用關鍵字 <a href="const.md"><strong>const</strong></a>的常數運算式，例如：<br/>
<pre class="syntax" data-space="preserve"><code>const short x = 2;</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2157"></span><span id="midl2157"></span><dl> <dt><strong>MIDL2157</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_enum_must_not_be_defined_in_a_parameter-type_specification"></span><span id="STRUCT_UNION_ENUM_MUST_NOT_BE_DEFINED_IN_A_PARAMETER-TYPE_SPECIFICATION"></span>結構/等位/列舉不得在參數類型規格中定義</dt> <dd> 結構、等位或列舉型別必須在函式原型之外明確陳述。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2158"></span><span id="midl2158"></span><dl> <dt><strong>MIDL2158</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__attribute_must_be_applied_only_on_non-void_pointer_types"></span><span id="_ALLOCATE__ATTRIBUTE_MUST_BE_APPLIED_ONLY_ON_NON-VOID_POINTER_TYPES"></span>[配置] 屬性必須只套用在非 void 指標類型上</dt> <dd> [<a href="allocate.md"><strong>配置</strong></a>] 屬性是針對複雜的以指標為基礎的資料結構所設計。 當指定 [配置] 屬性時，存根檔會遍歷資料結構，以計算所有可從指標存取的所有物件的總大小，以及資料結構中的所有其他指標。 將類型變更為 void 指標類型或移除 [<strong>配置</strong>] 屬性，並使用另一個方法來判斷其配置大小，例如 <strong>sizeof</strong> 運算子。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2159"></span><span id="midl2159"></span><dl> <dt><strong>MIDL2159</strong></dt> </dl></td>
<td><dl> <dt><span id="array_or_equivalent_pointer_construct_cannot_derive_from_a_nonencapsulated_union"></span><span id="ARRAY_OR_EQUIVALENT_POINTER_CONSTRUCT_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>陣列或對等指標結構無法衍生自 nonencapsulated 聯集</dt> <dd> 每個聯集都必須與判別相關聯。 不允許等位陣列，因為它們不提供相關聯的判別。 結構的陣列，其中結構會封裝等位及其判別，因為存根可以使用判別來判斷每個聯集的大小。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2160"></span><span id="midl2160"></span><dl> <dt><strong>MIDL2160</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_an_error_status_t_type"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_AN_ERROR_STATUS_T_TYPE"></span>欄位不能衍生自 error_status_t 類型</dt> <dd> <a href="error-status-t.md"><strong>Error_status_t</strong></a>類型只能用來做為參數或傳回型別。 它不能內嵌在結構或等位的欄位中。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2161"></span><span id="midl2161"></span><dl> <dt><strong>MIDL2161</strong></dt> </dl></td>
<td><dl> <dt><span id="union_has_at_least_one_arm_without_a_case_label"></span><span id="UNION_HAS_AT_LEAST_ONE_ARM_WITHOUT_A_CASE_LABEL"></span>聯集至少有一個 arm，沒有 case 標籤</dt> <dd> Union 宣告不符合 union 的必要 MIDL 語法。 每個聯集 arm 都需要一個案例標籤或預設標籤，以選取該聯集 arm。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2162"></span><span id="midl2162"></span><dl> <dt><strong>MIDL2162</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_or_return_value_must_not_derive_from_a_type_that_has__ignore__applied_to_it"></span><span id="PARAMETER_OR_RETURN_VALUE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS__IGNORE__APPLIED_TO_IT"></span>參數或傳回值不能衍生自已套用 [ignore] 的類型</dt> <dd> [<a href="ignore.md"><strong>忽略</strong></a>] 屬性是只能套用至欄位（例如結構和陣列的欄位）的欄位屬性。 [<strong>Ignore</strong>] 屬性工作表示存根不應該在傳輸期間對指標進行取值，而且當它與必須取值的其他屬性（例如 [<a href="out-idl.md"><strong>out</strong></a>] 參數和函式傳回值）衝突時，就不能使用。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2163"></span><span id="midl2163"></span><dl> <dt><strong>MIDL2163</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_already_has_a_pointer_attribute_applied_to_it"></span><span id="POINTER_ALREADY_HAS_A_POINTER_ATTRIBUTE_APPLIED_TO_IT"></span>指標已經套用了指標屬性</dt> <dd> 只有其中一個指標屬性（[<a href="ref.md"><strong>ref</strong></a>]、[<a href="unique.md"><strong>unique</strong></a>] 或 [<a href="ptr.md"><strong>ptr</strong></a>]）可以套用至單一指標。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2164"></span><span id="midl2164"></span><dl> <dt><strong>MIDL2164</strong></dt> </dl></td>
<td><dl> <dt><span id="field_parameter_must_not_derive_from_a_structure_that_is_recursive_through_a_ref_pointer"></span><span id="FIELD_PARAMETER_MUST_NOT_DERIVE_FROM_A_STRUCTURE_THAT_IS_RECURSIVE_THROUGH_A_REF_POINTER"></span>field/parameter 不能衍生自透過 ref 指標遞迴的結構</dt> <dd> 根據定義，參考指標不能設定為 <strong>Null</strong>。 使用參考指標定義的遞迴資料結構沒有 <strong>Null</strong> 元素，而且依慣例為非終止。 您可以使用 [<a href="unique.md"><strong>unique</strong></a>] 指標屬性，讓資料結構指定 <strong>Null</strong> 元素，或將資料結構重新定義為非遞迴資料結構。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2165"></span><span id="midl2165"></span><dl> <dt><strong>MIDL2165</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_field_deriving_from_a_void_pointer_needs__c_ext"></span><span id="USE_OF_FIELD_DERIVING_FROM_A_VOID_POINTER_NEEDS__C_EXT"></span>使用衍生自 void 指標的欄位需要/c_ext</dt> <dd> 只有當您使用 MIDL 預設編譯器設定時，才允許在 IDL 檔案中使用類型 <strong>void *</strong> 和其他類型和類型限定詞。 使用 <a href="-osf.md"><strong>/osf</strong></a> 參數會覆寫此預設值。 如果您必須在憑證相容性模式中進行編譯，您將需要重新定義指標類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2166"></span><span id="midl2166"></span><dl> <dt><strong>MIDL2166</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_this_attribute_needs__ms_ext"></span><span id="USE_OF_THIS_ATTRIBUTE_NEEDS__MS_EXT"></span>使用此屬性需要/ms_ext</dt> <dd> 這項語言功能是 DCE IDL 的 Microsoft 延伸模組。 如果您要在憑證相容性模式下編譯 ( <a href="-osf.md"><strong>/osf</strong></a> ) ，就無法使用這項功能。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2167"></span><span id="midl2167"></span><dl> <dt><strong>MIDL2167</strong></dt> </dl></td>
<td><dl> <dt><span id="this_attribute_only_allowed_with_new_format_type_libraries"></span><span id="THIS_ATTRIBUTE_ONLY_ALLOWED_WITH_NEW_FORMAT_TYPE_LIBRARIES"></span>這個屬性只能搭配新的格式類型程式庫使用</dt> <dd> 若要使用此屬性，您需要 Windows 2000 或更新版本所提供的 Oleaut32.dll 版本。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2168"></span><span id="midl2168"></span><dl> <dt><strong>MIDL2168</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wchar_t_needs__ms_ext_or__c_ext"></span><span id="USE_OF_WCHAR_T_NEEDS__MS_EXT_OR__C_EXT"></span>使用 wchar_t 需求/ms_ext 或/c_ext</dt> <dd> 寬字元類型代表 DCE IDL 的延伸模組。 當您指定 <a href="-osf.md"><strong>/osf</strong></a> 參數時，MIDL 編譯器不接受寬字元類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2169"></span><span id="midl2169"></span><dl> <dt><strong>MIDL2169</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_need__ms_ext_or__c_ext"></span><span id="UNNAMED_FIELDS_NEED__MS_EXT_OR__C_EXT"></span>未命名的欄位需要/ms_ext 或/c_ext</dt> <dd> DCE IDL 不支援使用未命名的結構或內嵌在其他結構或等位中的等位。 在「DCE IDL」中，所有這類內嵌欄位都必須命名為。 當您指定 <a href="-osf.md"><strong>/osf</strong></a> 參數時，MIDL 編譯器不允許它們使用。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2170"></span><span id="midl2170"></span><dl> <dt><strong>MIDL2170</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_can_derive_only_from_struct_union_types"></span><span id="UNNAMED_FIELDS_CAN_DERIVE_ONLY_FROM_STRUCT_UNION_TYPES"></span>未命名的欄位只能衍生自結構/等位類型</dt> <dd> 支援未命名欄位之 DCE IDL 的 Microsoft 延伸模組只適用于結構和等位。 您必須將名稱指派給欄位，或將欄位重新定義為符合這種限制。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2171"></span><span id="midl2171"></span><dl> <dt><strong>MIDL2171</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_union_cannot_derive_from_a_conformant_varying_array_or_its_pointer_equivalent"></span><span id="FIELD_OF_A_UNION_CANNOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY_OR_ITS_POINTER_EQUIVALENT"></span>等位的欄位無法衍生自符合/變化的陣列或其對等指標</dt> <dd> 符合標準的陣列不能單獨出現在聯集內，但必須伴隨指定陣列大小的值。 請使用由符合標準的陣列和指定其大小的識別碼所組成的結構，而不是使用陣列做為聯集 arm。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2172"></span><span id="midl2172"></span><dl> <dt><strong>MIDL2172</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__ptr__for_all_unattributed_pointers_in_interface"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__PTR__FOR_ALL_UNATTRIBUTED_POINTERS_IN_INTERFACE"></span>未指定 [pointer_default] 屬性，假設 [ptr] 針對介面中的所有未歸屬指標</dt> <dd> 「DCE IDL」實指定每個 IDL 檔案中的所有指標都必須與指標屬性相關聯。 如果未將明確指標屬性指派給參數或指標類型，而且在 IDL 檔案中未指定任何 [<a href="pointer-default.md"><strong>pointer_default</strong></a>] 屬性 <a href="ptr.md"><strong>，則完整的指標屬性指標</strong></a> 會與指標相關聯。 您可以藉由指定 [<strong>pointer_default</strong>] 屬性，或指定 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 參數將未歸屬指標的預設值變更為 [<a href="unique.md"><strong>unique</strong></a>]，來變更指標屬性。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2173"></span><span id="midl2173"></span><dl> <dt><strong>MIDL2173</strong></dt> </dl></td>
<td><dl> <dt><span id="initializing_expression_must_resolve_to_a_constant_expression"></span><span id="INITIALIZING_EXPRESSION_MUST_RESOLVE_TO_A_CONSTANT_EXPRESSION"></span>初始化運算式必須解析為常數運算式</dt> <dd> 如果使用運算式做為初始化運算式，則運算式必須是常數運算式。 這在所有 MIDL 編譯器模式中都是如此。 運算式必須可在編譯時間進行解析。 指定常值常數或解析成常數的運算式，而不是變數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2174"></span><span id="midl2174"></span><dl> <dt><strong>MIDL2174</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_type_integer__char__Boolean_or_enum"></span><span id="attribute_expression_must_be_of_type_integer__char__boolean_or_enum"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_TYPE_INTEGER__CHAR__BOOLEAN_OR_ENUM"></span>屬性運算式的類型必須是 integer、char、Boolean 或 enum</dt> <dd> 指定的型別無法解析為有效的 switch 型別。 使用整數、字元、 <a href="byte.md"><strong>位元組</strong></a>、 <a href="boolean.md"><strong>布林值</strong></a>或 <a href="enum.md"><strong>列舉</strong></a> 類型，或是衍生自其中一個類型的類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2175"></span><span id="midl2175"></span><dl> <dt><strong>MIDL2175</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_constant"></span><span id="ILLEGAL_CONSTANT"></span>不合法的常數</dt> <dd> 指定的常數超出指定之類型的有效範圍。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2176"></span><span id="midl2176"></span><dl> <dt><strong>MIDL2176</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_not_implemented__ignored"></span><span id="ATTRIBUTE_NOT_IMPLEMENTED__IGNORED"></span>未執行屬性;忽視</dt> <dd> 這一版的 Microsoft RPC 不會執行指定的屬性。 MIDL 編譯器會繼續處理 IDL 檔案，就像屬性不存在一樣。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2177"></span><span id="midl2177"></span><dl> <dt><strong>MIDL2177</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a__ref__pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A__REF__POINTER"></span>傳回類型不能衍生自 [ref] 指標</dt> <dd> 定義為指標類型的函數傳回值必須指定為 [<a href="unique.md"><strong>unique</strong></a>] 或 <a href="ptr.md"><strong>完整</strong></a> 指標。 您無法使用參考指標。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2178"></span><span id="midl2178"></span><dl> <dt><strong>MIDL2178</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._You_must_specify_the__ms_ext_switch"></span><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._you_must_specify_the__ms_ext_switch"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_A_VARIABLE_NAME_OR_A_POINTER_DEREFERENCE_EXPRESSION_IN_THIS_MODE._YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>在此模式中，屬性運算式必須是變數名稱或指標取值運算式。您必須指定/ms_ext 參數</dt> <dd> DCE IDL 編譯器需要變數或指標變數指定與 [<a href="size-is.md"><strong>size_is</strong></a>] 屬性相關聯的大小。 如果您想要利用 Microsoft 擴充功能來允許常數運算式定義 [<strong>size_is</strong>] 屬性，則無法使用 <a href="-osf.md"><strong>/osf</strong></a> 編譯器參數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2179"></span><span id="midl2179"></span><dl> <dt><strong>MIDL2179</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_recursive_nonencapsulated_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_RECURSIVE_NONENCAPSULATED_UNION"></span>參數不能衍生自遞迴 nonencapsulated 聯集</dt> <dd> 聯集必須包含判別，因此等位不能有另一個聯集做為專案。 當聯集是包含判別之結構的一部分時，就可以內嵌在另一個聯集內。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2180"></span><span id="midl2180"></span><dl> <dt><strong>MIDL2180</strong></dt> </dl></td>
<td><dl> <dt><span id="binding-handle_parameter_cannot_be__out__only"></span><span id="BINDING-HANDLE_PARAMETER_CANNOT_BE__OUT__ONLY"></span>系結-控制碼參數不可以是 [out]</dt> <dd> MIDL 編譯器所識別的控制碼參數，與此作業的系結控制碼必須是 [<a href="in.md"><strong>in</strong></a>] 參數。 [<a href="out-idl.md"><strong>out</strong></a>]-用戶端 stub 上的唯一參數未定義，且必須在用戶端上定義系結控制碼。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2181"></span><span id="midl2181"></span><dl> <dt><strong>MIDL2181</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_handle_cannot_be__unique__or__ptr_"></span><span id="POINTER_TO_A_HANDLE_CANNOT_BE__UNIQUE__OR__PTR_"></span>控制碼的指標不能是 [unique] 或 [ptr]</dt> <dd> 您無法針對控制碼的指標使用 unique 和 full 指標屬性。 這些屬性允許 <strong>null</strong>值，且系結控制碼不可以是 <strong>null</strong>。 您可以使用 [<a href="ref.md"><strong>ref</strong></a>] 屬性來衍生參考指標的系結控制碼參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2182"></span><span id="midl2182"></span><dl> <dt><strong>MIDL2182</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_that_is_not_a_binding_handle_must_not_derive_from_handle_t"></span><span id="PARAMETER_THAT_IS_NOT_A_BINDING_HANDLE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>不是系結控制碼的參數不能衍生自 handle_t</dt> <dd> 基本控制碼類型 <a href="handle-t.md"><strong>handle_t</strong></a> 不是透過網路傳輸的有效資料類型。 將參數類型變更為 <strong>handle_t</strong>以外的類型，或移除參數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2183"></span><span id="midl2183"></span><dl> <dt><strong>MIDL2183</strong></dt> </dl></td>
<td><dl> <dt><span id="unexpected_end_of_file_found"></span><span id="UNEXPECTED_END_OF_FILE_FOUND"></span>找到非預期的檔案結尾</dt> <dd> MIDL 編譯器找到檔案結尾之後，才能夠順利解析檔案的所有語法元素。 確認檔案結尾有終止的右大括弧字元 (} ) ，或檢查語法。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2184"></span><span id="midl2184"></span><dl> <dt><strong>MIDL2184</strong></dt> </dl></td>
<td><dl> <dt><span id="type_deriving_from_handle_t_must_not_have__transmit_as__applied_to_it"></span><span id="TYPE_DERIVING_FROM_HANDLE_T_MUST_NOT_HAVE__TRANSMIT_AS__APPLIED_TO_IT"></span>衍生自 handle_t 的類型不得套用 [transmit_as]</dt> <dd> 基本控制碼類型 <a href="handle-t.md"><strong>handle_t</strong></a> 不會透過網路傳輸。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2185"></span><span id="midl2185"></span><dl> <dt><strong>MIDL2185</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_be_applied_to_a_type_that_has__handle__applied_to_it"></span><span id="_CONTEXT_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__HANDLE__APPLIED_TO_IT"></span>[coNtext_handle] 不得套用至已套用 [handle] 的類型</dt> <dd> [<a href="context-handle.md"><strong>CoNtext_handle</strong></a>] 和 [<a href="handle.md"><strong>handle</strong></a>] 屬性無法套用至相同的類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2186"></span><span id="midl2186"></span><dl> <dt><strong>MIDL2186</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_void_or_void__"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_VOID_OR_VOID__"></span>無法在衍生自 void 或 void 的型別上指定 [handle] *</dt> <dd> 使用 [<a href="handle.md"><strong>handle</strong></a>] 屬性指定的型別可透過網路傳輸，但是類型 <strong>void *</strong> 不是 transmissible 類型。 控制碼類型必須解析為衍生自 transmissible 基底類型的類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2187"></span><span id="midl2187"></span><dl> <dt><strong>MIDL2187</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._You_must_specify__ms_ext_or__c_ext"></span><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._you_must_specify__ms_ext_or__c_ext"></span><span id="PARAMETER_MUST_HAVE_EITHER__IN____OUT__OR__IN_OUT__IN_THIS_MODE._YOU_MUST_SPECIFY__MS_EXT_OR__C_EXT"></span>參數在此模式中必須有 [in]、[out] 或 [in，out]。您必須指定/ms_ext 或/c_ext</dt> <dd> DCE IDL 編譯器要求所有參數都必須有明確的方向參數。 若要將 Microsoft 擴充功能用於 DCE IDL，您無法使用 <a href="-osf.md"><strong>/osf</strong></a> 參數，它會覆寫 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 和 <a href="-c-ext.md"><strong>/c_ext</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2188"></span><span id="midl2188"></span><dl> <dt><strong>MIDL2188</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_derive_from__void__for__transmit_as____represent_as____wire_marshal____user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_DERIVE_FROM__VOID__FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL____USER_MARSHAL_"></span>在 &quot; &quot; [transmit_as]、[represent_as]、[wire_marshal]、[user_marshal] 中，傳輸的類型可能無法衍生自 void</dt> <dd> [<a href="transmit-as.md"><strong>Transmit_as</strong></a>] 屬性僅適用于指標類型。 使用 <strong>void *</strong> 類型來取代 <a href="void.md"><strong>void</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2189"></span><span id="midl2189"></span><dl> <dt><strong>MIDL2189</strong></dt> </dl></td>
<td><dl> <dt><span id="_void__must_be_specified_on_the_first_and_only_parameter_specification"></span><span id="_VOID__MUST_BE_SPECIFIED_ON_THE_FIRST_AND_ONLY_PARAMETER_SPECIFICATION"></span>&quot;&quot;必須在第一個和唯一的參數規格上指定 void</dt> <dd> 關鍵字 <a href="void.md"><strong>void</strong></a> 與其他函式參數一起出現錯誤。 若要指定沒有參數的函式，關鍵字 <strong>void</strong> 必須是參數清單的唯一元素，如下列範例所示：<br/>
<pre class="syntax" data-space="preserve"><code>void Moo(void)</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2190"></span><span id="midl2190"></span><dl> <dt><strong>MIDL2190</strong></dt> </dl></td>
<td><dl> <dt><span id="_switch_is__must_be_specified_only_on_a_type_deriving_from_a_nonencapsulated_union"></span><span id="_SWITCH_IS__MUST_BE_SPECIFIED_ONLY_ON_A_TYPE_DERIVING_FROM_A_NONENCAPSULATED_UNION"></span>必須只在衍生自 nonencapsulated 聯集的型別上指定 [switch_is]</dt> <dd> 未正確套用 [<a href="switch-is.md"><strong>switch_is</strong></a>] 關鍵字。 只能搭配 <a href="nonencapsulated-unions.md">nonencapsulated 聯集類型</a>使用。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2191"></span><span id="midl2191"></span><dl> <dt><strong>MIDL2191</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structures_are_not_implemented_in_this_version"></span><span id="STRINGABLE_STRUCTURES_ARE_NOT_IMPLEMENTED_IN_THIS_VERSION"></span>stringable 結構不會在此版本中執行</dt> <dd> 「DCE IDL」可讓屬性 [<a href="string.md"><strong>string</strong></a>] 套用至結構，而此結構的元素只包含字元、位元組或解析成字元或位元組的類型。 這項功能在 Microsoft RPC 中不受支援。 [<strong>String</strong>] 屬性無法套用至整個結構。 不過，它可以套用至每個個別陣列。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2192"></span><span id="midl2192"></span><dl> <dt><strong>MIDL2192</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_type_can_only_be_integral__char__Boolean_or_enum"></span><span id="switch_type_can_only_be_integral__char__boolean_or_enum"></span><span id="SWITCH_TYPE_CAN_ONLY_BE_INTEGRAL__CHAR__BOOLEAN_OR_ENUM"></span>參數類型只能是整數、字元、布林值或列舉</dt> <dd> 指定的型別無法解析為有效的 switch 型別。 使用整數、字元、 <a href="byte.md"><strong>位元組</strong></a>、 <a href="boolean.md"><strong>布林值</strong></a>、 <a href="enum.md"><strong>列舉</strong></a> 類型或衍生自其中一個類型的類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2193"></span><span id="midl2193"></span><dl> <dt><strong>MIDL2193</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_handle_t"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_HANDLE_T"></span>必須在衍生自 handle_t 的型別上指定 [handle]</dt> <dd> 控制碼類型必須使用一個或多個控制碼類型或屬性來定義。 使用基本類型 <a href="handle-t.md"><strong>handle_t</strong></a> 或屬性 [<a href="handle.md"><strong>控制碼</strong></a>]，但不能同時使用兩者。 使用者定義控制碼類型必須是 transmissible，但不會在網路上傳輸 <strong>handle_t</strong> 類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2194"></span><span id="midl2194"></span><dl> <dt><strong>MIDL2194</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_handle_t_must_not_be_an__out__parameter"></span><span id="PARAMETER_DERIVING_FROM_HANDLE_T_MUST_NOT_BE_AN__OUT__PARAMETER"></span>衍生自 handle_t 的參數不得為 [out] 參數</dt> <dd> 基本型別 <a href="handle-t.md"><strong>handle_t</strong></a> 的控制碼只對定義它的應用程式端有意義。 類型 <strong>handle_t</strong> 不會在網路上傳輸。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2195"></span><span id="midl2195"></span><dl> <dt><strong>MIDL2195</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_derives_from__unique__or__ptr__pointer_dereference"></span><span id="ATTRIBUTE_EXPRESSION_DERIVES_FROM__UNIQUE__OR__PTR__POINTER_DEREFERENCE"></span>屬性運算式衍生自 [unique] 或 [ptr] 指標取值</dt> <dd> 雖然 [<a href="unique.md"><strong>unique</strong></a>] 和 <a href="ptr.md"><strong>full</strong></a> 指標屬性允許指標有 <strong>null</strong> 值，但定義 size 或 length 屬性的運算式絕對不能有 <strong>null</strong> 值。 使用指標時，MIDL 會將運算式限制為 [<a href="ref.md"><strong>ref</strong></a>] 指標。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2196"></span><span id="midl2196"></span><dl> <dt><strong>MIDL2196</strong></dt> </dl></td>
<td><dl> <dt><span id="_cpp_quote__requires__ms_ext"></span><span id="_CPP_QUOTE__REQUIRES__MS_EXT"></span>&quot;cpp_quote &quot; 需要/ms_ext</dt> <dd> <a href="cpp-quote.md"><strong>Cpp_quote</strong></a>屬性是 DCE IDL 的 Microsoft 延伸模組。 請勿使用會覆寫<a href="-ms-ext.md"><strong>/ms_ext</strong></a>的 MIDL 編譯器參數<a href="-osf.md"><strong>/osf</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2197"></span><span id="midl2197"></span><dl> <dt><strong>MIDL2197</strong></dt> </dl></td>
<td><dl> <dt><span id="quoted_uuid_requires__ms_ext"></span><span id="QUOTED_UUID_REQUIRES__MS_EXT"></span>引號 uuid 需要/ms_ext</dt> <dd> 在引號內指定 UUID 值的能力，是 Microsoft 對 DCE IDL 的擴充功能。 請勿使用會覆寫<a href="-ms-ext.md"><strong>/ms_ext</strong></a>的 MIDL 編譯器參數<a href="-osf.md"><strong>/osf</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2198"></span><span id="midl2198"></span><dl> <dt><strong>MIDL2198</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_nonencapsulated_union"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>傳回類型不能衍生自 nonencapsulated 聯集</dt> <dd> Nonencapsulated 聯集不能當做函數傳回型別使用。 若要傳回聯集類型，請將聯集類型指定為 [<a href="out-idl.md"><strong>out</strong></a>] 或 [<strong>in，out</strong>] 參數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2199"></span><span id="midl2199"></span><dl> <dt><strong>MIDL2199</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_conformant_structure"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_CONFORMANT_STRUCTURE"></span>傳回類型不能衍生自符合標準的結構</dt> <dd> 傳回類型的大小必須是常數。 您無法將包含符合標準陣列的結構指定為傳回型別，即使結構也包含其大小規範也一樣。 若要傳回符合的結構，請將結構指定為 [<a href="out-idl.md"><strong>out</strong></a>] 或 [<strong>in，out</strong>] 參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2200"></span><span id="midl2200"></span><dl> <dt><strong>MIDL2200</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_deriving_from_a_generic_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_GENERIC_HANDLE"></span>[transmit_as] 不得套用至衍生自泛型控制碼的型別</dt> <dd> 在此版本中，[<a href="handle.md"><strong>控制碼</strong></a>] 和 [<a href="transmit-as.md"><strong>transmit_as</strong></a>] 屬性無法在相同的類型上結合。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2201"></span><span id="midl2201"></span><dl> <dt><strong>MIDL2201</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_that_has__transmit_as__applied_to_it"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__TRANSMIT_AS__APPLIED_TO_IT"></span>[控制碼] 不得套用至已套用 [transmit_as] 的類型</dt> <dd> 在此版本中，[<a href="handle.md"><strong>控制碼</strong></a>] 和 [<a href="transmit-as.md"><strong>transmit_as</strong></a>] 屬性無法在相同的類型上結合。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2202"></span><span id="midl2202"></span><dl> <dt><strong>MIDL2202</strong></dt> </dl></td>
<td><dl> <dt><span id="type_specified_for_the_const_declaration_is_invalid"></span><span id="TYPE_SPECIFIED_FOR_THE_CONST_DECLARATION_IS_INVALID"></span>為 const 宣告指定的類型無效</dt> <dd> 常數宣告的限制為整數、字元、寬字元、字串和布林值類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2203"></span><span id="midl2203"></span><dl> <dt><strong>MIDL2203</strong></dt> </dl></td>
<td><dl> <dt><span id="operand_to_the_sizeof_operator_is_not_supported"></span><span id="OPERAND_TO_THE_SIZEOF_OPERATOR_IS_NOT_SUPPORTED"></span>不支援對 sizeof 運算子的運算元</dt> <dd> MIDL 編譯器只支援簡單類型的 <strong>sizeof</strong> 運算。 指定的運算元未評估為整數類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2204"></span><span id="midl2204"></span><dl> <dt><strong>MIDL2204</strong></dt> </dl></td>
<td><dl> <dt><span id="this_name_already_used_as_a_const_identifier_name"></span><span id="THIS_NAME_ALREADY_USED_AS_A_CONST_IDENTIFIER_NAME"></span>此名稱已用來作為 const 識別碼名稱</dt> <dd> 先前已使用識別碼來識別 <a href="const.md"><strong>const</strong></a> 宣告中的常數。 變更其中一個識別碼的名稱，讓識別碼是唯一的。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2205"></span><span id="midl2205"></span><dl> <dt><strong>MIDL2205</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_error_status_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_ERROR_STATUS_T"></span>類型 error_status_t 的重新定義不一致</dt> <dd> 類型 <a href="error-status-t.md"><strong>error_status_t</strong></a> 必須解析為類型不 <strong>帶正負</strong>號的 long。 無法使用其他型別定義。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2206"></span><span id="midl2206"></span><dl> <dt><strong>MIDL2206</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__value_out_of_range_of_switch_type"></span><span id="_CASE__VALUE_OUT_OF_RANGE_OF_SWITCH_TYPE"></span>[case] 值超出切換類型範圍</dt> <dd> 與 switch 語句案例相關聯的值超出指定參數類型的範圍。 例如，在 case 語句中使用長整數值以進行短整數類型時，就會發生這個錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2207"></span><span id="midl2207"></span><dl> <dt><strong>MIDL2207</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_wchar_t_needs__ms_ext"></span><span id="PARAMETER_DERIVING_FROM_WCHAR_T_NEEDS__MS_EXT"></span>衍生自 wchar_t 需要/ms_ext 的參數</dt> <dd> 寬字元類型 <a href="wchar-t.md"><strong>wchar_t</strong></a> 是 DCE IDL 的 Microsoft 延伸模組。 請勿使用 MIDL 編譯器參數 <a href="-osf.md"><strong>/osf</strong></a>，它會覆寫 <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2208"></span><span id="midl2208"></span><dl> <dt><strong>MIDL2208</strong></dt> </dl></td>
<td><dl> <dt><span id="this_interface_has_only_callbacks"></span><span id="THIS_INTERFACE_HAS_ONLY_CALLBACKS"></span>此介面只有回呼</dt> <dd> 回呼只會在遠端程序呼叫的內容中有效。 介面必須針對不包含 [<a href="callback.md"><strong>回呼</strong></a>] 屬性的遠端程序呼叫，至少包含一個函數原型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2209"></span><span id="midl2209"></span><dl> <dt><strong>MIDL2209</strong></dt> </dl></td>
<td><dl> <dt><span id="redundantly_specified_attribute__ignored"></span><span id="REDUNDANTLY_SPECIFIED_ATTRIBUTE__IGNORED"></span>重複指定的屬性;忽視</dt> <dd> 指定的屬性已套用一次以上。 系統會忽略相同屬性的多個實例。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2210"></span><span id="midl2210"></span><dl> <dt><strong>MIDL2210</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_type_used_for_an_implicit_handle"></span><span id="CONTEXT_HANDLE_TYPE_USED_FOR_AN_IMPLICIT_HANDLE"></span>用於隱含控制碼的內容控制碼類型</dt> <dd> 使用 [<a href="context-handle.md"><strong>coNtext_handle</strong></a>] 屬性定義的類型已指定為 [ <a href="implicit-handle.md"><strong>implicit_handle</strong></a>] 屬性中的控制碼類型。 這些屬性無法以這種方式結合。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2211"></span><span id="midl2211"></span><dl> <dt><strong>MIDL2211</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_options_specified_for__allocate_"></span><span id="CONFLICTING_OPTIONS_SPECIFIED_FOR__ALLOCATE_"></span>針對 [配置] 指定的衝突選項</dt> <dd> 為 ACF 屬性 [<a href="allocate.md"><strong>配置</strong></a>] 指定的選項代表衝突的指示詞。 例如，您可以指定選項 all_nodes 或選項 single_node，但不能同時指定兩者。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2212"></span><span id="midl2212"></span><dl> <dt><strong>MIDL2212</strong></dt> </dl></td>
<td><dl> <dt><span id="error_while_writing_to_file"></span><span id="ERROR_WHILE_WRITING_TO_FILE"></span>寫入檔案時發生錯誤</dt> <dd> 寫入檔案時發生錯誤。 這種狀況的原因可能是與磁碟空間、檔案控制代碼、檔案存取限制和硬體故障相關的錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2213"></span><span id="midl2213"></span><dl> <dt><strong>MIDL2213</strong></dt> </dl></td>
<td><dl> <dt><span id="no_switch_type_found_at_definition_of_union__using_the__switch_is__type"></span><span id="NO_SWITCH_TYPE_FOUND_AT_DEFINITION_OF_UNION__USING_THE__SWITCH_IS__TYPE"></span>在 union 的定義中找不到使用 [switch_is] 類型的 switch 類型</dt> <dd> Union 定義不包含明確的 [<a href="switch-type.md"><strong>switch_type</strong></a>] 屬性。 [<a href="switch-is.md"><strong>Switch_is</strong></a>] 屬性所指定之變數的型別會當做 switch 型別使用。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2214"></span><span id="midl2214"></span><dl> <dt><strong>MIDL2214</strong></dt> </dl></td>
<td><dl> <dt><span id="semantic_check_incomplete_due_to_previous_errors"></span><span id="SEMANTIC_CHECK_INCOMPLETE_DUE_TO_PREVIOUS_ERRORS"></span>語義檢查因為先前的錯誤而未完成</dt> <dd> MIDL 編譯器會對輸入檔進行兩個傳遞， (s) 來解析任何向前宣告。 因為第一次傳遞時發生錯誤，所以尚未執行檢查第二次。 與向前宣告相關的未報告錯誤可能仍會出現在檔案中。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2215"></span><span id="midl2215"></span><dl> <dt><strong>MIDL2215</strong></dt> </dl></td>
<td><dl> <dt><span id="handle_parameter_or_return_type_is_not_supported_on_a__callback__procedure"></span><span id="HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A__CALLBACK__PROCEDURE"></span>在 [回呼] 程式上不支援控制碼參數或傳回類型</dt> <dd> 在從用戶端到伺服器的呼叫內容中，會出現 [<a href="callback.md"><strong>回呼</strong></a>] 程式，並使用與原始呼叫相同的系結控制碼。 回呼函式中不允許明確的系結控制碼參數或傳回類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2216"></span><span id="midl2216"></span><dl> <dt><strong>MIDL2216</strong></dt> </dl></td>
<td><dl> <dt><span id="_ptr__does_not_support_aliasing_in_this_version"></span><span id="_PTR__DOES_NOT_SUPPORT_ALIASING_IN_THIS_VERSION"></span>[ptr] 不支援此版本中的別名</dt> <dd> 當資料可透過一個以上的指標或變數名稱存取時，就會發生別名。 移除別名。 如需詳細資訊，請參閱 <a href="/windows/desktop/Rpc/unique-pointers">唯一指標</a>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2217"></span><span id="midl2217"></span><dl> <dt><strong>MIDL2217</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_already_defined_as_a_context_handle"></span><span id="PARAMETER_ALREADY_DEFINED_AS_A_CONTEXT_HANDLE"></span>參數已定義為內容控制碼</dt> <dd> 參數之前已定義為內容控制碼。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2218"></span><span id="midl2218"></span><dl> <dt><strong>MIDL2218</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_derive_from_handle_t"></span><span id="_CONTEXT_HANDLE__MUST_NOT_DERIVE_FROM_HANDLE_T"></span>[coNtext_handle] 不能衍生自 handle_t</dt> <dd> 三個控制碼特性：型別 <a href="handle-t.md"><strong>handle_t</strong></a>、屬性 [<a href="handle.md"><strong>handle</strong></a>] 和屬性 [<a href="context-handle.md"><strong>coNtext_handle</strong></a>] 都是互斥的。 一次只能將一個特性套用至類型或參數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2219"></span><span id="midl2219"></span><dl> <dt><strong>MIDL2219</strong></dt> </dl></td>
<td><dl> <dt><span id="array_size_exceeds_65536_bytes"></span><span id="ARRAY_SIZE_EXCEEDS_65536_BYTES"></span>陣列大小超過65536個位元組</dt> <dd> 在某些 Microsoft 平臺上，transmissible 資料大小上限是64K。 重新設計您的應用程式，讓所有傳輸的資料都能容納在 transmissible 大小上限內。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2220"></span><span id="midl2220"></span><dl> <dt><strong>MIDL2220</strong></dt> </dl></td>
<td><dl> <dt><span id="structure_size_exceeds_65536_bytes"></span><span id="STRUCTURE_SIZE_EXCEEDS_65536_BYTES"></span>結構大小超過65536個位元組</dt> <dd> 在某些 Microsoft 平臺上，transmissible 資料大小上限是64K。 重新設計您的應用程式，讓所有傳輸的資料都能容納在 transmissible 大小上限內。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2221"></span><span id="midl2221"></span><dl> <dt><strong>MIDL2221</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_nonencapsulated_union_cannot_be_another_nonencapsulated_union"></span><span id="FIELD_OF_A_NONENCAPSULATED_UNION_CANNOT_BE_ANOTHER_NONENCAPSULATED_UNION"></span>nonencapsulated 聯集的欄位不可以是另一個 nonencapsulated 聯集</dt> <dd> 在遠端程序呼叫中傳輸的等位需要有相關聯的資料項目，也就是判別，可選取聯集 arm。 嵌套于其他等位中的等位不提供判別;如此一來，就無法以這種形式傳送。 建立包含聯集及其判別的結構。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2222"></span><span id="midl2222"></span><dl> <dt><strong>MIDL2222</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_attribute_s__applied_on_an_embedded_array__ignored"></span><span id="POINTER_ATTRIBUTE_S__APPLIED_ON_AN_EMBEDDED_ARRAY__IGNORED"></span>指標屬性 (s) 套用於內嵌陣列;忽視</dt> <dd> 只有當陣列是最上層參數時，才能將指標屬性套用至陣列。 其他套用至內嵌于其他資料結構之陣列的指標屬性都會被忽略。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2223"></span><span id="midl2223"></span><dl> <dt><strong>MIDL2223</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__is_illegal_on_either_the_transmitted_or_presented_type_for__transmit_as____represent_as____wire_marshal___or__user_marshal_"></span><span id="_ALLOCATE__IS_ILLEGAL_ON_EITHER_THE_TRANSMITTED_OR_PRESENTED_TYPE_FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL___OR__USER_MARSHAL_"></span>[配置] 對 [transmit_as]、[represent_as]、[wire_marshal] 或 [user_marshal] 的傳輸或呈現類型不合法</dt> <dd> [<a href="transmit-as.md"><strong>Transmit_as</strong></a>] 和 [<a href="allocate.md"><strong>配置</strong></a>] 屬性無法同時套用至相同的類型。 [<strong>Transmit_as</strong>] 屬性會區分所呈現和傳輸的類型，而 [<strong>配置</strong>] 屬性則會假設所顯示的型別與傳送的型別相同。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2224"></span><span id="midl2224"></span><dl> <dt><strong>MIDL2224</strong></dt> </dl></td>
<td>必須在此匯入模式中指定 [switch_type]<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2225"></span><span id="midl2225"></span><dl> <dt><strong>MIDL2225</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__type_undefined__assuming_generic_handle"></span><span id="_IMPLICIT_HANDLE__TYPE_UNDEFINED__ASSUMING_GENERIC_HANDLE"></span>[implicit_handle] 未定義的類型;假設泛型控制碼</dt> <dd> 在 ACF 中指定的控制碼類型未定義于 IDL 檔案中。 MIDL 編譯器會假設控制碼類型會解析為基本控制碼類型 <a href="handle-t.md"><strong>handle_t</strong></a>。 如果您希望控制碼的行為類似于使用者定義或泛型控制碼，請將 [<a href="handle.md"><strong>handle</strong></a>] 屬性加入至類型定義。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2226"></span><span id="midl2226"></span><dl> <dt><strong>MIDL2226</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_error_status_t"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>陣列元素不能衍生自 error_status_t</dt> <dd> 在這一版的 Microsoft RPC 中，類型 <a href="error-status-t.md"><strong>error_status_t</strong></a> 只能以參數或傳回類型的形式出現。 它不能出現在陣列中。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2227"></span><span id="midl2227"></span><dl> <dt><strong>MIDL2227</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__illegal_on_a_type_deriving_from_a_primitive_generic_context_handle"></span><span id="_ALLOCATE__ILLEGAL_ON_A_TYPE_DERIVING_FROM_A_PRIMITIVE_GENERIC_CONTEXT_HANDLE"></span>在衍生自基本/泛型/內容控制碼的類型上，[配置] 不合法</dt> <dd> 根據設計，ACF 屬性 [<a href="allocate.md"><strong>配置</strong></a>] 無法套用至控制碼類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2228"></span><span id="midl2228"></span><dl> <dt><strong>MIDL2228</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_or_presented_type_must_not_derive_from_error_status_t"></span><span id="TRANSMITTED_OR_PRESENTED_TYPE_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>傳送或顯示的類型不能衍生自 error_status_t</dt> <dd> 在這一版的 Microsoft RPC 中，類型 <a href="error-status-t.md"><strong>error_status_t</strong></a> 不能與 [<a href="transmit-as.md"><strong>transmit_as</strong></a>] 屬性搭配使用。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2229"></span><span id="midl2229"></span><dl> <dt><strong>MIDL2229</strong></dt> </dl></td>
<td><dl> <dt><span id="discriminant_of_a_union_must_not_derive_from_a_field_with__ignore__applied_to_it"></span><span id="DISCRIMINANT_OF_A_UNION_MUST_NOT_DERIVE_FROM_A_FIELD_WITH__IGNORE__APPLIED_TO_IT"></span>union 的判別不能衍生自已套用 [ignore] 的欄位</dt> <dd> 遠端程序呼叫中使用的聯集，必須與另一個資料項目（稱為判別）相關聯，以選取聯集 arm。 必須傳送判別。 [<a href="ignore.md"><strong>Ignore</strong></a>] 屬性無法套用至聯集判別。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2230"></span><span id="midl2230"></span><dl> <dt><strong>MIDL2230</strong></dt> </dl></td>
<td><dl> <dt><span id="_nocode__ignored_for_server_side_since___server_none__not_specified"></span><span id="_NOCODE__IGNORED_FOR_SERVER_SIDE_SINCE___SERVER_NONE__NOT_SPECIFIED"></span>已忽略伺服器端的 [了 nocode]，因為 &quot; &quot; 未指定/server none</dt> <dd> 當 [<a href="nocode.md"><strong>了 nocode</strong></a>] 屬性套用至正在產生伺服器 stub 檔案的介面中的程式時，某些 DCE IDL 編譯器會產生錯誤。 因為伺服器必須支援所有作業，所以 [<strong>了 nocode</strong>] 不得套用到此模式中的程式，或者您必須使用 MIDL 編譯器參數 <a href="-server.md"><strong>/server</strong></a> none 來明確指定不會產生任何伺服器常式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2231"></span><span id="midl2231"></span><dl> <dt><strong>MIDL2231</strong></dt> </dl></td>
<td><dl> <dt><span id="no_remote_procedures_specified_in_non-_local__interface__no_client_server_stubs_will_be_generated"></span><span id="NO_REMOTE_PROCEDURES_SPECIFIED_IN_NON-_LOCAL__INTERFACE__NO_CLIENT_SERVER_STUBS_WILL_BE_GENERATED"></span>未在非 [本機] 介面中指定任何遠端程式;不會產生任何用戶端/伺服器 stub</dt> <dd> 提供的介面沒有任何遠端程式，因此只會產生標頭檔。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2232"></span><span id="midl2232"></span><dl> <dt><strong>MIDL2232</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_cases_specified_for_encapsulated_union"></span><span id="TOO_MANY_DEFAULT_CASES_SPECIFIED_FOR_ENCAPSULATED_UNION"></span>為封裝聯集指定了太多預設案例</dt> <dd> 封裝聯集只能有一個預設值： arm。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2233"></span><span id="midl2233"></span><dl> <dt><strong>MIDL2233</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_interfaces_specified_for_coclass"></span><span id="TOO_MANY_DEFAULT_INTERFACES_SPECIFIED_FOR_COCLASS"></span>指定給 coclass 的預設介面太多</dt> <dd> <a href="coclass.md"><strong>Coclass</strong></a>最多可以有兩個 [<a href="default.md"><strong>default</strong></a>] 成員，一個用來表示傳出的 (來源) 介面或分配介面，另一個則代表傳入的 (接收) 介面或多介面。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2234"></span><span id="midl2234"></span><dl> <dt><strong>MIDL2234</strong></dt> </dl></td>
<td><dl> <dt><span id="items_with__defaultvtable__must_also_have__source_"></span><span id="ITEMS_WITH__DEFAULTVTABLE__MUST_ALSO_HAVE__SOURCE_"></span>具有 [defaultvtable] 的專案也必須有 [來源]</dt> <dd> <a href="defaultvtable.md"><strong>Defaultvtable</strong></a>介面會建立物件的第二個來源介面，讓接收器透過 V 資料表接收事件。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2235"></span><span id="midl2235"></span><dl> <dt><strong>MIDL2235</strong></dt> </dl></td>
<td><dl> <dt><span id="union_specification_with_no_fields_is_illegal"></span><span id="UNION_SPECIFICATION_WITH_NO_FIELDS_IS_ILLEGAL"></span>沒有欄位的聯集規格不合法</dt> <dd> 等位必須至少有一個欄位。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2236"></span><span id="midl2236"></span><dl> <dt><strong>MIDL2236</strong></dt> </dl></td>
<td><dl> <dt><span id="value_out_of_range"></span><span id="VALUE_OUT_OF_RANGE"></span>值超出範圍</dt> <dd> 提供的大小寫值超出 switch 型別的範圍。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2237"></span><span id="midl2237"></span><dl> <dt><strong>MIDL2237</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_be_applied_on_a_pointer_type"></span><span id="_CONTEXT_HANDLE__MUST_BE_APPLIED_ON_A_POINTER_TYPE"></span>[coNtext_handle] 必須套用於指標類型上</dt> <dd> 內容控制碼一律必須是指標類型。 DCE 指定所有內容控制碼都必須輸入為 <strong>void *</strong>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2238"></span><span id="midl2238"></span><dl> <dt><strong>MIDL2238</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_handle_t"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>傳回類型不能衍生自 handle_t</dt> <dd>無法傳回<a href="handle-t.md"><strong>handle_t</strong></a> 。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2239"></span><span id="midl2239"></span><dl> <dt><strong>MIDL2239</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_deriving_from_a_context_handle"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_CONTEXT_HANDLE"></span>[handle] 不得套用至衍生自內容控制碼的型別</dt> <dd> 類型不能同時為內容控制碼和一般控制碼。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2240"></span><span id="midl2240"></span><dl> <dt><strong>MIDL2240</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="FIELD_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>從 int 衍生的 &quot; 欄位 &quot; 必須有大小規範 &quot; &quot; ， &quot; 也就 &quot; 是 long、short 或 &quot; long &quot; 的 &quot; int&quot;</dt> <dd> 類型 <a href="int.md"><strong>int</strong></a> 不會在16位系統上 transmissible，因為 <strong>int</strong> 的大小在電腦之間可能不同。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2241"></span><span id="midl2241"></span><dl> <dt><strong>MIDL2241</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_void_or_void__"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_VOID_OR_VOID__"></span>欄位不能衍生自 void 或 void *</dt> <dd> <strong>void</strong> 和 <strong>void *</strong> 無法當做遠端程式的參數類型使用。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2242"></span><span id="midl2242"></span><dl> <dt><strong>MIDL2242</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_structure_containing_bit-fields"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_STRUCTURE_CONTAINING_BIT-FIELDS"></span>欄位不能衍生自包含位欄位的結構</dt> <dd> 包含位欄位的結構不能當做遠端程式的參數或傳回類型使用。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2243"></span><span id="midl2243"></span><dl> <dt><strong>MIDL2243</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_non-rpcable_union"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_NON-RPCABLE_UNION"></span>欄位不能衍生自非 rpcable 聯集</dt> <dd> Union 必須指定為 nonencapsulated 聯集或封裝聯集，才能進行傳輸。 一般 C 等位缺少跨網路傳輸聯集所需的判別。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2244"></span><span id="midl2244"></span><dl> <dt><strong>MIDL2244</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_pointer_to_a_function"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>欄位不能衍生自函式的指標</dt> <dd> 無法將函式的指標傳送至遠端程式。 函式的指標會指向函式程式碼，而不能使用 RPC 跨網路傳輸任何函式程式碼。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2245"></span><span id="midl2245"></span><dl> <dt><strong>MIDL2245</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__fault_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__FAULT_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>無法在參數和傳回類型上使用 [fault_status]</dt> <dd> 每個程式只能使用一次屬性 [<a href="fault-status.md"><strong>fault_status</strong></a>]。 [<a href="comm-status.md"><strong>Comm_status</strong></a>] 屬性可以單獨使用。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2246"></span><span id="midl2246"></span><dl> <dt><strong>MIDL2246</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_too_complicated_for__Oi_modes__using__Os"></span><span id="return_type_too_complicated_for__oi_modes__using__os"></span><span id="RETURN_TYPE_TOO_COMPLICATED_FOR__OI_MODES__USING__OS"></span>傳回型別對/Oi 模式而言太複雜，請使用/Os</dt> <dd> 以傳值方式傳遞的大型傳回類型只能由 <a href="-os.md"><strong>/os</strong></a> 優化存根處理。 此常式的存根將使用 <strong>/os</strong> 優化產生。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2247"></span><span id="midl2247"></span><dl> <dt><strong>MIDL2247</strong></dt> </dl></td>
<td><dl> <dt><span id="generic_handle_type_too_large_for__Oi_modes__using__Os"></span><span id="generic_handle_type_too_large_for__oi_modes__using__os"></span><span id="GENERIC_HANDLE_TYPE_TOO_LARGE_FOR__OI_MODES__USING__OS"></span>泛型控制碼類型對/Oi 模式而言太大，請使用/Os</dt> <dd> 以傳值方式傳遞的大型泛型控制碼類型只能由 <a href="-os.md"><strong>/os</strong></a> 優化存根處理。 此常式的存根將使用 <strong>/os</strong> 優化產生。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2248"></span><span id="midl2248"></span><dl> <dt><strong>MIDL2248</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate_all_nodes___on_an__in_out__parameter_may_orphan_the_original_memory"></span><span id="_ALLOCATE_ALL_NODES___ON_AN__IN_OUT__PARAMETER_MAY_ORPHAN_THE_ORIGINAL_MEMORY"></span>[在 [in，out] 參數上配置 (all_nodes) ] 可能會孤立原始記憶體</dt> <dd> 在 [<a href="in.md"><strong>in</strong></a>， <a href="out-idl.md"><strong>out</strong></a>] 參數上使用 [<a href="allocate.md"><strong>配置</strong></a> (all_nodes) ] 必須針對 [<strong>out</strong>] 方向重新配置連續的記憶體，因此損壞 [<strong>in</strong>] 參數。 不建議使用這種方式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2249"></span><span id="midl2249"></span><dl> <dt><strong>MIDL2249</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_have_a__ref__pointer_as_a_union_arm"></span><span id="CANNOT_HAVE_A__REF__POINTER_AS_A_UNION_ARM"></span>不能將 [ref] 指標作為聯集 arm</dt> <dd> 參考指標一律必須指向有效的記憶體，但當 [<strong>in</strong>] 方向使用另一種類型時，具有參考指標的 [<a href="in.md"><strong>in</strong></a>， <a href="out-idl.md"><strong>out</strong></a>] 聯集可能會傳回參考指標。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2250"></span><span id="midl2250"></span><dl> <dt><strong>MIDL2250</strong></dt> </dl></td>
<td><dl> <dt><span id="return_of_context_handles_not_supported_for__Oi_modes__using__Os"></span><span id="return_of_context_handles_not_supported_for__oi_modes__using__os"></span><span id="RETURN_OF_CONTEXT_HANDLES_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>使用/Os/Oi 模式不支援傳回內容控制碼</dt> <dd> MIDL 在完全解讀的優化模式下不支援內容控制碼。 切換至混合模式優化。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2251"></span><span id="midl2251"></span><dl> <dt><strong>MIDL2251</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__Oi_modes__using__Os"></span><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__oi_modes__using__os"></span><span id="USE_OF_THE_EXTRA__COMM_STATUS__OR__FAULT_STATUS__PARAMETER_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>使用/Os/Oi 模式不支援使用額外的 [comm_status] 或 [fault_status] 參數</dt> <dd> [<a href="comm-status.md"><strong>Comm_status</strong></a>] 和 [<a href="fault-status.md"><strong>fault_status</strong></a>] 屬性只能由 <a href="-os.md"><strong>/os</strong></a> 優化存根處理。 此常式的存根將使用 <strong>/os</strong> 優化產生。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2252"></span><span id="midl2252"></span><dl> <dt><strong>MIDL2252</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__Oi_modes__using__Os"></span><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__oi_modes__using__os"></span><span id="USE_OF_AN_UNKNOWN_TYPE_FOR__REPRESENT_AS__OR__USER_MARSHAL__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>使用/Os 的/Oi 模式不支援對 [represent_as] 或 [user_marshal] 使用未知的類型</dt> <dd> 使用具有未在 IDL 檔案中定義之區欄位型別的 [<a href="represent-as.md"><strong>represent_as</strong></a>] 屬性或匯入的 IDL 檔案，只能由 <a href="-os.md"><strong>/os</strong></a> 優化存根處理。 此常式的存根將使用 <strong>/os</strong> 優化產生。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2253"></span><span id="midl2253"></span><dl> <dt><strong>MIDL2253</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__Oi_modes___using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__oi_modes___using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_ON_RETURN_TYPE_FOR__OI_MODES___USING__OS"></span>/Oi 模式的傳回型別不支援具有 [transmit_as] 或 [represent_as] 的陣列類型，請使用/Os</dt> <dd> 傳回已套用 [<a href="transmit-as.md"><strong>transmit_as</strong></a>] 或 [<a href="represent-as.md"><strong>represent_as</strong></a>] 的陣列，只能由 <a href="-os.md"><strong>/os</strong></a> 優化存根處理。 此常式的存根將使用 <strong>/os</strong> 優化產生。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2254"></span><span id="midl2254"></span><dl> <dt><strong>MIDL2254</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__Oi_modes__using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__oi_modes__using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_PASS-BY-VALUE_FOR__OI_MODES__USING__OS"></span>具有 [transmit_as] 或 [represent_as] 的陣列類型不支援/Oi 模式的傳遞值（使用/Os）</dt> <dd> 完全解讀的優化不支援這個動作。 切換至混合模式優化。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2255"></span><span id="midl2255"></span><dl> <dt><strong>MIDL2255</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__requires__ms_ext"></span><span id="_CALLBACK__REQUIRES__MS_EXT"></span>[回呼] 需要/ms_ext</dt> <dd> [<a href="callback.md"><strong>回呼</strong></a>] 屬性是 Microsoft 擴充功能，需要啟用 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 參數。 請勿使用覆寫<strong>/ms_ext</strong>的<a href="-osf.md"><strong>/osf</strong></a>進行編譯。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2256"></span><span id="midl2256"></span><dl> <dt><strong>MIDL2256</strong></dt> </dl></td>
<td><dl> <dt><span id="circular_interface_dependency"></span><span id="CIRCULAR_INTERFACE_DEPENDENCY"></span>迴圈介面相依性</dt> <dd> 此介面使用本身 (直接或間接) 作為基底介面。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2257"></span><span id="midl2257"></span><dl> <dt><strong>MIDL2257</strong></dt> </dl></td>
<td><dl> <dt><span id="only_IUnknown_may_be_used_as_the_root_interface"></span><span id="only_iunknown_may_be_used_as_the_root_interface"></span><span id="ONLY_IUNKNOWN_MAY_BE_USED_AS_THE_ROOT_INTERFACE"></span>只有 IUnknown 可以用來做為根介面</dt> <dd> 目前，所有介面都必須有 <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> 作為根介面。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2258"></span><span id="midl2258"></span><dl> <dt><strong>MIDL2258</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_iid_is__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_IID_IS__MAY_ONLY_BE_APPLIED_TO_POINTERS_TO_INTERFACES"></span>[IID_IS] 只可套用至介面的指標</dt> <dd> 您只能將 [<a href="iid-is.md"><strong>iid_is</strong></a>] 屬性套用至介面指標，但可以將它們指定為 <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> * 的指標。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2259"></span><span id="midl2259"></span><dl> <dt><strong>MIDL2259</strong></dt> </dl></td>
<td><dl> <dt><span id="interfaces_may_only_be_used_in_pointer-to-interface_constructs"></span><span id="INTERFACES_MAY_ONLY_BE_USED_IN_POINTER-TO-INTERFACE_CONSTRUCTS"></span>介面只可用於指標對介面的結構中</dt> <dd> 除了基底介面或介面指標之外，無法使用介面名稱。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2260"></span><span id="midl2260"></span><dl> <dt><strong>MIDL2260</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_pointers_must_have_a_UUID_IID"></span><span id="interface_pointers_must_have_a_uuid_iid"></span><span id="INTERFACE_POINTERS_MUST_HAVE_A_UUID_IID"></span>介面指標必須有 UUID/IID</dt> <dd> [<a href="iid-is.md"><strong>Iid_is</strong></a>] 運算式的基底類型必須是 UUID/GUID/iid 類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2261"></span><span id="midl2261"></span><dl> <dt><strong>MIDL2261</strong></dt> </dl></td>
<td><dl> <dt><span id="definitions_and_declarations_outside_of_interface_body_requires__ms_ext"></span><span id="DEFINITIONS_AND_DECLARATIONS_OUTSIDE_OF_INTERFACE_BODY_REQUIRES__MS_EXT"></span>介面主體外部的定義和宣告需要/ms_ext</dt> <dd> 將宣告和定義放在任何介面主體之外是 Microsoft 擴充功能，而且需要使用 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2262"></span><span id="midl2262"></span><dl> <dt><strong>MIDL2262</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_interfaces_in_one_file_requires__ms_ext"></span><span id="MULTIPLE_INTERFACES_IN_ONE_FILE_REQUIRES__MS_EXT"></span>一個檔案中的多個介面需要/ms_ext</dt> <dd> 在單一 idl 檔案中使用多個介面是 Microsoft 擴充功能，當您在 <a href="-osf.md"><strong>/osf</strong></a> 模式中編譯時無法使用。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2263"></span><span id="midl2263"></span><dl> <dt><strong>MIDL2263</strong></dt> </dl></td>
<td><dl> <dt><span id="only_one_of__implicit_handle____auto_handle___or__explicit_handle__allowed"></span><span id="ONLY_ONE_OF__IMPLICIT_HANDLE____AUTO_HANDLE___OR__EXPLICIT_HANDLE__ALLOWED"></span>只允許 [implicit_handle]、[auto_handle] 或 [explicit_handle] 的其中一個</dt> <dd> 每一個介面只能有這三個屬性的其中一個。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2264"></span><span id="midl2264"></span><dl> <dt><strong>MIDL2264</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__references_a_type_which_is_not_a_handle"></span><span id="_IMPLICIT_HANDLE__REFERENCES_A_TYPE_WHICH_IS_NOT_A_HANDLE"></span>[implicit_handle] 參考不是控制碼的類型</dt> <dd> 隱含控制碼必須是其中一個控制碼類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2265"></span><span id="midl2265"></span><dl> <dt><strong>MIDL2265</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__procs_may_only_be_used_with___env_win32_"></span><span id="_OBJECT__PROCS_MAY_ONLY_BE_USED_WITH___ENV_WIN32_"></span>[object] 過程只能搭配 &quot; /env win32 使用&quot;</dt> <dd> 具有 [<a href="object.md"><strong>物件</strong></a>] 屬性的介面無法與16位環境搭配使用。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2266"></span><span id="midl2266"></span><dl> <dt><strong>MIDL2266</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__with_-env_dos_win16_not_supported_for__Oi__using__Os"></span><span id="_callback__with_-env_dos_win16_not_supported_for__oi__using__os"></span><span id="_CALLBACK__WITH_-ENV_DOS_WIN16_NOT_SUPPORTED_FOR__OI__USING__OS"></span>[回呼] 搭配-env dos/win16 不支援/Oi，使用/Os</dt> <dd> 16位環境中的回呼只能由 <a href="-os.md"><strong>/os</strong></a> 優化存根處理。 此常式的存根將使用 <strong>/os</strong> 優化產生。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2267"></span><span id="midl2267"></span><dl> <dt><strong>MIDL2267</strong></dt> </dl></td>
<td><dl> <dt><span id="float_double_not_supported_as_top-level_parameter_for__Oi_mode__using__Os"></span><span id="float_double_not_supported_as_top-level_parameter_for__oi_mode__using__os"></span><span id="FLOAT_DOUBLE_NOT_SUPPORTED_AS_TOP-LEVEL_PARAMETER_FOR__OI_MODE__USING__OS"></span>使用/Os，不支援 float/double 作為/Oi 模式的最上層參數</dt> <dd> Float 和 double 類型只能由 <a href="-os.md"><strong>/os</strong></a> 優化存根作為參數處理。 此常式的存根將使用 <strong>/os</strong> 優化產生。 結構、陣列或等位內的 float 和 double 類型仍可使用<strong>/os</strong>處理。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2268"></span><span id="midl2268"></span><dl> <dt><strong>MIDL2268</strong></dt> </dl></td>
<td><dl> <dt><span id="pointers_to_context_handles_may_not_be_used_as_return_values"></span><span id="POINTERS_TO_CONTEXT_HANDLES_MAY_NOT_BE_USED_AS_RETURN_VALUES"></span>內容控制碼的指標不可以當做傳回值使用</dt> <dd> 內容控制碼必須當做直接傳回值使用，而不是間接傳回值。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2269"></span><span id="midl2269"></span><dl> <dt><strong>MIDL2269</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_in_an_object_interface_must_return_an_HRESULT"></span><span id="procedures_in_an_object_interface_must_return_an_hresult"></span><span id="PROCEDURES_IN_AN_OBJECT_INTERFACE_MUST_RETURN_AN_HRESULT"></span>物件介面中的程式必須傳回 HRESULT</dt> <dd> 物件介面中沒有-[<a href="local.md"><strong>local</strong></a>] 屬性的所有程式都必須傳回<strong>HRESULT</strong> / <strong>SCODE</strong>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2270"></span><span id="midl2270"></span><dl> <dt><strong>MIDL2270</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_UUID"></span><span id="duplicate_uuid"></span><span id="DUPLICATE_UUID"></span>UUID 重複</dt> <dd> 與 Uuid 相同必須是唯一的。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2271"></span><span id="midl2271"></span><dl> <dt><strong>MIDL2271</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_IUnknown"></span><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_iunknown"></span><span id="_OBJECT__INTERFACES_MUST_DERIVE_FROM_ANOTHER__OBJECT__INTERFACE_SUCH_AS_IUNKNOWN"></span>[object] 介面必須衍生自另一個 [object] 介面，例如 IUnknown</dt> <dd> 只有當您使用物件介面時，才允許使用介面繼承。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2272"></span><span id="midl2272"></span><dl> <dt><strong>MIDL2272</strong></dt> </dl></td>
<td><dl> <dt><span id="_async__interface_must_derive_from_another__async__interface"></span><span id="_ASYNC__INTERFACE_MUST_DERIVE_FROM_ANOTHER__ASYNC__INTERFACE"></span> (async) 介面必須衍生自另一個 (async) 介面</dt> <dd> 物件介面（同步和非同步）必須衍生自 <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> 或某些其他基底 OLE 介面。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2273"></span><span id="midl2273"></span><dl> <dt><strong>MIDL2273</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__expression_must_be_a_pointer_to_IID_structure"></span><span id="_iid_is__expression_must_be_a_pointer_to_iid_structure"></span><span id="_IID_IS__EXPRESSION_MUST_BE_A_POINTER_TO_IID_STRUCTURE"></span>[IID_IS] 運算式必須是 IID 結構的指標</dt> <dd> [<a href="iid-is.md"><strong>Iid_is</strong></a>] 運算式的基底類型必須是 UUID/GUID/iid 類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2274"></span><span id="midl2274"></span><dl> <dt><strong>MIDL2274</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__type_must_be_a__local__procedure"></span><span id="_CALL_AS__TYPE_MUST_BE_A__LOCAL__PROCEDURE"></span>[call_as] 類型必須是 [local] 程式</dt> <dd> [<a href="call-as.md"><strong>Call_as</strong></a>] 類型的目標（如果已定義）必須套用 [ <a href="local.md"><strong>本機</strong></a>]。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2275"></span><span id="midl2275"></span><dl> <dt><strong>MIDL2275</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined__call_as__must_not_be_used_in_an_object_interface"></span><span id="UNDEFINED__CALL_AS__MUST_NOT_BE_USED_IN_AN_OBJECT_INTERFACE"></span>未定義的 [call_as] 不能用於物件介面</dt> <dd> 您必須定義 [<a href="call-as.md"><strong>call_as</strong></a>] 類型的目標。 請確定您已為呼叫和呼叫的應用程式提供 <strong>call_as</strong> 常式。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2276"></span><span id="midl2276"></span><dl> <dt><strong>MIDL2276</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__may_not_be_used_with__encode__or__decode_"></span><span id="_AUTO_HANDLE__MAY_NOT_BE_USED_WITH__ENCODE__OR__DECODE_"></span>[auto_handle] 不能與 [編碼] 或 [解碼] 搭配使用</dt> <dd> [ <a href="encode.md"><strong>編碼</strong></a> <a href="decode.md"><strong>] 和 [解碼</strong></a>] 屬性只能搭配明確的控制碼或隱含控制碼使用。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2277"></span><span id="midl2277"></span><dl> <dt><strong>MIDL2277</strong></dt> </dl></td>
<td><dl> <dt><span id="normal_procedures_are_not_allowed_in_an_interface_with__encode__or__decode_"></span><span id="NORMAL_PROCEDURES_ARE_NOT_ALLOWED_IN_AN_INTERFACE_WITH__ENCODE__OR__DECODE_"></span>具有 [編碼] 或 [解碼] 的介面中不允許一般程式</dt> <dd> 包含 [<a href="encode.md"><strong>編碼</strong></a><a href="decode.md"><strong>] 或 [解碼</strong></a>] 程式的介面也不能有遠端程式。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2278"></span><span id="midl2278"></span><dl> <dt><strong>MIDL2278</strong></dt> </dl></td>
<td><dl> <dt><span id="top-level_conformance_or_variance_not_allowed_with__encode__or__decode_"></span><span id="TOP-LEVEL_CONFORMANCE_OR_VARIANCE_NOT_ALLOWED_WITH__ENCODE__OR__DECODE_"></span>[編碼] 或 [解碼] 不允許最上層的一致性或變異數</dt> <dd> 具有最上層一致性或變異數的類型無法使用類型序列化，因為沒有任何方法可提供調整大小/延長。 但是，包含這些結構的結構卻可以使用型別序列化。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2279"></span><span id="midl2279"></span><dl> <dt><strong>MIDL2279</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameters_may_not_have__const_"></span><span id="_OUT__PARAMETERS_MAY_NOT_HAVE__CONST_"></span>[out] 參數可能沒有 &quot; const&quot;</dt> <dd> 因為已改變 [<a href="out-idl.md"><strong>out</strong></a>] 參數，所以不能將它宣告為 sa 常數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2280"></span><span id="midl2280"></span><dl> <dt><strong>MIDL2280</strong></dt> </dl></td>
<td><dl> <dt><span id="return_values_may_not_have__const_"></span><span id="RETURN_VALUES_MAY_NOT_HAVE__CONST_"></span>傳回值可能沒有 &quot; const&quot;</dt> <dd> 由於函數值是在函式傳回時設定的，因此這個值不得宣告為常數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2281"></span><span id="midl2281"></span><dl> <dt><strong>MIDL2281</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_use_of__retval__attribute"></span><span id="INVALID_USE_OF__RETVAL__ATTRIBUTE"></span>不正確 &quot; retval &quot; 屬性用法</dt> <dd> 請檢查以確定您未使用 [<a href="optional.md"><strong>optional</strong></a>] 屬性，而 [<a href="retval.md"><strong>retval</strong></a>] 參數是清單中的最後一個參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2282"></span><span id="midl2282"></span><dl> <dt><strong>MIDL2282</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_calling_conventions_illegal"></span><span id="MULTIPLE_CALLING_CONVENTIONS_ILLEGAL"></span>多個呼叫慣例不合法</dt> <dd> 單一程式只能套用一個呼叫慣例。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2283"></span><span id="midl2283"></span><dl> <dt><strong>MIDL2283</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_illegal_on__object__procedure"></span><span id="ATTRIBUTE_ILLEGAL_ON__OBJECT__PROCEDURE"></span>[object] 程式上的屬性不合法</dt> <dd> 上述屬性僅適用于介面中沒有 [<a href="object.md"><strong>物件</strong></a>] 屬性的程式。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2284"></span><span id="midl2284"></span><dl> <dt><strong>MIDL2284</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__interface_pointers_must_use_double_indirection"></span><span id="_OUT__INTERFACE_POINTERS_MUST_USE_DOUBLE_INDIRECTION"></span>[out] 介面指標必須使用雙重間接取值</dt> <dd> 因為改變的值是介面的指標，所以在指標上方必須有另一個間接取值層級，才能傳回。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2285"></span><span id="midl2285"></span><dl> <dt><strong>MIDL2285</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_used_twice_as_the_caller_in__call_as_"></span><span id="PROCEDURE_USED_TWICE_AS_THE_CALLER_IN__CALL_AS_"></span>程式在 [call_as] 中使用兩次作為呼叫者</dt> <dd> 給定的 [<a href="local.md"><strong>local</strong></a>] 程式只能使用一次作為 [<a href="call-as.md"><strong>call_as</strong></a>] 的目標，以避免發生名稱衝突。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2286"></span><span id="midl2286"></span><dl> <dt><strong>MIDL2286</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__target_must_have__local__in_an_object_interface"></span><span id="_CALL_AS__TARGET_MUST_HAVE__LOCAL__IN_AN_OBJECT_INTERFACE"></span>[call_as] 目標在物件介面中必須有 [local]</dt> <dd> [<a href="call-as.md"><strong>Call_as</strong></a>] 的目標必須是目前介面中定義的 [<a href="local.md"><strong>local</strong></a>] 程式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2287"></span><span id="midl2287"></span><dl> <dt><strong>MIDL2287</strong></dt> </dl></td>
<td><dl> <dt><span id="_code__and__nocode__may_not_be_used_together"></span><span id="_CODE__AND__NOCODE__MAY_NOT_BE_USED_TOGETHER"></span>[程式碼] 和 [了 nocode] 可能不會一起使用</dt> <dd> 這兩個屬性互相衝突，無法一起使用。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2288"></span><span id="midl2288"></span><dl> <dt><strong>MIDL2288</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_HRESULT_or_error_status_t"></span><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_hresult_or_error_status_t"></span><span id="PROCEDURES_WITH__MAYBE__OR__MESSAGE__ATTRIBUTES_MAY_NOT_HAVE__OUT__PARAMS__OR_RETURN_VALUES_MUST_BE_OF_TYPE_HRESULT_OR_ERROR_STATUS_T"></span>具有 [可能] 或 [message] 屬性的程式可能沒有 [out] params，或傳回值的類型必須是 HRESULT 或 error_status_t</dt> <dd> 由於 [<a href="maybe.md"><strong>或許</strong></a>] 程式永遠不會傳回，因此沒有任何方法可取得傳回值。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2289"></span><span id="midl2289"></span><dl> <dt><strong>MIDL2289</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_function_must_be_used"></span><span id="POINTER_TO_FUNCTION_MUST_BE_USED"></span>必須使用函式的指標</dt> <dd> 雖然函式型別定義可在 <a href="-c-ext.md"><strong>/c_ext</strong></a> 模式中使用，但只能做為函式的指標。 它們永遠不能以參數或遠端程式的傳回值來傳送。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2290"></span><span id="midl2290"></span><dl> <dt><strong>MIDL2290</strong></dt> </dl></td>
<td><dl> <dt><span id="functions_may_not_be_passed_in_an_RPC_operation"></span><span id="functions_may_not_be_passed_in_an_rpc_operation"></span><span id="FUNCTIONS_MAY_NOT_BE_PASSED_IN_AN_RPC_OPERATION"></span>函式可能不會在 RPC 操作中傳遞</dt> <dd> 函式和函式指標無法以參數或遠端程式的傳回值形式傳遞。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2291"></span><span id="midl2291"></span><dl> <dt><strong>MIDL2291</strong></dt> </dl></td>
<td><dl> <dt><span id="hyper_double_not_supported_as_return_value_for__Oi_modes__using__Os"></span><span id="hyper_double_not_supported_as_return_value_for__oi_modes__using__os"></span><span id="HYPER_DOUBLE_NOT_SUPPORTED_AS_RETURN_VALUE_FOR__OI_MODES__USING__OS"></span>使用/Os 時，不支援使用/Oi 模式的傳回值作為超/雙精度浮點數</dt> <dd> 只有 <a href="-os.md"><strong>/os</strong></a> 優化存根才能處理超和雙精度浮點數的值。 此常式的存根將使用 <strong>/os</strong> 優化產生。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2292"></span><span id="midl2292"></span><dl> <dt><strong>MIDL2292</strong></dt> </dl></td>
<td><dl> <dt><span id="_pragma_pack_pop__without_matching__pragma_pack_push_"></span><span id="_PRAGMA_PACK_POP__WITHOUT_MATCHING__PRAGMA_PACK_PUSH_"></span>#pragma pack (pop) 沒有相符的 #pragma 套件 (push) </dt> <dd> #pragma pack (push) 和 #pragma pack (pop) 必須出現在成對的配對中。 至少指定了一個或多個 #pragma 套件 (推入) s。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2293"></span><span id="midl2293"></span><dl> <dt><strong>MIDL2293</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structure_fields_must_be_byte_char_wchar_t"></span><span id="STRINGABLE_STRUCTURE_FIELDS_MUST_BE_BYTE_CHAR_WCHAR_T"></span>stringable 結構欄位必須是 byte/char/wchar_t</dt> <dd> 類型 [<a href="string.md"><strong>字串</strong></a>] 只能套用至其欄位全都是 byte 類型的結構，或是等於 byte 的類型定義。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2294"></span><span id="midl2294"></span><dl> <dt><strong>MIDL2294</strong></dt> </dl></td>
<td><dl> <dt><span id="_notify__not_supported_for__Oi_modes__using__Os"></span><span id="_notify__not_supported_for__oi_modes__using__os"></span><span id="_NOTIFY__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>[通知]/Oi 模式不支援使用/Os</dt> <dd> [<a href="notify.md"><strong>通知</strong></a>] 屬性只能由 <a href="-os.md"><strong>/os</strong></a> 優化存根處理。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2295"></span><span id="midl2295"></span><dl> <dt><strong>MIDL2295</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle_parameter_or_return_type_is_not_supported_on_a_procedure_in_an__object__interface"></span><span id="_HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span> 在 [物件] 介面中的程式上不支援控制碼參數或傳回類型</dt> <dd> 控制碼不能與 [ <a href="object.md"><strong>object</strong></a>] 介面一起使用。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2296"></span><span id="midl2296"></span><dl> <dt><strong>MIDL2296</strong></dt> </dl></td>
<td><dl> <dt><span id="ANSI_C_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ansi_c_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ANSI_C_ONLY_ALLOWS_THE_LEFTMOST_ARRAY_BOUND_TO_BE_UNSPECIFIED"></span>ANSI C 只允許未指定最左邊的陣列系結</dt> <dd> 在符合標準的陣列中，ANSI C 只允許最左邊的 (最重要的) 陣列系結至未指定。 如果有多個維度一致，MIDL 會嘗試將 &quot; 1 放 &quot; 在其他符合標準的維度中。 如果其他維度是在不同的類型定義中定義，則無法這麼做。 請嘗試將所有陣列維度放在陣列宣告上，以避免發生這種情況。 在任何情況下，請注意由編譯器完成的陣列索引計算;您可能需要使用實際大小來進行自己的計算。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2297"></span><span id="midl2297"></span><dl> <dt><strong>MIDL2297</strong></dt> </dl></td>
<td><dl> <dt><span id="by-value_union_parameters_not_supported_for__Oi_modes__using__Os"></span><span id="by-value_union_parameters_not_supported_for__oi_modes__using__os"></span><span id="BY-VALUE_UNION_PARAMETERS_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>/Oi 模式不支援使用/Os 值的 union 參數</dt> <dd> 完全解讀的優化不支援這個動作。 切換至混合模式優化。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2298"></span><span id="midl2298"></span><dl> <dt><strong>MIDL2298</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__attribute_is_ignored_on_an__object__interface"></span><span id="_VERSION__ATTRIBUTE_IS_IGNORED_ON_AN__OBJECT__INTERFACE"></span>[version] 在 [object] 介面上略過屬性</dt> <dd> [<a href="object.md"><strong>物件</strong></a>] 屬性會識別 COM 介面。 COM 介面的介面屬性清單不能包含 [ <a href="version.md"><strong>版本</strong></a>] 屬性。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2299"></span><span id="midl2299"></span><dl> <dt><strong>MIDL2299</strong></dt> </dl></td>
<td><dl> <dt><span id="_size_is__or__max_is__attribute_is_invalid_on_a_fixed_array"></span><span id="_SIZE_IS__OR__MAX_IS__ATTRIBUTE_IS_INVALID_ON_A_FIXED_ARRAY"></span>固定陣列上的 [size_is] 或 [max_is] 屬性無效</dt> <dd> 固定大小的陣列不能使用 <a href="size-is.md"><strong>size_is</strong></a> 或 <a href="max-is.md"><strong>max_is</strong></a> 屬性。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2300"></span><span id="midl2300"></span><dl> <dt><strong>MIDL2300</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__are_invalid_in_an__object__interface"></span><span id="_ENCODE__OR__DECODE__ARE_INVALID_IN_AN__OBJECT__INTERFACE"></span>[object] 介面中的 [編碼] 或 [解碼] 無效</dt> <dd> [<a href="object.md"><strong>物件</strong></a>] 屬性會識別 COM 介面。 [<a href="encode.md"><strong>編碼</strong></a> <a href="decode.md"><strong>] 和 [解碼</strong></a>] 屬性會啟用序列化。 也就是說，您可以提供和控制資料封送處理和 unmarshal 的緩衝區，不過，您無法在 COM 介面上執行序列化。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2301"></span><span id="midl2301"></span><dl> <dt><strong>MIDL2301</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__on_a_type_requires__ms_ext"></span><span id="_ENCODE__OR__DECODE__ON_A_TYPE_REQUIRES__MS_EXT"></span>類型需要/ms_ext 上的 [編碼] 或 [解碼]</dt> <dd> 序列化不是 DCE IDL 規格的一部分。 它是 Microsoft 擴充功能，需要使用 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 命令列參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2302"></span><span id="midl2302"></span><dl> <dt><strong>MIDL2302</strong></dt> </dl></td>
<td><dl> <dt><span id="int_not_supported_on__env_win16_or__env_dos"></span><span id="INT_NOT_SUPPORTED_ON__ENV_WIN16_OR__ENV_DOS"></span>/env win16 或/env dos 不支援 int</dt> <dd> 16位的 Microsoft 平臺不支援在 IDL 檔案中使用 <a href="int.md"><strong>int</strong></a> 類型。 使用<a href="small.md"><strong>small</strong></a>、 <a href="short.md"><strong>short</strong></a>或<a href="long.md"><strong>long</strong></a>限定<strong>int</strong>類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2303"></span><span id="midl2303"></span><dl> <dt><strong>MIDL2303</strong></dt> </dl></td>
<td><dl> <dt><span id="_bstring__may_only_be_applied_to_a_pointer_to__char__or__whchar_t_"></span><span id="_BSTRING__MAY_ONLY_BE_APPLIED_TO_A_POINTER_TO__CHAR__OR__WHCHAR_T_"></span>[bstring] 僅適用于 &quot; char &quot; 或 &quot; whchar_t 的指標&quot;</dt> <dd> 此錯誤已淘汰。 僅提供回溯相容性。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2304"></span><span id="midl2304"></span><dl> <dt><strong>MIDL2304</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_a_procedure_in_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span>在 [object] 介面中的程式上，屬性無效</dt> <dd> COM 介面中的程式上不允許指定的屬性。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2305"></span><span id="midl2305"></span><dl> <dt><strong>MIDL2305</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_AN__OBJECT__INTERFACE"></span>在 [object] 介面上的屬性無效</dt> <dd> COM 介面中不允許指定的屬性。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2306"></span><span id="midl2306"></span><dl> <dt><strong>MIDL2306</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_parameters_or_stack_too_big_for__Oi_modes__using__Os"></span><span id="too_many_parameters_or_stack_too_big_for__oi_modes__using__os"></span><span id="TOO_MANY_PARAMETERS_OR_STACK_TOO_BIG_FOR__OI_MODES__USING__OS"></span>太多參數或堆疊太大而無法/Oi 模式，請使用/Os</dt> <dd> 此警告已淘汰。 僅提供回溯相容性。 它指出遠端程式的呼叫會導致堆疊成長到大於 64 K 的範圍。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2307"></span><span id="midl2307"></span><dl> <dt><strong>MIDL2307</strong></dt> </dl></td>
<td><dl> <dt><span id="no_attributes_on_ACF_file_typedef__so_no_effect"></span><span id="no_attributes_on_acf_file_typedef__so_no_effect"></span><span id="NO_ATTRIBUTES_ON_ACF_FILE_TYPEDEF__SO_NO_EFFECT"></span>ACF 檔 typedef 沒有任何屬性，因此沒有任何作用</dt> <dd> IDL 檔案應包含所有不具有屬性的 typedef 語句。 這些檔案不應該出現在 ACF 檔中。 如果有的話，MIDL 編譯器會將它們解釋為多餘的，並加以忽略。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2308"></span><span id="midl2308"></span><dl> <dt><strong>MIDL2308</strong></dt> </dl></td>
<td><dl> <dt><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__Oi_modes__using__Os"></span><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__oi_modes__using__os"></span><span id="CALLING_CONVENTIONS_OTHER_THAN___STDCALL_OR___CDECL_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>使用/Os 來呼叫/Oi 模式以外的 __stdcall 或 __cdecl 不支援的慣例</dt> <dd> 呼叫慣例（例如 <strong>__pascal</strong> 或 <strong>__fastcall</strong> ）會變更堆疊的格式。 <a href="-oi.md"><strong>/Oi</strong></a>模式僅支援<strong>__stdcall</strong>和<strong>__cdecl</strong>呼叫慣例。 如果您必須使用其他呼叫慣例，請使用 <a href="-os.md"><strong>/os</strong></a> 模式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2309"></span><span id="midl2309"></span><dl> <dt><strong>MIDL2309</strong></dt> </dl></td>
<td><dl> <dt><span id="Too_many_delegation_methods_in_the_interface__require_Windows_2000_or_greater"></span><span id="too_many_delegation_methods_in_the_interface__require_windows_2000_or_greater"></span><span id="TOO_MANY_DELEGATION_METHODS_IN_THE_INTERFACE__REQUIRE_WINDOWS_2000_OR_GREATER"></span>介面中有太多委派方法，需要 Windows 2000 或更高版本</dt> <dd> 一個介面可以繼承自另一個介面。 當它執行時，基底介面的方法會被視為委派。 沒有衍生的介面可以包含256個以上的委派方法。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2310"></span><span id="midl2310"></span><dl> <dt><strong>MIDL2310</strong></dt> </dl></td>
<td><dl> <dt><span id="auto_handles_not_supported_with__env_mac_or__env_powermac"></span><span id="AUTO_HANDLES_NOT_SUPPORTED_WITH__ENV_MAC_OR__ENV_POWERMAC"></span>/env mac 或/env powermac 不支援的自動控制碼</dt> <dd> 編譯 PowerMac 的 IDL 檔案時，無法使用自動系結控制碼。 您必須指定明確或隱含控制碼。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2311"></span><span id="midl2311"></span><dl> <dt><strong>MIDL2311</strong></dt> </dl></td>
<td><dl> <dt><span id="statements_outside_library_block_are_illegal_in_mktyplib_compatibility_mode"></span><span id="STATEMENTS_OUTSIDE_LIBRARY_BLOCK_ARE_ILLEGAL_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>程式庫區塊外部的語句在 mktyplib.exe 相容性模式中是不合法的</dt> <dd> 當您編譯 IDL 檔案時，可能需要指定 <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> 命令列參數。<br/>
<blockquote>
[!Note]<br />
Mktyplib.exe 工具已淘汰。 請改用 MIDL 編譯器。
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2312"></span><span id="midl2312"></span><dl> <dt><strong>MIDL2312</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_syntax_unless_using_mktyplib_compatibility_mode"></span><span id="ILLEGAL_SYNTAX_UNLESS_USING_MKTYPLIB_COMPATIBILITY_MODE"></span>除非使用 mktyplib.exe 相容性模式，否則語法不合法</dt> <dd> 當您編譯 IDL 檔案時，可能需要指定 <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> 命令列參數。<br/>
<blockquote>
[!Note]<br />
Mktyplib.exe 工具已淘汰。 請改用 MIDL 編譯器。
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2313"></span><span id="midl2313"></span><dl> <dt><strong>MIDL2313</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_definition__must_use_typedef_in_mktyplib_compatibility_mode"></span><span id="ILLEGAL_DEFINITION__MUST_USE_TYPEDEF_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>不合法的定義，必須在 mktyplib.exe 相容性模式中使用 typedef</dt> <dd> 當您編譯 IDL 檔案時，可能需要指定 <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> 命令列參數。<br/>
<blockquote>
[!Note]<br />
Mktyplib.exe 工具已淘汰。 請改用 MIDL 編譯器。
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2314"></span><span id="midl2314"></span><dl> <dt><strong>MIDL2314</strong></dt> </dl></td>
<td><dl> <dt><span id="explicit_pointer_attribute__ptr___ref__ignored_for_interface_pointers"></span><span id="EXPLICIT_POINTER_ATTRIBUTE__PTR___REF__IGNORED_FOR_INTERFACE_POINTERS"></span>已忽略介面指標的明確指標屬性 [ptr] [ref]</dt> <dd> 介面的指標不能有 IDL 屬性。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2315"></span><span id="midl2315"></span><dl> <dt><strong>MIDL2315</strong></dt> </dl></td>
<td><a href="-oi.md"><strong>/Oi</strong></a>模式未針對 PowerMac 執行，切換至<a href="-os.md"> <strong>/os</strong></a><br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2316"></span><span id="midl2316"></span><dl> <dt><strong>MIDL2316</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_used_in_attribute"></span><span id="ILLEGAL_EXPRESSION_TYPE_USED_IN_ATTRIBUTE"></span>屬性中使用的運算式類型不合法</dt> <dd> 指標的預設值應該是常數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2317"></span><span id="midl2317"></span><dl> <dt><strong>MIDL2317</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_type_used_in_pipe"></span><span id="ILLEGAL_TYPE_USED_IN_PIPE"></span>管道中使用的類型不合法</dt> <dd> 管道僅限於基本的 IDL 資料類型。 例如，您不能指定陣列的管道。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2318"></span><span id="midl2318"></span><dl> <dt><strong>MIDL2318</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_uses_pipes__using__Oicf"></span><span id="procedure_uses_pipes__using__oicf"></span><span id="PROCEDURE_USES_PIPES__USING__OICF"></span>程式使用管道，使用/Oicf</dt> <dd> 您選取的模式不支援管道。 MIDL 編譯器偵測到在您的介面中使用一或多個管道。 因此，它會在 <a href="-oi.md"><strong>/Oicf</strong></a> 模式中編譯您的 IDL 檔案。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2319"></span><span id="midl2319"></span><dl> <dt><strong>MIDL2319</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_has_an_attribute_that_requires_use_of__Oif__switching_modes"></span><span id="procedure_has_an_attribute_that_requires_use_of__oif__switching_modes"></span><span id="PROCEDURE_HAS_AN_ATTRIBUTE_THAT_REQUIRES_USE_OF__OIF__SWITCHING_MODES"></span>程式具有需要使用/Oif、切換模式的屬性</dt> <dd> 您必須在<a href="-oi.md"><strong>/Oif</strong></a>模式中編譯 [<a href="async.md"><strong>async</strong></a>] 程式。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2320"></span><span id="midl2320"></span><dl> <dt><strong>MIDL2320</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_optimization_requirements__cannot_optimize"></span><span id="CONFLICTING_OPTIMIZATION_REQUIREMENTS__CANNOT_OPTIMIZE"></span>衝突的優化需求，無法優化</dt> <dd> 此錯誤通常表示您同時指定了 <a href="-os.md"><strong>/os</strong></a> 和 <a href="-oi.md"><strong>/Oi</strong></a> (或 <strong>/Oi</strong>) MIDL 編譯器模式的變異。 這也可能表示您在 IDL 和 ACL 檔案中指定的功能需要使用這兩種模式。 您必須選取一個模式或另一個模式來優化。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2321"></span><span id="midl2321"></span><dl> <dt><strong>MIDL2321</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_cannot_be_array_elements__or_members_of_structures_or_unions"></span><span id="PIPES_CANNOT_BE_ARRAY_ELEMENTS__OR_MEMBERS_OF_STRUCTURES_OR_UNIONS"></span>管道不可以是陣列元素，也不能是結構或等位的成員</dt> <dd> 管道資料類型只能是最上層參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2322"></span><span id="midl2322"></span><dl> <dt><strong>MIDL2322</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_pipe_usage"></span><span id="INVALID_PIPE_USAGE"></span>不正確管道使用方式</dt> <dd> 您無法使用具有 [<a href="transmit-as.md"><strong>transmit_as</strong></a>]、[<a href="represent-as.md"><strong>represent_as</strong></a>] 或 [<a href="user-marshal.md"><strong>user_marshal</strong></a>] 屬性的管道。 此外，管道不能當做傳回類型使用。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2323"></span><span id="midl2323"></span><dl> <dt><strong>MIDL2323</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>功能需要 advanced 解讀優化選項;使用-Oicf</dt> <dd> 此錯誤指出 MIDL 編譯器命令列參數（例如 <a href="-robust.md"><strong>/robust</strong></a> ）需要使用 <a href="-oi.md"><strong>/Oicf</strong></a> 模式。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2324"></span><span id="midl2324"></span><dl> <dt><strong>MIDL2324</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>功能需要 advanced 解讀優化選項;使用-Oicf</dt> <dd> 此警告表示 MIDL 編譯器命令列參數（例如 <a href="-robust.md"><strong>/robust</strong></a> ）需要使用 <a href="-oi.md"><strong>/Oicf</strong></a> 模式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2329"></span><span id="midl2329"></span><dl> <dt><strong>MIDL2329</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oic"></span><span id="the_optimization_option_is_being_phased_out__use_-oic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OIC"></span>優化選項即將淘汰，請使用-Oic</dt> <dd> MIDL 命令列上指定了 <a href="-oi.md"><strong>/Oi1</strong></a> 優化模式。 不再支援此模式，因此應該改用 <strong>/Oicf</strong> 。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2330"></span><span id="midl2330"></span><dl> <dt><strong>MIDL2330</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oicf"></span><span id="the_optimization_option_is_being_phased_out__use_-oicf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OICF"></span>優化選項即將淘汰，請使用-Oicf</dt> <dd> MIDL 命令列上指定了 <a href="-oi.md"><strong>/Oi2</strong></a> 優化模式。 不再支援此模式，因此應該改用 <strong>/Oicf</strong> 。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2331"></span><span id="midl2331"></span><dl> <dt><strong>MIDL2331</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-ic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-IC"></span>優化選項即將淘汰，請使用-ic</dt> <dd> 在 [optimize] ACF 屬性中指定了 i1 優化模式。 不再支援此模式，因此應該改用 icf。<br/> 範例 ACF 檔：<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i1&quot;)] roo();    //MIDL 2331</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2332"></span><span id="midl2332"></span><dl> <dt><strong>MIDL2332</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-icf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-ICF"></span>優化選項即將淘汰，請使用-icf</dt> <dd> 在 [optimize] ACF 屬性中指定了 i2 優化模式。 不再支援此模式，因此應該改用 icf。<br/> 範例 ACF 檔：<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i2&quot;)] roo();    //MIDL 2332</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2333"></span><span id="midl2333"></span><dl> <dt><strong>MIDL2333</strong></dt> </dl></td>
<td><dl> <dt><span id="the_-old_and_-new_switches_are_obsolete__use_-oldtlb_and_-newtlb"></span><span id="THE_-OLD_AND_-NEW_SWITCHES_ARE_OBSOLETE__USE_-OLDTLB_AND_-NEWTLB"></span>-old 和-new 參數已過時，請使用-newtlb oldtlb 和-newtlb</dt> <dd> 此訊息已過時，而且 MIDL 不再省略。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2334"></span><span id="midl2334"></span><dl> <dt><strong>MIDL2334</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_argument_value"></span><span id="ILLEGAL_ARGUMENT_VALUE"></span>不合法的引數值</dt> <dd> 允許的/O 命令列參數變數包括 <a href="-os.md"><strong>/os</strong></a>、 <a href="-oi.md"><strong>/Oi</strong></a>、 <strong>/Oic</strong>、 <strong>/Oicf</strong>和 <strong>/Oif</strong>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2335"></span><span id="midl2335"></span><dl> <dt><strong>MIDL2335</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_constant"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_CONSTANT"></span>常數中的運算式類型不合法</dt> <dd> 運算式不會評估為常數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2336"></span><span id="midl2336"></span><dl> <dt><strong>MIDL2336</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_enum"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_ENUM"></span>列舉中的運算式類型不合法</dt> <dd> <a href="enum.md"><strong>列舉</strong></a>定義中的列舉值不會評估為整數類資料類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2337"></span><span id="midl2337"></span><dl> <dt><strong>MIDL2337</strong></dt> </dl></td>
<td><dl> <dt><span id="unsatisfied_forward_declaration"></span><span id="UNSATISFIED_FORWARD_DECLARATION"></span>不滿足的向前宣告</dt> <dd> MIDL 編譯器無法解析向前宣告的定義。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2338"></span><span id="midl2338"></span><dl> <dt><strong>MIDL2338</strong></dt> </dl></td>
<td><dl> <dt><span id="switches_are_contradictory"></span><span id="SWITCHES_ARE_CONTRADICTORY"></span>參數互相矛盾</dt> <dd> 當您編譯 IDL 檔案時，不能同時使用 <a href="-osf.md"><strong>/osf</strong></a> 和 <a href="-ms-ext.md"><strong>/ms_ext</strong></a> 命令列參數。 您必須選擇其中一個。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2339"></span><span id="midl2339"></span><dl> <dt><strong>MIDL2339</strong></dt> </dl></td>
<td><dl> <dt><span id="MIDL_cannot_generate_HOOKOLE_information_for_the_non-rpc-able_union"></span><span id="midl_cannot_generate_hookole_information_for_the_non-rpc-able_union"></span><span id="MIDL_CANNOT_GENERATE_HOOKOLE_INFORMATION_FOR_THE_NON-RPC-ABLE_UNION"></span>MIDL 無法產生非 rpc 型聯集的 HOOKOLE 資訊</dt> <dd> 此錯誤已淘汰。 它是為了回溯相容性而提供。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2340"></span><span id="midl2340"></span><dl> <dt><strong>MIDL2340</strong></dt> </dl></td>
<td><dl> <dt><span id="no_case_expression_found_for_union"></span><span id="NO_CASE_EXPRESSION_FOUND_FOR_UNION"></span>找不到 union 的 case 運算式</dt> <dd> Union 的每個欄位都必須有一個具有常數運算式的 case 語句。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2341"></span><span id="midl2341"></span><dl> <dt><strong>MIDL2341</strong></dt> </dl></td>
<td><dl> <dt><span id="_user_marshal__and__wire_marshal__not_supported_with_-Oi_and_-Oic_flags__use_-Os_or_-Oicf"></span><span id="_user_marshal__and__wire_marshal__not_supported_with_-oi_and_-oic_flags__use_-os_or_-oicf"></span><span id="_USER_MARSHAL__AND__WIRE_MARSHAL__NOT_SUPPORTED_WITH_-OI_AND_-OIC_FLAGS__USE_-OS_OR_-OICF"></span>[user_marshal] 和 [wire_marshal] 不支援-Oi 和-Oic 旗標，請使用-Os 或-Oicf</dt> <dd> [<a href="user-marshal.md"><strong>User_marshal</strong></a>] 和 [<a href="wire-marshal.md"><strong>wire_marshal</strong></a>] 屬性需要特定的優化功能，僅適用于具有快速格式字串的 <a href="-oi.md"><strong>/Oicf</strong></a> (無程式碼 proxy) 或 <a href="-os.md"><strong>/os</strong></a> (混合模式封送處理) 。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2342"></span><span id="midl2342"></span><dl> <dt><strong>MIDL2342</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_can_t_be_used_with_data_serialization__i.e.__encode__and_or__decode_"></span><span id="PIPES_CAN_T_BE_USED_WITH_DATA_SERIALIZATION__I.E.__ENCODE__AND_OR__DECODE_"></span>管道無法用於資料序列化，亦即 [編碼] 和/或 [解碼]</dt> <dd> 您無法將管道作為參數傳遞給具有 [<a href="encode.md"><strong>編碼</strong></a><a href="decode.md"><strong>] 或 [解碼</strong></a>] 屬性的程式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2343"></span><span id="midl2343"></span><dl> <dt><strong>MIDL2343</strong></dt> </dl></td>
<td><dl> <dt><span id="all_pipe_interface_pointers_must_use_single_indirection"></span><span id="ALL_PIPE_INTERFACE_POINTERS_MUST_USE_SINGLE_INDIRECTION"></span>所有管道介面指標都必須使用單一間接取值</dt> <dd> 您無法以這種方式使用管道介面指標。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2344"></span><span id="midl2344"></span><dl> <dt><strong>MIDL2344</strong></dt> </dl></td>
<td><dl> <dt><span id="_iid_is____cannot_be_used_with_a_pipe_interface_pointer"></span><span id="_IID_IS____CANNOT_BE_USED_WITH_A_PIPE_INTERFACE_POINTER"></span>[iid_is () ] 不能與管道介面指標一起使用</dt> <dd> 此訊息已淘汰。 編譯器不再使用此訊息。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2345"></span><span id="midl2345"></span><dl> <dt><strong>MIDL2345</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_or_inapplicable_-lcid_switch"></span><span id="INVALID_OR_INAPPLICABLE_-LCID_SWITCH"></span>無效或不適用-lcid 參數</dt> <dd> 您指定的本機識別碼 (LCID) 無效。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2346"></span><span id="midl2346"></span><dl> <dt><strong>MIDL2346</strong></dt> </dl></td>
<td><dl> <dt><span id="the_specified_lcid_is_different_from_previous_specification"></span><span id="THE_SPECIFIED_LCID_IS_DIFFERENT_FROM_PREVIOUS_SPECIFICATION"></span>指定的 lcid 與先前的規格不同</dt> <dd> /Lcid 和 [<a href="lcid.md"><strong>lcid</strong></a>] 中指定的值不同。 MIDL 編譯器將會使用最後一個定義的。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2347"></span><span id="midl2347"></span><dl> <dt><strong>MIDL2347</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_is_not_allowed_outside_of_a_library_block"></span><span id="IMPORTLIB_IS_NOT_ALLOWED_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>不允許在程式庫區塊之外使用 importlib</dt> <dd> 所有 [<a href="importlib.md"><strong>importlib</strong></a>] 語句都應出現在 [連結<a href="library.md"><strong>庫</strong></a>] 區塊中。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2348"></span><span id="midl2348"></span><dl> <dt><strong>MIDL2348</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_floating_point_value"></span><span id="INVALID_FLOATING_POINT_VALUE"></span>不正確浮點值</dt> <dd> MIDL 不應發出此錯誤。 如果您看到此錯誤，請將錯誤回報給 Microsoft，以提供重現錯誤所需的所有檔案，包括您的 IDL 檔案、ACF 檔、標頭等等。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2349"></span><span id="midl2349"></span><dl> <dt><strong>MIDL2349</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_member"></span><span id="INVALID_MEMBER"></span>不正確成員</dt> <dd> 程式不可以是程式庫的成員。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2350"></span><span id="midl2350"></span><dl> <dt><strong>MIDL2350</strong></dt> </dl></td>
<td><dl> <dt><span id="possible_invalid_member"></span><span id="POSSIBLE_INVALID_MEMBER"></span>可能是不正確成員</dt> <dd> 若要成為程式庫的有效成員，程式庫元素必須是模組、產生介面、coclass、if 語句、結構、等位、列舉或正向宣告。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2351"></span><span id="midl2351"></span><dl> <dt><strong>MIDL2351</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_pipe_and_interface_types"></span><span id="MISMATCH_IN_PIPE_AND_INTERFACE_TYPES"></span>管道和介面類別型不符</dt> <dd> 此訊息已淘汰。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2352"></span><span id="midl2352"></span><dl> <dt><strong>MIDL2352</strong></dt> </dl></td>
<td><dl> <dt><span id="string__varying_array__conformant_array_and_full_pointer_parameters_may_be_incompatible_with_pipe_parameters_during_run_time"></span><span id="STRING__VARYING_ARRAY__CONFORMANT_ARRAY_AND_FULL_POINTER_PARAMETERS_MAY_BE_INCOMPATIBLE_WITH_PIPE_PARAMETERS_DURING_RUN_TIME"></span>字串、不同陣列、符合標準的陣列和完整指標參數，在執行時間中可能與管道參數不相容</dt> <dd> 結合一個或多個 [in] 字串、不同陣列、符合標準的陣列和完整指標參數和任何 [in] 管道參數的方法，會產生只在 Windows 電腦上的 <strong>ncacn_ *</strong> 和 <a href="ncalrpc.md"><strong>ncalrpc</strong></a> 通訊協定序列上執行的存根產生。 使用存根來呼叫 <strong>ncadg_ *</strong> 通訊協定序列或接受來自其他憑證 DCE RPC 廠商的呼叫，可能會在執行時間于伺服器上產生錯誤。 從 Windows Server 2003 開始，就會發生此錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2353"></span><span id="midl2353"></span><dl> <dt><strong>MIDL2353</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_be_in"></span><span id="PARAMETER_MUST_BE_IN"></span>參數必須在</dt> <dd> 非同步控制碼必須是 [<a href="in.md"><strong>in</strong></a>] 參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2354"></span><span id="midl2354"></span><dl> <dt><strong>MIDL2354</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_type_of_an__async__object_must_be_a_double_pointer_to_an_interface"></span><span id="PARAMETER_TYPE_OF_AN__ASYNC__OBJECT_MUST_BE_A_DOUBLE_POINTER_TO_AN_INTERFACE"></span>[async] 物件的參數類型必須是介面的雙指標</dt> <dd> 參數的類型必須是 <strong>IAsyncManager</strong> * *。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2355"></span><span id="midl2355"></span><dl> <dt><strong>MIDL2355</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_async_handle_type"></span><span id="INCORRECT_ASYNC_HANDLE_TYPE"></span>不正確的非同步控制碼類型</dt> <dd> 控制碼類型應該是 <strong>IAsyncManager</strong> 或衍生自 <strong>IAsyncManager</strong>的類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2356"></span><span id="midl2356"></span><dl> <dt><strong>MIDL2356</strong></dt> </dl></td>
<td><dl> <dt><span id="the__internal__switch_enables_unsupported_features__use_with_caution"></span><span id="THE__INTERNAL__SWITCH_ENABLES_UNSUPPORTED_FEATURES__USE_WITH_CAUTION"></span>&quot;內部 &quot; 交換器啟用不支援的功能，請謹慎使用</dt> <dd> 請避免使用此參數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2357"></span><span id="midl2357"></span><dl> <dt><strong>MIDL2357</strong></dt> </dl></td>
<td><dl> <dt><span id="async_procedures_cannot_use_auto_handle"></span><span id="ASYNC_PROCEDURES_CANNOT_USE_AUTO_HANDLE"></span>非同步程式無法使用自動控制碼</dt> <dd> 具有 [<a href="async.md"><strong>async</strong></a>] 屬性的程式需要明確控制碼。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2358"></span><span id="midl2358"></span><dl> <dt><strong>MIDL2358</strong></dt> </dl></td>
<td><dl> <dt><span id="error_status_t_should_have_both__comm_status__and__fault_status_"></span><span id="ERROR_STATUS_T_SHOULD_HAVE_BOTH__COMM_STATUS__AND__FAULT_STATUS_"></span>error_status_t 應同時具有 [comm_status] 和 [fault_status]</dt> <dd> 使用 IDL 屬性 [或許] 或 [message] 指定了程式，但傳回型別只有 ACF 屬性 [comm_status] 或 [fault_status]。 這兩個 ACF 屬性都是必要的。<br/> 範例 ACF 檔：<br/>
<pre class="syntax" data-space="preserve"><code>[comm_status] roo();    //MIDL 2358
[fault_status] bar();    //MIDL 2358
[comm_status, fault_status] baz();    //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2359"></span><span id="midl2359"></span><dl> <dt><strong>MIDL2359</strong></dt> </dl></td>
<td><dl> <dt><span id="this_construct_is_only_allowed_within_a_library_block"></span><span id="THIS_CONSTRUCT_IS_ONLY_ALLOWED_WITHIN_A_LIBRARY_BLOCK"></span>此結構只能在程式庫區塊內使用</dt> <dd> 模組只能在程式庫區塊內發生。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2360"></span><span id="midl2360"></span><dl> <dt><strong>MIDL2360</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_type_redefinition"></span><span id="INVALID_TYPE_REDEFINITION"></span>不正確類型重新定義</dt> <dd> 在不存在類型上遞迴定義了新的類型。<br/> 範例：<br/>
<pre class="syntax" data-space="preserve"><code>typedef roo roo[10];    //MIDL 2360</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2361"></span><span id="midl2361"></span><dl> <dt><strong>MIDL2361</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with_a__vararg__attribute_must_have_a_SAFEARRAY_VARIANT__parameter__param_order_is__vararg____lcid____retval_"></span><span id="procedures_with_a__vararg__attribute_must_have_a_safearray_variant__parameter__param_order_is__vararg____lcid____retval_"></span><span id="PROCEDURES_WITH_A__VARARG__ATTRIBUTE_MUST_HAVE_A_SAFEARRAY_VARIANT__PARAMETER__PARAM_ORDER_IS__VARARG____LCID____RETVAL_"></span>具有 [vararg] 屬性的程式必須有 SAFEARRAY (VARIANT) 參數;param 順序為 [vararg]、[lcid]、[retval]</dt> <dd> 具有 [<a href="vararg.md"><strong>vararg</strong></a>] 屬性之程式的大部分參數都必須在 <strong>SAFEARRAY (VARIANT) </strong> 參數之前發生。 <strong>SAFEARRAY (VARIANT) </strong>參數必須存在。 如果參數清單中包含具有 [ <a href="lcid.md"><strong>lcid</strong></a>] 屬性的參數，則必須遵循 <strong>SAFEARRAY (VARIANT) </strong> 參數。 如果參數清單包含具有 [<a href="retval.md"><strong>retval</strong></a>] 屬性的參數，則必須在具有 [<strong>lcid</strong>] 屬性的參數之後發生。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2363"></span><span id="midl2363"></span><dl> <dt><strong>MIDL2363</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_methods_in_the_interface__requires_Windows_2000_or_greater"></span><span id="too_many_methods_in_the_interface__requires_windows_2000_or_greater"></span><span id="TOO_MANY_METHODS_IN_THE_INTERFACE__REQUIRES_WINDOWS_2000_OR_GREATER"></span>介面中有太多方法，需要 Windows 2000 或更高版本</dt> <dd> 當您在 <a href="-oi.md"><strong>/Oicf</strong></a> 模式中進行編譯時，MIDL 編譯器不允許在介面中使用1024以上的方法。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2364"></span><span id="midl2364"></span><dl> <dt><strong>MIDL2364</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_is_being_phased_out"></span><span id="SWITCH_IS_BEING_PHASED_OUT"></span>切換即將淘汰</dt> <dd> 下列參數已過時：/<strong>hookole</strong>、/<strong>env win16</strong>和/<strong>env</strong>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2365"></span><span id="midl2365"></span><dl> <dt><strong>MIDL2365</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_derive_from_IAdviseSink__IAdviseSink2__or_IAdviseSinkEx"></span><span id="cannot_derive_from_iadvisesink__iadvisesink2__or_iadvisesinkex"></span><span id="CANNOT_DERIVE_FROM_IADVISESINK__IADVISESINK2__OR_IADVISESINKEX"></span>無法衍生自 IAdviseSink、IAdviseSink2 或 IAdviseSinkEx</dt> <dd> 無法擴充這些介面。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2366"></span><span id="midl2366"></span><dl> <dt><strong>MIDL2366</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_assign_a_default_value"></span><span id="CANNOT_ASSIGN_A_DEFAULT_VALUE"></span>無法指派預設值</dt> <dd> Visual Basic 中允許指派預設值給參數，但在 c + + 中則不允許。 如果您使用 c + +，則會忽略預設值。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2367"></span><span id="midl2367"></span><dl> <dt><strong>MIDL2367</strong></dt> </dl></td>
<td><dl> <dt><span id="type_library_generation_for_DOS_Win16_MAC_is_not_supported"></span><span id="type_library_generation_for_dos_win16_mac_is_not_supported"></span><span id="TYPE_LIBRARY_GENERATION_FOR_DOS_WIN16_MAC_IS_NOT_SUPPORTED"></span>不支援 DOS/Win16/MAC 的類型程式庫產生</dt> <dd> MIDL 不支援16位的類型程式庫。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2368"></span><span id="midl2368"></span><dl> <dt><strong>MIDL2368</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library__ignored"></span><span id="ERROR_GENERATING_TYPE_LIBRARY__IGNORED"></span>產生類型程式庫時發生錯誤，已忽略</dt> <dd> 產生類型程式庫時發生非嚴重錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2369"></span><span id="midl2369"></span><dl> <dt><strong>MIDL2369</strong></dt> </dl></td>
<td><dl> <dt><span id="exceeded_stack_size_for__Oi__using__Os"></span><span id="exceeded_stack_size_for__oi__using__os"></span><span id="EXCEEDED_STACK_SIZE_FOR__OI__USING__OS"></span>使用/Os 超過/Oi 的堆疊大小</dt> <dd> -Oi 優化模式的參數限制為128個位元組的堆疊空間。 編譯器已自動切換至 Os 優化模式，以解決這項限制。<br/> 若要避免這個警告，請使用-Oicf 或-Os 優化模式。 您可以在命令列上變更優化模式，方法是指定-Oicf 或-Os，而不是-Oi，或在 ACF 檔案中新增 [optimize9 &quot; icf &quot;) ] 或將 [ (&quot; s &quot;) ] 屬性優化。<br/> 當以傳值方式將大型結構傳遞為參數時，通常會發生這個警告。 您可以改為傳遞結構的指標，來降低所需的堆疊大小。<br/> 範例：<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
char a[127];
}
large;
//This function has a stack size of 132 (x86) or 136 (alpha) on 32-bit systems
void roo(large s, int a);    //MIDL 2360
// workaround: pass by reference
void bar (large *s, int a);</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2370"></span><span id="midl2370"></span><dl> <dt><strong>MIDL2370</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__robust_requires__Oicf__switching_modes"></span><span id="use_of__robust_requires__oicf__switching_modes"></span><span id="USE_OF__ROBUST_REQUIRES__OICF__SWITCHING_MODES"></span>使用/robust 需要/Oicf、切換模式</dt> <dd> 當您在命令列上指定<a href="-robust.md"><strong>/robust</strong></a>參數時，必須在<a href="-oi.md"><strong>/Oicf</strong></a>模式中進行編譯。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2371"></span><span id="midl2371"></span><dl> <dt><strong>MIDL2371</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_range_specified"></span><span id="INCORRECT_RANGE_SPECIFIED"></span>指定了不正確的範圍</dt> <dd> [<a href="range.md"><strong>範圍</strong></a>] 屬性中指定的最大值小於最小值。<br/> 範例：<br/>
<pre class="syntax" data-space="preserve"><code>void roo([range(3,2)] int a);    //MIDL 2371</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2372"></span><span id="midl2372"></span><dl> <dt><strong>MIDL2372</strong></dt> </dl></td>
<td><dl> <dt><span id="_invalid_combination_of__in__only_and__out__parameters_for__async_uuid__interface"></span><span id="_INVALID_COMBINATION_OF__IN__ONLY_AND__OUT__PARAMETERS_FOR__ASYNC_UUID__INTERFACE"></span> [in] 和 [out] 參數的組合無效 [async_uuid] 介面</dt> <dd> 這種類型的介面只允許使用 [<a href="in.md"><strong>in</strong></a>] 或 [<a href="out-idl.md"><strong>out</strong></a>] 參數的簡單屬性組合。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2373"></span><span id="midl2373"></span><dl> <dt><strong>MIDL2373</strong></dt> </dl></td>
<td><dl> <dt><span id="DOS__Win16_and_MAC_platforms_are_not_supported_with__robust"></span><span id="dos__win16_and_mac_platforms_are_not_supported_with__robust"></span><span id="DOS__WIN16_AND_MAC_PLATFORMS_ARE_NOT_SUPPORTED_WITH__ROBUST"></span>/Robust 不支援 DOS、Win16 和 MAC 平臺</dt> <dd> MIDL 支援 Microsoft Windows 2000 或更新版本上的 <a href="-robust.md"><strong>/robust</strong></a> 參數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2374"></span><span id="midl2374"></span><dl> <dt><strong>MIDL2374</strong></dt> </dl></td>
<td><dl> <dt><span id="support_for_NT_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__Oif."></span><span id="support_for_nt_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__oif."></span><span id="SUPPORT_FOR_NT_3.51_STYLE_STUBLESS_PROXIES_FOR_OBJECT_INTERFACES_WILL_BE_PHASED_OUT__USE__OIF."></span>物件介面的 NT 3.51 樣式 stubless proxy 支援將會被分段出;使用/Oif。</dt> <dd> 此模式已淘汰。 使用 <a href="-oi.md"><strong>/Oif</strong></a> 或 <strong>/Oicf</strong>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2375"></span><span id="midl2375"></span><dl> <dt><strong>MIDL2375</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__with__robust_requires__Oicf"></span><span id="_encode__or__decode__with__robust_requires__oicf"></span><span id="_ENCODE__OR__DECODE__WITH__ROBUST_REQUIRES__OICF"></span>[編碼] 或 [解碼]/robust 需要/Oicf</dt> <dd> 當指定 <a href="-robust.md"><strong>/robust</strong></a> 參數時，無法執行序列化。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2377"></span><span id="midl2377"></span><dl> <dt><strong>MIDL2377</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_attributes_specified"></span><span id="CONFLICTING_ATTRIBUTES_SPECIFIED"></span>指定了衝突的屬性</dt> <dd> 同時指定 [<a href="context-handle-serialize.md"><strong>coNtext_handle_serialize</strong></a>] 和 [<a href="context-handle-noserialize.md"><strong>coNtext_handle_noserialize</strong></a>]。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2378"></span><span id="midl2378"></span><dl> <dt><strong>MIDL2378</strong></dt> </dl></td>
<td><dl> <dt><span id="_serialize____noserialize__can_be_applied_to_context_handles"></span><span id="_SERIALIZE____NOSERIALIZE__CAN_BE_APPLIED_TO_CONTEXT_HANDLES"></span>[序列化]，[noserialize] 可以套用至 coNtext_handles</dt> <dd> ACF 屬性 [coNtext_handle_serialize] 或 [coNtext_handle_noserialize] 只能套用至屬於內容控制碼的類型。<br/> 範例 IDL 檔案：<br/>
<pre class="syntax" data-space="preserve"><code>typedef /*[context_handle] */ void *PV;    //Note: PV is *not* a context handle.</code></pre>
範例 ACF 檔：<br/>
<pre class="syntax" data-space="preserve"><code>typedef [context_handle_serialize] PV;    //MIDL 2378</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2379"></span><span id="midl2379"></span><dl> <dt><strong>MIDL2379</strong></dt> </dl></td>
<td><dl> <dt><span id="The_compiler_reached_a_limit_for_a_format_string_representation._See_documentation_for_advice."></span><span id="the_compiler_reached_a_limit_for_a_format_string_representation._see_documentation_for_advice."></span><span id="THE_COMPILER_REACHED_A_LIMIT_FOR_A_FORMAT_STRING_REPRESENTATION._SEE_DOCUMENTATION_FOR_ADVICE."></span>編譯器已達到格式字串表示的限制。請參閱檔以取得建議。</dt> <dd> MIDL 編譯器的格式字串有 64 KB 的限制。 當 IDL 檔案包含其他 IDL 檔案時，通常會發生這個錯誤。 所有 include 語句所產生的複合 IDL 檔案超過封送處理引擎解譯器之類型表示表的限制。 請嘗試使用匯入指示詞，而不是 IDL 檔案中的 include 指示詞。 如需詳細資訊，請參閱匯 <a href="importing-system-header-files.md">入系統標頭檔</a>、 <a href="include.md"><strong>包含</strong></a>和匯 <a href="import.md"><strong>入</strong></a>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2380"></span><span id="midl2380"></span><dl> <dt><strong>MIDL2380</strong></dt> </dl></td>
<td><dl> <dt><span id="wire_format_may_be_incorrect__you_may_need_to_use_-ms_conf_struct__see_documentation_for_advice"></span><span id="WIRE_FORMAT_MAY_BE_INCORRECT__YOU_MAY_NEED_TO_USE_-MS_CONF_STRUCT__SEE_DOCUMENTATION_FOR_ADVICE"></span>電傳格式可能不正確，您可能需要使用-ms_conf_struct，請參閱檔中的建議</dt> <dd> MIDL 編譯器無法產生資料的 transmissible 格式。 取得此錯誤的一個常見方式是在複雜結構內定義 <strong>ms_conf_struct</strong> 。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2381"></span><span id="midl2381"></span><dl> <dt><strong>MIDL2381</strong></dt> </dl></td>
<td><dl> <dt><span id="a_stack_size_or_an_offset_bigger_than_64_K_limit._See_documentation_for_advice."></span><span id="a_stack_size_or_an_offset_bigger_than_64_k_limit._see_documentation_for_advice."></span><span id="A_STACK_SIZE_OR_AN_OFFSET_BIGGER_THAN_64_K_LIMIT._SEE_DOCUMENTATION_FOR_ADVICE."></span>堆疊大小或大於 64 K 限制的位移。請參閱檔以取得建議。</dt> <dd> 呼叫會產生大於 64 KB 的堆疊。 嘗試以較小的區塊傳遞資料。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2382"></span><span id="midl2382"></span><dl> <dt><strong>MIDL2382</strong></dt> </dl></td>
<td><dl> <dt><span id="an_interpreter_mode_forced_for_64-bit_platform_"></span><span id="AN_INTERPRETER_MODE_FORCED_FOR_64-BIT_PLATFORM_"></span>針對64位平臺強制執行解譯器模式 </dt> <dd> 64位平臺需要/Oicf 編譯模式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2383"></span><span id="midl2383"></span><dl> <dt><strong>MIDL2383</strong></dt> </dl></td>
<td><dl> <dt><span id="The_array_element_size_is_bigger_than_64_KB_limit."></span><span id="the_array_element_size_is_bigger_than_64_kb_limit."></span><span id="THE_ARRAY_ELEMENT_SIZE_IS_BIGGER_THAN_64_KB_LIMIT."></span>陣列元素大小大於 64 KB 的限制。</dt> <dd> 所有陣列元素的大小必須小於 64 KB。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2384"></span><span id="midl2384"></span><dl> <dt><strong>MIDL2384</strong></dt> </dl></td>
<td><dl> <dt><span id="there_can_be_only_one__Icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="there_can_be_only_one__icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="THERE_CAN_BE_ONLY_ONE__ICID__PARAMETER_IN_A_METHOD__AND_IT_SHOULD_BE_LAST_OR_SECOND_TO_LAST_IF_LAST_PARAMETER_HAS__RETVAL_"></span>方法中只能有一個 [Icid] 參數，且如果最後一個參數有 [retval]，它應該是最後一個或第二個</dt> <dd> 具有 [<a href="lcid.md"><strong>lcid</strong></a>] 屬性的參數必須發生在最後。 唯一的例外狀況是當有一個具有 [<a href="retval.md"><strong>retval</strong></a>] 屬性的參數時。 當兩者都發生時，參數清單中最後一個參數的第二個參數必須有 [ <strong>lcid</strong>] 屬性。 最後一個參數必須有 [<strong>retval</strong>] 屬性。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2385"></span><span id="midl2385"></span><dl> <dt><strong>MIDL2385</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_syntax_for_midl_pragma"></span><span id="INCORRECT_SYNTAX_FOR_MIDL_PRAGMA"></span>midl_pragma 的語法不正確</dt> <dd> MIDL 編譯器在 midl_pragma 語句中偵測到未知的語法錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2386"></span><span id="midl2386"></span><dl> <dt><strong>MIDL2386</strong></dt> </dl></td>
<td><dl> <dt><span id="__int3264_is_not_supported_in__osf_mode"></span><span id="__INT3264_IS_NOT_SUPPORTED_IN__OSF_MODE"></span>/osf 模式中不支援 __int3264</dt> <dd> 如果您需要使用 __int3264，請在/ms-ext 模式中進行編譯。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2387"></span><span id="midl2387"></span><dl> <dt><strong>MIDL2387</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_symbol_in_type_library"></span><span id="UNRESOLVED_SYMBOL_IN_TYPE_LIBRARY"></span>類型程式庫中未解析的符號</dt> <dd> 編譯器無法解析類型程式庫中的正式宣告或參考型別。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2388"></span><span id="midl2388"></span><dl> <dt><strong>MIDL2388</strong></dt> </dl></td>
<td><dl> <dt><span id="async_pipes_cannot_be_passed_by_value"></span><span id="ASYNC_PIPES_CANNOT_BE_PASSED_BY_VALUE"></span>無法以傳值方式傳遞非同步管道</dt> <dd> 非同步管道應以傳址或傳址方式傳遞。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2389"></span><span id="midl2389"></span><dl> <dt><strong>MIDL2389</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_offset_exceed_64-KB_limit_for_interpreted_procedures"></span><span id="parameter_offset_exceed_64-kb_limit_for_interpreted_procedures"></span><span id="PARAMETER_OFFSET_EXCEED_64-KB_LIMIT_FOR_INTERPRETED_PROCEDURES"></span>參數位移超過 64 KB 的解讀程式限制</dt> <dd> 此錯誤通常表示程式有太多參數。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2390"></span><span id="midl2390"></span><dl> <dt><strong>MIDL2390</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_array_element"></span><span id="INVALID_ARRAY_ELEMENT"></span>陣列元素無效</dt> <dd> 無法使用管道作為陣列元素。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2391"></span><span id="midl2391"></span><dl> <dt><strong>MIDL2391</strong></dt> </dl></td>
<td><dl> <dt><span id="dispinterface_members_must_be_methods__properties_or_interfaces"></span><span id="DISPINTERFACE_MEMBERS_MUST_BE_METHODS__PROPERTIES_OR_INTERFACES"></span>分派介面成員必須是方法、屬性或介面</dt> <dd> 分派介面不能包含類型定義、結構、列舉或等位。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2392"></span><span id="midl2392"></span><dl> <dt><strong>MIDL2392</strong></dt> </dl></td>
<td><dl> <dt><span id="_local__procedure_without__call_as_"></span><span id="_LOCAL__PROCEDURE_WITHOUT__CALL_AS_"></span>[local] 沒有 [call_as] 的程式</dt> <dd> 具有 [<a href="local.md"><strong>local</strong></a>] 屬性的物件程式也需要 [<a href="call-as.md"><strong>call_as</strong></a>] 屬性。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2393"></span><span id="midl2393"></span><dl> <dt><strong>MIDL2393</strong></dt> </dl></td>
<td><dl> <dt><span id="multi_dimensional_vector__switching_to__Oicf"></span><span id="multi_dimensional_vector__switching_to__oicf"></span><span id="MULTI_DIMENSIONAL_VECTOR__SWITCHING_TO__OICF"></span>多維度向量，切換至/Oicf</dt> <dd> <a href="-os.md"><strong>/Os</strong></a>優化模式不支援多維度 nonfixed 大小陣列。 編譯器已自動將此函式的優化模式切換為/<strong>Oicf</strong> 。 <br/> 您可以藉由在 MIDL 命令列上指定/<strong>Oicf</strong> ，或使用 IDL 檔案中的 <strong>midl_pragma</strong> 警告 (disable： 2393) 來變更編譯器模式，藉以全域隱藏這個警告。 您可以藉由將 [<strong>optimize (&quot; icf &quot;) </strong>] 屬性新增至 ACF 檔案中的函式，來變更個別函式的優化模式。<br/> 下列範例示範此警告：<br/>
<pre class="syntax" data-space="preserve"><code>void roo(long s1, [size_is(s1)] long a[][30];    //MIDL2393
void bar(long s1, long s2, [size_is(s1,s2) long **a);//MIDL2393</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2395"></span><span id="midl2395"></span><dl> <dt><strong>MIDL2395</strong></dt> </dl></td>
<td><dl> <dt><span id="type_or_construct_not_supported_in_a_library_block_because_Oleaut32.dll_support_for_64-KB_polymorphic_types_is_missing"></span><span id="type_or_construct_not_supported_in_a_library_block_because_oleaut32.dll_support_for_64-kb_polymorphic_types_is_missing"></span><span id="TYPE_OR_CONSTRUCT_NOT_SUPPORTED_IN_A_LIBRARY_BLOCK_BECAUSE_OLEAUT32.DLL_SUPPORT_FOR_64-KB_POLYMORPHIC_TYPES_IS_MISSING"></span>程式庫區塊中不支援類型或結構，因為缺少 64-KB 多型類型的 Oleaut32.dll 支援</dt> <dd> OLE automation 不支援多型類型 (例如 _int3264、INT_PTR 等) 。 這些類型在32位和64位平臺之間具有不相容的資料標記法。 在64位平臺上，遠端呼叫會在執行時間失敗。<br/>
<blockquote>
[!Note]<br />
請注意，在 Windows 2000 版本中，OLE Automation 會在執行時間轉換32位 TLB 資訊，以支援64位 TLB 檔案。 因此，MIDL 只支援32位的 TLB 產生。
</blockquote>
<br/> 如果使用 MIDL 來產生標頭檔， <a href="-notlb.md"><strong>/notlb</strong></a> 參數將會抑制 TLB 檔案的產生。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2396"></span><span id="midl2396"></span><dl> <dt><strong>MIDL2396</strong></dt> </dl></td>
<td><dl> <dt><span id="old_interpreter_code_being_generated_for_64b"></span><span id="OLD_INTERPRETER_CODE_BEING_GENERATED_FOR_64B"></span>針對64b 產生的舊解譯器程式碼</dt> <dd> 此錯誤已淘汰。 如果您看到此錯誤，請向 Microsoft 回報錯誤，以提供您的 IDL 檔案、ACF 檔案和完整 MIDL 命令列。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2397"></span><span id="midl2397"></span><dl> <dt><strong>MIDL2397</strong></dt> </dl></td>
<td><dl> <dt><span id="the_compiler_switch_is_not_supported_anymore"></span><span id="THE_COMPILER_SWITCH_IS_NOT_SUPPORTED_ANYMORE"></span>不再支援編譯器參數</dt> <dd> 不再支援指定的參數或參數。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2398"></span><span id="midl2398"></span><dl> <dt><strong>MIDL2398</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_execute_MIDL_engine"></span><span id="cannot_execute_midl_engine"></span><span id="CANNOT_EXECUTE_MIDL_ENGINE"></span>無法執行 MIDL 引擎</dt> <dd> 從 Windows 2000 版 (MIDL 版本 5.03.279) ，會使用兩個可執行檔來執行 MIDL 編譯器： Midl.exe (驅動程式) ，以及 Midlc.exe 編譯器引擎 (。 此錯誤表示 Midl.exe 無法啟動 Midlc.exe。 請確定 Midlc.exe 與 Midl.exe 位於相同的目錄中，而且它們是相同的版本。<br/> 此錯誤可能是因為複製 Midl.exe 但無法從最新的散發 Midlx.exe 所造成。 在不含任何參數的命令列上執行 <strong>midl</strong> 和/或 <strong>midlc</strong> ，以查看可執行檔的版本號碼。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2399"></span><span id="midl2399"></span><dl> <dt><strong>MIDL2399</strong></dt> </dl></td>
<td><dl> <dt><span id="bad_commands_from_driver"></span><span id="BAD_COMMANDS_FROM_DRIVER"></span>驅動程式中的命令錯誤</dt> <dd> 從 Windows 2000 版 (MIDL 版本 5.03.279) ，會使用兩個可執行檔來執行 MIDL 編譯器： Midl.exe (驅動程式) ，以及 Midlc.exe 編譯器引擎 (。 此錯誤表示用來將命令從 Midl.exe 傳遞至 Midlc.exe 的暫存檔案遺失或損毀。 請確定 Midlc.exe 與 Midl.exe 位於相同的目錄中，而且它們是相同的版本。<br/> 錯誤可能是因為嘗試直接執行 Midlc.exe，或從最新的散發套件中複製 Midl.exe 而不是 Midlc.exe 所造成。 在不含任何參數的命令列上執行 <strong>midl</strong> 和/或 <strong>midlc</strong> ，以查看可執行檔的版本號碼。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2400"></span><span id="midl2400"></span><dl> <dt><strong>MIDL2400</strong></dt> </dl></td>
<td><dl> <dt><span id="for_ole_automation__optional_parameters_should_be_VARIANT_or_VARIANT__"></span><span id="for_ole_automation__optional_parameters_should_be_variant_or_variant__"></span><span id="FOR_OLE_AUTOMATION__OPTIONAL_PARAMETERS_SHOULD_BE_VARIANT_OR_VARIANT__"></span>若為 ole automation，選擇性參數應為 VARIANT 或 VARIANT *</dt> <dd> OLE Automation 要求所有 [optional] 參數的類型都是 <strong>variant</strong> 或 <strong>variant *</strong>。<br/> 在 OLE automation 中，使用非變異參數可能會導致呼叫在執行時間失敗，或是傳遞 [<a href="optional.md"><strong>optional</strong></a>] 參數未定義的資料。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2401"></span><span id="midl2401"></span><dl> <dt><strong>MIDL2401</strong></dt> </dl></td>
<td><dl> <dt><span id="_defaultvalue__is_applied_to_a_non-VARIANT_and__optional_._Please_remove__optional_"></span><span id="_defaultvalue__is_applied_to_a_non-variant_and__optional_._please_remove__optional_"></span><span id="_DEFAULTVALUE__IS_APPLIED_TO_A_NON-VARIANT_AND__OPTIONAL_._PLEASE_REMOVE__OPTIONAL_"></span>[defaultvalue] 套用至非變異和 [選擇性]。請移除 [選用]</dt> <dd> [<a href="defaultvalue.md"><strong>Defaultvalue</strong></a>] 屬性意指 [<a href="optional.md"><strong>optional</strong></a>]。 [ <strong>Optional</strong>] 屬性不是必要的。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2402"></span><span id="midl2402"></span><dl> <dt><strong>MIDL2402</strong></dt> </dl></td>
<td><dl> <dt><span id="_optional__attribute_is_inapplicable_outside_of_a_library_block"></span><span id="_OPTIONAL__ATTRIBUTE_IS_INAPPLICABLE_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>[optional] 屬性是在程式庫區塊之外不適用</dt> <dd> [ <a href="optional.md"><strong>Optional</strong></a>] 屬性隱含的功能不適用於程式庫區塊以外介面所產生的 proxy。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2403"></span><span id="midl2403"></span><dl> <dt><strong>MIDL2403</strong></dt> </dl></td>
<td><dl> <dt><span id="The_data_type_of_the__Icid__parameter_must_be_long"></span><span id="the_data_type_of_the__icid__parameter_must_be_long"></span><span id="THE_DATA_TYPE_OF_THE__ICID__PARAMETER_MUST_BE_LONG"></span>[Icid] 參數的資料類型必須是 long</dt> <dd> OLE Automation 要求具有 [<strong>Icid</strong>] 屬性的參數必須是 <a href="long.md"><strong>long</strong></a>類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2404"></span><span id="midl2404"></span><dl> <dt><strong>MIDL2404</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput____propget__or__propref__can_t_have_more_than_one_required_parameter_after__optional__one"></span><span id="PROCEDURES_WITH__PROPPUT____PROPGET__OR__PROPREF__CAN_T_HAVE_MORE_THAN_ONE_REQUIRED_PARAMETER_AFTER__OPTIONAL__ONE"></span>具有 [propput]、[propget] 或 [propref] 的程式在 [optional] 之後不能有一個以上的必要參數</dt> <dd> 使用 [<a href="propput.md"><strong>propput</strong></a>]、[<a href="propget.md"><strong>propget</strong></a>] 或 [ <a href="propputref.md"><strong>propputref</strong></a>] 時，不能有一個以上的參數<a href="optional.md"><strong>沒有 [選擇性</strong></a><strong>]。</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2405"></span><span id="midl2405"></span><dl> <dt><strong>MIDL2405</strong></dt> </dl></td>
<td><dl> <dt><span id="_comm_status__or__fault_status__with_pickling_requires_-Oicf"></span><span id="_comm_status__or__fault_status__with_pickling_requires_-oicf"></span><span id="_COMM_STATUS__OR__FAULT_STATUS__WITH_PICKLING_REQUIRES_-OICF"></span>[comm_status] 或 [fault_status] with pickling 需要-Oicf</dt> <dd> 舊的<strong>Oi</strong> 優化模式不支援使用 [ <a href="comm-status.md"><strong>comm_status</strong></a>] 或 [ <a href="fault-status.md"><strong>fault_status</strong></a>] 搭配 pickling (也就是使用 [ <a href="encode.md"><strong>編碼</strong></a>] 和/ <a href="decode.md"><strong>或 [解碼</strong></a>] ) 的程式或參數。<br/> 您可以在 MIDL 命令列上指定-<strong>Oicf</strong> 或針對個別函式，藉由在 ACF 檔案中將 [optimize (&quot; icf： ) ] 屬性新增至函式，來全域隱藏這個警告。<br/> 一般情況下，建議使用-<strong>Oicf</strong> 優化模式，而不是透過<strong>Oi</strong> 模式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2406"></span><span id="midl2406"></span><dl> <dt><strong>MIDL2406</strong></dt> </dl></td>
<td><dl> <dt><span id="midl_driver_and_compiler_version_mismatch"></span><span id="MIDL_DRIVER_AND_COMPILER_VERSION_MISMATCH"></span>midl 驅動程式和編譯器版本不符</dt> <dd> 從 Windows 2000 版本 (MIDL 版本 5.03.279) 會使用兩個可執行檔來執行 MIDL 編譯器： Midl.exe (驅動程式) ，以及 Midlc.exe 編譯器引擎 (。 此錯誤指出 Midl.exe 的版本不符合 Midlc.exe 的版本。<br/> 此錯誤可能是因為複製 Midl.exe 但無法從最新的散發 Midlc.exe 所造成。 在不含任何參數的命令列上執行 <strong>midl</strong> 和/或 <strong>midlc</strong> ，以查看可執行檔的版本號碼。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2407"></span><span id="midl2407"></span><dl> <dt><strong>MIDL2407</strong></dt> </dl></td>
<td><dl> <dt><span id="no_intermediate_file_specified__use_Midl.exe"></span><span id="no_intermediate_file_specified__use_midl.exe"></span><span id="NO_INTERMEDIATE_FILE_SPECIFIED__USE_MIDL.EXE"></span>未指定中繼檔案：使用 Midl.exe</dt> <dd> 從 Windows 2000 版 (MIDL 版本 5.03.279) ，會使用兩個可執行檔來執行 MIDL 編譯器： Midl.exe (驅動程式) ，以及 Midlc.exe 編譯器引擎 (。 此錯誤表示 Midlc.exe 是直接執行，而不是使用 Midl.exe。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2408"></span><span id="midl2408"></span><dl> <dt><strong>MIDL2408</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_parameter_in_a_procedure"></span><span id="PROCESSING_PROBLEM_WITH_A_PARAMETER_IN_A_PROCEDURE"></span>進程中的參數處理問題</dt> <dd> 從 TLB 匯入資料時，以及當程式具有無效參數時，可能會看到此錯誤。 <br/> 如果您看到此錯誤，請向 Microsoft 回報錯誤。 指定您的 IDL 檔案、ACF 檔、TLB 檔案和完整 MIDL 命令列。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2409"></span><span id="midl2409"></span><dl> <dt><strong>MIDL2409</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_field_in_a_structure"></span><span id="PROCESSING_PROBLEM_WITH_A_FIELD_IN_A_STRUCTURE"></span>處理結構中的欄位時發生問題</dt> <dd> 從 TLB 匯入資料時，以及當結構的結構或等位欄位無效時，可能會出現此錯誤。<br/> 如果您看到此錯誤，請向 Microsoft 回報錯誤。 指定您的 IDL 檔案、ACF 檔、TLB 檔案和完整 MIDL 命令列。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2410"></span><span id="midl2410"></span><dl> <dt><strong>MIDL2410</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_FORMAT_STRING_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>偵測到內部編譯器不一致：格式字串位移無效。如需詳細資訊，請參閱檔。</dt> <dd> MIDL 編譯器偵測到其內部資料結構中的值無效。 這可能是因為遞迴或編譯器違反本身內部資料的表示限制所造成。 若要找出及/或解決此問題，請嘗試簡化 IDL 檔案。 若要這麼做，您可以簡化複雜的參數和遞迴資料結構，或藉由分割來使 IDL 檔案變得更小。 此訊息可能伴隨著診斷輸出，並提供問題的其他相關資訊。<br/> 如果您看到此錯誤，請向 Microsoft 回報錯誤。 指定 IDL 檔案、ACF 檔、完整 MIDL 命令列，以及診斷輸出（如果有的話）。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2411"></span><span id="midl2411"></span><dl> <dt><strong>MIDL2411</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_TYPE_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>偵測到內部編譯器不一致：類型位移無效。如需詳細資訊，請參閱檔。</dt> <dd> MIDL 編譯器偵測到其內部資料結構中的值無效。 這可能是由遞迴結構或編譯器違反本身內部資料的表示限制所造成。 若要找出並（或）解決此問題，請嘗試簡化 IDL 檔案。 若要這麼做，您可以簡化複雜的參數和遞迴資料結構，或是藉由分割來使 IDL 檔案變得更小。 此訊息可能伴隨著診斷輸出，並提供問題的其他相關資訊。<br/> 如果您看到此錯誤，請向 Microsoft 回報錯誤。 指定 IDL 檔案、ACF 檔、完整 MIDL 命令列，以及診斷輸出（如果有的話）。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2412"></span><span id="midl2412"></span><dl> <dt><strong>MIDL2412</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAY_roo__syntax_is_not_supported_outside_of_the_library_block__use_LPSAFEARRAY_for_proxy"></span><span id="safearray_roo__syntax_is_not_supported_outside_of_the_library_block__use_lpsafearray_for_proxy"></span><span id="SAFEARRAY_ROO__SYNTAX_IS_NOT_SUPPORTED_OUTSIDE_OF_THE_LIBRARY_BLOCK__USE_LPSAFEARRAY_FOR_PROXY"></span>無法在程式庫區塊外部使用 SAFEARRAY (roo) 語法，請對 proxy 使用 LPSAFEARRAY</dt> <dd> 在程式庫區塊外部不允許明確類型的 Safearray。 請改用 LPSAFEARRAY。<br/> 下列範例示範此錯誤：<br/>
<pre class="syntax" data-space="preserve"><code>void roo(SAFEARRAY(long) *a); //MIDL2412 when outside a library block
void roo(LPSAFEAEEAY a);         //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2413"></span><span id="midl2413"></span><dl> <dt><strong>MIDL2413</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_fields_are_not_supported"></span><span id="BIT_FIELDS_ARE_NOT_SUPPORTED"></span>不支援位欄位</dt> <dd> MIDL 不支援 C 樣式位欄位。 這適用于 proxy 產生以及 TLB 產生。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2414"></span><span id="midl2414"></span><dl> <dt><strong>MIDL2414</strong></dt> </dl></td>
<td><dl> <dt><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-Oicf__using_-OI"></span><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-oicf__using_-oi"></span><span id="FLOATING_POINT_OR_COMPLEX_RETURN_TYPES_WITH__DECODE__ARE_NOT_SUPPORTED_IN_-OICF__USING_-OI"></span>使用-OI 的 Oicf 中不支援具有 [解碼] 的浮點或複雜傳回類型</dt> <dd> Oicf 樣式 pickling 不支援具有浮點或結構/等位傳回類型的程式。 32位的解決方式是在使用 [編碼] 和/或 [解碼] ) 序列化資料 (時，使用-Oi 優化模式。 不過，由於舊的 Oi 樣式解譯器和 pickling 支援已預定在 Windows 2000 版本之後淘汰，因此強烈建議您使用指標作為此問題的解決方式。 另請注意，通常會將介面方法變更為使用 [out，ref] 指標，而不是傳回值，而導致問題在網路上完全相容，而且可以輕鬆地隱藏在應用層。 <br/> 在 MIDL 命令列上指定-Oi 或針對個別函式，藉由在 ACF 檔案的函式中新增 [optimize (&quot; i &quot;) ] 屬性，即可全域隱藏這個警告。<br/> 下列範例示範此問題：<br/> roo .idl： <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
roo. acf： <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
解決這項限制的其中一個方法是傳遞 [out] 參數來保存結果，而不是使用傳回值：<br/> roo .idl： <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer</code></pre>
roo. acf： <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
如先前所述，上述解決方案不只適用于新介面，也適用于舊介面的解決方法。 新輸出引數的網路標記法與傳回 &quot; &quot; 值相同， (請注意 void 作為新的傳回值) 。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2415"></span><span id="midl2415"></span><dl> <dt><strong>MIDL2415</strong></dt> </dl></td>
<td><dl> <dt><span id="the_return_type_is_not_supported_for_64-bit_when_using__decode_"></span><span id="THE_RETURN_TYPE_IS_NOT_SUPPORTED_FOR_64-BIT_WHEN_USING__DECODE_"></span>使用 [解碼] 時，64位不支援傳回類型</dt> <dd> 使用 [ <a href="encode.md"><strong>編碼</strong></a> <a href="decode.md"><strong>] 和/或 [解碼</strong></a>] ) 執行資料序列化 (時，64位模式不支援具有浮點或結構/等位傳回類型的程式。 這與舊版樣式-Oi 解譯器和64位平臺上不支援的資料序列化程式有關。 如需詳細資訊，請參閱 MIDL2414 的描述。 <br/> 下列範例示範此錯誤：<br/> roo .idl： <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
roo. acf： <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
建議您將下列各項作為新舊介面的解決方式。 使用 [out] 參數來保存結果，而不是使用傳回值：<br/> roo .idl： <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer.</code></pre>
roo. acf： <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
請注意，在網路上，此解決方案完全是回溯相容的，因為 [ref，out] 指標或雙精度的網路標記法與雙精度相同。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2416"></span><span id="midl2416"></span><dl> <dt><strong>MIDL2416</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_contain_a_full_pointer_for_either__wire_marshal__or__user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_CONTAIN_A_FULL_POINTER_FOR_EITHER__WIRE_MARSHAL__OR__USER_MARSHAL_"></span>傳送的型別不能包含 [wire_marshal] 或 [user_marshal] 的完整指標</dt> <dd> 具有 [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] 或 [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] 屬性的類型，不能包含完整的 ( [ <strong>ptr</strong>] ) 指標。 請改用 [ <a href="unique.md"><strong>unique</strong></a>] 或 [ <a href="ref.md"><strong>ref</strong></a>]。<br/> 下列範例示範此錯誤：<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
    [ptr] long *a;    //Should use [ref] or [unique] instead
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2:
void roo(st2 *s);    //MIDL2416</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2417"></span><span id="midl2417"></span><dl> <dt><strong>MIDL2417</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_must_either_be_a_pointer_or_have_a_constant_size_for__wire_marshal__and__user_marshal_"></span><span id="TRANSMITTED_TYPE_MUST_EITHER_BE_A_POINTER_OR_HAVE_A_CONSTANT_SIZE_FOR__WIRE_MARSHAL__AND__USER_MARSHAL_"></span>傳輸的類型必須是指標，或具有 [wire_marshal] 和 [user_marshal] 的常數大小</dt> <dd> 具有 [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] 或 [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] 屬性的最上層類型，在編譯時期必須有妥善定義的大小。 它們不能是或包含一致或不同大小的陣列。<br/> 下列範例示範此錯誤：<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2;
void roo(st2 *s);        //MIDL2417</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2418"></span><span id="midl2418"></span><dl> <dt><strong>MIDL2418</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propget__must_have_at_least_one_parameter_or_a_return_value"></span><span id="PROCEDURES_WITH__PROPGET__MUST_HAVE_AT_LEAST_ONE_PARAMETER_OR_A_RETURN_VALUE"></span>具有 [propget] 的程式必須至少有一個參數或傳回值</dt> <dd> 具有 [propget] 屬性的程式必須有一些傳回屬性值的方法。 它們必須至少有一個 [<a href="-out.md"><strong>out</strong></a>] 參數或傳回值。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2461"></span><span id="midl2461"></span><dl> <dt><strong>MIDL2461</strong></dt> </dl></td>
<td><dl> <dt><span id="The__readonly__attribute_was_applied_at_the_method_level."></span><span id="the__readonly__attribute_was_applied_at_the_method_level."></span><span id="THE__READONLY__ATTRIBUTE_WAS_APPLIED_AT_THE_METHOD_LEVEL."></span>[Readonly] 屬性是在方法層級套用。</dt> <dd> [Readonly] 屬性只能套用於參數層級。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2465"></span><span id="midl2465"></span><dl> <dt><strong>MIDL2465</strong></dt> </dl></td>
<td><dl> <dt><span id="Structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="STRUCTURES_CONTAINING_CONFORMANT_ARRAYS_MUST_BE_PASSED_BY_REFERENCE"></span>包含符合標準陣列的結構必須以傳址方式傳遞</dt> <dd> RPC 中的最上層參數必須在編譯時期具有妥善定義的大小。 它們不能是，也不能包含一致或不同大小的陣列。 此外，使用者無法編碼/解碼沒有妥善定義大小的型別。 應用程式必須以傳址方式傳遞符合結構/一致的不同結構。<br/> 下列範例示範此錯誤：<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
void roo(st1 s);        //MIDL2465
 
on .acf file
typedef [encode,decode] st1; //MIDL2465</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL9008"></span><span id="midl9008"></span><dl> <dt><strong>MIDL9008</strong></dt> </dl></td>
<td><dl> <dt><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._See_documentation_for_a_workaround."></span><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._see_documentation_for_a_workaround."></span><span id="_INTERNAL_COMPILER_PROBLEM__SYSTEM_ERROR_CODE__-_THE_COMPILER_CANNOT_CONTINUE_FOR_AN_UNKNOWN_REASON._SEE_DOCUMENTATION_FOR_A_WORKAROUND."></span> 編譯器內部問題 <system error code> - ：編譯器無法繼續，原因不明。 請參閱檔以瞭解因應措施。</dt> <dd> 編譯器無法繼續，且錯誤的原因不明。 十六進位錯誤號碼是系統錯誤識別碼。 編譯可能因為外部問題而失敗，例如記憶體不足的狀況。 在這種情況下，您可以在 Winerror.h 中找到詳細資訊。 <br/> 有兩種情況通常會產生此錯誤：<br/>
<ul>
<li>在 IDL 檔案中偵測到錯誤之後，MIDL 編譯器無法復原。 如果 MIDL 傳回任何關於 IDL 檔案的錯誤訊息，請嘗試修正它們並重新編譯。 如果沒有任何錯誤訊息，編譯器可能會在報告錯誤之前失敗。 在報告內部編譯器錯誤的行上尋找語法錯誤。</li>
<li>MIDL 編譯器無法在指定的優化選項下產生正確的程式碼。 請嘗試變更編譯器模式、在混合模式優化 (/<a href="-os.md"><strong>Os</strong></a>) 中進行編譯，或移除所有優化。 或者，使用/NO_FORMAT_OPT 旗標來重新編譯，以抑制 MIDL 的程式和類型描述元的預設優化。</li>
</ul>
偶而發生此錯誤的原因是 IDL 檔案正確，且未使用任何優化選項。 如果發生這種情況，請嘗試藉由移除任何最近的修改、簡化或重新排列資料類型、變更原型，或開始將 IDL 檔案的部分標記為批註，以找出問題代碼，以重寫報告錯誤的區域中的程式碼區段。<br/> 如果這些選項都無法運作，或是您認為問題可能與 Midl.exe 中的錯誤有關，請通知 Microsoft，提供所有相關的詳細資料。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

