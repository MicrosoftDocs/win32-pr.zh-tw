---
description: 針對所有與 IInkAnalyzer 相關聯的筆墨抓取10個分析替代項。
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: 'IInkAnalyzer：： GetAlternates 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: deb430c7573abc4e0964e83d508b98813e29e90d0185c6a9ff9a49bc529d1f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043725"
---
# <a name="iinkanalyzergetalternates-method"></a>IInkAnalyzer：： GetAlternates 方法

針對所有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的筆墨抓取10個分析替代項。

## <a name="syntax"></a>語法


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppAlternates* \[擴展\]
</dt> <dd>

與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯之所有筆墨的前10個 [**IAnalysisAlternate**](ianalysisalternate.md)物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppAlternates* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

Top 替代會傳回為集合的第一個替代。

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

[**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternatesForStrokes 方法**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： ModifyTopAlternate 方法**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

