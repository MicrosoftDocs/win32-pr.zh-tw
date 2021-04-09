---
description: 修改指出此 ICoNtextNode 為部分或完整擴展的值。
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'ICoNtextNode：： SetPartiallyPopulated 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026252"
---
# <a name="icontextnodesetpartiallypopulated-method"></a>ICoNtextNode：： SetPartiallyPopulated 方法

修改指出此 [**ICoNtextNode**](icontextnode.md) 為部分或完整擴展的值。

## <a name="syntax"></a>語法


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fPartiallyPopulated* \[在\]
</dt> <dd>

**變異 \_** 如果已部分填入此 [**ICoNtextNode**](icontextnode.md) ，則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用這個方法。 如需詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

虛擬化您的檔樹狀結構時，請務必設定 PropertyGuidsForCoNtextNodes RotatedBoundingBox 值， (在所有 CoNtextNode 物件上使用 CoNtextNode. AddPropertyValue) 。 RotatedBoundingBox 屬性是由 InkAnalyzer 計算，而且根據預設，應該在所有寫入 CoNtextNodes 上。 但是，如果您的應用程式會藉由設定 PartiallyPopulated 屬性來虛擬化分析結果，則在處理 PopulateCoNtextNode 事件時，請務必填入 RotatedBoundingBox 屬性。 若無法設定 RotatedBoundingBox 屬性，將會導致目前的分析作業中使用的檔資料可能更多

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**\_IAnalysisProxyEvents：:P opulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[**ICoNtextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**ICoNtextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




