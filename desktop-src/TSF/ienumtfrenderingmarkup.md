---
title: IEnumTfRenderingMarkup 介面
description: IEnumTfRenderingMarkup 介面是由 TSF 管理員所執行，並由應用程式使用。 此介面可透過 ITfCoNtextRenderingMarkup GetRenderingMarkup 來抓取，並列舉轉譯標記資訊。
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- IEnumTfRenderingMarkup 介面文字服務架構
- IEnumTfRenderingMarkup 介面文字服務架構，說明
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023887"
---
# <a name="ienumtfrenderingmarkup-interface"></a>IEnumTfRenderingMarkup 介面

**IEnumTfRenderingMarkup** 介面是由 TSF 管理員所執行，並由應用程式使用。 此介面可由 [ITfCoNtextRenderingMarkup：： GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) 抓取，並列舉轉譯標記資訊。



| IEnumTfRenderingMarkup 方法            | Description                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [複製](ienumtfrenderingmarkup-clone.md) | **IEnumTfRenderingMarkup：： Clone** 方法會建立枚舉器物件的複本。                                                                  |
| [下一步](ienumtfrenderingmarkup-next.md)   | **IEnumTfRenderingMarkup：： Next** 方法會從目前位置取得列舉順序中指定的元素數目。          |
| [重設](ienumtfrenderingmarkup-reset.md) | **IEnumTfRenderingMarkup：： Reset** 方法會將目前的位置移至列舉序列的開頭，以重設列舉值物件。 |
| [Skip](ienumtfrenderingmarkup-skip.md)   | **IEnumTfRenderingMarkup：： Skip** 方法會從目前位置取得列舉順序中指定的元素數目。          |



 

## <a name="members"></a>成員

**IEnumTfRenderingMarkup** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。

## <a name="remarks"></a>備註

> [!Note]  
> 這個介面目前不在公用標頭檔中。 若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。

 

 

 