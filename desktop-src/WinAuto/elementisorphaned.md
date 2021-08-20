---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf30478d7ca68f823cd3d87158f92af71ae1afb14bf8d17295eedee2b4a144d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829365"
---
# <a name="elementisorphaned"></a>ElementIsOrphaned

## <a name="text"></a>Text

元素是樹狀結構中的孤立 IAccessible

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

針對指定座標取得之物件 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的位址是專案樹狀結構中孤立元素的參考。

這個問題適用于依賴螢幕閱讀程式和鍵盤進行導覽的人員，因為元素將被視為不可見，而且不會向使用者宣告。

## <a name="possible-causes"></a>可能的原因

-   驗證期間的使用者互動，例如將焦點移至非目標 HWND，並干擾驗證程式。
-   不正確或不正確 MSAA 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[流覽點擊測試和螢幕位置](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




