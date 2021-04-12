---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372037"
---
# <a name="tabbedtounknownelement"></a>TabbedToUnknownElement

## <a name="text"></a>Text

Tab 鍵已移至目標 hwnd 外部的專案。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

使用標準鍵盤流覽 (Tab 或 Shift + Tab) 會導致焦點移至驗證目標的 HWND 之外。

AccChecker 會在執行任何驗證工作之前，將元素樹狀結構向上移至所選驗證目標的最上層 HWND。 如果選擇要驗證的 HWND 是更複雜的工作區的一部分，這會減少產生的偽造錯誤數目。

## <a name="possible-causes"></a>可能的原因

-   驗證目標不需要有定位的執行，就能提供完整的功能。
-   驗證期間的使用者互動，例如將焦點移至非目標 HWND，並干擾驗證程式。

 

 




