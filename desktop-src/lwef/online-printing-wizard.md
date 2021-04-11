---
title: 線上列印嚮導
description: Windows Vista Online 列印嚮導可協助使用者訂購相片，使其無法從參與的線上列印零售商進行列印。
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- 線上列印嚮導
- 圖示，線上列印嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8536eea7a51eddb2dbb46d10c9291a60edfdc74e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315094"
---
# <a name="online-printing-wizard"></a><span data-ttu-id="32bec-105">線上列印嚮導</span><span class="sxs-lookup"><span data-stu-id="32bec-105">Online Printing Wizard</span></span>

<span data-ttu-id="32bec-106">Windows Vista Online 列印嚮導可協助使用者訂購相片，使其無法從參與的線上列印零售商進行列印。</span><span class="sxs-lookup"><span data-stu-id="32bec-106">The Windows Vista Online Printing Wizard helps users order prints of photos from participating online printing retailers.</span></span> <span data-ttu-id="32bec-107">此 wizard 的設計目的是要讓任何應用程式以程式設計方式叫用它，以便讓使用者能夠訂購相片的列印。</span><span class="sxs-lookup"><span data-stu-id="32bec-107">This wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to order prints of photos.</span></span> <span data-ttu-id="32bec-108">您可以在 Windows Vista 上使用相片列印嚮導。</span><span class="sxs-lookup"><span data-stu-id="32bec-108">The Photo Printing Wizard is available on Windows Vista.</span></span> <span data-ttu-id="32bec-109">適用于 Windows 的 PIX</span><span class="sxs-lookup"><span data-stu-id="32bec-109">PIX for Windows</span></span>

-   [<span data-ttu-id="32bec-110">線上列印嚮導所提供的功能</span><span class="sxs-lookup"><span data-stu-id="32bec-110">Features Provided by the Online Print Wizard</span></span>](#features-provided-by-the-online-print-wizard)
-   [<span data-ttu-id="32bec-111">支援的相片檔案格式</span><span class="sxs-lookup"><span data-stu-id="32bec-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="32bec-112">以程式設計方式啟動線上列印嚮導</span><span class="sxs-lookup"><span data-stu-id="32bec-112">Programmatically Launching the Online Print Wizard</span></span>](#programmatically-launching-the-online-print-wizard)
-   [<span data-ttu-id="32bec-113">存取線上列印嚮導圖示</span><span class="sxs-lookup"><span data-stu-id="32bec-113">Accessing the Online Print Wizard Icon</span></span>](#accessing-the-online-print-wizard-icon)
-   [<span data-ttu-id="32bec-114">線上列印嚮導 MRU 屬性</span><span class="sxs-lookup"><span data-stu-id="32bec-114">Online Print Wizard MRU Properties</span></span>](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a><span data-ttu-id="32bec-115">線上列印嚮導所提供的功能</span><span class="sxs-lookup"><span data-stu-id="32bec-115">Features Provided by the Online Print Wizard</span></span>

<span data-ttu-id="32bec-116">Windows Vista Online 列印嚮導可讓使用者從一部參與的線上列印零售商訂購沖印。</span><span class="sxs-lookup"><span data-stu-id="32bec-116">The Windows Vista Online Printing Wizard enables users to order prints from a selection of participating online printing retailers.</span></span> <span data-ttu-id="32bec-117">叫用時，wizard：</span><span class="sxs-lookup"><span data-stu-id="32bec-117">When invoked, the wizard:</span></span>

1.  <span data-ttu-id="32bec-118">接受要排序列印的檔案或檔案清單。</span><span class="sxs-lookup"><span data-stu-id="32bec-118">Accepts a file or list of files for which prints are to be ordered.</span></span>
2.  <span data-ttu-id="32bec-119">自動抓取目前參與的線上列印零售商清單，並讓使用者選取要購買相片的零售商。</span><span class="sxs-lookup"><span data-stu-id="32bec-119">Automatically retrieves the current list of participating online printing retailers, and enables the user to select the retailer from which to purchase the photo prints.</span></span>
3.  <span data-ttu-id="32bec-120">引導使用者完成進程或訂購列印。</span><span class="sxs-lookup"><span data-stu-id="32bec-120">Guides the user through the process or ordering prints.</span></span>

<span data-ttu-id="32bec-121">任何應用程式都可以受益于 Windows Vista Online 列印嚮導所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="32bec-121">Any application can benefit from the features offered by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="32bec-122">應用程式只需要傳入要排序列印的檔案或檔案，嚮導就會引導使用者完成訂購程式。</span><span class="sxs-lookup"><span data-stu-id="32bec-122">An application need only pass in the file or files for which prints will be ordered, and the wizard guides the user through the ordering process.</span></span>

<span data-ttu-id="32bec-123">下圖顯示 Windows Vista Online 列印嚮導，顯示參與線上列印零售商的範例清單。</span><span class="sxs-lookup"><span data-stu-id="32bec-123">The following figure shows the Windows Vista Online Printing Wizard displaying an example list of participating online printing retailers.</span></span>

![windows vista online 列印嚮導](images/opw.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="32bec-125">支援的相片檔案格式</span><span class="sxs-lookup"><span data-stu-id="32bec-125">Supported Photo File Formats</span></span>

<span data-ttu-id="32bec-126">Windows Vista Online 列印嚮導支援已安裝 Windows 影像處理元件 (WIC) 編解碼器的任何影像檔案格式。</span><span class="sxs-lookup"><span data-stu-id="32bec-126">The Windows Vista Online Printing Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="32bec-127">WIC 提供數個標準編解碼器，包括：</span><span class="sxs-lookup"><span data-stu-id="32bec-127">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="32bec-128">點陣圖 (BMP)</span><span class="sxs-lookup"><span data-stu-id="32bec-128">Bitmap (BMP)</span></span>
-   <span data-ttu-id="32bec-129">圖形交換格式 (GIF)</span><span class="sxs-lookup"><span data-stu-id="32bec-129">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="32bec-130"> (.ICO) 的圖示格式</span><span class="sxs-lookup"><span data-stu-id="32bec-130">Icon Format (ICO)</span></span>
-   <span data-ttu-id="32bec-131">JPEG 格式 (JPEG)</span><span class="sxs-lookup"><span data-stu-id="32bec-131">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="32bec-132">可攜式網路圖形 (PNG)</span><span class="sxs-lookup"><span data-stu-id="32bec-132">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="32bec-133">標記的影像檔案格式 (TIFF)</span><span class="sxs-lookup"><span data-stu-id="32bec-133">Tagged Image File Format (TIFF)</span></span>
-   <span data-ttu-id="32bec-134">Windows Media 相片格式</span><span class="sxs-lookup"><span data-stu-id="32bec-134">Windows Media Photo format</span></span>

<span data-ttu-id="32bec-135">如需 WIC 和 WIC 編解碼器的詳細資訊，請參閱 [Windows 影像處理元件](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="32bec-135">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).</span></span>

<span data-ttu-id="32bec-136">線上列印零售商所支援的檔案格式會因零售商而異;特定零售商可能不支援 Windows Vista Online 列印嚮導所支援的所有檔案格式。</span><span class="sxs-lookup"><span data-stu-id="32bec-136">File formats supported by online printing retailers vary from retailer to retailer; it is possible that a particular retailer may not support all of the file formats supported by the Windows Vista Online Printing Wizard.</span></span> <span data-ttu-id="32bec-137">如果使用者嘗試使用所選零售商不支援的格式來訂購列印，則 Windows Vista Online 列印嚮導會通知使用者，選取的零售商不支援所提交的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="32bec-137">If the user attempts to order prints in a format that is not supported by the selected retailer, the Windows Vista Online Printing Wizard notifies the user that the selected retailer does not support the submitted file format.</span></span>

## <a name="programmatically-launching-the-online-print-wizard"></a><span data-ttu-id="32bec-138">以程式設計方式啟動線上列印嚮導</span><span class="sxs-lookup"><span data-stu-id="32bec-138">Programmatically Launching the Online Print Wizard</span></span>

<span data-ttu-id="32bec-139">若要叫用 Windows Vista Online 列印嚮導，請使用下列類別識別碼呼叫 [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面 (CLSID) ：</span><span class="sxs-lookup"><span data-stu-id="32bec-139">To invoke the Windows Vista Online Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
CLSID_PublishDropTarget
```



<span data-ttu-id="32bec-140">此 CLSID 定義于 Shobjidl.h .h 和 Shobjidl.h 中。</span><span class="sxs-lookup"><span data-stu-id="32bec-140">This CLSID is defined in Shobjidl.h and Shobjidl.idl.</span></span> <span data-ttu-id="32bec-141">Windows Vista Online 列印嚮導所要處理的檔案會在 [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) 物件中指定。</span><span class="sxs-lookup"><span data-stu-id="32bec-141">The files to be processed by the Windows Vista Online Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="32bec-142">下列程式碼範例示範如何叫用 Windows Vista Online 列印嚮導。</span><span class="sxs-lookup"><span data-stu-id="32bec-142">The following code example demonstrates how to invoke the Windows Vista Online Printing Wizard.</span></span>


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a><span data-ttu-id="32bec-143">存取線上列印嚮導圖示</span><span class="sxs-lookup"><span data-stu-id="32bec-143">Accessing the Online Print Wizard Icon</span></span>

<span data-ttu-id="32bec-144">Windows Vista Online 列印嚮導會匯出可由呼叫它的應用程式存取及顯示的圖示。</span><span class="sxs-lookup"><span data-stu-id="32bec-144">The Windows Vista Online Printing Wizard exports an icon that can be accessed and displayed by applications which call it.</span></span> <span data-ttu-id="32bec-145">下圖顯示 Windows Vista Online 列印嚮導圖示。</span><span class="sxs-lookup"><span data-stu-id="32bec-145">The following figure shows the Windows Vista Online Printing Wizard icon.</span></span>

![windows vista online 列印嚮導圖示](images/opw-icon.png)

<span data-ttu-id="32bec-147">下列程式碼範例將示範如何藉由讀取 **OPWIcon** 屬性，來取得 Windows Vista Online 列印嚮導圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="32bec-147">The following code example demonstrates how to retrieve the index for the Windows Vista Online Printing Wizard icon by reading the **OPWIcon** property.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a><span data-ttu-id="32bec-148">線上列印嚮導 MRU 屬性</span><span class="sxs-lookup"><span data-stu-id="32bec-148">Online Print Wizard MRU Properties</span></span>

<span data-ttu-id="32bec-149">Windows Vista Online 列印嚮導會定義三個與最近使用的 (MRU) 線上列印零售商相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="32bec-149">The Windows Vista Online Printing Wizard defines three properties that are related to the most recently used (MRU) online printing retailer.</span></span>



| <span data-ttu-id="32bec-150">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="32bec-150">Property Name</span></span> | <span data-ttu-id="32bec-151">屬性值/函數</span><span class="sxs-lookup"><span data-stu-id="32bec-151">Property Value/Function</span></span>                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32bec-152">**MRUIcon**</span><span class="sxs-lookup"><span data-stu-id="32bec-152">**MRUIcon**</span></span>   | <span data-ttu-id="32bec-153">您可以從這個屬性讀取最近使用之線上列印零售商的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="32bec-153">The index of the icon for the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="32bec-154">**MRUName**</span><span class="sxs-lookup"><span data-stu-id="32bec-154">**MRUName**</span></span>   | <span data-ttu-id="32bec-155">您可以從這個屬性讀取最近使用的線上列印零售商的名稱。</span><span class="sxs-lookup"><span data-stu-id="32bec-155">The name of the most recently used online printing retailer can be read from this property.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="32bec-156">**UseMRU**</span><span class="sxs-lookup"><span data-stu-id="32bec-156">**UseMRU**</span></span>    | <span data-ttu-id="32bec-157">**VARIANT** **VT \_ BOOL** 值，表示 wizard 是否應略過線上列印零售商選取頁面，並改用最近使用的線上列印零售商。</span><span class="sxs-lookup"><span data-stu-id="32bec-157">A **VARIANT** **VT\_BOOL** value indicating whether the wizard should skip the online printing retailer selection page, and just use the most recently used online printing retailer instead.</span></span> <span data-ttu-id="32bec-158">將此屬性設定為 **VARIANT \_ TRUE** ，以略過 [零售商選取] 頁面。</span><span class="sxs-lookup"><span data-stu-id="32bec-158">Set this property to **VARIANT\_TRUE** to skip the retailer selection page.</span></span> |



 

<span data-ttu-id="32bec-159">下列程式碼範例示範如何設定 UseMRU 屬性，讓 Windows Vista Online 列印嚮導略過線上列印零售商選取頁面，並自動選取最近使用的零售商。</span><span class="sxs-lookup"><span data-stu-id="32bec-159">The following code example demonstrates how to set the UseMRU property so the Windows Vista Online Printing Wizard bypasses the online printing retailer selection page and automatically selects the most recently used retailer.</span></span>


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



<span data-ttu-id="32bec-160">下列程式碼範例示範如何讀取 MRUName 和 MRUIcon 屬性。</span><span class="sxs-lookup"><span data-stu-id="32bec-160">The following code example demonstrates how to read the MRUName and MRUIcon properties.</span></span>


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 