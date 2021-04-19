---
description: 抓取集合中位於指定索引位置的 IAnalysisAlternate 物件。
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'IAnalysisAlternates：： GetAnalysisAlternate 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966727"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a>IAnalysisAlternates：： GetAnalysisAlternate 方法

抓取集合中位於指定索引位置的 [**IAnalysisAlternate**](ianalysisalternate.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulIndex* \[在\]
</dt> <dd>

要取得之 [**IAnalysisAlternate**](ianalysisalternate.md) 物件的以零為基底的索引。

</dd> <dt>

*ppAlternate* \[擴展\]
</dt> <dd>

集合中位於指定索引位置之 [**IAnalysisAlternate**](ianalysisalternate.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，當您不再需要流量分析替代時，請在 ppAlternate 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \*  。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

