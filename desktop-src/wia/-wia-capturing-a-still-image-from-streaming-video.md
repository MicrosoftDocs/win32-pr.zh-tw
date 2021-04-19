---
description: 下列範例會使用 IWiaVideo 介面來建立串流影片預覽，並從該串流影片取得靜止影像。 此範例假設您有一個有效的視窗控制碼 (HWND) 。
ms.assetid: bca00825-32a7-40b2-9ca9-23475e3218a8
title: 從串流影片中捕捉靜止影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf43acdb1bd472a9d5a5dca2344b2f4ad37f474a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969374"
---
# <a name="capturing-a-still-image-from-streaming-video"></a>從串流影片中捕捉靜止影像

下列範例會使用 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) 介面來建立串流影片預覽，並從該串流影片取得靜止影像。 此範例假設您有一個有效的視窗控制碼 (HWND) 。

> [!Note]  
> Windows 映像取得 (WIA) 不支援 Windows Server 2003、Windows Vista 或更新版本中的影片裝置。 針對這些版本的 Windows，請使用 [DirectShow](/previous-versions//ms783323(v=vs.85)) 從影片取得影像。

 


```
    //
    // Set up variables
    //

    HRESULT             hr                  = S_OK;
    IWiaDevMgr          *pIWiaDevMgr        = NULL;
    IWiaVideo           *pWiaVideo          = NULL;
    IEnumWIA_DEV_INFO   *pWiaEnumDevInfo    = NULL;
    IWiaItem            *pRootItem          = NULL;
    IWiaPropertyStorage *pIWiaPropStorage   = NULL;
    ULONG               ulFetched           = NULL;
    BSTR                DeviceID            = NULL;
    BSTR                ImagesDirectory     = NULL;
    BSTR                FileName            = NULL;
    BOOL                bFound              = FALSE;

    //
    // Initialize COM for this thread
    //
    CoInitializeEx(NULL, COINIT_MULTITHREADED);

    //
    // Create the WIA Device Manager.  Use this to find WIA streaming 
    //   video devices.
    //

    hr = CoCreateInstance(CLSID_WiaDevMgr,
                          NULL,
                          CLSCTX_LOCAL_SERVER,
                          IID_IWiaDevMgr,
                          (void**)&pIWiaDevMgr);

    //
    // Create the WIA Video object.  Use this to display video and capture 
    // still images from the video stream.
    //

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WiaVideo,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWiaVideo,
                              (LPVOID *) &pWiaVideo);
    }

    //
    // To find the first WIA-supported streaming video device,
    // enumerate all the WIA devices and query the
    // WIA_DIP_DEV_TYPE property.
    //
    if (SUCCEEDED(hr))
    {
        //
        // Enumerate WIA devices on the system
        //

        hr = pIWiaDevMgr->EnumDeviceInfo(WIA_DEVINFO_ENUM_LOCAL,
                                         &pWiaEnumDevInfo);
    }

    //
    // Reset the enumeration to start at the beginning of the list.
    //
    if (SUCCEEDED(hr))
    {
        //
        // Call Reset on Enumerator
        //

        hr = pWiaEnumDevInfo->Reset();
    }

    while ((SUCCEEDED(hr)) && (!bFound))
    {
        IWiaPropertyStorage *pIWiaPropStg = NULL;

        //
        // Get the next WIA device
        //

        hr = pWiaEnumDevInfo->Next(1,
                                   &pIWiaPropStg,
                                   &ulFetched);

        if (hr == S_OK)
        {
            //
            // Get the device type of the device
            //

            PROPSPEC    PropSpec[2];
            PROPVARIANT PropVar[2];

            memset(PropVar,0,sizeof(PropVar));

            PropSpec[0].ulKind = PRSPEC_PROPID;
            PropSpec[0].propid = WIA_DIP_DEV_ID;
            PropSpec[1].ulKind = PRSPEC_PROPID;
            PropSpec[1].propid = WIA_DIP_DEV_TYPE;

            //
            // Get the type and the ID of each device
            //

            hr = pIWiaPropStg->ReadMultiple(sizeof(PropSpec)/sizeof(PROPSPEC),
                                            PropSpec,
                                            PropVar);

            //
            // If the device is a streaming video device, get
            // its ID
            //

            if (GET_STIDEVICE_TYPE(PropVar[1].lVal) == StiDeviceTypeStreamingVideo)
            {
                DeviceID = PropVar[0].bstrVal;
                bFound = TRUE;
            }
        }

        if (pIWiaPropStg)
        {
            pIWiaPropStg->Release();
            pIWiaPropStg = NULL;
        }
    }

    if (!bFound)
    {
        //
        // No WIA video streaming devices found. There is nothing left
        // to do.  Set result to E_FAIL.
        //
        hr = E_FAIL;
    }

    //
    // If you found a WIA streaming video device, get the directory in
    // which the new images will be stored.
    //
    if (SUCCEEDED(hr))
    {
        //
        // Create a WIA device and get the recommended
        // images directory.
        //

        hr = pIWiaDevMgr->CreateDevice(DeviceID,
                                       &pRootItem);

        //
        // Device has been created; now get its property storage interface.
        //
        if (SUCCEEDED(hr))
        {
            hr = pRootItem->QueryInterface(IID_IWiaPropertyStorage,
                                           &pIWiaPropStorage);
        }
    }

    //
    // Property storeage interface is on the WIA device; now
    // ask for the WIA_DPV_IMAGES_DIRECTORY property.
    //
    if (SUCCEEDED(hr))
    {
        PROPSPEC    PropSpec2[1];
        PROPVARIANT PropVar2[1];

        memset(PropVar2, 0, sizeof(PropVar2));

        PropSpec2[0].ulKind = PRSPEC_PROPID;
        PropSpec2[0].propid = WIA_DPV_IMAGES_DIRECTORY;

        hr = pIWiaPropStorage->ReadMultiple(sizeof(PropSpec2)/sizeof(PROPSPEC),
                                            PropSpec2,
                                            PropVar2);

        if (SUCCEEDED(hr))
        {
            ImagesDirectory = PropVar2[0].bstrVal;
        }
    }

    //
    // Tell the WIA Video object about the images directory 
    // to store pictures into. You asked the WIA device
    // for the images directory, now pass this value to the WIA Video
    // object.
    //
    if (SUCCEEDED(hr))
    {
        //
        // Set the images directory
        //

        hr = pWiaVideo->put_ImagesDirectory(ImagesDirectory);
    }

    //
    // Create the video.  When this function returns, you should see
    // live video playing in our hWnd window.
    //
    // The hWnd is the window handle of the window created to host the video.
    //
    if (SUCCEEDED(hr))
    {
        hr = pWiaVideo->CreateVideoByWiaDevID(DeviceID, hWnd, FALSE, TRUE);
    }


    //
    // Take a picture. When this function returns, WIA Video will have already
    // captured a still image from the video stream and saved the image in
    // the FileName file.
    //
    if (SUCCEEDED(hr))
    {
        hr = pWiaVideo->TakePicture(&FileName);
    }

    //
    // Run this code when you are shutting down your application.
    //

    //
    // Exit the application and destroy the video playback.
    //
    if (pWiaVideo)
    {
        pWiaVideo->DestroyVideo();
    }

    //
    // Release all the interface pointers acquired.
    //

    if (pWiaEnumDevInfo)
    {
        pWiaEnumDevInfo->Release();
        pWiaEnumDevInfo = NULL;
    }

    if (pRootItem)
    {
        pRootItem->Release();
        pRootItem = NULL;
    }

    if (pIWiaPropStorage)
    {
        pIWiaPropStorage->Release();
        pIWiaPropStorage = NULL;
    }

    if (pIWiaDevMgr)
    {
        pIWiaDevMgr->Release();
        pIWiaDevMgr = NULL;
    }

    if (pWiaVideo)
    {
        pWiaVideo->Release();
        pWiaVideo = NULL;
    }

    //
    // Free all the BSTRs you received.
    //

    if (DeviceID != NULL)
    {
        SysFreeString(DeviceID);
        DeviceID = NULL;
    }

    if (ImagesDirectory != NULL)
    {
        SysFreeString(ImagesDirectory);
        ImagesDirectory = NULL;
    }

    //
    // Uninitialize COM for this thread.
    //
    CoUninitialize();

    //
    // Exit application
    //
    return hr;
}
```



 

 
