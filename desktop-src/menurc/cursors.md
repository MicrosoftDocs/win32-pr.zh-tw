---
title: 資料指標
description: 本節討論資料指標，這是螢幕上的位置是由指標裝置（例如滑鼠、畫筆或軌跡球）控制的小型圖片。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- 資源，資料指標
- 資料指標，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9014befcc41161d7491af97186b33088f508dd8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021529"
---
# <a name="cursors"></a><span data-ttu-id="d6e02-105">資料指標</span><span class="sxs-lookup"><span data-stu-id="d6e02-105">Cursors</span></span>

<span data-ttu-id="d6e02-106">游標是螢幕上的位置，由指標裝置（例如，滑鼠、畫筆或軌跡球）控制的小型圖片。</span><span class="sxs-lookup"><span data-stu-id="d6e02-106">A cursor is a small picture whose location on the screen is controlled by a pointing device, such as a mouse, pen, or trackball.</span></span> <span data-ttu-id="d6e02-107">在此總覽的其餘部分，「滑鼠」一詞是指任何指標裝置。</span><span class="sxs-lookup"><span data-stu-id="d6e02-107">In the remainder of this overview, the term mouse refers to any pointing device.</span></span>

<span data-ttu-id="d6e02-108">當使用者移動滑鼠時，系統會據以移動游標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-108">When the user moves the mouse, the system moves the cursor accordingly.</span></span> <span data-ttu-id="d6e02-109">資料指標函數可讓應用程式建立、載入、顯示、動畫、移動、限制和終結資料指標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-109">The cursor functions enable applications to create, load, display, animate, move, confine, and destroy cursors.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="d6e02-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="d6e02-110">In This Section</span></span>



| <span data-ttu-id="d6e02-111">Name</span><span class="sxs-lookup"><span data-stu-id="d6e02-111">Name</span></span>                                     | <span data-ttu-id="d6e02-112">描述</span><span class="sxs-lookup"><span data-stu-id="d6e02-112">Description</span></span>                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="d6e02-113">關於資料指標</span><span class="sxs-lookup"><span data-stu-id="d6e02-113">About Cursors</span></span>](about-cursors.md)       | <span data-ttu-id="d6e02-114">討論標準資料指標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-114">Discusses the standard cursors.</span></span><br/>                    |
| [<span data-ttu-id="d6e02-115">使用資料指標</span><span class="sxs-lookup"><span data-stu-id="d6e02-115">Using Cursors</span></span>](using-cursors.md)       | <span data-ttu-id="d6e02-116">討論如何執行與資料指標相關的工作。</span><span class="sxs-lookup"><span data-stu-id="d6e02-116">Discusses how to perform tasks related to cursors.</span></span><br/> |
| [<span data-ttu-id="d6e02-117">資料指標參考</span><span class="sxs-lookup"><span data-stu-id="d6e02-117">Cursor Reference</span></span>](cursor-reference.md) | <span data-ttu-id="d6e02-118">包含 API 參考。</span><span class="sxs-lookup"><span data-stu-id="d6e02-118">Contains the API reference.</span></span><br/>                        |



 

### <a name="cursor-functions"></a><span data-ttu-id="d6e02-119">資料指標函數</span><span class="sxs-lookup"><span data-stu-id="d6e02-119">Cursor Functions</span></span>



| <span data-ttu-id="d6e02-120">Name</span><span class="sxs-lookup"><span data-stu-id="d6e02-120">Name</span></span>                                                 | <span data-ttu-id="d6e02-121">描述</span><span class="sxs-lookup"><span data-stu-id="d6e02-121">Description</span></span>                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6e02-122">**ClipCursor**</span><span class="sxs-lookup"><span data-stu-id="d6e02-122">**ClipCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | <span data-ttu-id="d6e02-123">將游標範圍設為螢幕上的矩形區域。</span><span class="sxs-lookup"><span data-stu-id="d6e02-123">Confines the cursor to a rectangular area on the screen.</span></span> <span data-ttu-id="d6e02-124">如果後續的游標位置 (由 [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) 函式所設定，或滑鼠) 位於矩形外，系統會自動調整位置，以將游標放在矩形區域內。</span><span class="sxs-lookup"><span data-stu-id="d6e02-124">If a subsequent cursor position (set by the [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) function or the mouse) lies outside the rectangle, the system automatically adjusts the position to keep the cursor inside the rectangular area.</span></span> <br/> |
| [<span data-ttu-id="d6e02-125">**CopyCursor**</span><span class="sxs-lookup"><span data-stu-id="d6e02-125">**CopyCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | <span data-ttu-id="d6e02-126">複製指定的資料指標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-126">Copies the specified cursor.</span></span> <br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="d6e02-127">**CreateCursor**</span><span class="sxs-lookup"><span data-stu-id="d6e02-127">**CreateCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | <span data-ttu-id="d6e02-128">建立具有指定大小、位模式和作用點的資料指標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-128">Creates a cursor having the specified size, bit patterns, and hot spot.</span></span> <br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="d6e02-129">**DestroyCursor**</span><span class="sxs-lookup"><span data-stu-id="d6e02-129">**DestroyCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | <span data-ttu-id="d6e02-130">終結資料指標，並釋出資料指標所佔用的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="d6e02-130">Destroys a cursor and frees any memory the cursor occupied.</span></span> <span data-ttu-id="d6e02-131">請勿使用這個函數來終結共用資料指標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-131">Do not use this function to destroy a shared cursor.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="d6e02-132">**GetClipCursor**</span><span class="sxs-lookup"><span data-stu-id="d6e02-132">**GetClipCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | <span data-ttu-id="d6e02-133">抓取游標所限制之矩形區域的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-133">Retrieves the screen coordinates of the rectangular area to which the cursor is confined.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="d6e02-134">**GetCursor**</span><span class="sxs-lookup"><span data-stu-id="d6e02-134">**GetCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | <span data-ttu-id="d6e02-135">抓取目前資料指標的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d6e02-135">Retrieves a handle to the current cursor.</span></span> <br/>                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="d6e02-136">**GetCursorInfo**</span><span class="sxs-lookup"><span data-stu-id="d6e02-136">**GetCursorInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | <span data-ttu-id="d6e02-137">抓取全域資料指標的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d6e02-137">Retrieves information about the global cursor.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="d6e02-138">**GetCursorPos**</span><span class="sxs-lookup"><span data-stu-id="d6e02-138">**GetCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | <span data-ttu-id="d6e02-139">以螢幕座標抓取游標的位置。</span><span class="sxs-lookup"><span data-stu-id="d6e02-139">Retrieves the cursor's position, in screen coordinates.</span></span><br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="d6e02-140">**GetPhysicalCursorPos**</span><span class="sxs-lookup"><span data-stu-id="d6e02-140">**GetPhysicalCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | <span data-ttu-id="d6e02-141">抓取資料指標在實體座標中的位置。</span><span class="sxs-lookup"><span data-stu-id="d6e02-141">Retrieves the position of the cursor in physical coordinates.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="d6e02-142">**LoadCursor**</span><span class="sxs-lookup"><span data-stu-id="d6e02-142">**LoadCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | <span data-ttu-id="d6e02-143">從可執行檔 ( 載入指定的資料指標資源。EXE) 與應用程式實例相關聯的檔案。</span><span class="sxs-lookup"><span data-stu-id="d6e02-143">Loads the specified cursor resource from the executable (.EXE) file associated with an application instance.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="d6e02-144">**LoadCursorFromFile**</span><span class="sxs-lookup"><span data-stu-id="d6e02-144">**LoadCursorFromFile**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | <span data-ttu-id="d6e02-145">根據檔案中包含的資料來建立資料指標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-145">Creates a cursor based on data contained in a file.</span></span> <br/>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="d6e02-146">**SetCursor**</span><span class="sxs-lookup"><span data-stu-id="d6e02-146">**SetCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | <span data-ttu-id="d6e02-147">設定資料指標圖形。</span><span class="sxs-lookup"><span data-stu-id="d6e02-147">Sets the cursor shape.</span></span> <br/>                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="d6e02-148">**SetCursorPos**</span><span class="sxs-lookup"><span data-stu-id="d6e02-148">**SetCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | <span data-ttu-id="d6e02-149">將游標移至指定的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-149">Moves the cursor to the specified screen coordinates.</span></span> <span data-ttu-id="d6e02-150">如果新座標不在最新的 [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) 函式呼叫所設定的螢幕矩形內，系統會自動調整座標，讓游標停留在矩形內。</span><span class="sxs-lookup"><span data-stu-id="d6e02-150">If the new coordinates are not within the screen rectangle set by the most recent [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) function call, the system automatically adjusts the coordinates so that the cursor stays within the rectangle.</span></span> <br/>    |
| [<span data-ttu-id="d6e02-151">**SetPhysicalCursorPos**</span><span class="sxs-lookup"><span data-stu-id="d6e02-151">**SetPhysicalCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | <span data-ttu-id="d6e02-152">設定資料指標在實體座標中的位置。</span><span class="sxs-lookup"><span data-stu-id="d6e02-152">Sets the position of the cursor in physical coordinates.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="d6e02-153">**SetSystemCursor**</span><span class="sxs-lookup"><span data-stu-id="d6e02-153">**SetSystemCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | <span data-ttu-id="d6e02-154">讓應用程式自訂系統資料指標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-154">Enables an application to customize the system cursors.</span></span> <span data-ttu-id="d6e02-155">它會將 *id* 參數所指定的系統資料指標內容取代為 *hcur* 參數所指定之資料指標的內容，然後終結 *hcur*。</span><span class="sxs-lookup"><span data-stu-id="d6e02-155">It replaces the contents of the system cursor specified by the *id* parameter with the contents of the cursor specified by the *hcur* parameter and then destroys *hcur*.</span></span> <br/>                                                          |
| [<span data-ttu-id="d6e02-156">**ShowCursor**</span><span class="sxs-lookup"><span data-stu-id="d6e02-156">**ShowCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | <span data-ttu-id="d6e02-157">顯示或隱藏游標。</span><span class="sxs-lookup"><span data-stu-id="d6e02-157">Displays or hides the cursor.</span></span> <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a><span data-ttu-id="d6e02-158">資料指標通知</span><span class="sxs-lookup"><span data-stu-id="d6e02-158">Cursor Notifications</span></span>



| <span data-ttu-id="d6e02-159">Name</span><span class="sxs-lookup"><span data-stu-id="d6e02-159">Name</span></span>                                  | <span data-ttu-id="d6e02-160">描述</span><span class="sxs-lookup"><span data-stu-id="d6e02-160">Description</span></span>                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6e02-161">**WM \_ SETCURSOR**</span><span class="sxs-lookup"><span data-stu-id="d6e02-161">**WM\_SETCURSOR**</span></span>](wm-setcursor.md) | <span data-ttu-id="d6e02-162">如果滑鼠導致游標在視窗內移動，且未捕捉到滑鼠輸入，則傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="d6e02-162">Sent to a window if the mouse causes the cursor to move within a window and mouse input is not captured.</span></span> <br/> |



 

### <a name="cursor-structures"></a><span data-ttu-id="d6e02-163">資料指標結構</span><span class="sxs-lookup"><span data-stu-id="d6e02-163">Cursor Structures</span></span>



| <span data-ttu-id="d6e02-164">Name</span><span class="sxs-lookup"><span data-stu-id="d6e02-164">Name</span></span>                             | <span data-ttu-id="d6e02-165">描述</span><span class="sxs-lookup"><span data-stu-id="d6e02-165">Description</span></span>                                    |
|----------------------------------|------------------------------------------------|
| [<span data-ttu-id="d6e02-166">**CURSORINFO**</span><span class="sxs-lookup"><span data-stu-id="d6e02-166">**CURSORINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-cursorinfo) | <span data-ttu-id="d6e02-167">包含全域資料指標資訊。</span><span class="sxs-lookup"><span data-stu-id="d6e02-167">Contains global cursor information.</span></span><br/> |



 

 

 





