---
description: Enhanced-Format 中繼檔
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Enhanced-Format 中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972685"
---
# <a name="enhanced-format-metafiles"></a><span data-ttu-id="208c1-103">Enhanced-Format 中繼檔</span><span class="sxs-lookup"><span data-stu-id="208c1-103">Enhanced-Format Metafiles</span></span>

<span data-ttu-id="208c1-104">*增強格式的中繼檔* 是由下列元素所組成：</span><span class="sxs-lookup"><span data-stu-id="208c1-104">The *enhanced-format metafile* consists of the following elements:</span></span>

-   <span data-ttu-id="208c1-105">標頭</span><span class="sxs-lookup"><span data-stu-id="208c1-105">A header</span></span>
-   <span data-ttu-id="208c1-106">GDI 物件控制碼的資料表</span><span class="sxs-lookup"><span data-stu-id="208c1-106">A table of handles to GDI objects</span></span>
-   <span data-ttu-id="208c1-107">私用調色板</span><span class="sxs-lookup"><span data-stu-id="208c1-107">A private palette</span></span>
-   <span data-ttu-id="208c1-108">中繼檔記錄的陣列</span><span class="sxs-lookup"><span data-stu-id="208c1-108">An array of metafile records</span></span>

<span data-ttu-id="208c1-109">增強的中繼檔提供真正的裝置獨立性。</span><span class="sxs-lookup"><span data-stu-id="208c1-109">Enhanced metafiles provide true device independence.</span></span> <span data-ttu-id="208c1-110">您可以將儲存在增強型中繼檔中的圖片，視為在特定時刻拍攝之影片顯示的「快照集」。</span><span class="sxs-lookup"><span data-stu-id="208c1-110">You can think of the picture stored in an enhanced metafile as a "snapshot" of the video display taken at a particular moment.</span></span> <span data-ttu-id="208c1-111">此「快照集」會維護其維度，不論它在印表機上的位置、繪圖器、桌面或任何應用程式的工作區。</span><span class="sxs-lookup"><span data-stu-id="208c1-111">This "snapshot" maintains its dimensions no matter where it appears on a printer, a plotter, the desktop, or in the client area of any application.</span></span>

<span data-ttu-id="208c1-112">您可以使用增強的中繼檔儲存使用 GDI 函數所建立的圖片 (包括) 的新路徑和轉換函式。</span><span class="sxs-lookup"><span data-stu-id="208c1-112">You can use enhanced metafiles to store a picture created by using the GDI functions (including new path and transformation functions).</span></span> <span data-ttu-id="208c1-113">由於增強的元檔案格式是標準化的，因此以這種格式儲存的圖片可以從一個應用程式複製到另一個應用程式;而且，由於圖片與裝置無關，因此保證會在任何輸出裝置上維持其形狀與比例。</span><span class="sxs-lookup"><span data-stu-id="208c1-113">Because the enhanced metafile format is standardized, pictures that are stored in this format can be copied from one application to another; and, because the pictures are truly device independent, they are guaranteed to maintain their shape and proportion on any output device.</span></span>

-   [<span data-ttu-id="208c1-114">增強的中繼檔記錄</span><span class="sxs-lookup"><span data-stu-id="208c1-114">Enhanced Metafile Records</span></span>](enhanced-metafile-records.md)
-   [<span data-ttu-id="208c1-115">增強的中繼檔建立</span><span class="sxs-lookup"><span data-stu-id="208c1-115">Enhanced Metafile Creation</span></span>](enhanced-metafile-creation.md)
-   [<span data-ttu-id="208c1-116">增強的中繼檔作業</span><span class="sxs-lookup"><span data-stu-id="208c1-116">Enhanced Metafile Operations</span></span>](enhanced-metafile-operations.md)

 

 



