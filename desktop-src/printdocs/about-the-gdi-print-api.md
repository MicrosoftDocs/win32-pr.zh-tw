---
description: GDI 列印 API 中函式的其中一個主要功能是支援裝置獨立性。
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: 關於 GDI 列印 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978305"
---
# <a name="about-the-gdi-print-api"></a><span data-ttu-id="2c325-103">關於 GDI 列印 API</span><span class="sxs-lookup"><span data-stu-id="2c325-103">About the GDI Print API</span></span>

<span data-ttu-id="2c325-104">GDI 列印 API 中函式的其中一個主要功能是支援裝置獨立性。</span><span class="sxs-lookup"><span data-stu-id="2c325-104">One of the chief features of the functions in the GDI print API is their support of device independence.</span></span> <span data-ttu-id="2c325-105">應用程式不會發出裝置特定的命令以在特定印表機或繪圖器上繪製輸出，而是從圖形裝置介面呼叫高階函式 (GDI) 。</span><span class="sxs-lookup"><span data-stu-id="2c325-105">Instead of issuing device-specific commands to draw output on a particular printer or plotter, an application calls high-level functions from the graphics device interface (GDI).</span></span> <span data-ttu-id="2c325-106">例如，若要列印點陣圖影像，應用程式可以呼叫 [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) 函式，並提供點陣圖的座標，以及識別來源和目的地裝置內容 (dc) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2c325-106">For example, to print a bitmapped image, an application can call the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function, supplying the coordinates for the bitmap as well as handles identifying the source and destination device contexts (DCs).</span></span> <span data-ttu-id="2c325-107">然後，印表機驅動程式會將對 **BitBlt** 的呼叫轉換為原始裝置命令。</span><span class="sxs-lookup"><span data-stu-id="2c325-107">The call to **BitBlt** is then converted to raw device commands by a printer driver.</span></span> <span data-ttu-id="2c325-108">設備磁碟機是動態連結程式庫 (DLL) ，可支援 (DDI) 的設備磁碟機介面。</span><span class="sxs-lookup"><span data-stu-id="2c325-108">A device driver is a dynamic-link library (DLL) that supports the device driver interface (DDI).</span></span> <span data-ttu-id="2c325-109">當設備磁碟機處理圖形引擎對 DDI 函式的呼叫時，會產生原始的裝置命令。</span><span class="sxs-lookup"><span data-stu-id="2c325-109">A device driver generates raw device commands when it processes calls to DDI functions made by the graphics engine.</span></span> <span data-ttu-id="2c325-110">印表機會在列印影像時處理這些命令。</span><span class="sxs-lookup"><span data-stu-id="2c325-110">The commands are processed by the printer when it prints the image.</span></span> <span data-ttu-id="2c325-111">這些命令的語法、數目和類型會因裝置而異。</span><span class="sxs-lookup"><span data-stu-id="2c325-111">The syntax, number, and type of these commands vary from device to device.</span></span>

<span data-ttu-id="2c325-112">本總覽提供下列主題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c325-112">This overview provides information on the following topics.</span></span>

<dl>

[<span data-ttu-id="2c325-113">預設列印介面</span><span class="sxs-lookup"><span data-stu-id="2c325-113">Default Printing Interface</span></span>](default-printing-interface.md)  
[<span data-ttu-id="2c325-114">印表機裝置內容</span><span class="sxs-lookup"><span data-stu-id="2c325-114">Printer Device Contexts</span></span>](printer-output.md)  
[<span data-ttu-id="2c325-115">印表機轉義</span><span class="sxs-lookup"><span data-stu-id="2c325-115">Printer Escapes</span></span>](printer-escapes.md)  
[<span data-ttu-id="2c325-116">WYSIWYG 顯示和輸出</span><span class="sxs-lookup"><span data-stu-id="2c325-116">WYSIWYG Display and Output</span></span>](wysiwyg-display-and-output.md)  
[<span data-ttu-id="2c325-117">每位使用者的 DEVMODE</span><span class="sxs-lookup"><span data-stu-id="2c325-117">Per-User DEVMODE</span></span>](per-user-devmode.md)  
</dl>

 

 
