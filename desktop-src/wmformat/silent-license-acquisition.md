---
title: 無訊息授權取得
description: 無訊息授權取得
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows Media Format SDK，無提示授權取得
- Windows Media Format SDK，授權
- 數位版權管理 (DRM) ，無訊息授權取得
- DRM (數位版權管理) ，無訊息授權取得
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- DRM 用戶端擴充 Api，無提示授權取得
- 用戶端擴充 Api，取得無訊息授權
- 無訊息授權取得
- 授權，取得無訊息授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021736"
---
# <a name="silent-license-acquisition"></a><span data-ttu-id="d35a0-113">無訊息授權取得</span><span class="sxs-lookup"><span data-stu-id="d35a0-113">Silent License Acquisition</span></span>

<span data-ttu-id="d35a0-114">無訊息授權取得只需要單一方法呼叫，就能以非同步方式處理授權伺服器的所有網路通訊。</span><span class="sxs-lookup"><span data-stu-id="d35a0-114">Silent license acquisition requires only a single method call that handles all of the network communications with the license server asynchronously.</span></span>

<span data-ttu-id="d35a0-115">這種授權取得通常是用來回應嘗試存取受保護內容的使用者，例如，嘗試在 media player 應用程式中播放受保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="d35a0-115">This type of license acquisition is usually used as a response to the end user trying to access protected content—for example, trying to play a protected file in a media player application.</span></span> <span data-ttu-id="d35a0-116">因為無訊息授權取得會取得具有單一呼叫的授權，所以如果需要來自使用者的額外輸入（例如內容的付款），就不能使用它。</span><span class="sxs-lookup"><span data-stu-id="d35a0-116">Because silent license acquisition gets the license with a single call, it cannot be used if additional input from the user, such as payment for the content, is required.</span></span>

<span data-ttu-id="d35a0-117">若要執行無訊息授權取得，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d35a0-117">To perform silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="d35a0-118">呼叫 [**IWMDRMLicenseManagement：： AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d35a0-118">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="d35a0-119">從受保護的檔案傳入 DRM 標頭作為 *bstrHeaderData* 參數。</span><span class="sxs-lookup"><span data-stu-id="d35a0-119">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="d35a0-120">在 *bstrActions* 參數中指定您希望授權授與的許可權。</span><span class="sxs-lookup"><span data-stu-id="d35a0-120">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="d35a0-121">最後，將 *dwFlags* 參數設定為 WMDRM \_ 取得 \_ 授權 \_ 無訊息。</span><span class="sxs-lookup"><span data-stu-id="d35a0-121">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_SILENT.</span></span>
2.  <span data-ttu-id="d35a0-122">[**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)介面的陷阱事件。</span><span class="sxs-lookup"><span data-stu-id="d35a0-122">Trap events for the [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span> <span data-ttu-id="d35a0-123">當您收到 **MEWMDRMLicenseAcquisitionCompleted** 事件時，請呼叫 **IMFMediaEvent：： GetStatus** 方法（記載于媒體基礎檔中）來檢查其傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d35a0-123">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, check its return code by calling the **IMFMediaEvent::GetStatus** method, which is documented in the Media Foundation documentation.</span></span> <span data-ttu-id="d35a0-124">如果取出的 **HRESULT** 值是成功的程式碼，則表示授權已成功下載，且位於本機授權存放區，可供使用。</span><span class="sxs-lookup"><span data-stu-id="d35a0-124">If the retrieved **HRESULT** value is a success code, then the license was successfully downloaded and is in the local license store ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d35a0-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="d35a0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d35a0-126">**取得授權**</span><span class="sxs-lookup"><span data-stu-id="d35a0-126">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="d35a0-127">**使用媒體基礎事件模型**</span><span class="sxs-lookup"><span data-stu-id="d35a0-127">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




