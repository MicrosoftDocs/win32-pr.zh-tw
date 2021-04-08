---
title: '批註類型識別碼 (Uiautomationclient.dll .h) '
description: 本主題說明用來在檔中識別批註類型的已命名常數。
ms.assetid: 46948B7C-EC9F-4B55-B769-62EE8BE11D33
topic_type:
- apiref
api_name:
- AnnotationType_AdvancedProofingIssue
- AnnotationType_Author
- AnnotationType_CircularReferenceError
- AnnotationType_Comment
- AnnotationType_ConflictingChange
- AnnotationType_DataValidationError
- AnnotationType_DeletionChange
- AnnotationType_EditingLockedChange
- AnnotationType_Endnote
- AnnotationType_ExternalChange
- AnnotationType_Footer
- AnnotationType_Footnote
- AnnotationType_FormatChange
- AnnotationType_FormulaError
- AnnotationType_GrammarError
- AnnotationType_Header
- AnnotationType_Highlighted
- AnnotationType_InsertionChange
- AnnotationType_Mathematics
- AnnotationType_MoveChange
- AnnotationType_SpellingError
- AnnotationType_TrackChanges
- AnnotationType_Unknown
- AnnotationType_UnsyncedChange
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb628c8e6ada93546291cd9afb87c3194798b9f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685460"
---
# <a name="annotation-type-identifiers"></a>批註類型識別碼

本主題說明用來在檔中識別批註類型的已命名常數。



| 常數/值                                                                                                                                                                                                                                                                                                                                           | Description                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span id="AnnotationType_AdvancedProofingIssue"></span><span id="annotationtype_advancedproofingissue"></span><span id="ANNOTATIONTYPE_ADVANCEDPROOFINGISSUE"></span><dl> <dt>**AnnotationType \_AdvancedProofingIssue**</dt> <dt>60020</dt> </dl>     | Advanced 校對問題。<br/>                                                             |
| <span id="AnnotationType_Author"></span><span id="annotationtype_author"></span><span id="ANNOTATIONTYPE_AUTHOR"></span><dl> <dt>**AnnotationType \_作者**</dt> <dt>60019</dt> </dl>                                                                 | 檔的作者。<br/>                                                             |
| <span id="AnnotationType_CircularReferenceError"></span><span id="annotationtype_circularreferenceerror"></span><span id="ANNOTATIONTYPE_CIRCULARREFERENCEERROR"></span><dl> <dt>**AnnotationType \_CircularReferenceError**</dt> <dt>60022</dt> </dl> | 發生迴圈參考錯誤。<br/>                                               |
| <span id="AnnotationType_Comment"></span><span id="annotationtype_comment"></span><span id="ANNOTATIONTYPE_COMMENT"></span><dl> <dt>**AnnotationType \_批註**</dt> <dt>60003</dt> </dl>                                                             | 註解。 批註可以採用不同的表單，視應用程式而定。<br/>              |
| <span id="AnnotationType_ConflictingChange"></span><span id="annotationtype_conflictingchange"></span><span id="ANNOTATIONTYPE_CONFLICTINGCHANGE"></span><dl> <dt>**AnnotationType \_ConflictingChange**</dt> <dt>60018</dt> </dl>                     | 對檔所做的衝突變更。<br/>                                     |
| <span id="AnnotationType_DataValidationError"></span><span id="annotationtype_datavalidationerror"></span><span id="ANNOTATIONTYPE_DATAVALIDATIONERROR"></span><dl> <dt>**AnnotationType \_DataValidationError**</dt> <dt>60021</dt> </dl>             | 發生的資料驗證錯誤。<br/>                                                  |
| <span id="AnnotationType_DeletionChange"></span><span id="annotationtype_deletionchange"></span><span id="ANNOTATIONTYPE_DELETIONCHANGE"></span><dl> <dt>**AnnotationType \_DeletionChange**</dt> <dt>60012</dt> </dl>                                 | 對檔所做的刪除變更。<br/>                                        |
| <span id="AnnotationType_EditingLockedChange"></span><span id="annotationtype_editinglockedchange"></span><span id="ANNOTATIONTYPE_EDITINGLOCKEDCHANGE"></span><dl> <dt>**AnnotationType \_EditingLockedChange**</dt> <dt>60016</dt> </dl>             | 對檔所做的編輯鎖定變更。<br/>                                 |
| <span id="AnnotationType_Endnote"></span><span id="annotationtype_endnote"></span><span id="ANNOTATIONTYPE_ENDNOTE"></span><dl> <dt>**AnnotationType \_章節附註**</dt> <dt>60009</dt> </dl>                                                             | 檔的章節附註。<br/>                                                             |
| <span id="AnnotationType_ExternalChange"></span><span id="annotationtype_externalchange"></span><span id="ANNOTATIONTYPE_EXTERNALCHANGE"></span><dl> <dt>**AnnotationType \_ExternalChange**</dt> <dt>60017</dt> </dl>                                 | 對檔所做的外部變更。<br/>                                       |
| <span id="AnnotationType_Footer"></span><span id="annotationtype_footer"></span><span id="ANNOTATIONTYPE_FOOTER"></span><dl> <dt>**AnnotationType \_**</dt>頁尾 <dt>60007</dt> </dl>                                                                 | 檔中頁面的頁尾。<br/>                                                    |
| <span id="AnnotationType_Footnote"></span><span id="annotationtype_footnote"></span><span id="ANNOTATIONTYPE_FOOTNOTE"></span><dl> <dt>**AnnotationType \_註腳**</dt> <dt>60010</dt> </dl>                                                         | 檔中頁面的註腳。<br/>                                                  |
| <span id="AnnotationType_FormatChange"></span><span id="annotationtype_formatchange"></span><span id="ANNOTATIONTYPE_FORMATCHANGE"></span><dl> <dt>**AnnotationType \_FormatChange**</dt> <dt>60014</dt> </dl>                                         | 進行的格式變更。<br/>                                                          |
| <span id="AnnotationType_FormulaError"></span><span id="annotationtype_formulaerror"></span><span id="ANNOTATIONTYPE_FORMULAERROR"></span><dl> <dt>**AnnotationType \_FormulaError**</dt> <dt>60004</dt> </dl>                                         | 公式中有錯誤。 公式錯誤通常包含紅色文字和驚嘆號。<br/> |
| <span id="AnnotationType_GrammarError"></span><span id="annotationtype_grammarerror"></span><span id="ANNOTATIONTYPE_GRAMMARERROR"></span><dl> <dt>**AnnotationType \_GrammarError**</dt> <dt>60002</dt> </dl>                                         | 語法錯誤，通常以綠色波浪線表示。 <br/>                           |
| <span id="AnnotationType_Header"></span><span id="annotationtype_header"></span><span id="ANNOTATIONTYPE_HEADER"></span><dl> <dt>**AnnotationType \_標頭**</dt> <dt>60006</dt> </dl>                                                                 | 檔中頁面的標頭。<br/>                                                    |
| <span id="AnnotationType_Highlighted"></span><span id="annotationtype_highlighted"></span><span id="ANNOTATIONTYPE_HIGHLIGHTED"></span><dl> <dt>**AnnotationType \_反白顯示**</dt> <dt>60008</dt> </dl>                                             | 反白顯示的內容，通常是以對比的背景色彩表示。<br/>               |
| <span id="AnnotationType_InsertionChange"></span><span id="annotationtype_insertionchange"></span><span id="ANNOTATIONTYPE_INSERTIONCHANGE"></span><dl> <dt>**AnnotationType \_InsertionChange**</dt> <dt>60011</dt> </dl>                             | 對檔進行的插入變更。<br/>                                      |
| <span id="AnnotationType_Mathematics"></span><span id="annotationtype_mathematics"></span><span id="ANNOTATIONTYPE_MATHEMATICS"></span><dl> <dt>**AnnotationType \_數學**</dt> <dt>60023</dt> </dl>                                             | 包含數學的文字範圍。<br/>                                                    |
| <span id="AnnotationType_MoveChange"></span><span id="annotationtype_movechange"></span><span id="ANNOTATIONTYPE_MOVECHANGE"></span><dl> <dt>**AnnotationType \_MoveChange**</dt> <dt>60013</dt> </dl>                                                 | 對檔所做的移動變更。<br/>                                            |
| <span id="AnnotationType_SpellingError"></span><span id="annotationtype_spellingerror"></span><span id="ANNOTATIONTYPE_SPELLINGERROR"></span><dl> <dt>**AnnotationType \_SpellingError**</dt> <dt>60001</dt> </dl>                                     | 拼寫錯誤，通常以紅色波浪線表示。 <br/>                                |
| <span id="AnnotationType_TrackChanges"></span><span id="annotationtype_trackchanges"></span><span id="ANNOTATIONTYPE_TRACKCHANGES"></span><dl> <dt>**AnnotationType \_TrackChanges**</dt> <dt>60005</dt> </dl>                                         | 對檔所做的變更。<br/>                                                 |
| <span id="AnnotationType_Unknown"></span><span id="annotationtype_unknown"></span><span id="ANNOTATIONTYPE_UNKNOWN"></span><dl> <dt>**AnnotationType \_未知**</dt>的 <dt>60000</dt> </dl>                                                             | 批註類型未知。<br/>                                                         |
| <span id="AnnotationType_UnsyncedChange"></span><span id="annotationtype_unsyncedchange"></span><span id="ANNOTATIONTYPE_UNSYNCEDCHANGE"></span><dl> <dt>**AnnotationType \_UnsyncedChange**</dt> <dt>60015</dt> </dl>                                 | 對檔進行的未同步變更。<br/>                                       |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                            |
| 標頭<br/>                   | <dl> <dt>Uiautomationclient.dll。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**IAnnotationProvider::AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)
</dt> <dt>

[**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)
</dt> <dt>

[**IUIAutomationPattern::CachedAnnotationTypeId**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_cachedannotationtypeid)
</dt> <dt>

[**IUIAutomationPattern::CurrentAnnotationTypeId**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_currentannotationtypeid)
</dt> <dt>

[**IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationType**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcachedannotationtypes)
</dt> <dt>

[**IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationType**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcurrentannotationtypes)
</dt> <dt>

**概念**
</dt> <dt>

[消費者介面自動化文字內容的支援](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>

 

