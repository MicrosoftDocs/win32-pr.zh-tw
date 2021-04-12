---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023699"
---
# <a name="tabbingnotcyclic"></a>TabbingNotCyclic

## <a name="text"></a>Text

此應用程式中的定位鍵不是迴圈的。 向前或向後定位將 {0} 不會回到相同的控制項。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

使用標準鍵盤導覽 (Tab 或 Shift + Tab) 時，您無法在起始元素變成結束元素之前，先移動驗證目標的專案樹狀結構， (藉由反轉遍歷方向來) 使用相同數目的按鍵。 例如，向前 (Tab) x 次的 tab 鍵，從專案 A (0) 到專案 A (x) ，然後將反向定位 (Shift + Tab) x 次不會導致元素 A (重新取得焦點。

這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為在流覽之後，沒有可預測的方法可以返回控制項。

## <a name="possible-causes"></a>可能的原因

-   元素或其父代是未正確執行 tab 鍵的自訂控制項。 例如，未正確設定 MSAA 狀態屬性。
-   某些應用程式（例如 [記事本]）會顯示此行為本質。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[鍵盤使用者介面設計指導方針](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 