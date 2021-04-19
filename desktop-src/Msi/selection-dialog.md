---
description: 這個強制回應對話方塊可讓使用者選取特定的專案。
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: 選取對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989083"
---
# <a name="selection-dialog"></a>選取對話方塊

這個強制回應對話方塊可讓使用者選取特定的專案。

[選取範圍] 對話方塊包含發佈數個事件的 [SelectionTree 控制項](selectiontree-control.md) 。 這些工作通常是由 [文字](text-control.md)、 [圖示](icon-control.md)或 [點陣圖](bitmap-control.md) 控制項所訂閱，這些控制項會顯示描述、大小、路徑，以及反白顯示專案的圖示。

對話方塊上有一個可發佈[SelectionBrowse ControlEvent](selectionbrowse-controlevent.md)並產生[流覽對話方塊](browse-dialog.md)的[按鈕控制項](pushbutton-control.md)。 流覽控制項可讓使用者選取目錄。

只有在呼叫 [CostInitialize 動作](costinitialize-action.md) 和 [CostFinalize 動作](costfinalize-action.md) 之後，才會填入選取樹狀目錄。

選取專案對話方塊通常用來選取功能。 這些功能會列為 SelectionTree 控制項中的專案，並使用 [功能資料表](feature-table.md)的 [標題] 資料行中顯示的簡短文字字串標示。 功能資料表的 [描述] 資料行中的文字字串會以 [SelectionDescription ControlEvent](selectiondescription-controlevent.md) 的形式發佈，並由 [選取範圍] 對話方塊中的 [文字控制項](text-control.md) 顯示。 選取樹狀結構控制項也會將控制碼發佈至反白專案的圖示。

 

 



