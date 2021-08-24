---
description: 除了更新區域之外，每個視窗都有一個可見區域，可定義使用者可見的視窗部分。
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: 視窗區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3f751303d8a971d010ea7dabf7604c24db892f88d9a4029f0189d303cf5a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727408"
---
# <a name="window-regions"></a>視窗區域

除了更新區域之外，每個視窗都有一個 *可見區域* ，可定義使用者可見的視窗部分。 只要視窗變更大小，或每次移動另一個視窗時，系統就會變更視窗的可見區域，使其遮蔽或公開視窗的一部分。 應用程式無法直接變更可見區域，但是系統會自動使用可見區域來建立針對視窗所抓取之任何顯示裝置內容的裁剪區域。

*裁剪區域* 會決定系統允許繪圖的位置。 當應用程式使用 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)、 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式來抓取顯示裝置內容時，系統會將裝置內容的裁剪區域設定為可見區域和更新區域的交集。 應用程式可以使用 [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)、 [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) 和 [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)等函式來變更裁剪區域，以進一步將繪圖限制為更新區域的特定部分。

WS \_ CLIPCHILDREN 和 ws \_ CLIPSIBLINGS 樣式會進一步指定系統如何計算視窗的可見區域。 如果視窗有一或兩個樣式，則可見區域會排除具有相同父視窗) 的任何子視窗或同級視窗 (視窗。 因此，在這些視窗中 intrude 的繪圖一律會被裁剪。

 

 



