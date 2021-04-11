---
description: 抓取值，這個值會指出 ICoNtextNode 物件是否已部分擴展或完整填入。
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'ICoNtextNode：： GetPartiallyPopulated 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b05cb8aae681a7302ae7da40a7412cf828fc159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113385"
---
# <a name="icontextnodegetpartiallypopulated-method"></a>ICoNtextNode：： GetPartiallyPopulated 方法

抓取值，這個值會指出 [**ICoNtextNode**](icontextnode.md) 物件是否已部分擴展或完整填入。

## <a name="syntax"></a>語法


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pfPartiallyPopulated* \[擴展\]
</dt> <dd>

**變異 \_** 如果這個 [**ICoNtextNode**](icontextnode.md)物件不包含完整資料，則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用這個方法。 如需詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

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

[**ICoNtextNode::SetPartiallyPopulated**](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[**ICoNtextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**\_IAnalysisProxyEvents：:P opulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




