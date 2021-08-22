---
title: 'Automation 元素屬性識別碼 (Uiautomationclient.dll .h) '
description: 本主題說明識別 Microsoft 消費者介面自動化專案屬性的命名常數。
ms.assetid: f7613ad1-0b75-46fb-b9ac-b1ae9eea4193
topic_type:
- apiref
api_name:
- UIA_AcceleratorKeyPropertyId
- UIA_AccessKeyPropertyId
- UIA_AnnotationObjectsPropertyId
- UIA_AnnotationTypesPropertyId
- UIA_AriaPropertiesPropertyId
- UIA_AriaRolePropertyId
- UIA_AutomationIdPropertyId
- UIA_BoundingRectanglePropertyId
- UIA_CenterPointPropertyId
- UIA_ClassNamePropertyId
- UIA_ClickablePointPropertyId
- UIA_ControllerForPropertyId
- UIA_ControlTypePropertyId
- UIA_CulturePropertyId
- UIA_DescribedByPropertyId
- UIA_FillColorPropertyId
- UIA_FillTypePropertyId
- UIA_FlowsFromPropertyId
- UIA_FlowsToPropertyId
- UIA_FrameworkIdPropertyId
- UIA_FullDescriptionPropertyId
- UIA_HasKeyboardFocusPropertyId
- UIA_HeadingLevelPropertyId
- UIA_HelpTextPropertyId
- UIA_IsContentElementPropertyId
- UIA_IsControlElementPropertyId
- UIA_IsDataValidForFormPropertyId
- UIA_IsEnabledPropertyId
- UIA_IsKeyboardFocusablePropertyId
- UIA_IsOffscreenPropertyId
- UIA_IsPasswordPropertyId
- UIA_IsPeripheralPropertyId
- UIA_IsRequiredForFormPropertyId
- UIA_ItemStatusPropertyId
- UIA_ItemTypePropertyId
- UIA_LabeledByPropertyId
- UIA_LandmarkTypePropertyId
- UIA_LevelPropertyId
- UIA_LiveSettingPropertyId
- UIA_LocalizedControlTypePropertyId
- UIA_LocalizedLandmarkTypePropertyId
- UIA_NamePropertyId
- UIA_NativeWindowHandlePropertyId
- UIA_OptimizeForVisualContentPropertyId
- UIA_OrientationPropertyId
- UIA_OutlineColorPropertyId
- UIA_OutlineThicknessPropertyId
- UIA_PositionInSetPropertyId
- UIA_ProcessIdPropertyId
- UIA_ProviderDescriptionPropertyId
- UIA_RotationPropertyId
- UIA_RuntimeIdPropertyId
- UIA_SizePropertyId
- UIA_SizeOfSetPropertyId
- UIA_VisualEffectsPropertyId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b373091ec34e71afbac32fca962ec380513acfcd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627694"
---
# <a name="automation-element-property-identifiers"></a>Automation 元素屬性識別碼

本主題說明識別 Microsoft 消費者介面自動化專案屬性的命名常數。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >常數/值</th>
<th >描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="UIA_AcceleratorKeyPropertyId"></span><span id="uia_acceleratorkeypropertyid"></span><span id="UIA_ACCELERATORKEYPROPERTYID"></span><dl> <dt><strong>UIA_AcceleratorKeyPropertyId</strong></dt> <dt>30006</dt> </dl></td>
<td >識別 <strong>AcceleratorKey</strong> 屬性，這是包含快速鍵的字串 (也稱為 automation 元素) 組合的快速鍵。 <br/> 快速鍵組合會叫用動作。 例如，CTRL + O 通常用來叫用 [開啟檔案] 通用對話方塊。 具有 <strong>AcceleratorKey</strong> 屬性的 automation 專案可以針對相當於快速鍵 <a href="uiauto-implementinginvoke.md">命令的動作</a> 來執行叫用控制項模式。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AccessKeyPropertyId"></span><span id="uia_accesskeypropertyid"></span><span id="UIA_ACCESSKEYPROPERTYID"></span><dl> <dt><strong>UIA_AccessKeyPropertyId</strong></dt> <dt>30007</dt> </dl></td>
<td >識別 <strong>AccessKey</strong> 屬性，這是包含 automation 元素之存取金鑰字元的字串。<br/> 存取金鑰 (有時稱為助憶鍵) 是在功能表、功能表項目的文字或控制項（例如按鈕）的標籤中，會啟用相關功能表功能的字元。 例如，若要開啟 [檔案] 功能表（存取金鑰通常是 F），使用者可以按下 ALT + F。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AnnotationObjectsPropertyId"></span><span id="uia_annotationobjectspropertyid"></span><span id="UIA_ANNOTATIONOBJECTSPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationObjectsPropertyId</strong></dt> <dt>30156</dt> </dl></td>
<td >識別 <strong>AnnotationObjects</strong> 屬性，這是檔中 annotation 物件的清單，例如 comment、header、頁尾等等。<br/> Variant 類型： <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> 預設值：空陣列<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AnnotationTypesPropertyId"></span><span id="uia_annotationtypespropertyid"></span><span id="UIA_ANNOTATIONTYPESPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationTypesPropertyId</strong></dt> <dt>30155</dt> </dl></td>
<td >識別 <strong>AnnotationTypes</strong> 屬性，這是檔中批註類型的清單，例如批註、頁首、頁尾等等。<br/> Variant 類型： <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> 預設值：空陣列<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AriaPropertiesPropertyId"></span><span id="uia_ariapropertiespropertyid"></span><span id="UIA_ARIAPROPERTIESPROPERTYID"></span><dl> <dt><strong>UIA_AriaPropertiesPropertyId</strong></dt> <dt>30102</dt> </dl></td>
<td >識別 <strong>AriaProperties</strong> 屬性，此屬性是包含可存取之豐富網際網路應用程式的格式化字串， (ARIA) automation 元素的屬性資訊。 如需將 ARIA 狀態和屬性對應至消費者介面自動化屬性和函式的詳細資訊，請參閱 <a href="uiauto-ariaspecification.md">消費者介面自動化的 W3C 可存取的豐富網際網路應用程式規格</a>。<br/> <strong>AriaProperties</strong> 是成對名稱/值組的集合，其分隔符號為 <strong>=</strong> (等於) 和 <strong>;</strong> (分號) ，例如 &quot; checked = true; disabled = false &quot; 。 <strong>\</strong>當這些分隔字元或 <strong>\</strong> 出現在值中時， (反斜線) 會當做 escape 字元使用。 基於安全性和其他原因，此屬性的提供者可以採取步驟來驗證原始的 ARIA 屬性;不過，這不是必要的。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AriaRolePropertyId"></span><span id="uia_ariarolepropertyid"></span><span id="UIA_ARIAROLEPROPERTYID"></span><dl> <dt><strong>UIA_AriaRolePropertyId</strong></dt> <dt>30101</dt> </dl></td>
<td >識別 <strong>AriaRole</strong> 屬性，這是一個字串，其中包含 automation 元素 (ARIA) 角色資訊的可存取豐富網際網路應用程式。 如需將 ARIA 角色對應至消費者介面自動化控制項類型的詳細資訊，請參閱 <a href="uiauto-ariaspecification.md">消費者介面自動化的 W3C 可存取的豐富網際網路應用程式規格</a>。<br/>
<blockquote>
[!Note]<br />
使用者代理程式也可以選擇在 <strong>LocalizedControlType</strong> 屬性中提供 W3C ARIA 角色的當地語系化描述。 未指定當地語系化的字串時，系統會提供專案的預設 <strong>LocalizedControlType</strong> 字串。
</blockquote>
<br/> <br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AutomationIdPropertyId"></span><span id="uia_automationidpropertyid"></span><span id="UIA_AUTOMATIONIDPROPERTYID"></span><dl> <dt><strong>UIA_AutomationIdPropertyId</strong></dt> <dt>30011</dt> </dl></td>
<td >識別 <strong>AutomationId</strong> 屬性，這是一個字串，其中包含 Automation 元素 (ID) 的消費者介面自動化識別碼。<br/> 如果有的話，在應用程式的任何實例中，元素的 <strong>AutomationId</strong> 必須相同，無論當地語言為何。 此值在同一個專案中應該是唯一的，但在整個桌面中不一定是唯一的。 例如，應用程式的多個實例，或 Microsoft Windows 檔案總管中的多個資料夾檢視可以包含具有相同<strong>AutomationId</strong>屬性（例如 SystemMenuBar）的元素 &quot; &quot; 。<br/> 雖然一律建議對 <strong>AutomationId</strong> 的支援，以提供更佳的自動化測試支援，但此屬性並非強制性。 在支援的情況下， <strong>AutomationId</strong> 可用於建立可執行檔測試自動化腳本，不論 UI 語言為何。 用戶端不應該針對其他應用程式所公開的 <strong>AutomationId</strong> 值做出任何假設。 <strong>AutomationId</strong> 不保證會在應用程式的不同版本或組建之間保持穩定。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_BoundingRectanglePropertyId"></span><span id="uia_boundingrectanglepropertyid"></span><span id="UIA_BOUNDINGRECTANGLEPROPERTYID"></span><dl> <dt><strong>UIA_BoundingRectanglePropertyId</strong></dt> <dt>30001</dt> </dl></td>
<td >識別 <strong>BoundingRectangle</strong> 屬性，此屬性會指定完全括住 automation 元素之矩形的座標。 矩形是以實體畫面座標表示。 如果 UI 專案的圖形或可按式區域是不規則的，或如果專案被其他 UI 元素遮蔽，則它可以包含無法按一下的點。<br/> Variant 類型： <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> 預設值： [0，0，0，0]<br/>
<blockquote>
[!Note]<br />
如果專案目前未顯示 UI，則此屬性為 <strong>Null</strong> 。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_CenterPointPropertyId"></span><span id="uia_centerpointpropertyid"></span><span id="UIA_CENTERPOINTPROPERTYID"></span><dl> <dt><strong>UIA_CenterPointPropertyId</strong></dt> <dt>30165</dt> </dl></td>
<td >識別 <strong>CenterPoint</strong> 屬性，此屬性會指定 automation 元素的中心 X 和 Y 點座標。 座標空間是提供者以邏輯方式考慮頁面。<br/> Variant 類型： <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> 預設值： <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ClassNamePropertyId"></span><span id="uia_classnamepropertyid"></span><span id="UIA_CLASSNAMEPROPERTYID"></span><dl> <dt><strong>UIA_ClassNamePropertyId</strong></dt> <dt>30012</dt> </dl></td>
<td >識別 <strong>ClassName</strong> 屬性，它是一個字串，其中包含由控制項開發人員指派之 automation 元素的類別名稱。<br/> 類別名稱取決於消費者介面自動化提供者的執行，因此不一定是標準格式。 但是，如果已知類別名稱，就可以用它來驗證應用程式是否使用預期的 automation 元素。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ClickablePointPropertyId"></span><span id="uia_clickablepointpropertyid"></span><span id="UIA_CLICKABLEPOINTPROPERTYID"></span><dl> <dt><strong>UIA_ClickablePointPropertyId</strong></dt> <dt>30014</dt> </dl></td>
<td >識別 <strong>ClickablePoint</strong> 屬性，這是可按一下之 automation 元素的點。 如果專案完全或部分被另一個視窗遮蔽，則無法按一下專案。<br/> Variant 類型： <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> 預設值： <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ControllerForPropertyId"></span><span id="uia_controllerforpropertyid"></span><span id="UIA_CONTROLLERFORPROPERTYID"></span><dl> <dt><strong>UIA_ControllerForPropertyId</strong></dt> <dt>30104</dt> </dl></td>
<td >識別 <strong>ControllerFor</strong> 屬性，這是 automation 元素的陣列，可由支援這個屬性的 automation 專案操作。<br/> 當 automation 元素影響應用程式 UI 或桌面的一或多個區段時，會使用<strong>ControllerFor</strong> ;否則，很難將控制項作業的影響與 UI 元素產生關聯。<br/> 此識別碼通常用於 <a href="/windows/uwp/design/accessibility/accessible-text-requirements">自動建議的協助工具</a>。<br/> 提供者的 Variant 類型： <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> 用戶端的 Variant 類型： <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a> ) <br/> 預設值：空陣列<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ControlTypePropertyId"></span><span id="uia_controltypepropertyid"></span><span id="UIA_CONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ControlTypePropertyId</strong></dt> <dt>30003</dt> </dl></td>
<td >識別 <strong>ControlType</strong> 屬性，此屬性是可識別 automation 元素類型的類別。 <strong>ControlType</strong> 會依已知的 ui 控制項基本類型（例如按鈕或核取方塊）來定義 UI 元素的特性。 <br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值： <a href="uiauto-controltype-ids.md"> <strong>UIA_CustomControlTypeId</strong></a><br/>
<blockquote>
[!Note]<br />
只有當 automation 元素代表全新的控制項類型時，才使用預設值。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_CulturePropertyId"></span><span id="uia_culturepropertyid"></span><span id="UIA_CULTUREPROPERTYID"></span><dl> <dt><strong>UIA_CulturePropertyId</strong></dt> <dt>30015</dt> </dl></td>
<td >識別 <strong>文化</strong> 特性屬性，其中包含 automation 元素的地區設定識別碼 (例如， <code>0x0409</code> 針對 &quot; En-us &quot; 或英文 (美國) ) 。<br/> 每個地區設定都有一個唯一識別碼，這是由語言識別項和排序次序識別碼組成的32位值。 地區設定識別碼是標準的國際數值縮寫，而且具有唯一識別其中一個已安裝作業系統定義之地區設定所需的元件。 如需詳細資訊，請參閱 <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">語言識別項常數和字串</a>。<br/> 這個屬性可能會以每個控制項為基礎，但通常只能在應用層級上使用。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_DescribedByPropertyId"></span><span id="uia_describedbypropertyid"></span><span id="UIA_DESCRIBEDBYPROPERTYID"></span><dl> <dt><strong>UIA_DescribedByPropertyId</strong></dt> <dt>30105</dt> </dl></td>
<td >識別 <strong>DescribedBy</strong> 屬性，這是專案的陣列，可提供自動化元素的詳細資訊。<br/> 當應用程式 UI 的另一個區段解釋 automation 元素時，會使用<strong>DescribedBy</strong> 。 例如，屬性可指向 &quot; 85 群組中2529個專案的文字專案， &quot; 從複雜自訂清單物件選取10個專案。 <strong>DescribedBy</strong>屬性可以提供 ui 元素的快速存取權，而不是使用用戶端的物件模型來摘要類似的資訊，而是可以快速存取 ui 元素，而該專案可能已經提供實用的使用者資訊來描述 ui 元素。<br/> 提供者的 Variant 類型： <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> 用戶端的 Variant 類型： <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>) <br/> 預設值：空陣列<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FillColorPropertyId"></span><span id="uia_fillcolorpropertyid"></span><span id="UIA_FILLCOLORPROPERTYID"></span><dl> <dt><strong>UIA_FillColorPropertyId</strong></dt> <dt>30160</dt> </dl></td>
<td >識別 <strong>FillColor</strong> 屬性，此屬性會指定用來填滿 automation 元素的色彩。 這個屬性會指定為 COLORREF，這是用來指定 RGB 或 RGBA 色彩的32位值。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FillTypePropertyId"></span><span id="uia_filltypepropertyid"></span><span id="UIA_FILLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_FillTypePropertyId</strong></dt> <dt>30162</dt> </dl></td>
<td >識別 <strong>FillType</strong> 屬性，此屬性會指定用來填滿 automation 專案的模式，例如「無」、「色彩」、「漸層」、「圖片」、「模式」等等。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FlowsFromPropertyId"></span><span id="uia_flowsfrompropertyid"></span><span id="UIA_FLOWSFROMPROPERTYID"></span><dl> <dt><strong>UIA_FlowsFromPropertyId</strong></dt> <dt>30148</dt> </dl></td>
<td >識別 <strong>FlowsFrom</strong> 屬性，這是自動化專案的陣列，可在目前的 automation 元素之前建議讀取順序。 從 Windows 8 開始支援。<br/> <strong>FlowsFrom</strong>屬性會指定當自動化元素未以使用者所見的相同讀取順序來公開或結構化時的讀取順序。 雖然 <strong>FlowsFrom</strong> 屬性可以指定多個前置元素，但它通常只會包含讀取順序中的前一個專案。<br/> 提供者的 Variant 類型： <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> 用戶端的 Variant 類型： <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>) <br/> 預設值：空陣列<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FlowsToPropertyId"></span><span id="uia_flowstopropertyid"></span><span id="UIA_FLOWSTOPROPERTYID"></span><dl> <dt><strong>UIA_FlowsToPropertyId</strong></dt> <dt>30106</dt> </dl></td>
<td >識別 <strong>FlowsTo</strong> 屬性，這是 automation 專案的陣列，可在目前的 automation 元素之後建議讀取順序。<br/> <strong>FlowsTo</strong>屬性會指定當自動化元素未以使用者所見的相同讀取順序來公開或結構化時的讀取順序。 雖然 <strong>FlowsTo</strong> 屬性可以指定多個後續元素，但它通常只會包含讀取順序中的下一個元素。<br/> 提供者的 Variant 類型： <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> 用戶端的 Variant 類型： <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>) <br/> 預設值：空陣列<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FrameworkIdPropertyId"></span><span id="uia_frameworkidpropertyid"></span><span id="UIA_FRAMEWORKIDPROPERTYID"></span><dl> <dt><strong>UIA_FrameworkIdPropertyId</strong></dt> <dt>30024</dt> </dl></td>
<td >識別 <strong>FrameworkId</strong> 屬性，這是一個字串，其中包含 automation 元素所屬之基礎 UI 架構的名稱。<br/> <strong>FrameworkId</strong>可讓用戶端應用程式根據特定的 UI 架構，以不同的方式處理 automation 元素。 屬性值的範例包括 &quot; Win32 &quot; 、 &quot; WinForm &quot; 和 &quot; DirectUI &quot; 。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FullDescriptionPropertyId"></span><span id="uia_fulldescriptionpropertyid"></span><span id="UIA_FULLDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_FullDescriptionPropertyId</strong></dt> <dt>30159</dt> </dl></td>
<td ><strong>FullDescription</strong>屬性會公開當地語系化的字串，其中可以包含元素的延伸描述文字。 <strong>FullDescription</strong> 可包含元素的更完整描述，而不能符合專案 <strong>名稱</strong>。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_HasKeyboardFocusPropertyId"></span><span id="uia_haskeyboardfocuspropertyid"></span><span id="UIA_HASKEYBOARDFOCUSPROPERTYID"></span><dl> <dt><strong>UIA_HasKeyboardFocusPropertyId</strong></dt> <dt>30008</dt> </dl></td>
<td >識別 <strong>HasKeyboardFocus</strong> 屬性，這是布林值，指出 automation 元素是否具有鍵盤焦點。<br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_HeadingLevelPropertyId"></span><span id="uia_headinglevelpropertyid"></span><span id="UIA_HEADINGLEVELPROPERTYID"></span><dl> <dt><strong>UIA_HeadingLevelPropertyId</strong></dt> <dt>30173</dt> </dl></td>
<td >識別 <strong>HeadingLevel</strong> 屬性，指出消費者介面自動化元素的標題層級。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值： <strong>HeadingLevel_None</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_HelpTextPropertyId"></span><span id="uia_helptextpropertyid"></span><span id="UIA_HELPTEXTPROPERTYID"></span><dl> <dt><strong>UIA_HelpTextPropertyId</strong></dt> <dt>30013</dt> </dl></td>
<td >識別 <strong>HelpText</strong> 屬性，這是與 automation 元素相關聯的解說文字字串。<br/> <strong>HelpText</strong>屬性可以支援出現在編輯或清單控制項中的預留位置文字。 例如，在 &quot; 這裡輸入 text for search &quot; 是一個很好的候選屬性，它是編輯控制項的 <strong>HelpText</strong> 屬性，會在使用者的實際輸入之前放置文字。 但是，它並不適合編輯控制項的 [名稱] 屬性。<br/> 當支援 <strong>HelpText</strong> 時，此字串必須符合應用程式 UI 語言或作業系統的預設 UI 語言。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsContentElementPropertyId"></span><span id="uia_iscontentelementpropertyid"></span><span id="UIA_ISCONTENTELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsContentElementPropertyId</strong></dt> <dt>30017</dt> </dl></td>
<td >識別 <strong>IsContentElement</strong> 屬性，這是布林值，指定專案是否出現在 automation 元素樹狀結構的內容視圖中。 如需詳細資訊，請參閱 <a href="uiauto-treeoverview.md">消費者介面自動化樹狀結構總覽</a>。<br/>
<blockquote>
[!Note]<br />
若要讓元素出現在內容視圖中， <strong>IsContentElement</strong> 屬性和 <strong>IsControlElement</strong> 屬性都必須為 <strong>TRUE</strong>。
</blockquote>
<br/> <br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>TRUE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsControlElementPropertyId"></span><span id="uia_iscontrolelementpropertyid"></span><span id="UIA_ISCONTROLELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsControlElementPropertyId</strong></dt> <dt>30016</dt> </dl></td>
<td >識別 <strong>IsControlElement</strong> 屬性，這是布林值，指定專案是否出現在 automation 元素樹狀結構的控制項視圖中。 如需詳細資訊，請參閱 <a href="uiauto-treeoverview.md">消費者介面自動化樹狀結構總覽</a>。<br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>TRUE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsDataValidForFormPropertyId"></span><span id="uia_isdatavalidforformpropertyid"></span><span id="UIA_ISDATAVALIDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsDataValidForFormPropertyId</strong></dt> <dt>30103</dt> </dl></td>
<td >識別 <strong>IsDataValidForForm</strong> 屬性，這是布林值，指出輸入或選取的值是否適用于與 automation 元素相關聯的表單規則。 例如，如果使用者 &quot; &quot; 針對需要5或9位數的郵遞區號欄位輸入425-555-5555， <strong>IsDataValidForForm</strong> 屬性可以設定為 <strong>FALSE</strong> ，表示資料無效。<br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>FALSE</strong><br/></td>
</tr>

<tr class="odd">
<td ><span id="UIA_IsDialogPropertyId"></span><span id="uia_isdialogpropertyid"></span><span id="UIA_ISDIALOGPROPERTYID"></span><dl> <dt><strong>UIA_IsDialogPropertyId</strong></dt> <dt>30174</dt> </dl></td>
<td >識別 <strong>IsDialog</strong> 屬性，這是布林值，指出 automation 元素是否為對話方塊視窗。 例如，螢幕讀取器之類的輔助技術通常會說出對話的標題、對話方塊中的焦點控制項，然後將對話的內容放到焦點控制項 (您要在 &quot; 關閉) 之前儲存變更 &quot; 。 若為標準視窗，螢幕讀取器通常會將視窗標題和焦點控制項一併放在一起。 <strong>IsDialog</strong>屬性可以設定為<strong>TRUE</strong> ，表示用戶端應用程式應該將元素視為對話方塊視窗。<br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>FALSE</strong><br/></td>
</tr>

<tr class="even">
<td ><span id="UIA_IsEnabledPropertyId"></span><span id="uia_isenabledpropertyid"></span><span id="UIA_ISENABLEDPROPERTYID"></span><dl> <dt><strong>UIA_IsEnabledPropertyId</strong></dt> <dt>30010</dt> </dl></td>
<td >識別 <strong>IsEnabled</strong> 屬性，這是布林值，指出 automation 元素所參考的 UI 專案是否已啟用，而且可以與互動。<br/> 當控制項的已啟用狀態為 <strong>FALSE</strong>時，會假設子控制項也未啟用。 當父控制項的狀態變更時，用戶端不應該預期子項目的屬性變更事件。<br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsKeyboardFocusablePropertyId"></span><span id="uia_iskeyboardfocusablepropertyid"></span><span id="UIA_ISKEYBOARDFOCUSABLEPROPERTYID"></span><dl> <dt><strong>UIA_IsKeyboardFocusablePropertyId</strong></dt> <dt>30009</dt> </dl></td>
<td >識別 <strong>IsKeyboardFocusable</strong> 屬性，這是布林值，指出 automation 元素是否可以接受鍵盤焦點。<br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsOffscreenPropertyId"></span><span id="uia_isoffscreenpropertyid"></span><span id="UIA_ISOFFSCREENPROPERTYID"></span><dl> <dt><strong>UIA_IsOffscreenPropertyId</strong></dt> <dt>30022</dt> </dl></td>
<td >識別 <strong>IsOffscreen</strong> 屬性，這是一個布林值，指出 automation 元素是否完全以視野顯示 (例如，在容器物件的元件之外的清單方塊中的專案) 或折迭 (例如，樹狀檢視或功能表中的專案，或在最小化的視窗) 中。 如果專案具有可按下的點，而使其無法接收焦點，則元素會被視為在螢幕上，而專案的某個部分是在螢幕上。<br/> 屬性的值不會受到其他視窗遮蔽的影響，也不會受到特定監視器上是否可見的元素影響。<br/> 如果 <strong>IsOffscreen</strong> 屬性為 <strong>TRUE</strong>，則會在螢幕上或折迭 UI 元素。 專案會暫時隱藏，但仍會保留在使用者的認知中，並繼續包含在 UI 模型中。 您可以藉由滾動、按一下下拉式清單等方式，將物件重新顯示。<br/> 使用者完全不會察覺的物件，或 &quot; 以程式設計方式隱藏的物件 &quot; (例如，已關閉的對話方塊，但應用程式仍會快取基礎物件) 不應該在 [automation 元素] 樹狀結構中的第一個位置 (，而不是將 <strong>IsOffscreen</strong> 的狀態設定為 [ <strong>TRUE</strong> ]) 。<br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsPasswordPropertyId"></span><span id="uia_ispasswordpropertyid"></span><span id="UIA_ISPASSWORDPROPERTYID"></span><dl> <dt><strong>UIA_IsPasswordPropertyId</strong></dt> <dt>30019</dt> </dl></td>
<td >識別 <strong>IsPassword</strong> 屬性，這是布林值，指出 automation 元素是否包含受保護的內容或密碼。<br/> 當 <strong>IsPassword</strong> 屬性為 <strong>TRUE</strong> ，且專案具有鍵盤焦點時，用戶端應用程式應該停用可能會公開使用者受保護資訊的鍵盤回應或鍵盤輸入意見反應。 嘗試存取受保護專案的 <strong>Value</strong> 屬性 (編輯控制項) 可能會導致錯誤發生。<br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsPeripheralPropertyId"></span><span id="uia_isperipheralpropertyid"></span><span id="UIA_ISPERIPHERALPROPERTYID"></span><dl> <dt><strong>UIA_IsPeripheralPropertyId</strong></dt> <dt>30150</dt> </dl></td>
<td >識別 <strong>IsPeripheral</strong> 屬性，這是布林值，指出 automation 元素是否代表週邊設備 UI。 周邊 UI 隨即出現並支援使用者互動，但不會在出現時取得鍵盤焦點。 週邊設備 UI 的範例包括快顯、flyouts、內容功能表或浮動通知。 從 Windows 8.1 開始支援。<br/> 當 <strong>IsPeripheral</strong> 屬性為 <strong>TRUE</strong>時，用戶端應用程式無法假設專案是由專案所使用，即使它目前為鍵盤互動。<br/> 這個屬性與下列控制項類型有關：<br/>
<ul>
<li><strong>UIA_GroupControlTypeId</strong></li>
<li><strong>UIA_MenuControlTypeId</strong></li>
<li><strong>UIA_PaneControlTypeId</strong></li>
<li><strong>UIA_ToolBarControlTypeId</strong></li>
<li><strong>UIA_ToolTipControlTypeId</strong></li>
<li><strong>UIA_WindowControlTypeId</strong></li>
<li><strong>UIA_CustomControlTypeId</strong></li>
</ul>
Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsRequiredForFormPropertyId"></span><span id="uia_isrequiredforformpropertyid"></span><span id="UIA_ISREQUIREDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsRequiredForFormPropertyId</strong></dt> <dt>30025</dt> </dl></td>
<td >識別 <strong>IsRequiredForForm</strong> 屬性，這是布林值，指出是否需要在表單上填入 automation 元素。<br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ItemStatusPropertyId"></span><span id="uia_itemstatuspropertyid"></span><span id="UIA_ITEMSTATUSPROPERTYID"></span><dl> <dt><strong>UIA_ItemStatusPropertyId</strong></dt> <dt>30026</dt> </dl></td>
<td >識別 <strong>ItemStatus</strong> 屬性，這是描述 automation 元素專案狀態的文字字串。<br/> <strong>ItemStatus</strong> 可讓用戶端判斷專案是否正在傳達專案的狀態，以及狀態是什麼。 例如，與訊息應用程式中的連絡人相關聯的專案可能會 &quot; 忙碌 &quot; 或 &quot; 連接 &quot; 。<br/> 當支援 <strong>ItemStatus</strong> 時，此字串必須符合應用程式 UI 語言或作業系統的預設 UI 語言。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ItemTypePropertyId"></span><span id="uia_itemtypepropertyid"></span><span id="UIA_ITEMTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ItemTypePropertyId</strong></dt> <dt>300021</dt> </dl></td>
<td >識別 <strong>ItemType</strong> 屬性，這是描述 automation 元素類型的文字字串。<br/> <strong>ItemType</strong> 可用來取得清單、樹狀檢視或資料方格中的專案相關資訊。 例如，檔案目錄檢視中的專案可能是檔檔 &quot; &quot; 或 &quot; 資料夾 &quot; 。<br/> 當支援 <strong>ItemType</strong> 時，此字串必須符合應用程式 UI 語言或作業系統的預設 UI 語言。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LabeledByPropertyId"></span><span id="uia_labeledbypropertyid"></span><span id="UIA_LABELEDBYPROPERTYID"></span><dl> <dt><strong>UIA_LabeledByPropertyId</strong></dt> <dt>30018</dt> </dl></td>
<td >識別 <strong>LabeledBy</strong> 屬性，這是包含此專案之文字標籤的 automation 元素。<br/> 您可以使用這個屬性來抓取下拉式方塊的靜態文字標籤。<br/> Variant 類型： <strong>VT_UNKNOWN</strong><br/> 預設值： <strong>Null</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LandmarkTypePropertyId"></span><span id="uia_landmarktypepropertyid"></span><span id="UIA_LANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LandmarkTypePropertyId</strong></dt> <dt>30157</dt> </dl></td>
<td >識別 <strong>LandmarkType</strong> 屬性，這是與元素相關聯的 <a href="landmark-type-identifiers.md"><strong>地標類型識別碼</strong></a> 。<br/> <strong>LandmarkType</strong>屬性描述代表元素群組的元素。 例如，搜尋地標可能代表一組用於搜尋的相關控制項。<br/> 如果使用 <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> ，則需要 <strong>UIA_LocalizedLandmarkTypePropertyId</strong> ，才能描述自訂地標。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LevelPropertyId"></span><span id="uia_levelpropertyid"></span><span id="UIA_LEVELPROPERTYID"></span><dl> <dt><strong>UIA_LevelPropertyId</strong></dt> <dt>30154</dt> </dl></td>
<td >識別 <strong>Level</strong> 屬性，它是與 automation 元素相關聯的1個整數。<br/> <strong>Level</strong>屬性描述元素在階層式或階層式階層結構內的位置。 例如，專案符號/編號清單、標題或其他結構化資料項目可以有各種父子式關聯性。 <strong>層級</strong> 描述專案所在結構中的位置。<br/> 建議將 <a href="/windows/desktop/WinAuto/uiauto-implementingcustomnavigation">CustomNavigation 控制項模式</a> 與 <strong>層級</strong>一起使用。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LiveSettingPropertyId"></span><span id="uia_livesettingpropertyid"></span><span id="UIA_LIVESETTINGPROPERTYID"></span><dl> <dt><strong>UIA_LiveSettingPropertyId</strong></dt> <dt>30135</dt> </dl></td>
<td >識別 <strong>LiveSetting</strong> 屬性，這是代表即時區域的 automation 元素所支援的屬性。 <strong>LiveSetting</strong>屬性指出 &quot; &quot; 用戶端應該用來通知使用者即時區域變更的禮貌程度層級。 這個屬性可以是 <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting"><strong>LiveSetting</strong></a> 列舉的其中一個值。 從 Windows 8 開始支援。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LocalizedControlTypePropertyId"></span><span id="uia_localizedcontroltypepropertyid"></span><span id="UIA_LOCALIZEDCONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedControlTypePropertyId</strong></dt> <dt>30004</dt> </dl></td>
<td >識別 <strong>LocalizedControlType</strong> 屬性，這是描述 automation 元素所代表之控制項類型的文字字串。 字串只能包含小寫字元：
<ul>
<li>更正： &quot; 按鈕&quot;</li>
<li>不正確： &quot; 按鈕&quot;</li>
</ul>
<br/> 當專案提供者未指定 <strong>LocalizedControlType</strong> 時，根據元素的控制項類型，架構會提供預設的當地語系化字串，例如 &quot; &quot; <a href="uiauto-supportbuttoncontroltype.md">按鈕</a> 控制項類型) 的按鈕 (。 具有 <strong>自訂</strong> 控制項類型的 automation 元素必須支援表示專案角色的當地語系化控制項類型字串 (例如， &quot; 自訂控制項的色彩選擇器，可 &quot; 讓使用者選擇並指定) 的色彩。<br/> 當提供自訂值時，字串必須符合應用程式 UI 語言或作業系統的預設 UI 語言。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LocalizedLandmarkTypePropertyId"></span><span id="uia_localizedlandmarktypepropertyid"></span><span id="UIA_LOCALIZEDLANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedLandmarkTypePropertyId</strong></dt> <dt>30158</dt> </dl></td>
<td >識別 <strong>LocalizedLandmarkType</strong>，這是一個文字字串，描述 automation 元素所代表的地標類型。<br/> 這應該與 <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> 一起使用，不過， <strong>LocalizedLandmarkType</strong> 應該一律優先于 <strong>LandmarkType</strong> ，並在 <strong>LandmarkType</strong>之前用來描述地標。<br/> 字串必須符合應用程式 UI 語言或作業系統預設的 UI 語言。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_NamePropertyId"></span><span id="uia_namepropertyid"></span><span id="UIA_NAMEPROPERTYID"></span><dl> <dt><strong>UIA_NamePropertyId</strong></dt> <dt>30005</dt> </dl></td>
<td >識別 <strong>name</strong> 屬性，它是保存 automation 元素名稱的字串。<br/> [ <strong>名稱</strong> ] 屬性應該與螢幕上的標籤文字相同。 例如，[ <strong>名稱</strong> ] 應 &quot; 流覽 &quot; 具有標籤流覽的按鈕元素 &quot; &quot; 。 <strong>Name</strong>屬性不能包含存取金鑰的助憶鍵字元 (也就是 &quot; & &quot;) ，也就是 UI 文字簡報中的底線。 此外，[ <strong>名稱</strong> ] 屬性不應為螢幕標籤的擴充或修改版本，因為名稱和標籤之間的不一致可能會在用戶端應用程式與使用者之間產生混淆。<br/> 當對應的標籤文字未顯示在螢幕上，或是以圖形取代時，您應該選擇替代文字。 替代文字應為應用程式 UI 語言的簡潔、直覺和當地語系化，或作業系統預設 UI 語言。 替代文字不應該是視覺效果詳細資料的詳細描述，而是 UI 函式或功能的簡短描述，就像是以簡單文字標記一樣。 例如，[Windows] [開始] 功能表按鈕的名稱為 [ &quot; 開始] &quot; (按鈕) 而不是 [ &quot; 藍色圓形球體圖形 Windows 標誌] (&quot; 按鈕) 。 如需詳細資訊，請參閱 <a href="/previous-versions/windows/desktop/dnacc/creating-text-equivalents-for-images">建立影像的對應文字</a>。<br/> 當 UI 標籤使用文字圖形 (例如，使用 &quot; >> &quot; 來將專案從左至右) 的按鈕時，應以適當的文字替代專案覆寫<strong>Name</strong>屬性 (例如， &quot; 加入 &quot;) 。 但是，不建議使用文字圖形作為 UI 標籤，因為當地語系化和協助工具的考慮。<br/> <strong>Name</strong>屬性不能包含控制項角色或類型資訊（例如 &quot; 按鈕 &quot; 或 &quot; 清單） &quot; ; 否則，當這兩個屬性附加時，將會與<strong>LocalizedControlType</strong>屬性中的文字發生衝突， (許多現有的輔助技術可進行此) 。<br/> <strong>Name</strong>屬性不能用來作為同級之間的唯一識別碼。 不過，只要與 UI 簡報一致，就可以在對等之間支援相同的 <strong>名稱</strong> 值。 針對測試自動化，用戶端應該考慮使用 <strong>AutomationId</strong> 或 <strong>RuntimeId</strong> 屬性。<br/> 文字控制項的 [ <strong>名稱</strong> ] 屬性不一定要與控制項內顯示的文字相同，只要 <strong>文字</strong> 模式也受到支援。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_NativeWindowHandlePropertyId"></span><span id="uia_nativewindowhandlepropertyid"></span><span id="UIA_NATIVEWINDOWHANDLEPROPERTYID"></span><dl> <dt><strong>UIA_NativeWindowHandlePropertyId</strong></dt> <dt>30020</dt> </dl></td>
<td >識別 <strong>NativeWindowHandle</strong> 屬性，這是一個整數，表示 automation 元素視窗的控制碼 (<strong>HWND</strong>) （如果存在的話）。否則，此屬性為0。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_OptimizeForVisualContentPropertyId"></span><span id="uia_optimizeforvisualcontentpropertyid"></span><span id="UIA_OPTIMIZEFORVISUALCONTENTPROPERTYID"></span><dl> <dt><strong>UIA_OptimizeForVisualContentPropertyId</strong></dt> <dt>30111</dt> </dl></td>
<td >識別 <strong>OptimizeForVisualContent</strong> 屬性，這是布林值，指出提供者是否只公開可見的元素。 提供者可以使用這個屬性，在使用非常大量的內容時將效能優化。 例如，當使用者逐頁流覽大量內容時，提供者可能會損毀不再可見的內容元素。 當內容元素損毀時，提供者應該傳回 <strong>UIA_E_ELEMENTNOTAVAILABLE</strong> 錯誤碼。 從 Windows 8 開始支援。<br/> Variant 類型： <strong>VT_BOOL</strong><br/> 預設值： <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_OrientationPropertyId"></span><span id="uia_orientationpropertyid"></span><span id="UIA_ORIENTATIONPROPERTYID"></span><dl> <dt><strong>UIA_OrientationPropertyId</strong></dt> <dt>300023</dt> </dl></td>
<td >識別 <strong>方向</strong> 屬性，指出由 automation 元素表示的控制項方向。 屬性會以 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType</strong></a> 列舉型別中的值表示。<br/> <strong>方向</strong>屬性是由可以垂直或水準方向的控制項（例如捲軸和滑杆）所支援。 否則，它一定會 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>，這表示控制項沒有方向。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值： 0 (<a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>) <br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_OutlineColorPropertyId"></span><span id="uia_outlinecolorpropertyid"></span><span id="UIA_OUTLINECOLORPROPERTYID"></span><dl> <dt><strong>UIA_OutlineColorPropertyId</strong></dt> <dt>30161</dt> </dl></td>
<td >識別 <strong>OutlineColor</strong> 屬性，此屬性會指定 automation 元素外框所使用的色彩。 這個屬性會指定為 <strong>COLORREF</strong>，這是用來指定 RGB 或 RGBA 色彩的32位值。<br/> Variant 類型： <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_OutlineThicknessPropertyId"></span><span id="uia_outlinethicknesspropertyid"></span><span id="UIA_OUTLINETHICKNESSPROPERTYID"></span><dl> <dt><strong>UIA_OutlineThicknessPropertyId</strong></dt> <dt>30164</dt> </dl></td>
<td >識別 <strong>OutlineThickness</strong> 屬性，此屬性會指定 automation 元素外框的寬度。<br/> Variant 類型： <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> 預設值： <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_PositionInSetPropertyId"></span><span id="uia_positioninsetpropertyid"></span><span id="UIA_POSITIONINSETPROPERTYID"></span><dl> <dt><strong>UIA_PositionInSetPropertyId</strong></dt> <dt>30152</dt> </dl></td>
<td >識別 <strong>>positioninset</strong> 屬性，這是與 automation 元素相關聯的1個整數。 <strong>>Positioninset</strong> 會在一組視為同級的元素中，描述專案的序數位置。<br/> <strong>>Positioninset</strong> 可與 <strong>SizeOfSet</strong> 屬性協調，以描述集合中的序數位置。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ProcessIdPropertyId"></span><span id="uia_processidpropertyid"></span><span id="UIA_PROCESSIDPROPERTYID"></span><dl> <dt><strong>UIA_ProcessIdPropertyId</strong></dt> <dt>30002</dt> </dl></td>
<td >識別 <strong>ProcessId</strong> 屬性，它是一個整數，表示 automation 元素 (識別碼) 的處理序識別碼。<br/> 作業系統會指派 (識別碼) 的處理序識別碼。 您可以在工作管理員的 [<strong>進程</strong>] 索引標籤的 [ <strong>PID</strong> ] 資料行中看到它。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ProviderDescriptionPropertyId"></span><span id="uia_providerdescriptionpropertyid"></span><span id="UIA_PROVIDERDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_ProviderDescriptionPropertyId</strong></dt> <dt>30107</dt> </dl></td>
<td >識別 <strong>ProviderDescription</strong> 屬性，這是一個格式字串，其中包含 Automation 元素之消費者介面自動化提供者的來源資訊，包括 proxy 資訊。<br/> Variant 類型： <strong>VT_BSTR</strong><br/> 預設值：空字串<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_RotationPropertyId"></span><span id="uia_rotationpropertyid"></span><span id="UIA_ROTATIONPROPERTYID"></span><dl> <dt><strong>UIA_RotationPropertyId</strong></dt> <dt>30166</dt> </dl></td>
<td >識別 <strong>旋轉</strong> 屬性，此屬性會以未指定的單位來指定旋轉的角度。<br/> Variant 類型： <strong>VT_R8</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_RuntimeIdPropertyId"></span><span id="uia_runtimeidpropertyid"></span><span id="UIA_RUNTIMEIDPROPERTYID"></span><dl> <dt><strong>UIA_RuntimeIdPropertyId</strong></dt> <dt>30000</dt> </dl></td>
<td >識別 <strong>RuntimeId</strong> 屬性，這是表示 automation 元素識別碼的整數陣列。<br/> 識別碼在桌面上是唯一的，但保證只有在產生它的桌面 UI 中才是唯一的。 您可以在一段時間內重複使用識別碼。<br/> <strong>RuntimeId</strong>的格式可能會變更。 傳回的識別碼應該視為不透明值，而且只用于比較。例如，判斷 automation 元素是否在快取中。<br/> Variant 類型： <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> 預設值： <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_SizePropertyId"></span><span id="uia_sizepropertyid"></span><span id="UIA_SIZEPROPERTYID"></span><dl> <dt><strong>UIA_SizePropertyId</strong></dt> <dt>30167</dt> </dl></td>
<td >識別 <strong>Size</strong> 屬性，這個屬性會指定 automation 元素的寬度和高度。<br/> Variant 類型： <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> 預設值： <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_SizeOfSetPropertyId"></span><span id="uia_sizeofsetpropertyid"></span><span id="UIA_SIZEOFSETPROPERTYID"></span><dl> <dt><strong>UIA_SizeOfSetPropertyId</strong></dt> <dt>30153</dt> </dl></td>
<td >識別 <strong>SizeOfSet</strong> 屬性，這是與 automation 元素相關聯的1個整數。 <strong>SizeOfSet</strong> 描述群組或集合中視為同級的自動化元素計數。<br/> <strong>SizeOfSet</strong> 可與 <strong>>positioninset</strong> 屬性協調，以描述集合中的專案計數。<br/> Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_VisualEffectsPropertyId"></span><span id="uia_visualeffectspropertyid"></span><span id="UIA_VISUALEFFECTSPROPERTYID"></span><dl> <dt><strong>UIA_VisualEffectsPropertyId</strong></dt> <dt>30163</dt> </dl></td>
<td >識別 <strong>VisualEffects</strong> 屬性，這是指定 automation 元素效果（例如陰影、反映、發光、軟邊緣或斜面）效果的位欄位。<br/> VisualEffects:<br/>
<ul>
<li>VisualEffects_Shadow：0x1</li>
<li>VisualEffects_Reflection：0x2</li>
<li>VisualEffects_Glow：0x4</li>
<li>VisualEffects_SoftEdges：0x8</li>
<li>VisualEffects_Bevel：0x10</li>
</ul>
Variant 類型： <strong>VT_I4</strong><br/> 預設值：0<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP \[ desktop apps \| UWP 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | WindowsServer 2003 \[ desktop app \| UWP 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Uiautomationclient.dll。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化屬性概觀](uiauto-propertiesoverview.md)
</dt> <dt>

[從消費者介面自動化元素抓取屬性](uiauto-propertiesforclients.md)
</dt> </dl>
