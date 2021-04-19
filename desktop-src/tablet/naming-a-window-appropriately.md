---
description: 適當地命名視窗和設定 Tablet PC 的視窗標題。
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: 適當地命名視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988329"
---
# <a name="naming-a-window-appropriately"></a>適當地命名視窗

將使用者易記的標題指派給每個視窗，即使視窗或其標題為不可見。 這可讓語音功能識別視窗和視窗階層。 此建議適用于所有視窗：具有可見畫面格的最上層視窗;子視窗，例如浮動調色板;自訂控制項;工具列以及視窗內的窗格（實作為子視窗時）。

有三種方式可以設定視窗標題：

-   呼叫 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或相關函式時，請在資源腳本中設定字串。
-   呼叫 [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) 函數。
-   使用在 [對話方塊中命名控制項](naming-controls-in-dialog-boxes.md)中所述的技術，在對話方塊中定義控制項的名稱。 這是標記編輯控制項的唯一方法，因為設定控制項內建標籤會變更控制項的內容。

您可以使用 Microsoft Active Accessibility 或 WM GETTEXT 訊息來查詢標題 \_ 。

如需使用 Active Accessibility 來查詢標題的詳細資訊，請參閱 [協助工具](/windows/desktop/accessibility) 一節。

 

 
