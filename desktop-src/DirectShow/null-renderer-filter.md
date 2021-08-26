---
description: Null 轉譯器篩選器會捨棄它收到的每個範例，而不顯示或轉譯範例資料。
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: 'Null 轉譯器篩選 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 2686c64b3251616ac8cefbe81a77282e5b1a7c6847ef965b6361759118b74756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050878"
---
# <a name="null-renderer-filter"></a>Null 轉譯器篩選

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

Null 轉譯器篩選器會捨棄它收到的每個範例，而不顯示或轉譯範例資料。



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) |
| 輸入 pin 媒體類型                    | 任何媒體類型                                                                                                       |
| 輸入 pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)               |
| 輸出 pin 媒體類型                   | 不適用。                                                                                                      |
| 輸出 pin 介面                    | 不適用。                                                                                                      |
| 篩選 CLSID                             | CLSID \_ NullRenderer                                                                                                  |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                                                    |
| 可執行檔                               | Qedit.dll                                                                                                            |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                                  |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                        |



 

## <a name="remarks"></a>備註

當圖形中的輸出釘選需要下游連接，但您不想從該 pin 轉譯資料時，請使用此篩選器。 藉由將輸出連接連接到 Null 轉譯器，您就可以完成連接，而不會轉譯資料。

雖然此篩選不會轉譯任何範例，但它會在捨棄範例之前等候每個樣本的呈現時間。 因此，圖形會以一般費率執行。 如果您想要儘快執行圖形，請將參考時鐘設定為 **Null**。 如需詳細資訊，請參閱[設定 Graph 時鐘](setting-the-graph-clock.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Qedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow編輯服務物件](directshow-editing-services-objects.md)
</dt> </dl>

 

 




