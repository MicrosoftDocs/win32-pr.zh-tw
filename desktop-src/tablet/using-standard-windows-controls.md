---
description: 盡可能使用標準 Windows 控制項，因為它們與 Microsoft Active Accessibility 的指導方針完全相容。 這包括 Windows (User32.dll) 所提供的控制項，以及 Windows 通用控制項程式庫 (Comctl32.dll) 。
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: 使用標準 Windows 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71beab38b4ee6ea6472a34b4edb190deed97731496eac7101859a9340c65ad0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449271"
---
# <a name="using-standard-windows-controls"></a>使用標準 Windows 控制項

盡可能使用標準 Windows 控制項，因為它們與 Microsoft Active Accessibility 的指導方針完全相容。 這包括 Windows (User32.dll) 所提供的控制項，以及 Windows 通用控制項程式庫 (Comctl32.dll) 。

每個標準 Windows 控制項都是特定類別的個別視窗，因此當焦點移至新的控制項時，就會通知協助工具輔助。 輔助工具可以決定控制項視窗類別，以及它可以傳送來查詢或改變控制項狀態的任何其他訊息。 輔助工具也可以識別父視窗內包含的所有子控制項，並識別任何控制項的父系。

某些常見的控制項非常有彈性，而且通常可以替代較不容易存取的自訂控制項和主控描繪的控制項。 例如，清單視圖可以取代主控描繪清單方塊，以顯示每個專案旁的核取方塊。 另一個範例是，增強型按鈕控制項可以顯示影像和文字。 之前，這需要使用自訂控制項。

 

 



