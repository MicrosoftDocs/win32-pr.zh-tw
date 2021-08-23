---
description: Swapinputs 屬性會指定是否交換轉換輸入。 如果值為 TRUE，則會交換輸入。 預設值為 FALSE。
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: swapinputs 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b74d16d9b195f504188f4684cf234a5b0c7627274c6e74d57e6824df20a0c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951707"
---
# <a name="swapinputs-attribute"></a>swapinputs 屬性

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`swapinputs`屬性指定是否交換轉換輸入。 如果值為 **TRUE**，則會交換輸入。 預設值為 **FALSE**。

## <a name="possible-values"></a>可能的值

下列值定義為 TRUE： y、Y、t、T、1。 下列值定義為 FALSE： n、N、f、F、0 (零) 。

## <a name="applies-to"></a>套用至

[**過渡**](transition-element.md)

## <a name="remarks"></a>備註

根據預設，轉換會從所有較低優先順序層級的複合開始至轉換所在的圖層。 如果 `swapinputs` 屬性是1，則會反轉此方向。 如需有關 DES 所使用之分層模型的詳細資訊，請參閱 [時間軸模型](the-timeline-model.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 屬性](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



