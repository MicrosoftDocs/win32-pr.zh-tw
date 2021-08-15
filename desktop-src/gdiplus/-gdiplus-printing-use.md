---
description: 只要稍微調整您的程式碼，您就可以將 Windows GDI+ 輸出傳送至印表機，而不是傳送至螢幕。
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: '列印 (GDI+) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f5807c976ef3224bc4b66afc0bb8637d79d725f12cbdebd3199d9710ae529a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885079"
---
# <a name="printing-gdi"></a>列印 (GDI+) 

只要稍微調整您的程式碼，您就可以將 Windows GDI+ 輸出傳送至印表機，而不是傳送至螢幕。 若要在印表機上進行繪製，請取得印表機的裝置內容控制碼，並將該控制碼傳遞給 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 的函式。 將您的 GDI+ 繪製命令放在[StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw)和[EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc)的呼叫之間。

下列主題涵蓋將 GDI+ 輸出傳送至印表機的詳細資訊：

-   [將 GDI+ 輸出傳送至印表機](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [顯示 [列印] 對話方塊](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [藉由提供印表機控制代碼來最佳化列印](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



