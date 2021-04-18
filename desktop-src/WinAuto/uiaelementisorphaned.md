---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964974"
---
# <a name="uiaelementisorphaned"></a>UiaElementIsOrphaned

## <a name="text"></a>Text

元素是樹狀結構中的孤立 AutomationElement

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

針對指定座標取得之物件 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面的位址是專案樹狀結構中孤立元素的參考。

這個問題適用于依賴螢幕閱讀程式和鍵盤進行導覽的人員，因為元素將被視為不可見，而且不會向使用者宣告。

## <a name="possible-causes"></a>可能的原因

-   驗證期間的使用者互動，例如將焦點移至非目標 HWND，並干擾驗證程式。
-   消費者介面自動化的執行不正確或無效。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IUIAutomationElement.ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




