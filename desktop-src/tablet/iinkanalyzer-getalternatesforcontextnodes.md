---
description: 抓取指定 ICoNtextNodes 集合中節點的分析替代項。
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc282906bae70a28f612a8c1fd0a5a67ea1343c73f5ededf0d6c85a8bfd60aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939857"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a>IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法

抓取指定 [**ICoNtextNodes**](icontextnodes.md) 集合中節點的分析替代項。

## <a name="syntax"></a>語法


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtextNodes* \[在\]
</dt> <dd>

傳回其分析替代專案的 [**ICoNtextNodes**](icontextnodes.md) 集合。

</dd> <dt>

*ulMaximumAlternates* \[在\]
</dt> <dd>

要傳回的最大替代專案數目。

</dd> <dt>

*ppAlternates* \[擴展\]
</dt> <dd>

包含分析替代專案的 [**IAnalysisAlternates**](ianalysisalternates.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppAlternates* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

Top [**IAnalysisAlternate**](ianalysisalternate.md) 會傳回為集合的第一個替代。

*PCoNtextNodes* 中的 [**ICoNtextNode**](icontextnode.md)物件不需要代表檔的相鄰區域。

針對節點中的每個分析提示， [**IInkAnalyzer**](iinkanalyzer.md) 只會傳回最上層的替代項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternatesForStrokes 方法**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： ModifyTopAlternate 方法**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

