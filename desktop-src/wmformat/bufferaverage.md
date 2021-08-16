---
title: BufferAverage
description: BufferAverage 屬性包含變數位元速率 (VBR) 資料流程所需的平均緩衝區大小。
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- BufferAverage windows Media 格式
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd839bff96f5ba327e585f8608bd4612fc047d354c24fee972e507ea5ca681f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656118"
---
# <a name="bufferaverage"></a>BufferAverage

**BufferAverage** 屬性包含變數位元速率 (VBR) 資料流程所需的平均緩衝區大小。

## <a name="global-constant"></a>全域常數

g \_ wszBufferAverage

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

存取寫入器物件的 **IWMHeaderInfo3** 介面時，您可以加入或變更此值。 在其他物件 (中繼資料編輯器、讀取器和同步讀取器) ，此值是唯讀的。

寫入器會自動為每個 VBR 串流寫入 **BufferAverage** 值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




