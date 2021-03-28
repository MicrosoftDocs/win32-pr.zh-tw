---
description: 若要編輯儲存在增強型中繼檔中的圖片，應用程式必須執行下列程式中所述的工作。
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: 編輯增強的中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114668"
---
# <a name="editing-an-enhanced-metafile"></a><span data-ttu-id="904d3-103">編輯增強的中繼檔</span><span class="sxs-lookup"><span data-stu-id="904d3-103">Editing an Enhanced Metafile</span></span>

<span data-ttu-id="904d3-104">若要編輯儲存在增強型中繼檔中的圖片，應用程式必須執行下列程式中所述的工作。</span><span class="sxs-lookup"><span data-stu-id="904d3-104">To edit a picture stored in an enhanced metafile, an application must perform the tasks described in the following procedure.</span></span>

<span data-ttu-id="904d3-105">**編輯儲存在增強型中繼檔中的圖片**</span><span class="sxs-lookup"><span data-stu-id="904d3-105">**To edit a picture stored in an enhanced metafile**</span></span>

1.  <span data-ttu-id="904d3-106">使用點擊測試來捕捉游標座標，並取出物件 (行、弧線、矩形、橢圓形、多邊形或不規則圖形) 的位置，讓使用者想要改變。</span><span class="sxs-lookup"><span data-stu-id="904d3-106">Use hit-testing to capture the cursor coordinates and retrieve the position of the object (line, arc, rectangle, ellipse, polygon, or irregular shape) that the user wants to alter.</span></span>
2.  <span data-ttu-id="904d3-107">將這些座標轉換為邏輯 (或全球) 單位。</span><span class="sxs-lookup"><span data-stu-id="904d3-107">Convert these coordinates to logical (or world) units.</span></span>
3.  <span data-ttu-id="904d3-108">呼叫 [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) 函數，並檢查每個中繼檔記錄。</span><span class="sxs-lookup"><span data-stu-id="904d3-108">Call the [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) function and examine each metafile record.</span></span>
4.  <span data-ttu-id="904d3-109">判斷指定的記錄是否對應至 GDI 繪圖函數。</span><span class="sxs-lookup"><span data-stu-id="904d3-109">Determine whether a given record corresponds to a GDI drawing function.</span></span>
5.  <span data-ttu-id="904d3-110">如果有的話，請判斷儲存在記錄中的座標是否對應至與使用者指定之座標相交的線條、弧線、橢圓形或其他圖形元素。</span><span class="sxs-lookup"><span data-stu-id="904d3-110">If it does, determine whether the coordinates stored in the record correspond to the line, arc, ellipse, or other graphics element that intersects the coordinates specified by the user.</span></span>
6.  <span data-ttu-id="904d3-111">尋找對應至使用者想要變更之輸出的記錄時，請清除畫面上對應至原始記錄的物件。</span><span class="sxs-lookup"><span data-stu-id="904d3-111">Upon finding the record that corresponds to the output that the user wants to alter, erase the object on the screen that corresponds to the original record.</span></span>
7.  <span data-ttu-id="904d3-112">從中繼檔中刪除對應的記錄，並將指標儲存到其位置。</span><span class="sxs-lookup"><span data-stu-id="904d3-112">Delete the corresponding record from the metafile, saving a pointer to its location.</span></span>
8.  <span data-ttu-id="904d3-113">允許使用者重繪或取代物件。</span><span class="sxs-lookup"><span data-stu-id="904d3-113">Permit the user to redraw or replace the object.</span></span>
9.  <span data-ttu-id="904d3-114">將用來繪製新物件的 GDI 函數轉換成一或多個增強中繼檔記錄。</span><span class="sxs-lookup"><span data-stu-id="904d3-114">Convert the GDI functions used to draw the new object into one or more enhanced-metafile records.</span></span>
10. <span data-ttu-id="904d3-115">將這些記錄儲存在增強的中繼檔中。</span><span class="sxs-lookup"><span data-stu-id="904d3-115">Store these records in the enhanced metafile.</span></span>

 

 



