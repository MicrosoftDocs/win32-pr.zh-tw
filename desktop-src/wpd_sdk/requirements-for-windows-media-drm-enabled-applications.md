---
description: Windows Media DRM-Enabled 應用程式的需求
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Windows Media DRM-Enabled 應用程式的需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982807"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a><span data-ttu-id="f62ef-103">Windows Media DRM-Enabled 應用程式的需求</span><span class="sxs-lookup"><span data-stu-id="f62ef-103">Requirements for Windows Media DRM-Enabled Applications</span></span>

<span data-ttu-id="f62ef-104">To create a Windows Media Digital Rights Management (DRM)-enabled application, you must have the headers and libraries described in the [General Requirements for Application Development](general-requirements-for-application-development.md) section of this document.</span><span class="sxs-lookup"><span data-stu-id="f62ef-104">To create a Windows Media Digital Rights Management (DRM)-enabled application, you must have the headers and libraries described in the [General Requirements for Application Development](general-requirements-for-application-development.md) section of this document.</span></span> <span data-ttu-id="f62ef-105">此外，在開啟裝置時，應用程式必須在用戶端資訊中提供其他屬性。</span><span class="sxs-lookup"><span data-stu-id="f62ef-105">In addition, the application will need to supply additional properties in the client information when opening the device.</span></span>

<span data-ttu-id="f62ef-106">下表說明啟用 Windows Media 受 DRM 保護的內容傳輸所需的兩個額外屬性。</span><span class="sxs-lookup"><span data-stu-id="f62ef-106">The two additional properties that are required to enable Windows Media DRM-protected content transfers are described in the following table.</span></span>



| <span data-ttu-id="f62ef-107">屬性</span><span class="sxs-lookup"><span data-stu-id="f62ef-107">Property</span></span>                                      | <span data-ttu-id="f62ef-108">描述</span><span class="sxs-lookup"><span data-stu-id="f62ef-108">Description</span></span>                              |
|-----------------------------------------------|------------------------------------------|
| <span data-ttu-id="f62ef-109">WPD \_ 用戶端 \_ WMDRM \_ 應用程式 \_ 私用 \_ 金鑰</span><span class="sxs-lookup"><span data-stu-id="f62ef-109">WPD\_CLIENT\_WMDRM\_APPLICATION\_PRIVATE\_KEY</span></span> | <span data-ttu-id="f62ef-110">指定應用程式的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="f62ef-110">Specifies the application's private key.</span></span> |
| <span data-ttu-id="f62ef-111">WPD \_ 用戶端 \_ WMDRM \_ 應用程式 \_ 憑證</span><span class="sxs-lookup"><span data-stu-id="f62ef-111">WPD\_CLIENT\_WMDRM\_APPLICATION\_CERTIFICATE</span></span>  | <span data-ttu-id="f62ef-112">指定應用程式的憑證。</span><span class="sxs-lookup"><span data-stu-id="f62ef-112">Specifies the application's certificate.</span></span> |



 

<span data-ttu-id="f62ef-113">當使用 [**IPortableDevice：： Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) 方法開啟裝置時，必須在應用程式的用戶端資訊中提供這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f62ef-113">These properties must be supplied in the application's client information when the device is opened with the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.</span></span> <span data-ttu-id="f62ef-114">當提供這些屬性時，WPD API 會允許受保護的內容傳輸。</span><span class="sxs-lookup"><span data-stu-id="f62ef-114">When these properties are supplied, the WPD API allows protected content transfers.</span></span> <span data-ttu-id="f62ef-115">如果應用程式已提供憑證和私密金鑰，則 API 會建立安全通道，以將受保護的 WMDRM 內容傳輸至裝置。</span><span class="sxs-lookup"><span data-stu-id="f62ef-115">If the application has provided a certificate and private key, the API will create a secure channel to transfer protected WMDRM content to the device.</span></span>

<span data-ttu-id="f62ef-116">如需有關建立和散發支援 Windows Media DRM 之 Windows 應用程式的詳細資訊，請參閱下列以 [windows 為基礎的授權應用程式](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) 主題。</span><span class="sxs-lookup"><span data-stu-id="f62ef-116">For information about creating and distributing Windows-based applications that support Windows Media DRM, see the following [Licensing Windows-based Applications](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) topic.</span></span>

## <a name="transferring-content"></a><span data-ttu-id="f62ef-117">傳送內容</span><span class="sxs-lookup"><span data-stu-id="f62ef-117">Transferring Content</span></span>

<span data-ttu-id="f62ef-118">若要傳送受 WMDRM 保護的內容，請使用 [**IPortableDeviceContent：： CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)。</span><span class="sxs-lookup"><span data-stu-id="f62ef-118">To transfer WMDRM protected content, use [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="f62ef-119">此方法可用於受保護和純文字的內容，而不需要額外的選項。</span><span class="sxs-lookup"><span data-stu-id="f62ef-119">This method can be used for both protected and clear content without additional options.</span></span> <span data-ttu-id="f62ef-120">WPD API 會根據內容是否受到保護或清除，自動選取受保護或清除的通道。</span><span class="sxs-lookup"><span data-stu-id="f62ef-120">The WPD API will automatically select the protected or clear channel depending on whether the content is protected or clear.</span></span> <span data-ttu-id="f62ef-121">它會與 WMDRM 安全內容提供者互動以處理 WMDRM 授權。</span><span class="sxs-lookup"><span data-stu-id="f62ef-121">It interfaces with the WMDRM Secure Content Provider to process the WMDRM licenses.</span></span>

## <a name="transferring-known-clear-content"></a><span data-ttu-id="f62ef-122">傳送已知的清楚內容</span><span class="sxs-lookup"><span data-stu-id="f62ef-122">Transferring Known Clear Content</span></span>

<span data-ttu-id="f62ef-123">如果您已啟用應用程式來處理受保護的內容，但您知道特定檔案未受到保護，您可以在呼叫 [**IPortableDeviceContent：： CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)以取得清除 **內容時，** 將 **WPD \_ API 選項 [ \_ \_ 使用 \_ 清除 \_ 資料流程 \_** ] 選項設定為 [TRUE]，以告知 WPD 略過 DRM 處理。</span><span class="sxs-lookup"><span data-stu-id="f62ef-123">If you've enabled your application to handle protected content, but you know that a specific file is not protected, you can tell WPD to skip the DRM processing by setting **WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM** option to TRUE in the input **IPortableDeviceValues** when calling [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) for clear content.</span></span>

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a><span data-ttu-id="f62ef-124">使用 IWMDRMDeviceApp 存取計量作業</span><span class="sxs-lookup"><span data-stu-id="f62ef-124">Accessing Metering Operations using IWMDRMDeviceApp</span></span>

<span data-ttu-id="f62ef-125">WPD 提供一種機制，可存取授權更新和計量資料抓取的 **IWMDRMDeviceApp** api。</span><span class="sxs-lookup"><span data-stu-id="f62ef-125">WPD provides a mechanism to access the **IWMDRMDeviceApp** APIs for license updates and metering data retrieval.</span></span> <span data-ttu-id="f62ef-126">若要透過 WPD 存取此 API，請從 [**IPortableDeviceContent：： CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)傳回的 **IStream** 呼叫 **IID \_ IWMDRMDeviceApp** 上的 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="f62ef-126">To access this API through WPD, call **QueryInterface** on **IID\_IWMDRMDeviceApp** from the **IStream** returned from [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="f62ef-127">這個 **IWMDRMDeviceApp** 實例系結至與您的 WMDRM 相容裝置 **IPortableDevice** 的連線，而不是已取得 **IStream** 之特定內容的連結。</span><span class="sxs-lookup"><span data-stu-id="f62ef-127">This **IWMDRMDeviceApp** instance tied to the **IPortableDevice** connection to your WMDRM-compatible device, and not the specific content where the **IStream** was obtained.</span></span> <span data-ttu-id="f62ef-128">WPD 會在內部包裝計量 Api，並使其可供您的應用程式存取。</span><span class="sxs-lookup"><span data-stu-id="f62ef-128">WPD internally wraps the metering APIs and makes it accessible to your application.</span></span> <span data-ttu-id="f62ef-129">您的應用程式應該 \_ \_ 針對 IWMDMDevice 參數使用 WMDRMDEVICEAPP use WPD \_ 裝置 \_ PTR 常數 \* 。</span><span class="sxs-lookup"><span data-stu-id="f62ef-129">Your application should use the WMDRMDEVICEAPP\_USE\_WPD\_DEVICE\_PTR constant for the *IWMDMDevice*\* parameter.</span></span>

<span data-ttu-id="f62ef-130">下列程式碼片段會示範這一點。</span><span class="sxs-lookup"><span data-stu-id="f62ef-130">The following code snippet demonstrates this.</span></span>


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



<span data-ttu-id="f62ef-131">應用程式私密金鑰和憑證的必要條件也同樣適用于此處。</span><span class="sxs-lookup"><span data-stu-id="f62ef-131">The same pre-requisite with the application private key and certificate applies here as well.</span></span> <span data-ttu-id="f62ef-132">如果金鑰/憑證無效，或 WMDRM 系統無法初始化， **QueryInferface** 呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="f62ef-132">If the key/certificate is invalid or if the WMDRM system fails to initialize, the **QueryInferface** call will fail.</span></span>

<span data-ttu-id="f62ef-133">如果您的應用程式已經執行先前受保護的內容傳輸，上述從 **IStream** 指標取得 **IWMDRMDeviceApp** 介面的方法就是很方便的方法，然後再繼續進行計量和授權同步處理作業。</span><span class="sxs-lookup"><span data-stu-id="f62ef-133">The above method to acquire the **IWMDRMDeviceApp** interface from the **IStream** pointer is just a convenience if your application is already doing a prior protected content transfer, before proceeding on to do metering and license synchronization operations.</span></span>

<span data-ttu-id="f62ef-134">對於需要存取 **IWMDRMDeviceApp** 的大部分應用程式，我們的建議是直接初始化 **IWMDRMDeviceApp** ，因為這不需要您的應用程式傳送受保護的內容或保存到傳輸介面，以便進行裝置計量和授權同步處理。此方法需要使用 Windows Media 裝置管理員 (WMDM) Api。</span><span class="sxs-lookup"><span data-stu-id="f62ef-134">Our recommendation for most applications that need to access **IWMDRMDeviceApp** is to initialize **IWMDRMDeviceApp** directly as this does not require your application to transfer protected content or hold on to the transfer interfaces in order to do device metering and license sync. This method will require usage of Windows Media Device Manager (WMDM) APIs.</span></span> <span data-ttu-id="f62ef-135">如需詳細資訊和範例程式碼，請參閱 WHDC 網站上的 [從 WPD 應用程式存取 WMDRM api](../windows-portable-devices.md) 白皮書。</span><span class="sxs-lookup"><span data-stu-id="f62ef-135">For details and sample code, refer to the [Accessing WMDRM APIs from a WPD Application](../windows-portable-devices.md) whitepaper on the WHDC site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f62ef-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="f62ef-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f62ef-137">**Windows 可攜式裝置**</span><span class="sxs-lookup"><span data-stu-id="f62ef-137">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
