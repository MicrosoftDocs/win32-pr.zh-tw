---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5acee341066ee5a456d412554ead3342c8513ae89e50a056a2372a291b0a88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052396"
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

 

 




