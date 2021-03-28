---
description: 裝置獨立性是 Microsoft Windows 的主要功能之一。
ms.assetid: f2a4c4cf-55e9-4129-8067-256552af49d2
title: 關於裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b686ec8b48492658f19531cb42161c043f178d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114244"
---
# <a name="about-device-contexts"></a><span data-ttu-id="bef51-103">關於裝置內容</span><span class="sxs-lookup"><span data-stu-id="bef51-103">About Device Contexts</span></span>

<span data-ttu-id="bef51-104">裝置獨立性是 Microsoft Windows 的主要功能之一。</span><span class="sxs-lookup"><span data-stu-id="bef51-104">Device independence is one of the chief features of Microsoft Windows.</span></span> <span data-ttu-id="bef51-105">應用程式可以在各種裝置上繪製和列印輸出。</span><span class="sxs-lookup"><span data-stu-id="bef51-105">Applications can draw and print output on a variety of devices.</span></span> <span data-ttu-id="bef51-106">支援此裝置獨立性的套裝軟體含在兩個動態連結程式庫中。</span><span class="sxs-lookup"><span data-stu-id="bef51-106">The software that supports this device independence is contained in two dynamic-link libraries.</span></span> <span data-ttu-id="bef51-107">第一個是 Gdi.dll，稱為「圖形裝置介面」， (GDI) ;第二個稱為設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bef51-107">The first, Gdi.dll, is referred to as the graphics device interface (GDI); the second is referred to as a device driver.</span></span> <span data-ttu-id="bef51-108">第二個名稱會取決於應用程式繪製輸出的裝置。</span><span class="sxs-lookup"><span data-stu-id="bef51-108">The name of the second depends on the device where the application draws output.</span></span> <span data-ttu-id="bef51-109">例如，如果應用程式在 VGA 顯示器上的視窗工作區中繪製輸出，此程式庫會 Vga.dll;如果應用程式在 Epson FX-80 印表機上列印輸出，則會 Epson9.dll 此程式庫。</span><span class="sxs-lookup"><span data-stu-id="bef51-109">For example, if the application draws output in the client area of its window on a VGA display, this library is Vga.dll; if the application prints output on an Epson FX-80 printer, this library is Epson9.dll.</span></span>

<span data-ttu-id="bef51-110">應用程式必須通知 GDI 載入特定的設備磁碟機，並在載入驅動程式之後，準備裝置以進行繪製作業 (例如選取線條色彩和寬度、筆刷模式和色彩、字型字型、裁剪區域等) 。</span><span class="sxs-lookup"><span data-stu-id="bef51-110">An application must inform GDI to load a particular device driver and, once the driver is loaded, to prepare the device for drawing operations (such as selecting a line color and width, a brush pattern and color, a font typeface, a clipping region, and so on).</span></span> <span data-ttu-id="bef51-111">這些工作是藉由建立和維護裝置內容 (DC) 來完成。</span><span class="sxs-lookup"><span data-stu-id="bef51-111">These tasks are accomplished by creating and maintaining a device context (DC).</span></span> <span data-ttu-id="bef51-112">DC 是一種結構，它會定義一組繪圖物件和其相關聯的屬性，以及影響輸出的圖形模式。</span><span class="sxs-lookup"><span data-stu-id="bef51-112">A DC is a structure that defines a set of graphic objects and their associated attributes, and the graphic modes that affect output.</span></span> <span data-ttu-id="bef51-113">繪圖物件包括用來繪製線條的畫筆、繪製和填滿的筆刷、用來複製或滾動螢幕元件的點陣圖、定義可用色彩集的調色板、用於裁剪的區域、其他作業，以及繪製和繪製作業的路徑。</span><span class="sxs-lookup"><span data-stu-id="bef51-113">The graphic objects include a pen for line drawing, a brush for painting and filling, a bitmap for copying or scrolling parts of the screen, a palette for defining the set of available colors, a region for clipping and other operations, and a path for painting and drawing operations.</span></span> <span data-ttu-id="bef51-114">不同于大部分的結構，應用程式永遠不會直接存取 DC;相反地，它會藉由呼叫各種函式，間接地在結構上運作。</span><span class="sxs-lookup"><span data-stu-id="bef51-114">Unlike most of the structures, an application never has direct access to the DC; instead, it operates on the structure indirectly by calling various functions.</span></span>

<span data-ttu-id="bef51-115">本總覽提供下列主題的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="bef51-115">This overview provides information on the following topics:</span></span>

-   [<span data-ttu-id="bef51-116">繪圖物件</span><span class="sxs-lookup"><span data-stu-id="bef51-116">Graphic Objects</span></span>](graphic-objects.md)
-   [<span data-ttu-id="bef51-117">圖形模式</span><span class="sxs-lookup"><span data-stu-id="bef51-117">Graphic Modes</span></span>](graphic-modes.md)
-   [<span data-ttu-id="bef51-118">裝置內容類型</span><span class="sxs-lookup"><span data-stu-id="bef51-118">Device Context Types</span></span>](device-context-types.md)
-   [<span data-ttu-id="bef51-119">裝置內容作業</span><span class="sxs-lookup"><span data-stu-id="bef51-119">Device Context Operations</span></span>](device-context-operations.md)
-   [<span data-ttu-id="bef51-120">具備 ICM 功能的裝置內容函式</span><span class="sxs-lookup"><span data-stu-id="bef51-120">ICM-Enabled Device Context Functions</span></span>](icm-enabled-device-context-functions.md)

<span data-ttu-id="bef51-121">有一個重要的概念是 DC 或視窗的版面配置，其描述從左至右或由右至左) 顯示 GDI 物件和 (文字的順序。</span><span class="sxs-lookup"><span data-stu-id="bef51-121">An important concept is the layout of a DC or a window, which describes the order in which GDI objects and text are revealed (either left-to-right or right-to-left).</span></span> <span data-ttu-id="bef51-122">如需詳細資訊，請參閱 [**視窗功能**](../winmsg/window-features.md) 和 [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) 和 [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout) 函式中的「視窗版面配置和鏡像」。</span><span class="sxs-lookup"><span data-stu-id="bef51-122">For more information, see "Window Layout and Mirroring" in [**Window Features**](../winmsg/window-features.md) and the [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) and [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout) functions.</span></span>

 

 
