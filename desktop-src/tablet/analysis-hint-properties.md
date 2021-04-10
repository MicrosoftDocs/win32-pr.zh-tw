---
description: 針對分析提示節點的屬性，定義 (Guid) 的全域唯一識別碼 (請參閱 ICoNtextNode：： GetType) 。
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: 'Analysis 提示屬性 (Iaguid .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936546"
---
# <a name="analysis-hint-properties"></a>分析提示屬性

針對分析提示節點的屬性，定義 (Guid) 的全域唯一識別碼 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。

下表描述每個常數所參考的資訊。



| 常數                                                                                                                                                                                                                                  | 描述                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <dt>**GUID \_ AHP \_ ALLOWPARTIALDICTIONARYTERMS**</dt> </dl>       | 分析提示是否允許部分字典詞彙。<br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <dt>**GUID \_ AHP \_ ANALYSISHINTNAME**</dt> </dl>                                        | 分析提示的名稱。<br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <dt>**GUID \_ AHP \_ COERCETOFACTOID**</dt> </dl>                                           | 筆跡分析器是否會限制其在提示區域內的筆墨分析，以符合模擬。<br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <dt>**GUID \_ AHP \_ ENABLEDUNICODECHARACTERRANGES**</dt> </dl> | 提示包含字元陣列，這些字元代表此 InkRecognizer 支援的一組受限制的 unicode 字元集。<br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <dt>**GUID \_ AHP 的 \_ 模擬**</dt> </dl>                                                                   | 分析提示上的模擬程式。<br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <dt>**GUID \_ AHP \_ 指南**</dt> </dl>                                                                         | [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md)結構，表示分析提示的指南。<br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <dt>**GUID \_ AHP \_ PREFIXTEXT**</dt> </dl>                                                          | 分析提示的前置詞文字。<br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <dt>**GUID \_ AHP \_ SUFFIXTEXT**</dt> </dl>                                                          | 分析提示上的尾碼文字。<br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <dt>**GUID \_ AHP \_ TOPINKBREAKSONLY**</dt> </dl>                                        | 筆墨辨識結果中的多個 segmentations 是否已停用。<br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <dt>**GUID \_ AHP \_ 單詞表**</dt> </dl>                                                                | 字串的陣列，表示分析提示的字組清單。<br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <dt>**GUID \_ AHP \_ WORDMODE**</dt> </dl>                                                                | 筆跡分析器是否會針對分析提示的多重單字結果排列單一單字結果的優先順序。<br/>                                      |



## <a name="remarks"></a>備註

這些 Guid 是用來識別 [**IInkAnalyzer**](iinkanalyzer.md) 可在分析提示內容節點上設定的屬性 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。

若要取得或設定 [**ICoNtextNode**](icontextnode.md) 的一般屬性，請參閱 [內容節點屬性](context-node-properties.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Iaguid。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[內容節點屬性](context-node-properties.md)
</dt> <dt>

[內容節點類型](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer：： CreateAnalysisHint 方法**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer：： GetAnalysisHintsByName 方法**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[**ICoNtextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**ICoNtextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**ICoNtextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**ICoNtextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**ICoNtextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**ICoNtextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




