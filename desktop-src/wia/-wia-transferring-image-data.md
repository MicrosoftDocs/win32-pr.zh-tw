---
description: 使用 IWiaDataTransfer 介面的方法，將資料從 Windows 映像取得 (WIA) 1.0 裝置傳送至應用程式。
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: 在 WIA 1.0 中傳送影像資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e2c1dfce551f105b0df1627f11e9b4ccb7ee8a420e395f3fd0cc1ba932f136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813668"
---
# <a name="transferring-image-data-in-wia-10"></a>在 WIA 1.0 中傳送影像資料

> [!Note]  
> 本教學課程將說明如何在 Windows XP 或更早版本執行的應用程式中傳送影像資料。 如需在將于 Windows Vista 或更新版本上執行的應用程式中傳送影像資料的相關資訊，請參閱[在 WIA 2.0 中傳送影像資料](-wia-transferring-image-data-in-wia2.md)。

 

使用 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)介面的方法，將資料從 Windows 映像取得 (WIA) 1.0 裝置傳送至應用程式。 此介面支援共用記憶體視窗，可將資料從裝置物件傳輸至應用程式，並在封送處理期間消除不必要的資料複本。

應用程式必須查詢影像專案，以取得其 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) 介面的指標，如下列程式碼範例所示：


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



在先前的程式碼中，假設 **pWiaItem** 是 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 介面的有效指標。 對 [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))的呼叫會以 **pWiaItem** 所參考專案的 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)介面指標填滿 **pWiaDataTransfer** 。

然後，應用程式會設定 [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構成員。 如需詳細資訊，請參閱 STGMEDIUM 和 [TYMED](/windows/win32/api/objidl/ne-objidl-tymed)。


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



如果您提供檔案名，則應該包含適當的副檔名;WIA 1.0 未提供副檔名。 如果 **StgMedium** 的 **LpszFileName** 成員為 **Null**，則 WIA 1.0 會產生已傳送資料的隨機檔案名和路徑。 請在呼叫 ReleaseStgMedium 之前移動或複製此檔案，因為此函式會刪除該檔案。

然後，應用程式會呼叫 [**IWiaDataTransfer：： idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) 方法來執行資料傳輸：


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



在 [**IWiaDataTransfer：： idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)的呼叫中，第二個參數會指定 [**IWiaDataCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) 介面的指標。 應用程式必須在資料傳輸期間執行此介面來接收回呼。 如需有關如何執行此介面的詳細資訊，請參閱 [**IWiaDataCallback：： BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)。

然後，應用程式會釋放 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) 介面的指標，並釋放 [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構中所配置的任何資料。

應用程式也可以使用記憶體內部資料傳輸（而不是檔案傳輸）來傳輸映射。 在此情況下，應用程式會使用 idtGetBandedData 方法來取代 idtGetData 方法。

以下是完整的資料傳輸範例：


```
HRESULT TransferWiaItem( IWiaItem *pWiaItem )
{
    //
    // Validate arguments
    //
    if (NULL == pWiaItem)
    {
        return E_INVALIDARG;
    }

    //
    // Get the IWiaPropertyStorage interface so you can set required properties.
    //
    IWiaPropertyStorage *pWiaPropertyStorage = NULL;
    HRESULT hr = pWiaItem->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaPropertyStorage );
    if (SUCCEEDED(hr))
    {
        //
        // Prepare PROPSPECs and PROPVARIANTs for setting the
        // media type and format
        //
        PROPSPEC PropSpec[2] = {0};
        PROPVARIANT PropVariant[2] = {0};
        const ULONG c_nPropCount = sizeof(PropVariant)/sizeof(PropVariant[0]);

        //
        // Use BMP as the output format
        //
        GUID guidOutputFormat = WiaImgFmt_BMP;

        //
        // Initialize the PROPSPECs
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_IPA_FORMAT;
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_IPA_TYMED;

        //
        // Initialize the PROPVARIANTs
        //
        PropVariant[0].vt = VT_CLSID;
        PropVariant[0].puuid = &guidOutputFormat;
        PropVariant[1].vt = VT_I4;
        PropVariant[1].lVal = TYMED_FILE;

        //
        // Set the properties
        //
        hr = pWiaPropertyStorage->WriteMultiple( c_nPropCount, PropSpec, PropVariant, WIA_IPA_FIRST );
        if (SUCCEEDED(hr))
        {
            //
            // Get the IWiaDataTransfer interface
            //
            IWiaDataTransfer *pWiaDataTransfer = NULL;
            hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
            if (SUCCEEDED(hr))
            {
                //
                // Create our callback class
                //
                CWiaDataCallback *pCallback = new CWiaDataCallback;
                if (pCallback)
                {
                    //
                    // Get the IWiaDataCallback interface from our callback class.
                    //
                    IWiaDataCallback *pWiaDataCallback = NULL;
                    hr = pCallback->QueryInterface( IID_IWiaDataCallback, (void**)&pWiaDataCallback );
                    if (SUCCEEDED(hr))
                    {
                        //
                        // Perform the transfer using default settings
                        //
                        STGMEDIUM stgMedium = {0};
                        StgMedium.tymed = TYMED_FILE;
                        hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
                        if (S_OK == hr)
                        {
                            //
                            // Print the filename (note that this filename is always
                            // a WCHAR string, not TCHAR).
                            //
                            _tprintf( TEXT("Transferred filename: %ws\n"), stgMedium.lpszFileName );

                            //
                            // Release any memory associated with the stgmedium
                            // This will delete the file stgMedium.lpszFileName.
                            //
                            ReleaseStgMedium( &stgMedium );
                        }

                        //
                        // Release the callback interface
                        //
                        pWiaDataCallback->Release();
                        pWiaDataCallback = NULL;
                    }

                    //
                    // Release our callback.  It should now delete itself.
                    //
                    pCallback->Release();
                    pCallback = NULL;
                }

                //
                // Release the IWiaDataTransfer
                //
                pWiaDataTransfer->Release();
                pWiaDataTransfer = NULL;
            }
        }

        //
        // Release the IWiaPropertyStorage
        //
        pWiaPropertyStorage->Release();
        pWiaPropertyStorage = NULL;
    }

    return hr;
}
```



 

 
