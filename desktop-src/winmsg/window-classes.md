---
description: 本主題說明視窗類別的類型、系統如何找出它們，以及定義屬於這些類別之 windows 預設行為的元素。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: '視窗類別 (視窗和訊息) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da95fc54a9527bade0d925c1f993cf853b0ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001429"
---
# <a name="window-classes-windows-and-messages"></a><span data-ttu-id="3952b-103">視窗類別 (視窗和訊息) </span><span class="sxs-lookup"><span data-stu-id="3952b-103">Window Classes (Windows and Messages)</span></span>

<span data-ttu-id="3952b-104">本主題說明視窗類別的類型、系統如何找出它們，以及定義屬於這些類別之 windows 預設行為的元素。</span><span class="sxs-lookup"><span data-stu-id="3952b-104">This topic describes the types of window classes, how the system locates them, and the elements that define the default behavior of windows that belong to them.</span></span>

<span data-ttu-id="3952b-105">視窗類別是一組屬性，可供系統用來作為建立視窗的範本。</span><span class="sxs-lookup"><span data-stu-id="3952b-105">A window class is a set of attributes that the system uses as a template to create a window.</span></span> <span data-ttu-id="3952b-106">每個視窗都是視窗類別的成員。</span><span class="sxs-lookup"><span data-stu-id="3952b-106">Every window is a member of a window class.</span></span> <span data-ttu-id="3952b-107">所有視窗類別都是進程特定的。</span><span class="sxs-lookup"><span data-stu-id="3952b-107">All window classes are process specific.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="3952b-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="3952b-108">In This Section</span></span>



| <span data-ttu-id="3952b-109">Name</span><span class="sxs-lookup"><span data-stu-id="3952b-109">Name</span></span>                                                 | <span data-ttu-id="3952b-110">描述</span><span class="sxs-lookup"><span data-stu-id="3952b-110">Description</span></span>                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3952b-111">關於視窗類別</span><span class="sxs-lookup"><span data-stu-id="3952b-111">About Window Classes</span></span>](about-window-classes.md)     | <span data-ttu-id="3952b-112">討論視窗類別。</span><span class="sxs-lookup"><span data-stu-id="3952b-112">Discusses window classes.</span></span> <span data-ttu-id="3952b-113">每個視窗類別都有一個相關聯的視窗程式，由相同類別的所有視窗共用。</span><span class="sxs-lookup"><span data-stu-id="3952b-113">Each window class has an associated window procedure shared by all windows of the same class.</span></span> <span data-ttu-id="3952b-114">視窗程式會處理該類別的所有視窗的訊息，因此會控制其行為和外觀。</span><span class="sxs-lookup"><span data-stu-id="3952b-114">The window procedure processes messages for all windows of that class and therefore controls their behavior and appearance.</span></span><br/> |
| [<span data-ttu-id="3952b-115">使用視窗類別</span><span class="sxs-lookup"><span data-stu-id="3952b-115">Using Window Classes</span></span>](using-window-classes.md)     | <span data-ttu-id="3952b-116">示範如何註冊本機視窗，並用它來建立主視窗。</span><span class="sxs-lookup"><span data-stu-id="3952b-116">Demonstrates how to register a local window and use it to create a main window.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="3952b-117">視窗類別參考</span><span class="sxs-lookup"><span data-stu-id="3952b-117">Window Class Reference</span></span>](window-class-reference.md) | <span data-ttu-id="3952b-118">包含 API 參考。</span><span class="sxs-lookup"><span data-stu-id="3952b-118">Contains the API reference.</span></span><br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a><span data-ttu-id="3952b-119">視窗類別函數</span><span class="sxs-lookup"><span data-stu-id="3952b-119">Window Class Functions</span></span>



| <span data-ttu-id="3952b-120">Name</span><span class="sxs-lookup"><span data-stu-id="3952b-120">Name</span></span>                                         | <span data-ttu-id="3952b-121">描述</span><span class="sxs-lookup"><span data-stu-id="3952b-121">Description</span></span>                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3952b-122">**GetClassInfoEx**</span><span class="sxs-lookup"><span data-stu-id="3952b-122">**GetClassInfoEx**</span></span>](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | <span data-ttu-id="3952b-123">抓取視窗類別的相關資訊，包括與視窗類別相關聯之小圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3952b-123">Retrieves information about a window class, including a handle to the small icon associated with the window class.</span></span> <span data-ttu-id="3952b-124">[**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)函式不會取出小圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3952b-124">The [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) function does not retrieve a handle to the small icon.</span></span><br/> |
| [<span data-ttu-id="3952b-125">**GetClassLong**</span><span class="sxs-lookup"><span data-stu-id="3952b-125">**GetClassLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | <span data-ttu-id="3952b-126">從與指定視窗相關聯的 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構中，抓取指定的32位 (**long**) 值。</span><span class="sxs-lookup"><span data-stu-id="3952b-126">Retrieves the specified 32-bit (**long**) value from the [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure associated with the specified window.</span></span> <br/>                                                                         |
| [<span data-ttu-id="3952b-127">**GetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="3952b-127">**GetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | <span data-ttu-id="3952b-128">從與指定視窗相關聯的 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) 結構抓取指定的值。</span><span class="sxs-lookup"><span data-stu-id="3952b-128">Retrieves the specified value from the [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure associated with the specified window.</span></span><br/>                                                                                            |
| [<span data-ttu-id="3952b-129">**GetClassName**</span><span class="sxs-lookup"><span data-stu-id="3952b-129">**GetClassName**</span></span>](/windows/win32/api/winuser/nf-winuser-getclassname)         | <span data-ttu-id="3952b-130">抓取指定的視窗所屬類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="3952b-130">Retrieves the name of the class to which the specified window belongs.</span></span> <br/>                                                                                                                                            |
| [<span data-ttu-id="3952b-131">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="3952b-131">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | <span data-ttu-id="3952b-132">抓取所指定視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3952b-132">Retrieves information about the specified window.</span></span> <span data-ttu-id="3952b-133">函式也會將指定之位移的32位 (**long**) 值抓取到額外的視窗記憶體。</span><span class="sxs-lookup"><span data-stu-id="3952b-133">The function also retrieves the 32-bit (**long**) value at the specified offset into the extra window memory.</span></span><br/>                                                    |
| [<span data-ttu-id="3952b-134">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="3952b-134">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | <span data-ttu-id="3952b-135">抓取所指定視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3952b-135">Retrieves information about the specified window.</span></span> <span data-ttu-id="3952b-136">函式也會將指定之位移的值抓取到額外的視窗記憶體。</span><span class="sxs-lookup"><span data-stu-id="3952b-136">The function also retrieves the value at a specified offset into the extra window memory.</span></span><br/>                                                                        |
| [<span data-ttu-id="3952b-137">**RegisterClass**</span><span class="sxs-lookup"><span data-stu-id="3952b-137">**RegisterClass**</span></span>](/windows/win32/api/winuser/nf-winuser-registerclassa)       | <span data-ttu-id="3952b-138">註冊視窗類別，以供後續使用於 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式的呼叫中。</span><span class="sxs-lookup"><span data-stu-id="3952b-138">Registers a window class for subsequent use in calls to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span><br/>                                                             |
| [<span data-ttu-id="3952b-139">**RegisterClassEx**</span><span class="sxs-lookup"><span data-stu-id="3952b-139">**RegisterClassEx**</span></span>](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | <span data-ttu-id="3952b-140">註冊視窗類別，以供後續使用於 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式的呼叫中。</span><span class="sxs-lookup"><span data-stu-id="3952b-140">Registers a window class for subsequent use in calls to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <br/>                                                            |
| [<span data-ttu-id="3952b-141">**SetClassLongPtr**</span><span class="sxs-lookup"><span data-stu-id="3952b-141">**SetClassLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | <span data-ttu-id="3952b-142">針對指定之視窗所屬類別的額外類別記憶體或 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) 結構，取代指定之位移的指定值。</span><span class="sxs-lookup"><span data-stu-id="3952b-142">Replaces the specified value at the specified offset in the extra class memory or the [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure for the class to which the specified window belongs.</span></span><br/>                              |
| [<span data-ttu-id="3952b-143">**SetClassWord**</span><span class="sxs-lookup"><span data-stu-id="3952b-143">**SetClassWord**</span></span>](/windows/win32/api/winuser/nf-winuser-setclassword)         | <span data-ttu-id="3952b-144">將指定之位移的16位 (**WORD**) 值取代為指定的視窗所屬之視窗類別的額外類別記憶體。</span><span class="sxs-lookup"><span data-stu-id="3952b-144">Replaces the 16-bit (**WORD**) value at the specified offset into the extra class memory for the window class to which the specified window belongs.</span></span><br/>                                                               |
| [<span data-ttu-id="3952b-145">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="3952b-145">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | <span data-ttu-id="3952b-146">變更指定之視窗的屬性。</span><span class="sxs-lookup"><span data-stu-id="3952b-146">Changes an attribute of the specified window.</span></span> <span data-ttu-id="3952b-147">函數也會將指定之位移的32位 (long) 值設定為額外的視窗記憶體。</span><span class="sxs-lookup"><span data-stu-id="3952b-147">The function also sets the 32-bit (long) value at the specified offset into the extra window memory.</span></span><br/>                                                                 |
| [<span data-ttu-id="3952b-148">**SetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="3952b-148">**SetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | <span data-ttu-id="3952b-149">變更指定之視窗的屬性。</span><span class="sxs-lookup"><span data-stu-id="3952b-149">Changes an attribute of the specified window.</span></span> <span data-ttu-id="3952b-150">函數也會在額外的視窗記憶體中的指定位移上設定值。</span><span class="sxs-lookup"><span data-stu-id="3952b-150">The function also sets a value at the specified offset in the extra window memory.</span></span><br/>                                                                                   |
| [<span data-ttu-id="3952b-151">**UnregisterClass**</span><span class="sxs-lookup"><span data-stu-id="3952b-151">**UnregisterClass**</span></span>](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | <span data-ttu-id="3952b-152">取消註冊視窗類別，釋放類別所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3952b-152">Unregisters a window class, freeing the memory required for the class.</span></span> <br/>                                                                                                                                            |



 

<span data-ttu-id="3952b-153">下列函式已過時。</span><span class="sxs-lookup"><span data-stu-id="3952b-153">The following functions are obsolete.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3952b-154">Name</span><span class="sxs-lookup"><span data-stu-id="3952b-154">Name</span></span></th>
<th><span data-ttu-id="3952b-155">描述</span><span class="sxs-lookup"><span data-stu-id="3952b-155">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3952b-156"><a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="3952b-156"><a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a></span></span></td>
<td><span data-ttu-id="3952b-157">抓取視窗類別的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3952b-157">Retrieves information about a window class.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3952b-158"><a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a>函式已被<a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>GetClassInfoEx</strong></a>函數取代。</span><span class="sxs-lookup"><span data-stu-id="3952b-158">The <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a> function has been superseded by the <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>GetClassInfoEx</strong></a> function.</span></span> <span data-ttu-id="3952b-159">但是，如果您不需要類別小型圖示的相關資訊，仍然可以使用 <strong>GetClassInfo</strong>。</span><span class="sxs-lookup"><span data-stu-id="3952b-159">You can still use <strong>GetClassInfo</strong>, however, if you do not need information about the class small icon.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3952b-160"><a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a></span><span class="sxs-lookup"><span data-stu-id="3952b-160"><a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a></span></span></td>
<td><span data-ttu-id="3952b-161">針對指定之視窗所屬的視窗類別，將指定之位移的16位 (<strong>字</strong>) 值移入額外類別記憶體。</span><span class="sxs-lookup"><span data-stu-id="3952b-161">Retrieves the 16-bit (<strong>WORD</strong>) value at the specified offset into the extra class memory for the window class to which the specified window belongs.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3952b-162"><em>NIndex</em>設定為 GCW_ATOM 以外的任何使用，此函式已被取代。</span><span class="sxs-lookup"><span data-stu-id="3952b-162">This function is deprecated for any use other than <em>nIndex</em> set to GCW_ATOM.</span></span> <span data-ttu-id="3952b-163">函式僅提供給 Windows 的16位版本相容。</span><span class="sxs-lookup"><span data-stu-id="3952b-163">The function is provided only for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="3952b-164">應用程式應該使用 <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>GetClassLong</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="3952b-164">Applications should use the <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>GetClassLong</strong></a> function.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3952b-165"><a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a></span><span class="sxs-lookup"><span data-stu-id="3952b-165"><a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a></span></span></td>
<td><span data-ttu-id="3952b-166">將指定之位移的指定32位 (<strong>long</strong>) 值取代為指定之視窗所屬類別的額外類別記憶體或 <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="3952b-166">Replaces the specified 32-bit (<strong>long</strong>) value at the specified offset into the extra class memory or the <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> structure for the class to which the specified window belongs.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3952b-167">此函數已被 <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>SetClassLongPtr</strong></a> 函數取代。</span><span class="sxs-lookup"><span data-stu-id="3952b-167">This function has been superseded by the <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>SetClassLongPtr</strong></a> function.</span></span> <span data-ttu-id="3952b-168">若要撰寫與32位和64位版本的 Windows 相容的程式碼，請使用 <strong>SetClassLongPtr</strong>。</span><span class="sxs-lookup"><span data-stu-id="3952b-168">To write code that is compatible with both 32-bit and 64-bit versions of Windows, use <strong>SetClassLongPtr</strong>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="window-class-structures"></a><span data-ttu-id="3952b-169">視窗類別結構</span><span class="sxs-lookup"><span data-stu-id="3952b-169">Window Class Structures</span></span>



| <span data-ttu-id="3952b-170">Name</span><span class="sxs-lookup"><span data-stu-id="3952b-170">Name</span></span>                             | <span data-ttu-id="3952b-171">描述</span><span class="sxs-lookup"><span data-stu-id="3952b-171">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3952b-172">**WNDCLASS**</span><span class="sxs-lookup"><span data-stu-id="3952b-172">**WNDCLASS**</span></span>](/windows/win32/api/winuser/ns-winuser-wndclassa)     | <span data-ttu-id="3952b-173">包含 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) 函數所註冊的視窗類別屬性。</span><span class="sxs-lookup"><span data-stu-id="3952b-173">Contains the window class attributes that are registered by the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function.</span></span> <br/> <span data-ttu-id="3952b-174">此結構已由與 [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)函數搭配使用的 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構所取代。</span><span class="sxs-lookup"><span data-stu-id="3952b-174">This structure has been superseded by the [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure used with the [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) function.</span></span> <span data-ttu-id="3952b-175">如果您不需要設定與視窗類別相關聯的小圖示，仍然可以使用 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) 和 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) 。</span><span class="sxs-lookup"><span data-stu-id="3952b-175">You can still use [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) and [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) if you do not need to set the small icon associated with the window class.</span></span><br/>                                                  |
| [<span data-ttu-id="3952b-176">**WNDCLASSEX**</span><span class="sxs-lookup"><span data-stu-id="3952b-176">**WNDCLASSEX**</span></span>](/windows/win32/api/winuser/ns-winuser-wndclassexa) | <span data-ttu-id="3952b-177">包含視窗類別資訊。</span><span class="sxs-lookup"><span data-stu-id="3952b-177">Contains window class information.</span></span> <span data-ttu-id="3952b-178">它會搭配 [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) 和 [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)  函數使用。</span><span class="sxs-lookup"><span data-stu-id="3952b-178">It is used with the [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) and [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)  functions.</span></span> <br/> <span data-ttu-id="3952b-179">[**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構類似于 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構。</span><span class="sxs-lookup"><span data-stu-id="3952b-179">The [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure is similar to the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure.</span></span> <span data-ttu-id="3952b-180">有兩種差異。</span><span class="sxs-lookup"><span data-stu-id="3952b-180">There are two differences.</span></span> <span data-ttu-id="3952b-181">**WNDCLASSEX** 包含 **cbSize** 成員（指定結構的大小）和 **hIconSm** 成員，其中包含與視窗類別相關聯之小圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3952b-181">**WNDCLASSEX** includes the **cbSize** member, which specifies the size of the structure, and the **hIconSm** member, which contains a handle to a small icon associated with the window class.</span></span><br/> |



 

 

 
