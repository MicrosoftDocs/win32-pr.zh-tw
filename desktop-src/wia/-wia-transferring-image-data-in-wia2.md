---
description: 由於影像資料傳輸是以資料流程為基礎，在 Windows 映像取得 (WIA) 2.0 中，因此您不需要指定目的地類型 (例如
ms.assetid: ebb9fce5-9450-4ffe-b480-b21670b60f90
title: 在 WIA 2.0 中傳送影像資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ded5c6cd8fb94b1beccd86c3cd8aef3018aed0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318439"
---
# <a name="transferring-image-data-in-wia-20"></a><span data-ttu-id="f9ae6-103">在 WIA 2.0 中傳送影像資料</span><span class="sxs-lookup"><span data-stu-id="f9ae6-103">Transferring Image Data in WIA 2.0</span></span>

> [!Note]  
> <span data-ttu-id="f9ae6-104">本教學課程示範如何在 Windows Vista 或更新版本上執行的應用程式中傳送影像資料。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-104">This tutorial demonstrates how to transfer image data in applications that run on Windows Vista or later.</span></span> <span data-ttu-id="f9ae6-105">如需在 Windows XP 或更早版本上執行的應用程式中傳送影像資料的相關資訊，請參閱 [WIA 1.0 中的傳輸影像資料](-wia-transferring-image-data.md) 。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-105">See [Transfering Image Data in WIA 1.0](-wia-transferring-image-data.md) for information about transferring image data in applications that run on Windows XP or earlier.</span></span>

 

<span data-ttu-id="f9ae6-106">因為影像資料傳輸在 Windows 映像取得中是以資料流程為基礎 (WIA) 2.0，所以您不需要指定目的地類型 (例如記憶體或檔案) 。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-106">Because image data transfer is stream-based in Windows Image Acquisition (WIA) 2.0, you do not need to specify a destination type (e.g. memory or file).</span></span> <span data-ttu-id="f9ae6-107">應用程式只會提供 WIA 2.0 要使用的資料流程，驅動程式會讀取或寫入資料流程。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-107">The application simply gives WIA 2.0 the stream to use, and the driver reads or writes to the stream.</span></span> <span data-ttu-id="f9ae6-108">資料流程可以是檔案資料流程、記憶體資料流程或任何其他類型的資料流程，並且對驅動程式是透明的。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-108">The stream can be a file stream, a memory stream, or any other type of stream, and is transparent to the driver.</span></span> <span data-ttu-id="f9ae6-109">使用資料流程也可讓您輕鬆地與影像處理篩選器整合。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-109">Using streams also provides an easy integration with the Image Processing filter.</span></span>

<span data-ttu-id="f9ae6-110">使用 [**IWiaTransfer**](-wia-iwiatransfer.md) 介面的方法，將資料從 WIA 2.0 裝置傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-110">Use the methods of the [**IWiaTransfer**](-wia-iwiatransfer.md) interface to transfer data from a WIA 2.0 device to an application.</span></span> <span data-ttu-id="f9ae6-111">這個介面可透過 [**IWiaItem2**](-wia-iwiaitem2.md) 介面取得。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-111">This interface is available through the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="f9ae6-112">**IWiaTransfer** 介面具有在裝置上要求上傳或下載資料的方法。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-112">The **IWiaTransfer** interface has methods for requesting uploading or downloading of data to and from a device.</span></span> <span data-ttu-id="f9ae6-113">這些方法會取得應用程式所提供的回呼，並使用應用程式為數據傳輸的實際目的地所提供的 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-113">These methods take a callback that the application provides, and use an [IStream](/windows/win32/api/objidl/nn-objidl-istream) provided by the application for the actual destination of the data transfer.</span></span>

<span data-ttu-id="f9ae6-114">應用程式必須查詢影像專案，以取得其 [**IWiaTransfer**](-wia-iwiatransfer.md) 介面的指標，如下列程式碼範例所示：</span><span class="sxs-lookup"><span data-stu-id="f9ae6-114">Applications must query an image item to obtain a pointer to its [**IWiaTransfer**](-wia-iwiatransfer.md) interface, as shown in the following code sample:</span></span>


```
    // Get the IWiaTransfer interface
    //
    IWiaTransfer *pWiaTransfer = NULL;
    hr = pIWiaItem2->QueryInterface(IID_IWiaTransfer,(void**)&pWiaTransfer);
```



<span data-ttu-id="f9ae6-115">在先前的程式碼中，我們假設 **pWiaItem2** 是 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的有效指標。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-115">In the previous code, we assume that **pWiaItem2** is a valid pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="f9ae6-116">對 [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))的呼叫會以 **pWiaItem2** 所參考專案的 [**IWiaTransfer**](-wia-iwiatransfer.md)介面指標填滿 **pWiaTransfer** 。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-116">The call to [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) fills **pWiaTransfer** with a pointer to the [**IWiaTransfer**](-wia-iwiatransfer.md) interface of the item referred to by **pWiaItem2**.</span></span>

<span data-ttu-id="f9ae6-117">然後，應用程式會將回呼物件具現化，如下所示。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-117">The application then instantiates the callback object, as shown here.</span></span>


```
    //   Instantiate the object which receives the callbacks
    //
    CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
```



<span data-ttu-id="f9ae6-118">應用程式接著會使用 [**IWiaItem2**](-wia-iwiaitem2.md)專案的 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)介面來設定屬性，並執行傳送。</span><span class="sxs-lookup"><span data-stu-id="f9ae6-118">The application next sets the properties by using [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface of [**IWiaItem2**](-wia-iwiaitem2.md) item, and performs the transfer.</span></span>

<span data-ttu-id="f9ae6-119">下載:</span><span class="sxs-lookup"><span data-stu-id="f9ae6-119">Downloading:</span></span>


```
    // Download   
    hr = pWiaTransfer->Download(0,pWiaClassCallback);
```



<span data-ttu-id="f9ae6-120">上傳：</span><span class="sxs-lookup"><span data-stu-id="f9ae6-120">Uploading:</span></span>


```
    //Create child item which eventually will be the uploaded image 
    IWiaItem2* pWiaItemChild = NULL;
    HRESULT hr = pIWiaItem2->CreateChildItem(WiaItemTypeImage|WiaItemTypeFile,0,bzUploadFileName,&pWiaItemChild);
    
    if(SUCCEEDED(hr))
    {
                
        //Set the format for the child item as BMP 
        IWiaPropertyStorage* pWiaChildPropertyStorage = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaChildPropertyStorage );
        if(SUCCEEDED(hr))
        {
            WritePropertyGuid(pWiaChildPropertyStorage,WIA_IPA_FORMAT,WiaImgFmt_BMP );

            //release pWiaChildPropertyStorage
            pWiaChildPropertyStorage->Release();
            pWiaChildPropertyStorage = NULL;
        }
        

        //Get the IWiaTransfer interface of the child
        IWiaTransfer* pWiaTransferChild = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransferChild );
        if(SUCCEEDED(hr)){
            IStream* pUploadStream = NULL;
                                        
            //Create stream on test.BMP file
            hr = SHCreateStreamOnFile(L"test.BMP",STGM_READ, &pUploadStream);
            if(SUCCEEDED(hr)){
                pWiaTransferChild->Upload(0,pUploadStream,pWiaClassCallback);
                
            }
         }
   
      }
```



<span data-ttu-id="f9ae6-121">以下是完整的資料傳輸範例：</span><span class="sxs-lookup"><span data-stu-id="f9ae6-121">Here is the complete data transfer sample:</span></span>


```
HRESULT TransferWiaItem( IWiaItem2 *pIWiaItem2)
{
    // Validate arguments
    if (NULL == pIWiaItem2)
    {
        _tprintf(TEXT("\nInvalid parameters passed"));
        return E_INVALIDARG;
    }
    
    // Get the IWiaTransfer interface
    IWiaTransfer *pWiaTransfer = NULL;
    HRESULT hr = pIWiaItem2->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransfer );
    if (SUCCEEDED(hr))
    {
        // Create our callback class
        CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
        if (pWiaClassCallback)
        {
            
              LONG lItemType = 0;
              hr = pIWiaItem2->GetItemType( &lItemType );

              //download all items which have WiaItemTypeTransfer flag set
              if(lItemType & WiaItemTypeTransfer)
              {

                  // If it is a folder, do folder download . Hence with one API call, all the leaf nodes of this folder 
                  // will be transferred
                  if ((lItemType & WiaItemTypeFolder))
                  {
                        _tprintf ( L"\nI am a folder item");
                        hr = pWiaTransfer->Download(WIA_TRANSFER_ACQUIRE_CHILDREN, pWiaClassCallback);
                        if(S_OK == hr)
                        {
                            _tprintf(TEXT("\npWiaTransfer->Download() on folder item SUCCEEDED"));
                        }
                        else if(S_FALSE == hr)
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item returned S_FALSE. Folder may not be having child items"),hr);
                        }
                        else if(FAILED(hr))
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item failed"),hr);
                        }
                   }

                  
                  // If this is an file type, do file download
                  else if (lItemType & WiaItemTypeFile )
                  {
                      hr = pWiaTransfer->Download(0,pWiaClassCallback);
                      if(S_OK == hr)
                      {
                          _tprintf(TEXT("\npWiaTransfer->Download() on file item SUCCEEDED"));
                      }
                      else if(S_FALSE == hr)
                      {
                          ReportError(TEXT("\npWiaTransfer->Download() on file item returned S_FALSE. File may be empty"),hr);
                      }
                      else if(FAILED(hr))
                      {
                         ReportError(TEXT("\npWiaTransfer->Download() on file item failed"),hr);
                      }
                  }                     
                }
                
                // Release our callback.  It should now delete itself.
                pWiaClassCallback->Release();
                pWiaClassCallback = NULL;
        }
        else
        {
            ReportError( TEXT("\nUnable to create CWiaTransferCallback class instance") );
        }
            
        // Release the IWiaTransfer
        pWiaTransfer->Release();
        pWiaTransfer = NULL;
    }
    else
    {
        ReportError( TEXT("\npIWiaItem2->QueryInterface failed on IID_IWiaTransfer"), hr );
    }
    return hr;
}

// Callback Class should be something like this:

class CWiaTransferCallback : public IWiaTransferCallback
{
public: // Constructors, destructor
    CWiaTransferCallback () : m_cRef(1) {};
    ~ CWiaTransferCallback () {};

public: // IWiaTransferCallback
    HRESULT __stdcall TransferCallback(
        LONG                lFlags,
        WiaTransferParams   *pWiaTransferParams)
    {
        HRESULT hr = S_OK;

        switch (pWiaTransferParams->lMessage)
        {
            case WIA_TRANSFER_MSG_STATUS:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_STREAM:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_TRANSFER:
                ...
                break;
            default:
                break;
        }

        return hr;
    }

    HRESULT __stdcall GetNextStream(
        LONG    lFlags,
        BSTR    bstrItemName,
        BSTR    bstrFullItemName,
        IStream **ppDestination)
    {

        HRESULT hr = S_OK;

        //  Return a new stream for this item's data.
        //
        hr = CreateDestinationStream(bstrItemName, ppDestination);
        return hr;
    }

public: // IUnknown
        .
        .
        . // Etc.

private:
    /// For ref counting implementation
    LONG                m_cRef;
};

```



 

 
