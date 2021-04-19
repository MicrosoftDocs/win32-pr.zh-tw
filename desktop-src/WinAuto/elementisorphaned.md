---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969487"
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

 

 




