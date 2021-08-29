---
description: 將多個筆劃的筆觸資料新增至自訂辨識器節點。
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'IInkAnalyzer：： AddStrokesToCustomRecognizer 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9c50bcd1faa9df94847e3100309fc8598511dd760fa5efd6ccdf84812020fd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719217"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a>IInkAnalyzer：： AddStrokesToCustomRecognizer 方法

將多個筆劃的筆觸資料新增至自訂辨識器節點。

## <a name="syntax"></a>語法


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulStrokeIdsCount* \[在\]
</dt> <dd>

要加入的筆劃數目。

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

</dd> <dt>

*pCustomRecognizer* \[在\]
</dt> <dd>

要加入筆劃之 **CustomRecognizer** 類型的 [**ICoNtextNode**](icontextnode.md) 。

</dd> <dt>

*ppCoNtextNodeStrokeAddedTo* \[擴展\]
</dt> <dd>

筆跡分析器新增筆劃的 [**ICoNtextNode**](icontextnode.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppCoNtextNodeStrokeAddedTo* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

當 *ppCoNtextNodeStrokeAddedTo* 為 **Null** 時，表示呼叫端對方法的傳回值不感興趣。

[**IInkAnalyzer**](iinkanalyzer.md)會將筆劃新增至類型 **CustomRecognizer** 的 [**ICoNtextNode**](icontextnode.md) (請參閱) 的 [內容節點類型](context-node-types.md)。 此節點位於根節點的子節點集合中 (請參閱 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 方法) 。

[**IInkAnalyzer**](iinkanalyzer.md)會將使用中輸入執行緒的文化特性識別碼指派給筆劃，然後將筆劃加入至 **CustomRecognizer** 節點下的第一個 **UnclassifiedInk** 節點。 如果沒有 **UnclassifiedInk** 節點存在，則會建立它。 如果與 **CustomRecognizer** 節點相關聯的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)不支援文化特性識別碼，則 **IInkAnalyzer** 會繼續分析並產生 [**IAnalysisWarning**](ianalysiswarning.md)警告。 此警告的 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) 值為 **AnalysisWarningCode \_ LanguageIdNotRespected**。

*plStrokePacketData* 包含所有筆劃的封包資料。 *pStrokePacketDescriptionGuids* 包含 (guid) 的全域唯一識別碼，描述每個筆劃中每個點所包含的封包資料類型。 如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。

> [!Note]  
> **IInkAnalyzer：： AddStrokesToCustomRecognizer 方法** 的單一呼叫中只能新增具有相同封包描述的筆劃。

 

這個方法會將中途區域擴展至區域目前值的聯集，以及加入之筆劃的周框方塊。

在下列情況下， [**IInkAnalyzer**](iinkanalyzer.md)會傳回 **E \_ INVALIDARG** 的 **HRESULT** 。

-   [**IInkAnalyzer**](iinkanalyzer.md)已經包含一個筆觸，其識別碼與要加入的其中一個筆劃具有相同的識別碼。
-   *PCustomRecognizer* 參數包含與不同 [**IInkAnalyzer**](iinkanalyzer.md)物件相關聯的自訂辨識器節點。
-   *PCustomRecognizer* 參數包含的 [**ICoNtextNode**](icontextnode.md)不是 **CustomRecognizer** 類型。

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

[內容節點類型](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokeToCustomRecognizer 方法**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer：： CreateCustomRecognizer 方法**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

