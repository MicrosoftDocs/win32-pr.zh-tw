---
title: 網際網路快速鍵
description: 網際網路快捷方式物件是用來建立網際網路網站的桌面快捷方式。
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- 網際網路快捷方式物件
- WebBrowser 控制項
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14bc2ed58f75522e59b9008ded7b0f1416a21fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023441"
---
# <a name="internet-shortcuts"></a><span data-ttu-id="136b2-106">網際網路快速鍵</span><span class="sxs-lookup"><span data-stu-id="136b2-106">Internet Shortcuts</span></span>

<span data-ttu-id="136b2-107">網際網路快捷方式物件是用來建立網際網路網站的桌面快捷方式。</span><span class="sxs-lookup"><span data-stu-id="136b2-107">The Internet shortcut object is used to create desktop shortcuts to Internet sites.</span></span> <span data-ttu-id="136b2-108">就像檔案系統中專案的快捷方式一樣，網際網路快速鍵會以圖示形式出現在桌面上。</span><span class="sxs-lookup"><span data-stu-id="136b2-108">Like shortcuts to items in the file system, Internet shortcuts take the form of an icon on the desktop.</span></span> <span data-ttu-id="136b2-109">當使用者按一下圖示時，就會啟動瀏覽器，並顯示與快捷方式相關聯的網站。</span><span class="sxs-lookup"><span data-stu-id="136b2-109">When the user clicks the icon, the browser is launched and displays the site associated with the shortcut.</span></span>

<span data-ttu-id="136b2-110">討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="136b2-110">The following topics are discussed.</span></span>

-   [<span data-ttu-id="136b2-111">建立網際網路快捷方式</span><span class="sxs-lookup"><span data-stu-id="136b2-111">Creating Internet Shortcuts</span></span>](#creating-internet-shortcuts)
    -   [<span data-ttu-id="136b2-112">從 WebBrowser 控制項建立網際網路快捷方式</span><span class="sxs-lookup"><span data-stu-id="136b2-112">Creating an Internet Shortcut from a WebBrowser Control</span></span>](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [<span data-ttu-id="136b2-113">從 URL 建立網際網路快捷方式</span><span class="sxs-lookup"><span data-stu-id="136b2-113">Creating an Internet Shortcut from a URL</span></span>](#creating-an-internet-shortcut-from-a-url)
-   [<span data-ttu-id="136b2-114">存取屬性儲存體</span><span class="sxs-lookup"><span data-stu-id="136b2-114">Accessing Property Storage</span></span>](#accessing-property-storage)
-   [<span data-ttu-id="136b2-115">介面</span><span class="sxs-lookup"><span data-stu-id="136b2-115">Interfaces</span></span>](#interfaces)
    -   [<span data-ttu-id="136b2-116">OLE 介面</span><span class="sxs-lookup"><span data-stu-id="136b2-116">OLE interfaces</span></span>](#ole-interfaces)
    -   [<span data-ttu-id="136b2-117">Shell 介面</span><span class="sxs-lookup"><span data-stu-id="136b2-117">Shell interfaces</span></span>](#shell-interfaces)
-   [<span data-ttu-id="136b2-118">函數</span><span class="sxs-lookup"><span data-stu-id="136b2-118">Functions</span></span>](#functions)
    -   [<span data-ttu-id="136b2-119">網際網路快速鍵公用程式函式</span><span class="sxs-lookup"><span data-stu-id="136b2-119">Internet shortcut utility functions</span></span>](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a><span data-ttu-id="136b2-120">建立網際網路快捷方式</span><span class="sxs-lookup"><span data-stu-id="136b2-120">Creating Internet Shortcuts</span></span>

<span data-ttu-id="136b2-121">您可以使用 WebBrowser 控制項或頁面的 URL 來建立網際網路快捷方式。</span><span class="sxs-lookup"><span data-stu-id="136b2-121">You can create an Internet shortcut by using a WebBrowser control or with the URL of the page.</span></span>

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a><span data-ttu-id="136b2-122">從 WebBrowser 控制項建立網際網路快捷方式</span><span class="sxs-lookup"><span data-stu-id="136b2-122">Creating an Internet Shortcut from a WebBrowser Control</span></span>

<span data-ttu-id="136b2-123">如果您的應用程式裝載了 WebBrowser 控制項，則可以使用網際網路快捷方式物件，以下列方式建立快捷方式。</span><span class="sxs-lookup"><span data-stu-id="136b2-123">If your application hosts a WebBrowser control, you can use the Internet shortcut object to create shortcuts in the following way.</span></span>

1.  <span data-ttu-id="136b2-124">使用 (clsid) clsid InternetShortcut 的類別識別碼，建立具有 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的網際網路快捷方式物件的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="136b2-124">Create an instance of the Internet shortcut object with [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), using a class identifier (CLSID) of CLSID\_InternetShortcut.</span></span>
2.  <span data-ttu-id="136b2-125">使用[IObjectWithSite：： SetSite](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite)，將 WebBrowser 的[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面指標傳遞至網際網路快捷方式物件。</span><span class="sxs-lookup"><span data-stu-id="136b2-125">Pass the pointer to the WebBrowser's [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface to the Internet shortcut object with [IObjectWithSite::SetSite](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span></span>
3.  <span data-ttu-id="136b2-126">當您想要建立 WebBrowser 控制項所要查看之頁面的快捷方式時，請呼叫網際網路快捷方式物件的 [IPersistFile：： Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 方法。</span><span class="sxs-lookup"><span data-stu-id="136b2-126">Call the Internet shortcut object's [IPersistFile::Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) method when you want to create a shortcut to the page being viewed by the WebBrowser control.</span></span>

<span data-ttu-id="136b2-127">將會在 [IPersistFile：： Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)中指定的位置建立快捷方式。</span><span class="sxs-lookup"><span data-stu-id="136b2-127">A shortcut will be created in the location specified in [IPersistFile::Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="136b2-128">這個位置可讓 WebBrowser 控制項還原其狀態，包括將正確檔載入至框架的工作。</span><span class="sxs-lookup"><span data-stu-id="136b2-128">This location enables the WebBrowser control to restore its state, which includes the task of loading of the correct documents into framesets.</span></span>

### <a name="creating-an-internet-shortcut-from-a-url"></a><span data-ttu-id="136b2-129">從 URL 建立網際網路快捷方式</span><span class="sxs-lookup"><span data-stu-id="136b2-129">Creating an Internet Shortcut from a URL</span></span>

<span data-ttu-id="136b2-130">如果您有想要連結之頁面的 URL，您也可以建立網際網路快捷方式。</span><span class="sxs-lookup"><span data-stu-id="136b2-130">You can also create an Internet shortcut if you have the URL of the page to which you want to link.</span></span>

1.  <span data-ttu-id="136b2-131">使用 CLSID 的 clsid InternetShortcut，建立具有 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的網際網路快捷方式物件的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="136b2-131">Create an instance of the Internet shortcut object with [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), using a CLSID of CLSID\_InternetShortcut.</span></span>
2.  <span data-ttu-id="136b2-132">您可以使用 [IUniformResourceLocator：： SetURL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) 方法來設定快速鍵中的 URL。</span><span class="sxs-lookup"><span data-stu-id="136b2-132">Use the [IUniformResourceLocator::SetURL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) method to set the URL in the shortcut.</span></span>
3.  <span data-ttu-id="136b2-133">使用 [IPersistFile：： save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 方法，將快捷方式檔案儲存至所需的位置。</span><span class="sxs-lookup"><span data-stu-id="136b2-133">Use the [IPersistFile::Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) method to save the shortcut file to a desired location.</span></span>

## <a name="accessing-property-storage"></a><span data-ttu-id="136b2-134">存取屬性儲存體</span><span class="sxs-lookup"><span data-stu-id="136b2-134">Accessing Property Storage</span></span>

<span data-ttu-id="136b2-135">網際網路快捷方式物件包含數個屬性，您可以使用下列程式，透過物件的 [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) 介面來存取這些屬性。</span><span class="sxs-lookup"><span data-stu-id="136b2-135">The Internet shortcut object contains several properties that you can access through the object's [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) interface with the following procedure.</span></span>

1.  <span data-ttu-id="136b2-136">藉由呼叫具有 IID IPropertySetStorage 的[QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得[IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="136b2-136">Get the [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) interface by calling [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) with IID\_IPropertySetStorage.</span></span>
2.  <span data-ttu-id="136b2-137">藉由呼叫 [IPropertySetStorage：： Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) with FMTID \_ Intshcut 或 FMTID \_ InternetSite 來取得 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) 介面，以存取網際網路快速鍵屬性儲存集。</span><span class="sxs-lookup"><span data-stu-id="136b2-137">Access the Internet shortcut property storage set by calling [IPropertySetStorage::Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) with FMTID\_Intshcut or FMTID\_InternetSite to obtain the [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) interface.</span></span>
3.  <span data-ttu-id="136b2-138">藉由傳遞適當的屬性識別碼，以 [IPropertyStorage：： ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) 讀取屬性儲存體資訊。</span><span class="sxs-lookup"><span data-stu-id="136b2-138">Read the property storage information with [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) by passing the appropriate property ID.</span></span>

<span data-ttu-id="136b2-139">使用 [4.70 版或更高版本](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85))的 Shell32.dll，您也可以藉由呼叫 [**IShellFolder：： BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) ，並將 *pidl* 參數設定為來取出 [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)介面。URL 檔案和 *riid* 參數設定為 IID \_ IPropertySetStorage。</span><span class="sxs-lookup"><span data-stu-id="136b2-139">With [version 4.70 or higher](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)) of Shell32.dll, you can also retrieve the [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) interface by calling [**IShellFolder::BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) with the *pidl* parameter set to the .URL file and the *riid* parameter set to IID\_IPropertySetStorage.</span></span>

<span data-ttu-id="136b2-140">下列屬性識別碼可針對 FMTID \_ Intshcut 要求。</span><span class="sxs-lookup"><span data-stu-id="136b2-140">The following property IDs can be requested for FMTID\_Intshcut.</span></span>



| <span data-ttu-id="136b2-141">PROPID</span><span class="sxs-lookup"><span data-stu-id="136b2-141">PROPID</span></span>               | <span data-ttu-id="136b2-142">Variant 類型</span><span class="sxs-lookup"><span data-stu-id="136b2-142">Variant Type</span></span> | <span data-ttu-id="136b2-143">Description</span><span class="sxs-lookup"><span data-stu-id="136b2-143">Description</span></span>                                 |
|----------------------|--------------|---------------------------------------------|
| <span data-ttu-id="136b2-144">PID \_ 是 \_ URL</span><span class="sxs-lookup"><span data-stu-id="136b2-144">PID\_IS\_URL</span></span>         | <span data-ttu-id="136b2-145">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-145">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-146">快速鍵導向的 URL</span><span class="sxs-lookup"><span data-stu-id="136b2-146">URL to which the shortcut leads</span></span>             |
| <span data-ttu-id="136b2-147">PID \_ 為 \_ NAME</span><span class="sxs-lookup"><span data-stu-id="136b2-147">PID\_IS\_NAME</span></span>        | <span data-ttu-id="136b2-148">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-148">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-149">網際網路快捷方式的名稱</span><span class="sxs-lookup"><span data-stu-id="136b2-149">Name of the Internet shortcut</span></span>               |
| <span data-ttu-id="136b2-150">PID \_ 為 \_ >\DREPLAYCLIENT\WORKINGDIR</span><span class="sxs-lookup"><span data-stu-id="136b2-150">PID\_IS\_WORKINGDIR</span></span>  | <span data-ttu-id="136b2-151">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-151">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-152">快速鍵的工作目錄</span><span class="sxs-lookup"><span data-stu-id="136b2-152">Working directory for the shortcut</span></span>          |
| <span data-ttu-id="136b2-153">PID \_ 是 \_ 熱鍵</span><span class="sxs-lookup"><span data-stu-id="136b2-153">PID\_IS\_HOTKEY</span></span>      | <span data-ttu-id="136b2-154">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="136b2-154">VT\_UI2</span></span>      | <span data-ttu-id="136b2-155">快速鍵的熱鍵</span><span class="sxs-lookup"><span data-stu-id="136b2-155">Hotkey for the shortcut</span></span>                     |
| <span data-ttu-id="136b2-156">PID \_ 為 \_ SHOWCMD</span><span class="sxs-lookup"><span data-stu-id="136b2-156">PID\_IS\_SHOWCMD</span></span>     | <span data-ttu-id="136b2-157">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="136b2-157">VT\_I4</span></span>       | <span data-ttu-id="136b2-158">顯示快捷方式的命令</span><span class="sxs-lookup"><span data-stu-id="136b2-158">Show command for shortcut</span></span>                   |
| <span data-ttu-id="136b2-159">PID \_ 為 \_ >ICONINDEX</span><span class="sxs-lookup"><span data-stu-id="136b2-159">PID\_IS\_ICONINDEX</span></span>   | <span data-ttu-id="136b2-160">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="136b2-160">VT\_I4</span></span>       | <span data-ttu-id="136b2-161">圖示的索引</span><span class="sxs-lookup"><span data-stu-id="136b2-161">Index of the icon</span></span>                           |
| <span data-ttu-id="136b2-162">PID \_ 為 \_ ICONFILE</span><span class="sxs-lookup"><span data-stu-id="136b2-162">PID\_IS\_ICONFILE</span></span>    | <span data-ttu-id="136b2-163">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-163">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-164">包含圖示的檔案</span><span class="sxs-lookup"><span data-stu-id="136b2-164">File that contains the icon</span></span>                 |
| <span data-ttu-id="136b2-165">PID \_ 為 \_ >WHATSNEW.CASTING</span><span class="sxs-lookup"><span data-stu-id="136b2-165">PID\_IS\_WHATSNEW</span></span>    | <span data-ttu-id="136b2-166">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-166">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-167">新功能文字</span><span class="sxs-lookup"><span data-stu-id="136b2-167">What's New text</span></span>                             |
| <span data-ttu-id="136b2-168">PID \_ 是 \_ 作者</span><span class="sxs-lookup"><span data-stu-id="136b2-168">PID\_IS\_AUTHOR</span></span>      | <span data-ttu-id="136b2-169">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-169">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-170">作者</span><span class="sxs-lookup"><span data-stu-id="136b2-170">Author</span></span>                                      |
| <span data-ttu-id="136b2-171">PID \_ 為 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="136b2-171">PID\_IS\_DESCRIPTION</span></span> | <span data-ttu-id="136b2-172">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-172">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-173">網站的描述文字</span><span class="sxs-lookup"><span data-stu-id="136b2-173">Description text of site</span></span>                    |
| <span data-ttu-id="136b2-174">PID \_ 為 \_ 批註</span><span class="sxs-lookup"><span data-stu-id="136b2-174">PID\_IS\_COMMENT</span></span>     | <span data-ttu-id="136b2-175">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-175">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-176">使用者批註批註</span><span class="sxs-lookup"><span data-stu-id="136b2-176">User annotated comment</span></span>                      |
| <span data-ttu-id="136b2-177">PID \_ 已 \_ 漫遊</span><span class="sxs-lookup"><span data-stu-id="136b2-177">PID\_IS\_ROAMED</span></span>      | <span data-ttu-id="136b2-178">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="136b2-178">VT\_BOOL</span></span>     | <span data-ttu-id="136b2-179">當快捷方式第一次漫遊時為 True</span><span class="sxs-lookup"><span data-stu-id="136b2-179">True when shortcut is roamed for first time</span></span> |



 

<span data-ttu-id="136b2-180">下列屬性識別碼可針對 FMTID \_ InternetSite 要求。</span><span class="sxs-lookup"><span data-stu-id="136b2-180">The following property IDs can be requested for FMTID\_InternetSite.</span></span>



| <span data-ttu-id="136b2-181">PROPID</span><span class="sxs-lookup"><span data-stu-id="136b2-181">PROPID</span></span>                     | <span data-ttu-id="136b2-182">Variant 類型</span><span class="sxs-lookup"><span data-stu-id="136b2-182">Variant Type</span></span> | <span data-ttu-id="136b2-183">Description</span><span class="sxs-lookup"><span data-stu-id="136b2-183">Description</span></span>                                       |
|----------------------------|--------------|---------------------------------------------------|
| <span data-ttu-id="136b2-184">PID \_ INTSITE \_ >WHATSNEW.CASTING</span><span class="sxs-lookup"><span data-stu-id="136b2-184">PID\_INTSITE\_WHATSNEW</span></span>     | <span data-ttu-id="136b2-185">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-185">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-186">新功能文字</span><span class="sxs-lookup"><span data-stu-id="136b2-186">What's New text</span></span>                                   |
| <span data-ttu-id="136b2-187">PID \_ INTSITE \_ 作者</span><span class="sxs-lookup"><span data-stu-id="136b2-187">PID\_INTSITE\_AUTHOR</span></span>       | <span data-ttu-id="136b2-188">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-188">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-189">作者</span><span class="sxs-lookup"><span data-stu-id="136b2-189">Author</span></span>                                            |
| <span data-ttu-id="136b2-190">PID \_ INTSITE \_ LASTVISIT</span><span class="sxs-lookup"><span data-stu-id="136b2-190">PID\_INTSITE\_LASTVISIT</span></span>    | <span data-ttu-id="136b2-191">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="136b2-191">VT\_FILETIME</span></span> | <span data-ttu-id="136b2-192">上次造訪時間網站</span><span class="sxs-lookup"><span data-stu-id="136b2-192">Time site was last visited</span></span>                        |
| <span data-ttu-id="136b2-193">PID \_ INTSITE \_ LASTMOD</span><span class="sxs-lookup"><span data-stu-id="136b2-193">PID\_INTSITE\_LASTMOD</span></span>      | <span data-ttu-id="136b2-194">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="136b2-194">VT\_FILETIME</span></span> | <span data-ttu-id="136b2-195">上次修改時間網站</span><span class="sxs-lookup"><span data-stu-id="136b2-195">Time site was last modified</span></span>                       |
| <span data-ttu-id="136b2-196">PID \_ INTSITE \_ VISITCOUNT</span><span class="sxs-lookup"><span data-stu-id="136b2-196">PID\_INTSITE\_VISITCOUNT</span></span>   | <span data-ttu-id="136b2-197">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="136b2-197">VT\_UI4</span></span>      | <span data-ttu-id="136b2-198">使用者造訪的次數</span><span class="sxs-lookup"><span data-stu-id="136b2-198">Number of times user has visited</span></span>                  |
| <span data-ttu-id="136b2-199">PID \_ INTSITE \_ 描述</span><span class="sxs-lookup"><span data-stu-id="136b2-199">PID\_INTSITE\_DESCRIPTION</span></span>  | <span data-ttu-id="136b2-200">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-200">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-201">網站的描述文字</span><span class="sxs-lookup"><span data-stu-id="136b2-201">Description text of site</span></span>                          |
| <span data-ttu-id="136b2-202">PID \_ INTSITE \_ 批註</span><span class="sxs-lookup"><span data-stu-id="136b2-202">PID\_INTSITE\_COMMENT</span></span>      | <span data-ttu-id="136b2-203">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-203">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-204">使用者批註批註</span><span class="sxs-lookup"><span data-stu-id="136b2-204">User annotated comment</span></span>                            |
| <span data-ttu-id="136b2-205">PID \_ INTSITE \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="136b2-205">PID\_INTSITE\_FLAGS</span></span>        | <span data-ttu-id="136b2-206">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="136b2-206">VT\_UI4</span></span>      | <span data-ttu-id="136b2-207">表示使用 PIDISF \_ 旗標 (請參閱下文) </span><span class="sxs-lookup"><span data-stu-id="136b2-207">Indicates use of PIDISF\_ flags (see below)</span></span>       |
| <span data-ttu-id="136b2-208">PID \_ INTSITE \_ CONTENTLEN</span><span class="sxs-lookup"><span data-stu-id="136b2-208">PID\_INTSITE\_CONTENTLEN</span></span>   | <span data-ttu-id="136b2-209">N/A</span><span class="sxs-lookup"><span data-stu-id="136b2-209">N/A</span></span>          | <span data-ttu-id="136b2-210">目前不支援</span><span class="sxs-lookup"><span data-stu-id="136b2-210">Not currently supported</span></span>                           |
| <span data-ttu-id="136b2-211">PID \_ INTSITE \_ CONTENTCODE</span><span class="sxs-lookup"><span data-stu-id="136b2-211">PID\_INTSITE\_CONTENTCODE</span></span>  | <span data-ttu-id="136b2-212">N/A</span><span class="sxs-lookup"><span data-stu-id="136b2-212">N/A</span></span>          | <span data-ttu-id="136b2-213">目前不支援</span><span class="sxs-lookup"><span data-stu-id="136b2-213">Not currently supported</span></span>                           |
| <span data-ttu-id="136b2-214">PID \_ INTSITE \_ 遞迴</span><span class="sxs-lookup"><span data-stu-id="136b2-214">PID\_INTSITE\_RECURSE</span></span>      | <span data-ttu-id="136b2-215">N/A</span><span class="sxs-lookup"><span data-stu-id="136b2-215">N/A</span></span>          | <span data-ttu-id="136b2-216">目前不支援</span><span class="sxs-lookup"><span data-stu-id="136b2-216">Not currently supported</span></span>                           |
| <span data-ttu-id="136b2-217">PID \_ INTSITE \_ 監看</span><span class="sxs-lookup"><span data-stu-id="136b2-217">PID\_INTSITE\_WATCH</span></span>        | <span data-ttu-id="136b2-218">N/A</span><span class="sxs-lookup"><span data-stu-id="136b2-218">N/A</span></span>          | <span data-ttu-id="136b2-219">目前不支援</span><span class="sxs-lookup"><span data-stu-id="136b2-219">Not currently supported</span></span>                           |
| <span data-ttu-id="136b2-220">PID \_ INTSITE \_ 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="136b2-220">PID\_INTSITE\_SUBSCRIPTION</span></span> | <span data-ttu-id="136b2-221">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="136b2-221">VT\_UI8</span></span>      | <span data-ttu-id="136b2-222">訂用帳戶管理員的 SUBSCRIPTIONCOOKIE 值</span><span class="sxs-lookup"><span data-stu-id="136b2-222">SUBSCRIPTIONCOOKIE value for subscription manager</span></span> |
| <span data-ttu-id="136b2-223">PID \_ INTSITE \_ URL</span><span class="sxs-lookup"><span data-stu-id="136b2-223">PID\_INTSITE\_URL</span></span>          | <span data-ttu-id="136b2-224">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-224">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-225">快速鍵導向的 URL</span><span class="sxs-lookup"><span data-stu-id="136b2-225">URL to which the shortcut leads</span></span>                   |
| <span data-ttu-id="136b2-226">PID \_ INTSITE \_ 標題</span><span class="sxs-lookup"><span data-stu-id="136b2-226">PID\_INTSITE\_TITLE</span></span>        | <span data-ttu-id="136b2-227">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-227">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-228">標題</span><span class="sxs-lookup"><span data-stu-id="136b2-228">Title</span></span>                                             |
| <span data-ttu-id="136b2-229">PID \_ INTSITE \_ 字碼頁</span><span class="sxs-lookup"><span data-stu-id="136b2-229">PID\_INTSITE\_CODEPAGE</span></span>     | <span data-ttu-id="136b2-230">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="136b2-230">VT\_UI4</span></span>      | <span data-ttu-id="136b2-231">檔的字碼頁</span><span class="sxs-lookup"><span data-stu-id="136b2-231">Codepage of the document</span></span>                          |
| <span data-ttu-id="136b2-232">PID \_ INTSITE \_ 追蹤</span><span class="sxs-lookup"><span data-stu-id="136b2-232">PID\_INTSITE\_TRACKING</span></span>     | <span data-ttu-id="136b2-233">N/A</span><span class="sxs-lookup"><span data-stu-id="136b2-233">N/A</span></span>          | <span data-ttu-id="136b2-234">目前不支援</span><span class="sxs-lookup"><span data-stu-id="136b2-234">Not currently supported</span></span>                           |
| <span data-ttu-id="136b2-235">PID \_ INTSITE \_ >ICONINDEX</span><span class="sxs-lookup"><span data-stu-id="136b2-235">PID\_INTSITE\_ICONINDEX</span></span>    | <span data-ttu-id="136b2-236">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="136b2-236">VT\_I4</span></span>       | <span data-ttu-id="136b2-237">圖示的索引</span><span class="sxs-lookup"><span data-stu-id="136b2-237">Index of the icon</span></span>                                 |
| <span data-ttu-id="136b2-238">PID \_ INTSITE \_ ICONFILE</span><span class="sxs-lookup"><span data-stu-id="136b2-238">PID\_INTSITE\_ICONFILE</span></span>     | <span data-ttu-id="136b2-239">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="136b2-239">VT\_LPWSTR</span></span>   | <span data-ttu-id="136b2-240">包含圖示的檔案</span><span class="sxs-lookup"><span data-stu-id="136b2-240">File that contains the icon</span></span>                       |
| <span data-ttu-id="136b2-241">已 \_ 漫遊的 PID INTSITE \_</span><span class="sxs-lookup"><span data-stu-id="136b2-241">PID\_INTSITE\_ROAMED</span></span>       | <span data-ttu-id="136b2-242">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="136b2-242">VT\_UI4</span></span>      | <span data-ttu-id="136b2-243">因為漫遊而新增了專案</span><span class="sxs-lookup"><span data-stu-id="136b2-243">The entry was added due to roaming</span></span>                |



 

<span data-ttu-id="136b2-244">以下是網際網路網站旗標。</span><span class="sxs-lookup"><span data-stu-id="136b2-244">The following are the Internet site flags.</span></span>



| <span data-ttu-id="136b2-245">旗標</span><span class="sxs-lookup"><span data-stu-id="136b2-245">Flag</span></span>                    | <span data-ttu-id="136b2-246">描述</span><span class="sxs-lookup"><span data-stu-id="136b2-246">Description</span></span>                                |
|-------------------------|--------------------------------------------|
| <span data-ttu-id="136b2-247">PIDISF \_ RECENTLYCHANGED</span><span class="sxs-lookup"><span data-stu-id="136b2-247">PIDISF\_RECENTLYCHANGED</span></span> | <span data-ttu-id="136b2-248">指出最近已變更網站</span><span class="sxs-lookup"><span data-stu-id="136b2-248">Indicates that a site was recently changed</span></span> |
| <span data-ttu-id="136b2-249">PIDISF \_ CACHEDSTICKY</span><span class="sxs-lookup"><span data-stu-id="136b2-249">PIDISF\_CACHEDSTICKY</span></span>    | <span data-ttu-id="136b2-250">目前不支援</span><span class="sxs-lookup"><span data-stu-id="136b2-250">Not currently supported</span></span>                    |
| <span data-ttu-id="136b2-251">PIDISF \_ CACHEIMAGES</span><span class="sxs-lookup"><span data-stu-id="136b2-251">PIDISF\_CACHEIMAGES</span></span>     | <span data-ttu-id="136b2-252">目前不支援</span><span class="sxs-lookup"><span data-stu-id="136b2-252">Not currently supported</span></span>                    |
| <span data-ttu-id="136b2-253">PIDISF \_ FOLLOWALLLINKS</span><span class="sxs-lookup"><span data-stu-id="136b2-253">PIDISF\_FOLLOWALLLINKS</span></span>  | <span data-ttu-id="136b2-254">目前不支援</span><span class="sxs-lookup"><span data-stu-id="136b2-254">Not currently supported</span></span>                    |



 

<span data-ttu-id="136b2-255">以下是網際網路漫遊歷程記錄所使用的值。</span><span class="sxs-lookup"><span data-stu-id="136b2-255">The following values are used for Internet roaming history.</span></span>



| <span data-ttu-id="136b2-256">已漫遊的 PID \_ INTSITE 值 \_</span><span class="sxs-lookup"><span data-stu-id="136b2-256">Value of PID\_INTSITE\_ROAMED</span></span>         | <span data-ttu-id="136b2-257">Description</span><span class="sxs-lookup"><span data-stu-id="136b2-257">Description</span></span>                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="136b2-258">值未設定或 PIDISR \_ \_ 為最 \_ 新狀態</span><span class="sxs-lookup"><span data-stu-id="136b2-258">Value not set or PIDISR\_UP\_TO\_DATE</span></span> | <span data-ttu-id="136b2-259">漫遊未修改此快取專案。</span><span class="sxs-lookup"><span data-stu-id="136b2-259">This cache entry has not been modified by roaming.</span></span>                                                                                                                       |
| <span data-ttu-id="136b2-260">PIDISR \_ 需要 \_ 新增</span><span class="sxs-lookup"><span data-stu-id="136b2-260">PIDISR\_NEEDS\_ADD</span></span>                    | <span data-ttu-id="136b2-261">漫遊已將此快取專案新增至快取。</span><span class="sxs-lookup"><span data-stu-id="136b2-261">This cache entry was added to the cache by roaming.</span></span> <span data-ttu-id="136b2-262">\_ \_ 完成專案的處理之後，將 PIDISR 設定為最新狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="136b2-262">Set PIDISR\_UP\_TO\_DATE once processing of the entry is complete.</span></span>                                                   |
| <span data-ttu-id="136b2-263">PIDISR \_ 需要 \_ 更新</span><span class="sxs-lookup"><span data-stu-id="136b2-263">PIDISR\_NEEDS\_UPDATE</span></span>                 | <span data-ttu-id="136b2-264">這個快取專案已經存在於本機電腦上，但已透過漫遊進行更新。</span><span class="sxs-lookup"><span data-stu-id="136b2-264">This cache entry already existed on the local machine, but it was updated by roaming.</span></span> <span data-ttu-id="136b2-265">\_ \_ 完成專案的處理之後，將 PIDISR 設定為最新狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="136b2-265">Set PIDISR\_UP\_TO\_DATE once processing of the entry is complete.</span></span>                 |
| <span data-ttu-id="136b2-266">PIDISR \_ 需要 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="136b2-266">PIDISR\_NEEDS\_DELETE</span></span>                 | <span data-ttu-id="136b2-267">漫遊偵測到應該刪除此快取專案。</span><span class="sxs-lookup"><span data-stu-id="136b2-267">Roaming detected that this cache entry should be deleted.</span></span> <span data-ttu-id="136b2-268">例如，使用者可能已清除其瀏覽器歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="136b2-268">For example, the user may have cleared his or her browser history.</span></span> <span data-ttu-id="136b2-269">使用 DeleteUrlCacheEntry 刪除專案。</span><span class="sxs-lookup"><span data-stu-id="136b2-269">Delete the entry using DeleteUrlCacheEntry.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="136b2-270">介面</span><span class="sxs-lookup"><span data-stu-id="136b2-270">Interfaces</span></span>

<span data-ttu-id="136b2-271">網際網路快捷方式物件會公開多個介面。</span><span class="sxs-lookup"><span data-stu-id="136b2-271">The Internet shortcut object exposes a number of interfaces.</span></span>

### <a name="ole-interfaces"></a><span data-ttu-id="136b2-272">OLE 介面</span><span class="sxs-lookup"><span data-stu-id="136b2-272">OLE interfaces</span></span>

-   [<span data-ttu-id="136b2-273">IDataObject</span><span class="sxs-lookup"><span data-stu-id="136b2-273">IDataObject</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [<span data-ttu-id="136b2-274">IPersistFile</span><span class="sxs-lookup"><span data-stu-id="136b2-274">IPersistFile</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [<span data-ttu-id="136b2-275">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="136b2-275">IPersistStream</span></span>](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [<span data-ttu-id="136b2-276">IOleCommandTarget</span><span class="sxs-lookup"><span data-stu-id="136b2-276">IOleCommandTarget</span></span>](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
-   [<span data-ttu-id="136b2-277">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="136b2-277">IPropertySetStorage</span></span>](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)
-   [<span data-ttu-id="136b2-278">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="136b2-278">IObjectWithSite</span></span>](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)

### <a name="shell-interfaces"></a><span data-ttu-id="136b2-279">Shell 介面</span><span class="sxs-lookup"><span data-stu-id="136b2-279">Shell interfaces</span></span>

-   [<span data-ttu-id="136b2-280">**ICoNtextMenu2**</span><span class="sxs-lookup"><span data-stu-id="136b2-280">**IContextMenu2**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)
-   [<span data-ttu-id="136b2-281">**IExtractIcon**</span><span class="sxs-lookup"><span data-stu-id="136b2-281">**IExtractIcon**</span></span>](/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona)
-   [<span data-ttu-id="136b2-282">**INewShortcutHook**</span><span class="sxs-lookup"><span data-stu-id="136b2-282">**INewShortcutHook**</span></span>](/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka)
-   [<span data-ttu-id="136b2-283">**IShellExtInit**</span><span class="sxs-lookup"><span data-stu-id="136b2-283">**IShellExtInit**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit)
-   [<span data-ttu-id="136b2-284">**IShellLink**</span><span class="sxs-lookup"><span data-stu-id="136b2-284">**IShellLink**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)
-   [<span data-ttu-id="136b2-285">**IShellPropSheetExt**</span><span class="sxs-lookup"><span data-stu-id="136b2-285">**IShellPropSheetExt**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
-   [<span data-ttu-id="136b2-286">**IQueryInfo**</span><span class="sxs-lookup"><span data-stu-id="136b2-286">**IQueryInfo**</span></span>](/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo)

## <a name="functions"></a><span data-ttu-id="136b2-287">函式</span><span class="sxs-lookup"><span data-stu-id="136b2-287">Functions</span></span>

<span data-ttu-id="136b2-288">有幾個公用程式函式可用於網際網路快捷方式物件。</span><span class="sxs-lookup"><span data-stu-id="136b2-288">There are several utility functions that can be used with the Internet shortcut object.</span></span>

### <a name="internet-shortcut-utility-functions"></a><span data-ttu-id="136b2-289">網際網路快速鍵公用程式函式</span><span class="sxs-lookup"><span data-stu-id="136b2-289">Internet shortcut utility functions</span></span>

-   [<span data-ttu-id="136b2-290">**InetIsOffline**</span><span class="sxs-lookup"><span data-stu-id="136b2-290">**InetIsOffline**</span></span>](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [<span data-ttu-id="136b2-291">**MIMEAssociationDialog**</span><span class="sxs-lookup"><span data-stu-id="136b2-291">**MIMEAssociationDialog**</span></span>](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [<span data-ttu-id="136b2-292">**TranslateURL**</span><span class="sxs-lookup"><span data-stu-id="136b2-292">**TranslateURL**</span></span>](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [<span data-ttu-id="136b2-293">**URLAssociationDialog**</span><span class="sxs-lookup"><span data-stu-id="136b2-293">**URLAssociationDialog**</span></span>](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 