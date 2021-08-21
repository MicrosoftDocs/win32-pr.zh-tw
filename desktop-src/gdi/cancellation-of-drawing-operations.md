---
description: 當複雜的繪圖應用程式執行冗長的圖形作業時，它們會耗用寶貴的系統資源。
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: 取消繪圖作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2ddf90842ed7da612e046f8cc44bc8972b236232f3757bd31a295377eafab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470028"
---
# <a name="cancellation-of-drawing-operations"></a>取消繪圖作業

當複雜的繪圖應用程式執行冗長的圖形作業時，它們會耗用寶貴的系統資源。 藉由充分利用系統的多工功能，應用程式可以使用執行緒和 [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) 函數來管理這些作業。 例如，如果執行緒 A 所執行的圖形作業正在耗用所需的資源，執行緒 B 可以呼叫 CancelDC 函式來終止該作業。

 

 



