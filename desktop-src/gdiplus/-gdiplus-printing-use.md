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
# <a name="printing-gdi"></a><span data-ttu-id="8f8b7-103">列印 (GDI +) </span><span class="sxs-lookup"><span data-stu-id="8f8b7-103">Printing (GDI+)</span></span>

<span data-ttu-id="8f8b7-104">只要稍微調整您的程式碼，您就可以將 Windows GDI + 輸出傳送至印表機，而不是傳送至螢幕。</span><span class="sxs-lookup"><span data-stu-id="8f8b7-104">With a few minor adjustments to your code, you can send Windows GDI+ output to a printer rather than to a screen.</span></span> <span data-ttu-id="8f8b7-105">若要在印表機上進行繪製，請取得印表機的裝置內容控制碼，並將該控制碼傳遞給 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 的函式。</span><span class="sxs-lookup"><span data-stu-id="8f8b7-105">To draw on a printer, obtain a device context handle for the printer and pass that handle to a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="8f8b7-106">將 GDI + 繪製命令放在 [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) 和 [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc)的呼叫之間。</span><span class="sxs-lookup"><span data-stu-id="8f8b7-106">Place your GDI+ drawing commands in between calls to [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="8f8b7-107">下列主題涵蓋將 GDI + 輸出傳送至印表機的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="8f8b7-107">The following topics cover sending GDI+ output to printers in more detail:</span></span>

-   [<span data-ttu-id="8f8b7-108">將 GDI+ 輸出傳送至印表機</span><span class="sxs-lookup"><span data-stu-id="8f8b7-108">Sending GDI+ Output to a Printer</span></span>](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   <span data-ttu-id="8f8b7-109">[顯示 [列印] 對話方塊](-gdiplus-displaying-a-print-dialog-box-use.md)</span><span class="sxs-lookup"><span data-stu-id="8f8b7-109">[Displaying a Print Dialog Box](-gdiplus-displaying-a-print-dialog-box-use.md)</span></span>
-   [<span data-ttu-id="8f8b7-110">藉由提供印表機控制代碼來最佳化列印</span><span class="sxs-lookup"><span data-stu-id="8f8b7-110">Optimizing Printing by Providing a Printer Handle</span></span>](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



