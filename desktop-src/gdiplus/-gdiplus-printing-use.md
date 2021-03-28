---
description: 只要稍微調整您的程式碼，您就可以將 Windows GDI + 輸出傳送至印表機，而不是傳送至螢幕。
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: '列印 (GDI +) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b60010bcb63c553a96c5d70826f3fe0d3d4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972849"
---
# <a name="printing-gdi"></a>列印 (GDI +) 

只要稍微調整您的程式碼，您就可以將 Windows GDI + 輸出傳送至印表機，而不是傳送至螢幕。 若要在印表機上進行繪製，請取得印表機的裝置內容控制碼，並將該控制碼傳遞給 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 的函式。 將 GDI + 繪製命令放在 [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) 和 [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc)的呼叫之間。

下列主題涵蓋將 GDI + 輸出傳送至印表機的詳細資訊：

-   [將 GDI+ 輸出傳送至印表機](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [顯示 [列印] 對話方塊](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [藉由提供印表機控制代碼來最佳化列印](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



