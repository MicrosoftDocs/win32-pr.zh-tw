---
description: 裝置內容 (DC) 是一種資料結構，用來定義繪圖物件、其相關聯的屬性，以及影響裝置上輸出的圖形模式。 若要建立 DC，請呼叫 CreateDC 函式;若要取出 DC，請呼叫 GetDC 函數。
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: 點陣圖、裝置內容和繪圖表面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6297eb3446d05d0fa21ac23c9de9f3416a300746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191960"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a><span data-ttu-id="ac6b9-104">點陣圖、裝置內容和繪圖表面</span><span class="sxs-lookup"><span data-stu-id="ac6b9-104">Bitmaps, Device Contexts, and Drawing Surfaces</span></span>

<span data-ttu-id="ac6b9-105">*裝置內容* (DC) 是一種資料結構，用來定義繪圖物件、其相關聯的屬性，以及影響裝置上輸出的圖形模式。</span><span class="sxs-lookup"><span data-stu-id="ac6b9-105">A *device context* (DC) is a data structure defining the graphics objects, their associated attributes, and the graphics modes affecting output on a device.</span></span> <span data-ttu-id="ac6b9-106">若要建立 DC，請呼叫 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 函式;若要取出 DC，請呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函數。</span><span class="sxs-lookup"><span data-stu-id="ac6b9-106">To create a DC, call the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function; to retrieve a DC, call the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="ac6b9-107">在傳回識別該 DC 的控制碼之前，系統會選取一個繪圖介面至 DC。</span><span class="sxs-lookup"><span data-stu-id="ac6b9-107">Before returning a handle that identifies that DC, the system selects a drawing surface into the DC.</span></span> <span data-ttu-id="ac6b9-108">如果應用程式呼叫 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 函式以建立 VGA 顯示器的裝置內容，此繪圖介面的維度為 640 480 圖元。</span><span class="sxs-lookup"><span data-stu-id="ac6b9-108">If the application called the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function to create a device context for a VGA display, the dimensions of this drawing surface are 640-by-480 pixels.</span></span> <span data-ttu-id="ac6b9-109">如果應用程式呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式，則維度會反映工作區的大小。</span><span class="sxs-lookup"><span data-stu-id="ac6b9-109">If the application called the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function, the dimensions reflect the size of the client area.</span></span>

<span data-ttu-id="ac6b9-110">在應用程式開始繪圖之前，必須藉由呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式，在 DC 中選取具有適當寬度和高度的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="ac6b9-110">Before an application can begin drawing, it must select a bitmap with the appropriate width and height into the DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="ac6b9-111">當應用程式將 DC 的控制碼傳遞給其中一個圖形裝置介面 (GDI) 繪圖函式時，所要求的輸出會出現在選取的繪圖介面上。</span><span class="sxs-lookup"><span data-stu-id="ac6b9-111">When an application passes the handle to the DC to one of the graphics device interface (GDI) drawing functions, the requested output appears on the drawing surface selected into the DC.</span></span>

<span data-ttu-id="ac6b9-112">如需詳細資訊，請參閱 [記憶體裝置](memory-device-contexts.md)內容。</span><span class="sxs-lookup"><span data-stu-id="ac6b9-112">For more information, see [Memory Device Contexts](memory-device-contexts.md).</span></span>

 

 



