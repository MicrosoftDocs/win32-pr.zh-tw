---
description: 清除 IInkAnalyzer 中的筆觸封包資料。
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'IInkAnalyzer：： ClearStrokeData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 823ceaa825b454af851fab43e233526285445c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469128"
---
# <a name="iinkanalyzerclearstrokedata-method"></a>IInkAnalyzer：： ClearStrokeData 方法

清除 [**IInkAnalyzer**](iinkanalyzer.md)中的筆觸封包資料。

## <a name="syntax"></a>語法


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lStrokeId* \[在\]
</dt> <dd>

已清除封包資料之筆劃的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

當筆觸的封包資料變更時（例如移動或轉換筆劃時），請使用這個方法。 當 [**IInkAnalyzer**](iinkanalyzer.md)需要筆劃封包資料來自已清除封包資料的筆劃時，就會引發 [**\_ IAnalysisEvents：： UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)事件。

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

[**IInkAnalyzer：： UpdateStrokesData 方法**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




