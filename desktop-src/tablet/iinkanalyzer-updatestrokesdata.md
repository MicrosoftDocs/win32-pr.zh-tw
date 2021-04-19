---
description: 更新指定筆劃的封包資料。
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'IInkAnalyzer：： UpdateStrokesData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972429"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a>IInkAnalyzer：： UpdateStrokesData 方法

更新指定筆劃的封包資料。

## <a name="syntax"></a>語法


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulStrokeIdsCount* \[在\]
</dt> <dd>

要更新的筆觸數目。

</dd> <dt>

*plStrokeIds* \[在\]
</dt> <dd>

包含筆觸識別碼的陣列。

</dd> <dt>

*ulStrokePacketDescriptionCount* \[在\]
</dt> <dd>

每個封包中的屬性數目。

</dd> <dt>

*pStrokePacketDescriptionGuids* \[在\]
</dt> <dd>

陣列，包含封包屬性識別碼。

</dd> <dt>

*pulPacketDataCountPerStroke* \[在\]
</dt> <dd>

陣列，其中包含每個筆劃中的封包數目。

</dd> <dt>

*plStrokePacketData* \[在\]
</dt> <dd>

陣列，其中包含筆觸的封包資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

*plStrokePacketData* 參數包含所有筆劃的封包資料。 *PStrokePacketDescriptionGuids* 參數包含 (guid) 的全域唯一識別碼，描述每個筆劃中每個點所包含的封包資料類型。 如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。

只有具有相同封包描述的筆觸可以在 **IInkAnalyzer：： UpdateStrokesData 方法** 的單一呼叫中更新。

這個方法不會更新筆墨分析器的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。

如果指定的筆劃沒有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會忽略識別碼。

如果任何指定的筆觸都沒有識別與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的筆劃，這個方法會傳回而不更新 **IInkAnalyzer**。

當 *plStrokeIds* 為 **Null** 時，這個方法會傳回錯誤碼。

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

[**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokeToCustomRecognizer 方法**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokesToCustomRecognizer 方法**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer：： ClearStrokeData 方法**](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




