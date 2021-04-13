---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c5807fa04f69271f2a2d38e7014b1cd17d4eaa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311229"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a>AccessibleObjectFromPointReturnedNullIAccessible

## <a name="text"></a>Text

AccessibleObjectFromPoint ({0} ， {1}) 傳回 null

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

針對指定座標取得之 UI 元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面位址為 Null。

## <a name="possible-causes"></a>可能的原因

-   驗證期間的使用者互動，例如將焦點移至非目標 HWND，並干擾驗證程式。
-   不正確或不正確 MSAA 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[流覽點擊測試和螢幕位置](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




