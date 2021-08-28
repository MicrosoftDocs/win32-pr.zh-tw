---
description: 為 ICoNtextNode 的屬性定義全域唯一識別碼 (Guid) 。
ms.assetid: 14992253-c384-43c1-9465-e015ea2348db
title: '內容節點屬性 (Iaguid .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNP_ALIGNMENTLEVEL
- GUID_CNP_ASCENDERS
- GUID_CNP_BASELINE
- GUID_CNP_CONFIDENCELEVEL
- GUID_CNP_CUSTOMRECOGNIZERID
- GUID_CNP_DESCENDERS
- GUID_CNP_MIDLINE
- GUID_CNP_NODEDATA
- GUID_CNP_RECOGNIZEDSTRING
- GUID_CNP_ROTATEDBOUNDINGBOX
- GUID_CNP_SEMANTICTYPE
- GUID_CNP_SHAPENAME
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: d8e151103c17a7f19a648b39ba4d6dfdae387886e52af287a80530b5c3cf1b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967727"
---
# <a name="context-node-properties"></a>內容節點屬性

為 [**ICoNtextNode**](icontextnode.md)的屬性定義全域唯一識別碼 (guid) 。

下表描述每個常數所參考的資訊。



| 常數                                                                                                                                                                                                 | 描述                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_CNP_ALIGNMENTLEVEL"></span><span id="guid_cnp_alignmentlevel"></span><dl> <dt>**GUID \_ CNP \_ ALIGNMENTLEVEL**</dt> </dl>             | 段落的對齊層級。<br/>                                                                                                               |
| <span id="GUID_CNP_ASCENDERS"></span><span id="guid_cnp_ascenders"></span><dl> <dt>**GUID \_ CNP \_ ASCENDERS**</dt> </dl>                            | 筆墨單字的 ascenders。<br/>                                                                                                                     |
| <span id="GUID_CNP_BASELINE"></span><span id="guid_cnp_baseline"></span><dl> <dt>**GUID \_ CNP \_ 基準**</dt> </dl>                               | 筆墨單字的基線。<br/>                                                                                                                      |
| <span id="GUID_CNP_CONFIDENCELEVEL"></span><span id="guid_cnp_confidencelevel"></span><dl> <dt>**GUID \_ CNP \_ CONFIDENCELEVEL**</dt> </dl>          | 辨識結果中的信賴等級。<br/>                                                                                                  |
| <span id="GUID_CNP_CUSTOMRECOGNIZERID"></span><span id="guid_cnp_customrecognizerid"></span><dl> <dt>**GUID \_ CNP \_ CUSTOMRECOGNIZERID**</dt> </dl> | 自訂辨識器節點之自訂筆跡辨識器的識別碼。<br/>                                                                         |
| <span id="GUID_CNP_DESCENDERS"></span><span id="guid_cnp_descenders"></span><dl> <dt>**GUID \_ CNP \_ 下行**</dt> </dl>                         | 筆墨單字的下行。<br/>                                                                                                                    |
| <span id="GUID_CNP_MIDLINE"></span><span id="guid_cnp_midline"></span><dl> <dt>**GUID \_ CNP \_ 中線**</dt> </dl>                                  | 筆墨單字的中線。<br/>                                                                                                                       |
| <span id="GUID_CNP_NODEDATA"></span><span id="guid_cnp_nodedata"></span><dl> <dt>**GUID \_ CNP \_ NODEDATA**</dt> </dl>                               | 影像或文字單字的影像資料或文字資料。<br/>                                                                                           |
| <span id="GUID_CNP_RECOGNIZEDSTRING"></span><span id="guid_cnp_recognizedstring"></span><dl> <dt>**GUID \_ CNP \_ RECOGNIZEDSTRING**</dt> </dl>       | 識別的字串。<br/>                                                                                                                            |
| <span id="GUID_CNP_ROTATEDBOUNDINGBOX"></span><span id="guid_cnp_rotatedboundingbox"></span><dl> <dt>**GUID \_ CNP \_ ROTATEDBOUNDINGBOX**</dt> </dl> | 旋轉的周框方塊。<br/>                                                                                                                         |
| <span id="GUID_CNP_SEMANTICTYPE"></span><span id="guid_cnp_semantictype"></span><dl> <dt>**GUID \_ CNP \_ SEMANTICTYPE**</dt> </dl>                   | 屬性包含用來定義批註之語義型別的相關資訊，例如，它是標注、批註等等。<br/> |
| <span id="GUID_CNP_SHAPENAME"></span><span id="guid_cnp_shapename"></span><dl> <dt>**GUID \_ CNP \_ SHAPENAME**</dt> </dl>                            | 筆墨繪圖節點的圖形名稱。<br/>                                                                                                            |



## <a name="remarks"></a>備註

這些 Guid 是用來識別 [**IInkAnalyzer**](iinkanalyzer.md) 可在 [**ICoNtextNode**](icontextnode.md)上設定的屬性。 筆墨分析器會根據內容節點的型別設定一些屬性資料 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。

若要取得或設定分析提示節點特有的屬性，請參閱 [**分析提示屬性**](analysis-hint-properties.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Iaguid。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[分析提示屬性](analysis-hint-properties.md)
</dt> <dt>

[內容節點類型](context-node-types.md)
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

 

 




