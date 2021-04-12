---
description: 抓取指定之筆劃的型別。
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'IInkAnalyzer：： GetStrokeType 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191403"
---
# <a name="iinkanalyzergetstroketype-method"></a>IInkAnalyzer：： GetStrokeType 方法

抓取指定之筆劃的型別。

## <a name="syntax"></a>語法


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lStrokeId* \[在\]
</dt> <dd>

筆觸識別碼。

</dd> <dt>

*pStrokeType* \[擴展\]
</dt> <dd>

指定之筆劃的分類。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果筆劃的類型是 [**StrokeType**](stroketype.md) 值 StrokeType 非 \_ 分類，則 [**IInkAnalyzer**](iinkanalyzer.md) 會在筆跡分析期間將筆劃分類。 否則， **IInkAnalyzer** 會使用筆劃上設定的類型。

[**IInkAnalyzer**](iinkanalyzer.md)不會將筆劃類型值設定為筆跡分析的一部分。 若要指定或變更筆觸類型，請使用 [**IInkAnalyzer：： SetStrokeType 方法**](iinkanalyzer-setstroketype.md) 或 [**IInkAnalyzer：： SetStrokesType 方法**](iinkanalyzer-setstrokestype.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer：： SetStrokeType 方法**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[**IInkAnalyzer：： SetStrokesType 方法**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




