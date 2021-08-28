---
description: 抓取位於指定之索引處的 IInkAnalysisRecognizer。
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'IInkAnalysisRecognizers：： GetInkAnalysisRecognizer 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6755b82beaea1bec9a38b9c15ea57a97c1d19fc4eecb5a2b55c80e2070562d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967337"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a>IInkAnalysisRecognizers：： GetInkAnalysisRecognizer 方法

抓取位於指定之索引處的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 。

## <a name="syntax"></a>語法


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulIndex* \[在\]
</dt> <dd>

要取得之 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 物件的以零為基底的索引。

</dd> <dt>

*ppInkAnalysisRecognizer* \[擴展\]
</dt> <dd>

位於指定索引處之 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 ppInkAnalysisRecognizer 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要使用筆墨分析辨識器時）。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

