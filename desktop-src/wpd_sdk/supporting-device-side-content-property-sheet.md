---
title: '支援裝置端內容 (PropertySheet) '
description: 瞭解如何使用 Windows Shell API 或 WPD API 來取得裝置物件的資料，而這些物件無法透過 Windows Vista 中的檔案系統存取。
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aeade3745c37296b334c54af9edcc768fb8c93e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404191"
---
# <a name="supporting-device-side-content"></a>支援裝置端內容

因為無法透過 Windows Vista 中的檔案系統存取裝置端內容，所以您必須使用 Windows Shell API 或 WPD API 來取得裝置物件的資料。 這是一般屬性工作表處理常式和 WPD 屬性工作表處理常式之間的主要差異。 下列範例程式碼示範如何使用 Windows Shell API 抓取裝置端內容。

第一個步驟是專案識別碼清單或 PIDL 的初始化。  (此清單包含指定裝置物件的唯一識別碼。 ) 


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



初始化函式會呼叫 ExaminePIDLArray 函式，此函式會抓取 \_ PIDL 陣列中 PIDL 所識別之物件的屬性。


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



除了初始化和處理專案識別碼清單之外，您的應用程式還必須執行 IShellPropSheetExt：： ReplacePage 方法，並插入適當的取代處理常式。 Windows Shell 會在每次要顯示可取代的屬性工作表時呼叫這個方法，讓您的應用程式有機會叫用對應的取代處理常式。 ReplacePage 方法之第一個參數的低字組是要顯示的特定屬性工作表的識別碼。 第一個參數的低字組中傳遞的值會對應至檔案 WpdShellExtension 中定義的值。 這些值及其描述會顯示在下表中。



| 值                                  | 描述                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| WPDNSE \_ PROPSHEET \_ 裝置 \_ 一般     | 對應至裝置的 [一般] 索引標籤。                              |
| \_一般 WPDNSE PROPSHEET \_ 儲存體 \_    | 對應至在裝置上找到之儲存體物件的 [一般] 索引標籤。    |
| \_一般 WPDNSE PROPSHEET \_ 內容 \_    | 對應至在裝置上找到之內容物件的 [一般] 索引標籤。      |
| WPDNSE \_ PROPSHEET \_ 內容 \_ 參考 | 對應至在裝置上找到的內容物件的 [參考] 索引標籤。 |
| WPDNSE \_ PROPSHEET \_ 內容 \_ 資源  | 對應至在裝置上找到的內容物件的 [資源] 索引標籤。  |
| WPDNSE \_ PROPSHEET \_ 內容 \_ 詳細資料    | 對應至在裝置上找到的內容物件的 [詳細資料] 索引標籤。      |



 

在範例屬性工作表延伸中，ReplacePage 方法會叫用兩個取代處理常式： \_ ReplaceDeviceGeneral 和 \_ ReplaceContentReferences。 這些處理常式會取代可延伸屬性工作表中的 [一般裝置] 和 [內容參考] 索引標籤。


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



由於使用者可以選取多個裝置，因此應用程式必須儲存 IShellExtInit：： Initialize 所傳回的 PIDL 陣列，然後檢查第一個參數的最高文字以進行 ReplacePage。 這個高位字中的零值對應至 PIDL 陣列中的第一個元素，其中一個值對應至第二個元素，依此類推。 在範例應用程式的 ReplacePage 函式中，這個高文字值會傳遞給這兩個取代處理常式。 接著，這些處理常式會使用這個值來識別特定的裝置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 



