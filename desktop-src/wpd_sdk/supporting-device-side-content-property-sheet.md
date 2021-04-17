---
title: '支援裝置端內容 (PropertySheet) '
description: 支援 Device-Side 內容
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7e054e4c545acd8f34583da5cd9ef3af347643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319943"
---
# <a name="supporting-device-side-content"></a><span data-ttu-id="2e40f-103">支援裝置端內容</span><span class="sxs-lookup"><span data-stu-id="2e40f-103">Supporting device-side content</span></span>

<span data-ttu-id="2e40f-104">因為無法透過 Windows Vista 中的檔案系統存取裝置端內容，所以您必須使用 Windows Shell API 或 WPD API 來取得裝置物件的資料。</span><span class="sxs-lookup"><span data-stu-id="2e40f-104">Because device-side content is not accessible through the file system in Windows Vista, you'll need to use either the Windows Shell API or the WPD API to retrieve data for device objects.</span></span> <span data-ttu-id="2e40f-105">這是一般屬性工作表處理常式和 WPD 屬性工作表處理常式之間的主要差異。</span><span class="sxs-lookup"><span data-stu-id="2e40f-105">This is the primary difference between a normal property sheet handler and a WPD property sheet handler.</span></span> <span data-ttu-id="2e40f-106">下列範例程式碼示範如何使用 Windows Shell API 抓取裝置端內容。</span><span class="sxs-lookup"><span data-stu-id="2e40f-106">The following sample code demonstrates the retrieval of device-side content using the Windows Shell API.</span></span>

<span data-ttu-id="2e40f-107">第一個步驟是專案識別碼清單或 PIDL 的初始化。</span><span class="sxs-lookup"><span data-stu-id="2e40f-107">The first step is the initialization of the item identifier list or PIDL.</span></span> <span data-ttu-id="2e40f-108"> (此清單包含指定裝置物件的唯一識別碼。 ) </span><span class="sxs-lookup"><span data-stu-id="2e40f-108">(This list contains the unique identifier for the given device object.)</span></span>


```C++
HRESULT CWPDPropSheet::_InitializePIDLArray(IDataObject *pDataObj)
{
    if (m_cfHIDA == 0)
    {
        m_cfHIDA = (CLIPFORMAT)RegisterClipboardFormat(CFSTR_SHELLIDLIST);
    }

    STGMEDIUM   medium;
    FORMATETC   fmte = {m_cfHIDA, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};

    m_pPropInfo = (PROPINFO*)LocalAlloc(LPTR, sizeof(PROPINFO));
    if (m_pPropInfo == NULL)
        return E_OUTOFMEMORY;

    AddRef_PropInfo(m_pPropInfo);

    HRESULT hr = pDataObj->GetData(&fmte, &medium);
    if (SUCCEEDED(hr))
    {
        SIZE_T cb = GlobalSize(medium.hGlobal);
        CIDA *pida = (CIDA*)GlobalAlloc(GPTR, cb);
        if (pida)
        {
            void *pv = GlobalLock(medium.hGlobal);
            if (pv != NULL)
            {
                CopyMemory(pida, pv, cb);
                GlobalUnlock(medium.hGlobal);
                m_pPropInfo->pida = pida;
                _ExaminePIDLArray();
            }
            else
            {
                hr = E_UNEXPECTED;
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
        ReleaseStgMedium(&medium);
    }

    return hr;
}
```



<span data-ttu-id="2e40f-109">初始化函式會呼叫 ExaminePIDLArray 函式，此函式會抓取 \_ PIDL 陣列中 PIDL 所識別之物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="2e40f-109">The initialization function calls the \_ExaminePIDLArray function, which retrieves the properties for object identified by a PIDL in the PIDL array.</span></span>


```C++
HRESULT CWPDPropSheet::_ExaminePIDLArray()
{
    CComPtr<IShellFolder2> spParentFolder;

    CComVariant  variant;

    LPITEMIDLIST pidl = NULL;
    HRESULT      hr = S_OK;
    UINT         index = 0;

    pidl = GetPIDL(m_pPropInfo->pida, index);
    if (pidl)
    {
        hr = SHBindToParent(pidl, IID_PPV_ARGS(&spParentFolder), NULL);
        IF_FAILED_JUMP(hr, Exit);
    }

    do
    {
        CComPtr<IPropertySetStorage> spSetStorage;
        CComPtr<IPropertyStorage>    spPropStorage;

        // Get the IpropertySetStorage interface for this PIDL. This method could also
        // be used to retrieve an IPortableDevice interface to allow more low-level interaction
        // with the WPD API.
        hr = spParentFolder->BindToObject(ILFindLastID(pidl), NULL, IID_PPV_ARGS(&spSetStorage));
        if (SUCCEEDED(hr))
        {
            hr = spSetStorage->Open(WPD_FUNCTIONAL_OBJECT_PROPERTIES_V1, STGM_READ, &spPropStorage);
            if (SUCCEEDED(hr))
            {
                PROPVARIANT PropVar = {0};
                PROPSPEC    PropSpec = {0};

                PropSpec.ulKind = PRSPEC_PROPID;
                PropSpec.propid = 2; // WPD_FUNCTIONAL_OBJECT_CATEGORY

                PropVariantInit(&PropVar);

                hr = spPropStorage->ReadMultiple(1, &PropSpec, &PropVar);
                if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                {
                    // The PIDL array contains a non-file object.
                    // This means we don't want to take over the
                    // default menu action.
                    m_bPIDAContainsOnlyFiles = FALSE;
                    PropVariantClear(&PropVar);
                    break;
                }
                else
                {
                    CComPtr<IPropertyStorage>    spObjectProperties;
                    hr = spSetStorage->Open(WPD_OBJECT_PROPERTIES_V1, STGM_READ, &spObjectProperties);
                    if (SUCCEEDED(hr))
                    {
                        PropSpec.ulKind = PRSPEC_PROPID;
                        PropSpec.propid = 7; // WPD_OBJECT_CONTENT_TYPE
                        
                        PropVariantClear(&PropVar);
                        hr = spObjectProperties->ReadMultiple(1, &PropSpec, &PropVar);
                        if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                        {
                            if (IsEqualGUID(*PropVar.puuid, WPD_CONTENT_TYPE_FOLDER))
                            {
                                // The PIDL array contains a folder object.
                                // This means we don't want to take over the
                                // default menu action.
                                m_bPIDAContainsOnlyFiles = FALSE;
                                PropVariantClear(&PropVar);
                                break;
                            }
                        }
                    }
                }

                PropVariantClear(&PropVar);
            }
        }

        UI_SAFE_ILFREE(pidl);

        pidl = GetPIDL(m_pPropInfo->pida, ++index);
    } while (pidl != NULL && index < m_pPropInfo->pida->cidl);

Exit:
    UI_SAFE_ILFREE(pidl);
    return hr;
}
```



<span data-ttu-id="2e40f-110">除了初始化和處理專案識別碼清單之外，您的應用程式還必須執行 IShellPropSheetExt：： ReplacePage 方法，並插入適當的取代處理常式。</span><span class="sxs-lookup"><span data-stu-id="2e40f-110">In addition to the initialization and processing of the item identifier list, your application will need to implement the IShellPropSheetExt::ReplacePage method and insert the appropriate replacement handlers.</span></span> <span data-ttu-id="2e40f-111">Windows Shell 會在每次要顯示可取代的屬性工作表時呼叫這個方法，讓您的應用程式有機會叫用對應的取代處理常式。</span><span class="sxs-lookup"><span data-stu-id="2e40f-111">The Windows Shell calls this method each time it is about to display a replaceable property sheet, giving your application a chance to invoke a corresponding replacement handler.</span></span> <span data-ttu-id="2e40f-112">ReplacePage 方法之第一個參數的低字組是要顯示的特定屬性工作表的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e40f-112">The low word of the first parameter to the ReplacePage method is an identifier for the given property sheet that Windows is about to display.</span></span> <span data-ttu-id="2e40f-113">第一個參數的低字組中傳遞的值會對應至檔案 WpdShellExtension 中定義的值。</span><span class="sxs-lookup"><span data-stu-id="2e40f-113">The values passed in the low word of the first parameter correspond to values defined in the file WpdShellExtension.h.</span></span> <span data-ttu-id="2e40f-114">這些值及其描述會顯示在下表中。</span><span class="sxs-lookup"><span data-stu-id="2e40f-114">These values and their descriptions appear in the following table.</span></span>



| <span data-ttu-id="2e40f-115">值</span><span class="sxs-lookup"><span data-stu-id="2e40f-115">Value</span></span>                                  | <span data-ttu-id="2e40f-116">描述</span><span class="sxs-lookup"><span data-stu-id="2e40f-116">Description</span></span>                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="2e40f-117">WPDNSE \_ PROPSHEET \_ 裝置 \_ 一般</span><span class="sxs-lookup"><span data-stu-id="2e40f-117">WPDNSE\_PROPSHEET\_DEVICE\_GENERAL</span></span>     | <span data-ttu-id="2e40f-118">對應至裝置的 [一般] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2e40f-118">Corresponds to the general tab for the device.</span></span>                              |
| <span data-ttu-id="2e40f-119">\_一般 WPDNSE PROPSHEET \_ 儲存體 \_</span><span class="sxs-lookup"><span data-stu-id="2e40f-119">WPDNSE\_PROPSHEET\_STORAGE\_GENERAL</span></span>    | <span data-ttu-id="2e40f-120">對應至在裝置上找到之儲存體物件的 [一般] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2e40f-120">Corresponds to the general tab for a storage object found on the device.</span></span>    |
| <span data-ttu-id="2e40f-121">\_一般 WPDNSE PROPSHEET \_ 內容 \_</span><span class="sxs-lookup"><span data-stu-id="2e40f-121">WPDNSE\_PROPSHEET\_CONTENT\_GENERAL</span></span>    | <span data-ttu-id="2e40f-122">對應至在裝置上找到之內容物件的 [一般] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2e40f-122">Corresponds to the general tab for content object found on the device.</span></span>      |
| <span data-ttu-id="2e40f-123">WPDNSE \_ PROPSHEET \_ 內容 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="2e40f-123">WPDNSE\_PROPSHEET\_CONTENT\_REFERENCES</span></span> | <span data-ttu-id="2e40f-124">對應至在裝置上找到的內容物件的 [參考] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2e40f-124">Corresponds to the references tab for a content object found on the device.</span></span> |
| <span data-ttu-id="2e40f-125">WPDNSE \_ PROPSHEET \_ 內容 \_ 資源</span><span class="sxs-lookup"><span data-stu-id="2e40f-125">WPDNSE\_PROPSHEET\_CONTENT\_RESOURCES</span></span>  | <span data-ttu-id="2e40f-126">對應至在裝置上找到的內容物件的 [資源] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2e40f-126">Corresponds to the resources tab for a content object found on the device.</span></span>  |
| <span data-ttu-id="2e40f-127">WPDNSE \_ PROPSHEET \_ 內容 \_ 詳細資料</span><span class="sxs-lookup"><span data-stu-id="2e40f-127">WPDNSE\_PROPSHEET\_CONTENT\_DETAILS</span></span>    | <span data-ttu-id="2e40f-128">對應至在裝置上找到的內容物件的 [詳細資料] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2e40f-128">Corresponds to a details tab for a content object found on the device.</span></span>      |



 

<span data-ttu-id="2e40f-129">在範例屬性工作表延伸中，ReplacePage 方法會叫用兩個取代處理常式： \_ ReplaceDeviceGeneral 和 \_ ReplaceContentReferences。</span><span class="sxs-lookup"><span data-stu-id="2e40f-129">In the sample property sheet extension, the ReplacePage method invokes two replacement handlers: \_ReplaceDeviceGeneral and \_ReplaceContentReferences.</span></span> <span data-ttu-id="2e40f-130">這些處理常式會取代可延伸屬性工作表中的 [一般裝置] 和 [內容參考] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="2e40f-130">These handlers replace the general device and the content references tabs in the extensible property sheets.</span></span>


```C++
STDMETHODIMP CWPDPropSheet::ReplacePage(UINT uPageID, LPFNADDPROPSHEETPAGE lpfnReplacePage, LPARAM lParam)
{
    HRESULT       hr = S_OK;

    if (LOWORD(uPageID) == WPDNSE_PROPSHEET_DEVICE_GENERAL)
    {
        hr = _ReplaceDeviceGeneral(HIWORD(uPageID), lpfnReplacePage, lParam);
    }
    else if (LOWORD(uPageID) == WPDNSE_PROPSHEET_CONTENT_REFERENCES)
    {
        hr = _ReplaceContentReferences(HIWORD(uPageID), lpfnReplacePage, lParam);
    }

    return hr;
}
```



<span data-ttu-id="2e40f-131">由於使用者可以選取多個裝置，因此應用程式必須儲存 IShellExtInit：： Initialize 所傳回的 PIDL 陣列，然後檢查第一個參數的最高文字以進行 ReplacePage。</span><span class="sxs-lookup"><span data-stu-id="2e40f-131">Because it is possible for a user to select multiple devices, an application will need to save the PIDL array returned by IShellExtInit::Initialize and then examine the high word of the first parameter to ReplacePage.</span></span> <span data-ttu-id="2e40f-132">這個高位字中的零值對應至 PIDL 陣列中的第一個元素，其中一個值對應至第二個元素，依此類推。</span><span class="sxs-lookup"><span data-stu-id="2e40f-132">A value of zero in this high word corresponds to the first element in the PIDL array, a value of one corresponds to the second element, and so on.</span></span> <span data-ttu-id="2e40f-133">在範例應用程式的 ReplacePage 函式中，這個高文字值會傳遞給這兩個取代處理常式。</span><span class="sxs-lookup"><span data-stu-id="2e40f-133">In the sample application's ReplacePage function, this high word value is passed to both replacement handlers.</span></span> <span data-ttu-id="2e40f-134">接著，這些處理常式會使用這個值來識別特定的裝置。</span><span class="sxs-lookup"><span data-stu-id="2e40f-134">These handlers, in turn, use this value to identify a particular device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e40f-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e40f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e40f-136">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="2e40f-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



