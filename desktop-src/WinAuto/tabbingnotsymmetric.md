---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6bda8de3e07f0ac6be3aa3a2a7bd750508dead1f5c2662391a056b258b36d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644098"
---
# <a name="tabbingnotsymmetric"></a>TabbingNotSymmetric

## <a name="text"></a>Text

向後定位和向前定位並不會產生相同的元素。 預期 {0} 但已接收 {1}

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

使用標準鍵盤流覽 (Tab 或 Shift + Tab) 時，如果迴圈的方向反轉，則無法在驗證目標的專案樹狀結構中重複執行的路徑。 例如，向前 (Tab) x 次的 tab 鍵，從專案 A (0) 到專案 A (x) ，然後將 (Shift + Tab) x 次，就會導致專案 A (0) 透過一組不同的中繼元素重新取得焦點。

這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員發生問題，因為進行中的動作會顯示為不穩定且無法預測。

## <a name="possible-causes"></a>可能的原因

-   多個元素或其父代是未正確執行 tab 鍵的自訂控制項。 例如，未正確設定 MSAA 狀態屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[鍵盤使用者介面設計指導方針](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 