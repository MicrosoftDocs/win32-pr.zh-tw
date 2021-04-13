---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300999"
---
# <a name="controltypenoexpectedpatternssupported"></a>ControlTypeNoExpectedPatternsSupported

## <a name="text"></a>Text

ControlType 為的元素 {0} 應至少支援下列其中一個模式： {1} 但此元素不會

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

專案的消費者介面自動化支援不符合消費者介面自動化規格，因為元素至少應支援其中一個提供的控制項模式清單，但不符合。 如此一來，這個元素可能無法正確地公開給輔助技術，這對使用者體驗可能會有嚴重的影響。

## <a name="possible-causes"></a>可能的原因

-   不完整的消費者介面自動化執行。
-   未正確設定 ControlType 屬性。

## <a name="remarks"></a>備註

AccChecker 會針對不定的進度列記錄這個錯誤訊息。 您可以忽略此訊息及/或將它新增至隱藏清單。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




