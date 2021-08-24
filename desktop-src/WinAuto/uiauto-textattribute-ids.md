---
title: 'Text 屬性識別碼 (Uiautomationclient.dll .h) '
description: 本主題說明用來識別 Microsoft 消費者介面自動化文字範圍之文字屬性的已命名常數。
ms.assetid: 67d86817-6a3f-4047-88d9-34f33f52a563
topic_type:
- apiref
api_name:
- UIA_AfterParagraphSpacingAttributeId
- UIA_AnimationStyleAttributeId
- UIA_AnnotationObjectsAttributeId
- UIA_AnnotationTypesAttributeId
- UIA_BackgroundColorAttributeId
- UIA_BeforeParagraphSpacingAttributeId
- UIA_BulletStyleAttributeId
- UIA_CapStyleAttributeId
- UIA_CaretBidiModeAttributeId
- UIA_CaretPositionAttributeId
- UIA_CultureAttributeId
- UIA_FontNameAttributeId
- UIA_FontSizeAttributeId
- UIA_FontWeightAttributeId
- UIA_ForegroundColorAttributeId
- UIA_HorizontalTextAlignmentAttributeId
- UIA_IndentationFirstLineAttributeId
- UIA_IndentationLeadingAttributeId
- UIA_IndentationTrailingAttributeId
- UIA_IsActiveAttributeId
- UIA_IsHiddenAttributeId
- UIA_IsItalicAttributeId
- UIA_IsReadOnlyAttributeId
- UIA_IsSubscriptAttributeId
- UIA_IsSuperscriptAttributeId
- UIA_LineSpacingAttributeId
- UIA_LinkAttributeId
- UIA_MarginBottomAttributeId
- UIA_MarginLeadingAttributeId
- UIA_MarginTopAttributeId
- UIA_MarginTrailingAttributeId
- UIA_OutlineStylesAttributeId
- UIA_OverlineColorAttributeId
- UIA_OverlineStyleAttributeId
- UIA_SelectionActiveEndAttributeId
- UIA_StrikethroughColorAttributeId
- UIA_StrikethroughStyleAttributeId
- UIA_StyleIdAttributeId
- UIA_StyleNameAttributeId
- UIA_TabsAttributeId
- UIA_TextFlowDirectionsAttributeId
- UIA_UnderlineColorAttributeId
- UIA_UnderlineStyleAttributeId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e84ba97b387097233b7a838fbe192585b9676b6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468765"
---
# <a name="text-attribute-identifiers"></a>Text 屬性識別碼

本主題說明用來識別 Microsoft 消費者介面自動化文字範圍之文字屬性的已命名常數。 這些常數會搭配下列方法使用：

-   [**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
-   [**ITextRangeProvider：： GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
-   [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
-   [**IUIAutomationTextRange：： GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)




| 常數/值 | Description | 
|----------------|-------------|
| <span id="UIA_AfterParagraphSpacingAttributeId"></span><span id="uia_afterparagraphspacingattributeid"></span><span id="UIA_AFTERPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_AfterParagraphSpacingAttributeId</strong></dt><dt>40042</dt></dl> | 識別 <strong>AfterParagraphSpacing</strong> 文字屬性，此屬性會指定段落後間距的大小。<br /> Variant 類型： <strong>VT_R8</strong><br /> 預設值：0<br /> | 
| <span id="UIA_AnimationStyleAttributeId"></span><span id="uia_animationstyleattributeid"></span><span id="UIA_ANIMATIONSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_AnimationStyleAttributeId</strong></dt><dt>40000</dt></dl> | 識別 <strong>AnimationStyle</strong> 文字屬性，指定套用至文字的動畫類型。 這個屬性會指定為 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"><strong>AnimationStyle</strong></a> 列舉型別中的值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"> <strong>AnimationStyle_None</strong></a><br /> | 
| <span id="UIA_AnnotationObjectsAttributeId"></span><span id="uia_annotationobjectsattributeid"></span><span id="UIA_ANNOTATIONOBJECTSATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationObjectsAttributeId</strong></dt><dt>40032</dt></dl> | 識別 <strong>AnnotationObjects</strong> 文字屬性，此屬性會維護 <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2"><strong>IUIAutomationElement2</strong></a> 介面的陣列，這個屬性會針對目前文字範圍中的每個專案執行 <a href="uiauto-implementingannotation.md">批註</a> 控制項模式。 每個元素也可以視需要執行其他控制項模式來描述批註。 例如，批註也會支援 <a href="uiauto-implementingtextandtextrange.md">文字</a> 控制項模式。 從 Windows 8 開始支援。<br /> Variant 類型： <strong>VT_UNKNOWN</strong><br /> 預設值：空陣列 <br /> | 
| <span id="UIA_AnnotationTypesAttributeId"></span><span id="uia_annotationtypesattributeid"></span><span id="UIA_ANNOTATIONTYPESATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationTypesAttributeId</strong></dt><dt>40031</dt></dl> | 識別 <strong>AnnotationTypes</strong> 文字屬性，此屬性會維護文字範圍的注釋類型識別碼清單。 如需可能值的清單，請參閱 <a href="uiauto-annotation-type-identifiers.md"><strong>批註類型識別碼</strong></a>。 從 Windows 8 開始支援。<br /> Variant 類型： <strong>VT_ARRAY</strong> | <strong>VT_I4</strong><br /> 預設值：空陣列 <br /> | 
| <span id="UIA_BackgroundColorAttributeId"></span><span id="uia_backgroundcolorattributeid"></span><span id="UIA_BACKGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_BackgroundColorAttributeId</strong></dt><dt>40001</dt></dl> | 識別 <strong>BackgroundColor</strong> 文字屬性，此屬性會指定文字的背景色彩。 這個屬性會指定為 <a href="/windows/win32/gdi/colorref">COLORREF</a>;用來指定 RGB 或 RGBA 色彩的32位值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值：0 <br /> | 
| <span id="UIA_BeforeParagraphSpacingAttributeId"></span><span id="uia_beforeparagraphspacingattributeid"></span><span id="UIA_BEFOREPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_BeforeParagraphSpacingAttributeId</strong></dt><dt>40041</dt></dl> | 識別 <strong>BeforeParagraphSpacing</strong> 文字屬性，此屬性會指定段落之前的間距大小。<br /> Variant 類型： <strong>VT_R8</strong><br /> 預設值：0<br /> | 
| <span id="UIA_BulletStyleAttributeId"></span><span id="uia_bulletstyleattributeid"></span><span id="UIA_BULLETSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_BulletStyleAttributeId</strong></dt><dt>40002</dt></dl> | 識別 <strong>BulletStyle</strong> 文字屬性，此屬性會指定文字範圍中使用的專案符號樣式。 這個屬性會指定為 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"><strong>BulletStyle</strong></a> 列舉型別中的值。<br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"> <strong>BulletStyle_None</strong></a><br /> | 
| <span id="UIA_CapStyleAttributeId"></span><span id="uia_capstyleattributeid"></span><span id="UIA_CAPSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_CapStyleAttributeId</strong></dt><dt>40003</dt></dl> | 識別 <strong>CapStyle</strong> 文字屬性，此屬性會指定文字的大小寫樣式。 這個屬性會指定為 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"><strong>CapStyle</strong></a> 列舉型別中的值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"> <strong>CapStyle_None</strong></a><br /> | 
| <span id="UIA_CaretBidiModeAttributeId"></span><span id="uia_caretbidimodeattributeid"></span><span id="UIA_CARETBIDIMODEATTRIBUTEID"></span><dl><dt><strong>UIA_CaretBidiModeAttributeId</strong></dt><dt>40039</dt></dl> | 識別 <strong>CaretBidiMode</strong> 文字屬性，指出文字範圍中的文字流動方向。 這個屬性會指定為 <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"><strong>CaretBidiMode</strong></a> 列舉型別中的值。 從 Windows 8 開始支援。<br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"> <strong>CaretBidiMode_LTR</strong></a><br /> | 
| <span id="UIA_CaretPositionAttributeId"></span><span id="uia_caretpositionattributeid"></span><span id="UIA_CARETPOSITIONATTRIBUTEID"></span><dl><dt><strong>UIA_CaretPositionAttributeId</strong></dt><dt>40038</dt></dl> | 識別 <strong>CaretPosition</strong> 文字屬性，指出插入號是否位於文字範圍中的文字行的開頭或結尾。 這個屬性會指定為 <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"><strong>CaretPosition</strong></a> 列舉型別中的值。 從 Windows 8 開始支援。<br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"> <strong>CaretPosition_Unknown</strong></a><br /> | 
| <span id="UIA_CultureAttributeId"></span><span id="uia_cultureattributeid"></span><span id="UIA_CULTUREATTRIBUTEID"></span><dl><dt><strong>UIA_CultureAttributeId</strong></dt><dt>40004</dt></dl> | 識別 <strong>文化</strong> 特性文字屬性，指定依地區設定識別碼 (LCID) 的文字地區設定。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值：應用程式 UI 的地區設定<br /> | 
| <span id="UIA_FontNameAttributeId"></span><span id="uia_fontnameattributeid"></span><span id="UIA_FONTNAMEATTRIBUTEID"></span><dl><dt><strong>UIA_FontNameAttributeId</strong></dt><dt>40005</dt></dl> | 識別 <strong>FontName</strong> 文字屬性，此屬性會指定字型的名稱。 範例：「Arial 黑色」;「Arial 窄」。 字型名稱字串未當地語系化。 <br /> Variant 類型： <strong>VT_BSTR</strong><br /> 預設值：空字串<br /> | 
| <span id="UIA_FontSizeAttributeId"></span><span id="uia_fontsizeattributeid"></span><span id="UIA_FONTSIZEATTRIBUTEID"></span><dl><dt><strong>UIA_FontSizeAttributeId</strong></dt><dt>40006</dt></dl> | 識別 <strong>FontSize</strong> 文字屬性，此屬性會指定字型的點大小。 <br /> Variant 類型： <strong>VT_R8</strong><br /> 預設值：0<br /> | 
| <span id="UIA_FontWeightAttributeId"></span><span id="uia_fontweightattributeid"></span><span id="UIA_FONTWEIGHTATTRIBUTEID"></span><dl><dt><strong>UIA_FontWeightAttributeId</strong></dt><dt>40007</dt></dl> | 識別 <strong>FontWeight</strong> 文字屬性，此屬性會指定字型的相對筆劃、粗細或粗細。 <strong>FontWeight</strong>屬性會在 GDI <a href="/windows/win32/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>結構的<strong>lfWeight</strong>成員和相關標準之後建立模型，而且可以是下列其中一個值：<ul><li>0 = <strong>DontCare</strong></li><li>100 = <strong>精簡</strong></li><li>200 = <strong>特細</strong> 或 <strong>超細</strong></li><li>300 = <strong>淺色</strong></li><li>400 = <strong>一般</strong> 或 <strong>一般</strong></li><li>500 = <strong>中</strong></li><li>600 = <strong>SemiBold</strong></li><li>700 = <strong>粗體</strong></li><li>800 = <strong>ExtraBold</strong> 或 <strong>特粗</strong></li><li>900 = <strong>重型</strong> 或 <strong>黑色</strong></li></ul><br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值：0<br /> | 
| <span id="UIA_ForegroundColorAttributeId"></span><span id="uia_foregroundcolorattributeid"></span><span id="UIA_FOREGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_ForegroundColorAttributeId</strong></dt><dt>40008</dt></dl> | 識別 <strong>ForegroundColor</strong> 文字屬性，此屬性會指定文字的前景色彩。 這個屬性會指定為 <a href="/windows/win32/gdi/colorref">COLORREF</a>，這是用來指定 RGB 或 RGBA 色彩的32位值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值：0<br /> | 
| <span id="UIA_HorizontalTextAlignmentAttributeId"></span><span id="uia_horizontaltextalignmentattributeid"></span><span id="UIA_HORIZONTALTEXTALIGNMENTATTRIBUTEID"></span><dl><dt><strong>UIA_HorizontalTextAlignmentAttributeId</strong></dt><dt>40009</dt></dl> | 識別 <strong>HorizontalTextAlignment</strong> 文字屬性，指定文字如何水準對齊。 這個屬性會指定為 <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"><strong>HorizontalTextAlignmentEnum</strong></a> 列舉型別中的值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"> <strong>HorizontalTextAlignment_Left</strong></a><br /> | 
| <span id="UIA_IndentationFirstLineAttributeId"></span><span id="uia_indentationfirstlineattributeid"></span><span id="UIA_INDENTATIONFIRSTLINEATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationFirstLineAttributeId</strong></dt><dt>40010</dt></dl> | 識別 <strong>IndentationFirstLine</strong> 文字屬性，指定要將段落的第一行縮排的距離（以點為單位）。 <br /> Variant 類型： <strong>VT_R8</strong><br /> 預設值：0<br /> | 
| <span id="UIA_IndentationLeadingAttributeId"></span><span id="uia_indentationleadingattributeid"></span><span id="UIA_INDENTATIONLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationLeadingAttributeId</strong></dt><dt>40011</dt></dl> | 識別 <strong>IndentationLeading</strong> 文字屬性，它會指定前置縮排（以點為單位）。 <br /> Variant 類型： <strong>VT_R8</strong><br /> 預設值：0<br /> | 
| <span id="UIA_IndentationTrailingAttributeId"></span><span id="uia_indentationtrailingattributeid"></span><span id="UIA_INDENTATIONTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationTrailingAttributeId</strong></dt><dt>40012</dt></dl> | 識別 <strong>IndentationTrailing</strong> 文字屬性，指定尾端的縮排（以點為單位）。 <br /> Variant 類型： <strong>VT_R8</strong><br /> 預設值：0<br /> | 
| <span id="UIA_IsActiveAttributeId"></span><span id="uia_isactiveattributeid"></span><span id="UIA_ISACTIVEATTRIBUTEID"></span><dl><dt><strong>UIA_IsActiveAttributeId</strong></dt><dt>40036</dt></dl> | 識別 <strong>IsActive</strong> 文字屬性，指出包含文字範圍的控制項是否有鍵盤焦點 (<strong>TRUE</strong>) 或不 (<strong>FALSE</strong>) 。 從 Windows 8 開始支援。<br /> Variant 類型： <strong>VT_BOOL</strong><br /> 預設值： <strong>FALSE</strong><br /> | 
| <span id="UIA_IsHiddenAttributeId"></span><span id="uia_ishiddenattributeid"></span><span id="UIA_ISHIDDENATTRIBUTEID"></span><dl><dt><strong>UIA_IsHiddenAttributeId</strong></dt><dt>40013</dt></dl> | 識別 <strong>IsHidden</strong> 文字屬性，指出文字是否隱藏 (<strong>TRUE</strong>) 或可見 (<strong>FALSE</strong>) 。 <br /> Variant 類型： <strong>VT_BOOL</strong><br /> 預設值： <strong>FALSE</strong><br /> | 
| <span id="UIA_IsItalicAttributeId"></span><span id="uia_isitalicattributeid"></span><span id="UIA_ISITALICATTRIBUTEID"></span><dl><dt><strong>UIA_IsItalicAttributeId</strong></dt><dt>40014</dt></dl> | 識別 <strong>IsItalic</strong> 文字屬性，指出文字是否為斜體 (<strong>TRUE</strong>) 或不 (<strong>FALSE</strong>) 。 <br /> Variant 類型： <strong>VT_BOOL</strong><br /> 預設值： <strong>FALSE</strong><br /> | 
| <span id="UIA_IsReadOnlyAttributeId"></span><span id="uia_isreadonlyattributeid"></span><span id="UIA_ISREADONLYATTRIBUTEID"></span><dl><dt><strong>UIA_IsReadOnlyAttributeId</strong></dt><dt>40015</dt></dl> | 識別 <strong>IsReadOnly</strong> 文字屬性，指出文字是否為唯讀 (<strong>TRUE</strong>) 或可 (<strong>FALSE</strong>) 修改。 <br /> Variant 類型： <strong>VT_BOOL</strong><br /> 預設值： <strong>FALSE</strong><br /> | 
| <span id="UIA_IsSubscriptAttributeId"></span><span id="uia_issubscriptattributeid"></span><span id="UIA_ISSUBSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSubscriptAttributeId</strong></dt><dt>40016</dt></dl> | 識別 <strong>IsSubscript</strong> 文字屬性，指出文字是否為 (<strong>TRUE</strong>) 的標值，或不 (<strong>FALSE</strong>) 。 <br /> Variant 類型： <strong>VT_BOOL</strong><br /> 預設值： <strong>FALSE</strong><br /> | 
| <span id="UIA_IsSuperscriptAttributeId"></span><span id="uia_issuperscriptattributeid"></span><span id="UIA_ISSUPERSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSuperscriptAttributeId</strong></dt><dt>40017</dt></dl> | 識別 <strong>IsSuperscript</strong> 文字屬性，指出文字是否為 (<strong>TRUE</strong>) 的標值，或不 (<strong>FALSE</strong>) 。 <br /> Variant 類型： <strong>VT_BOOL</strong><br /> 預設值： <strong>FALSE</strong><br /> | 
| <span id="UIA_LineSpacingAttributeId"></span><span id="uia_linespacingattributeid"></span><span id="UIA_LINESPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_LineSpacingAttributeId</strong></dt><dt>40040</dt></dl> | 識別 <strong>LineSpacing</strong> 文字屬性，此屬性會指定文字行之間的間距。<br /> Variant 類型： <strong>VT_BSTR</strong><br /> 預設值： "LineSpacingAttributeDefault"<br /> | 
| <span id="UIA_LinkAttributeId"></span><span id="uia_linkattributeid"></span><span id="UIA_LINKATTRIBUTEID"></span><dl><dt><strong>UIA_LinkAttributeId</strong></dt><dt>40035</dt></dl> | 識別 <strong>連結</strong> 文字屬性，其中包含文字範圍的 <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange"><strong>IUIAutomationTextRange</strong></a> 介面，這是檔中內部連結的目標。 從 Windows 8 開始支援。<br /> Variant 類型： <strong>VT_UNKNOWN</strong><br /> 預設值： <strong>Null</strong><br /> | 
| <span id="UIA_MarginBottomAttributeId"></span><span id="uia_marginbottomattributeid"></span><span id="UIA_MARGINBOTTOMATTRIBUTEID"></span><dl><dt><strong>UIA_MarginBottomAttributeId</strong></dt><dt>40018</dt></dl> | 識別 <strong>MarginBottom</strong> 文字屬性，指定套用至與文字範圍相關聯之頁面的下邊界大小（以點為單位）。 <br /> Variant 類型： <strong>VT_R8</strong><br /> 預設值：0<br /> | 
| <span id="UIA_MarginLeadingAttributeId"></span><span id="uia_marginleadingattributeid"></span><span id="UIA_MARGINLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginLeadingAttributeId</strong></dt><dt>40019</dt></dl> | 識別 <strong>MarginLeading</strong> 文字屬性，此屬性會指定套用至與文字範圍相關聯之頁面的前置邊界大小（以點為單位）。 <br /> Variant 類型： <strong>VT_R8</strong><br /> 預設值：0<br /> | 
| <span id="UIA_MarginTopAttributeId"></span><span id="uia_margintopattributeid"></span><span id="UIA_MARGINTOPATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTopAttributeId</strong></dt><dt>40020</dt></dl> | 識別 <strong>MarginTop</strong> 文字屬性，指定套用至與文字範圍相關聯之頁面的上邊界大小（以點為單位）。 <br /> Variant 類型： <strong>VT_R8</strong><br /> Ddefault 值：0<br /> | 
| <span id="UIA_MarginTrailingAttributeId"></span><span id="uia_margintrailingattributeid"></span><span id="UIA_MARGINTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTrailingAttributeId</strong></dt><dt>40021</dt></dl> | 識別 <strong>MarginTrailing</strong> 文字屬性，指定套用至與文字範圍相關聯之頁面的尾端邊界大小（以點為單位）。 <br /> Variant 類型： <strong>VT_R8</strong><br /> 預設值：0<br /> | 
| <span id="UIA_OutlineStylesAttributeId"></span><span id="uia_outlinestylesattributeid"></span><span id="UIA_OUTLINESTYLESATTRIBUTEID"></span><dl><dt><strong>UIA_OutlineStylesAttributeId</strong></dt><dt>40022</dt></dl> | 識別 <strong>OutlineStyles</strong> 文字屬性，此屬性會指定文字的外框樣式。 這個屬性會指定為 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"><strong>OutlineStyles</strong></a> 列舉型別中的值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"> <strong>OutlineStyles_None</strong></a><br /> | 
| <span id="UIA_OverlineColorAttributeId"></span><span id="uia_overlinecolorattributeid"></span><span id="UIA_OVERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineColorAttributeId</strong></dt><dt>40023</dt></dl> | 識別 <strong>OverlineColor</strong> 文字屬性，此屬性會指定頂線文字裝飾的色彩。 這個屬性會指定為 <a href="/windows/win32/gdi/colorref">COLORREF</a>，這是用來指定 RGB 或 RGBA 色彩的32位值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值：0<br /> | 
| <span id="UIA_OverlineStyleAttributeId"></span><span id="uia_overlinestyleattributeid"></span><span id="UIA_OVERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineStyleAttributeId</strong></dt><dt>40024</dt></dl> | 識別 <strong>OverlineStyle</strong> 文字屬性，此屬性會指定頂線文字裝飾的樣式。 這個屬性會指定為 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> 列舉型別中的值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_SelectionActiveEndAttributeId"></span><span id="uia_selectionactiveendattributeid"></span><span id="UIA_SELECTIONACTIVEENDATTRIBUTEID"></span><dl><dt><strong>UIA_SelectionActiveEndAttributeId</strong></dt><dt>40037</dt></dl> | 識別 <strong>SelectionActiveEnd</strong> 文字屬性，指出插入號相對於代表目前所選文字之文字範圍的位置。 這個屬性會指定為 <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"><strong>ActiveEnd</strong></a> 列舉的值。 從 Windows 8 開始支援。<br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"> <strong>ActiveEnd_None</strong></a><br /> | 
| <span id="UIA_StrikethroughColorAttributeId"></span><span id="uia_strikethroughcolorattributeid"></span><span id="UIA_STRIKETHROUGHCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughColorAttributeId</strong></dt><dt>40025</dt></dl> | 識別 <strong>StrikethroughColor</strong> 文字屬性，此屬性會指定刪除線文字裝飾的色彩。 這個屬性會指定為 <a href="/windows/win32/gdi/colorref">COLORREF</a>，這是用來指定 RGB 或 RGBA 色彩的32位值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值：0<br /> | 
| <span id="UIA_StrikethroughStyleAttributeId"></span><span id="uia_strikethroughstyleattributeid"></span><span id="UIA_STRIKETHROUGHSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughStyleAttributeId</strong></dt><dt>40026</dt></dl> | 識別 <strong>StrikethroughStyle</strong> 文字屬性，此屬性會指定刪除線文字裝飾的樣式。 這個屬性會指定為 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> 列舉型別中的值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_StyleIdAttributeId"></span><span id="uia_styleidattributeid"></span><span id="UIA_STYLEIDATTRIBUTEID"></span><dl><dt><strong>UIA_StyleIdAttributeId</strong></dt><dt>40034</dt></dl> | 識別 <strong>StyleId</strong> 文字屬性，指出文字範圍使用的文字樣式。 如需可能值的清單，請參閱 <a href="uiauto-style-identifiers.md"><strong>樣式識別碼</strong></a>。 從 Windows 8 開始支援。<br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值：0 <br /> | 
| <span id="UIA_StyleNameAttributeId"></span><span id="uia_stylenameattributeid"></span><span id="UIA_STYLENAMEATTRIBUTEID"></span><dl><dt><strong>UIA_StyleNameAttributeId</strong></dt><dt>40033</dt></dl> | 識別 <strong>StyleName</strong> 文字屬性，此屬性會識別文字範圍所使用之文字樣式的當地語系化名稱。 從 Windows 8 開始支援。<br /> Variant 類型： <strong>VT_BSTR</strong><br /> 預設值：空字串<br /> | 
| <span id="UIA_TabsAttributeId"></span><span id="uia_tabsattributeid"></span><span id="UIA_TABSATTRIBUTEID"></span><dl><dt><strong>UIA_TabsAttributeId</strong></dt><dt>40027</dt></dl> | 識別索引標籤文字屬性，這是指定文字範圍之 <strong>定位停駐點的</strong> 陣列。 每個陣列元素都會指定從開頭邊界開始的距離（以點為單位）。 <br /> Variant 類型： <strong> VT_ARRAY | VT_R8</strong><br /> 預設值：空陣列<br /> | 
| <span id="UIA_TextFlowDirectionsAttributeId"></span><span id="uia_textflowdirectionsattributeid"></span><span id="UIA_TEXTFLOWDIRECTIONSATTRIBUTEID"></span><dl><dt><strong>UIA_TextFlowDirectionsAttributeId</strong></dt><dt>40028</dt></dl> | 識別 <strong>TextFlowDirections</strong> 文字屬性，此屬性會指定文字流程的方向。 這個屬性會指定為 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"><strong>FlowDirections</strong></a> 列舉型別中的值組合。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"> <strong>FlowDirections_Default</strong></a><br /> | 
| <span id="UIA_UnderlineColorAttributeId"></span><span id="uia_underlinecolorattributeid"></span><span id="UIA_UNDERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineColorAttributeId</strong></dt><dt>40029</dt></dl> | 識別 <strong>UnderlineColor</strong> 文字屬性，此屬性會指定底線文字裝飾的色彩。 這個屬性會指定為 <a href="/windows/win32/gdi/colorref">COLORREF</a>，這是用來指定 RGB 或 RGBA 色彩的32位值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值：0<br /> | 
| <span id="UIA_UnderlineStyleAttributeId"></span><span id="uia_underlinestyleattributeid"></span><span id="UIA_UNDERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineStyleAttributeId</strong></dt><dt>40030</dt></dl> | 識別 <strong>UnderlineStyle</strong> 文字屬性，此屬性會指定底線文字裝飾的樣式。 這個屬性會指定為 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> 列舉型別中的值。 <br /> Variant 類型： <strong>VT_I4</strong><br /> 預設值： <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 




## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP \[ desktop apps \| UWP 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | WindowsServer 2003 \[ desktop app \| UWP 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Uiautomationclient.dll。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
</dt> <dt>

[**ITextRangeProvider：： GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
</dt> <dt>

[**IUIAutomation::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
</dt> <dt>

[**IUIAutomation：： GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)
</dt> <dt>

**概念**
</dt> <dt>

[消費者介面自動化文字內容的支援](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>
