---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315280"
---
# <a name="treemightbecyclic"></a>TreeMightBeCyclic

## <a name="text"></a>Text

樹狀結構是 {0} 層級深度。 這可能表示存取範圍樹狀結構是迴圈的，因此似乎是無限的。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

專案樹狀結構是迴圈的，樹狀目錄深度可能是無限的。

這個問題會讓依賴螢幕讀取器和鍵盤進行流覽的人員遇到問題，因為目標應用程式中的專案的控制不會有明顯的限制。

## <a name="possible-causes"></a>可能的原因

多個專案（或其父代）是未正確執行定位的自訂控制項。 例如，[MSAA [狀態](state-property.md) ] 屬性未正確更新。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[鍵盤使用者介面設計指導方針](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Windows 使用者經驗互動指導方針-鍵盤](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 