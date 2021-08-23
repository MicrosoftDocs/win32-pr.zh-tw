---
description: 將單一筆劃的筆觸資料新增至 IInkAnalyzer，並將使用中輸入執行緒的文化特性識別碼指派給筆劃。
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: 'IInkAnalyzer：： AddStroke 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f7ba08e779e115c243918d94e5b41e8a7d77f54fab92b045274135ead2ae0264
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590588"
---
# <a name="iinkanalyzeraddstroke-method"></a>IInkAnalyzer：： AddStroke 方法

將單一筆劃的筆觸資料新增至 [**IInkAnalyzer**](iinkanalyzer.md) ，並將使用中輸入執行緒的文化特性識別碼指派給筆劃。

## <a name="syntax"></a>語法


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lStrokeId* \[在\]
</dt> <dd>

要加入之筆劃的識別碼。

</dd> <dt>

*ulStrokePacketDataCount* \[在\]
</dt> <dd>

筆劃中的封包數目。

</dd> <dt>

*plStrokePacketData* \[在\]
</dt> <dd>

陣列，其中包含筆劃的封包資料。

</dd> <dt>

*ulStrokePacketDescriptionCount* \[在\]
</dt> <dd>

每個封包中的封包屬性數目。

</dd> <dt>

*pStrokePacketDescriptionGuids* \[在\]
</dt> <dd>

陣列，包含封包屬性識別碼。

</dd> <dt>

*ppCoNtextNodeStrokeAddedTo* \[擴展\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md)加入筆劃之 [**ICoNtextNode**](icontextnode.md)的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 *ppCoNtextNodeStrokeAddedTo* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

當 *ppCoNtextNodeStrokeAddedTo* 為 **Null** 時，表示呼叫端對方法的傳回值不感興趣。

[**IInkAnalyzer**](iinkanalyzer.md)會將筆劃新增至類型 UnclassifiedInk 的 [**ICoNtextNode**](icontextnode.md) (請參閱) 的 [內容節點類型](context-node-types.md)。 此節點位於根節點的子節點集合中 (請參閱 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md) 和 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 方法) 。

[**IInkAnalyzer**](iinkanalyzer.md)會將使用中輸入執行緒的文化特性識別碼指派給筆劃，然後將筆劃加入至筆墨分析器根節點下的第一個 UnclassifiedInk 內容節點，其中包含具有相同文化特性識別碼的筆觸。 如果筆墨分析器沒有具有相同文化特性識別碼的節點，它會在其根節點下建立新的 UnclassifiedInk 內容節點，並將筆劃加入新的 UnclassifiedInk 內容節點。

*plStrokePacketData* 包含筆劃中所有點的封包資料。 *pStrokePacketDescriptionGuids* 包含 (guid) 的全域唯一識別碼，描述筆劃中每個點所包含的封包資料類型。 如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。

這個方法會將中途區域展開至區域目前值的聯集，以及已加入筆劃的周框方塊。

如果 [**IInkAnalyzer**](iinkanalyzer.md)已包含具有相同筆觸識別碼的筆劃，則 **IInkAnalyzer** 會傳回 **E \_ INVALIDARG** 的 **HRESULT** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： RemoveStroke 方法**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer：： RemoveStrokes 方法**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

