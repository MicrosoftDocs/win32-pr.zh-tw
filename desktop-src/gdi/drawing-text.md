---
description: 繪製文字
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: " (Windows GDI) 繪製文字"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691888"
---
# <a name="drawing-text-windows-gdi"></a> (Windows GDI) 繪製文字

在應用程式選取適當的字型之後，設定所需的文字格式設定選項，並計算文字字串的必要字元寬度和高度值，它可以藉由呼叫任何文字輸出函數來開始繪製字元和符號：

-   [DrawText](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [DrawTextEx](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [PolyTextOut](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [TabbedTextOut](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

當應用程式呼叫其中一個函式時，作業系統會將呼叫傳遞給圖形引擎，然後再將呼叫傳遞給適當的設備磁碟機。 在設備磁碟機層級，所有這些呼叫都是由一或多個對驅動程式專屬 [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) 或 [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) 函式的呼叫所支援。 應用程式會藉由呼叫 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)快速轉換成裝置的 **ExtTextOut** 呼叫，以達成最快的執行速度。 不過，在某些情況下，應用程式應該呼叫其他三個函式的其中一個：例如，若要在指定之矩形區域的框線內繪製多行文字，呼叫 [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)會更有效率。 若要使用對齊的文字資料行來建立多行資料表，呼叫 [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta)會更有效率。

 

 
