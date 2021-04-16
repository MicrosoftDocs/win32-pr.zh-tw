---
title: 取得非無訊息授權
description: 取得非無訊息授權
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows Media Format SDK，非無訊息授權取得
- Windows Media Format SDK，授權
- 數位版權管理 (DRM) 、非無訊息授權取得
- DRM (數位版權管理) 、非無訊息授權取得
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- DRM 用戶端擴充 Api、非無訊息授權取得
- 用戶端擴充 Api、非無訊息授權取得
- 取得非無訊息授權
- 授權，非無訊息授權取得
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507428"
---
# <a name="non-silent-license-acquisition"></a><span data-ttu-id="8d553-113">取得非無訊息授權</span><span class="sxs-lookup"><span data-stu-id="8d553-113">Non-Silent License Acquisition</span></span>

<span data-ttu-id="8d553-114">非無訊息授權取得可讓授權提供者透過網頁與終端使用者互動，作為授權取得程式中的中繼步驟。</span><span class="sxs-lookup"><span data-stu-id="8d553-114">Non-silent license acquisition enables the license provider to interact with the end user through a Web page, as an intermediate step in the license acquisition process.</span></span> <span data-ttu-id="8d553-115">為了回應嘗試存取受保護內容的使用者，而起始了非無訊息授權取得。</span><span class="sxs-lookup"><span data-stu-id="8d553-115">Non-silent license acquisition is initiated in response to a user trying to access protected content.</span></span>

<span data-ttu-id="8d553-116">若要執行非無訊息授權取得，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="8d553-116">To perform non-silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="8d553-117">呼叫 [**IWMDRMLicenseManagement：： AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8d553-117">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="8d553-118">從受保護的檔案傳入 DRM 標頭作為 *bstrHeaderData* 參數。</span><span class="sxs-lookup"><span data-stu-id="8d553-118">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="8d553-119">在 *bstrActions* 參數中指定您希望授權授與的許可權。</span><span class="sxs-lookup"><span data-stu-id="8d553-119">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="8d553-120">最後，將 *dwFlags* 參數設定為 [WMDRM \_ 取得 \_ 授權 NONSILENT] \_ 。</span><span class="sxs-lookup"><span data-stu-id="8d553-120">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_NONSILENT.</span></span>
2.  <span data-ttu-id="8d553-121">**IWMDRMLicenseManagement** 介面的陷阱事件。</span><span class="sxs-lookup"><span data-stu-id="8d553-121">Trap events for the **IWMDRMLicenseManagement** interface.</span></span> <span data-ttu-id="8d553-122">當您收到 **MEWMDRMLicenseAcquisitionCompleted** 事件時，請呼叫 **IMFMediaEvent：： GetValue** 來取得其相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="8d553-122">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, get its associated value by calling **IMFMediaEvent::GetValue**.</span></span> <span data-ttu-id="8d553-123">值的類型應該是 VT UNKNOWN，也就是 \_ **IUnknown** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8d553-123">The value should be of type VT\_UNKNOWN, a pointer to an **IUnknown** interface.</span></span>
3.  <span data-ttu-id="8d553-124">針對步驟2中所抓取的 **IUnknown** 介面呼叫 **QueryInterface** 方法，以取得 [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)介面。</span><span class="sxs-lookup"><span data-stu-id="8d553-124">Call the **QueryInterface** method of the **IUnknown** interface retrieved in step 2 to get the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>
4.  <span data-ttu-id="8d553-125">呼叫 [**IWMDRMNonSilentLicenseAquisition：： GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) 來取得授權挑戰。</span><span class="sxs-lookup"><span data-stu-id="8d553-125">Call [**IWMDRMNonSilentLicenseAquisition::GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) to retrieve the license challenge.</span></span> <span data-ttu-id="8d553-126">如果您沒有授權伺服器的 URL，也請呼叫 [**IWMDRMNonSilentLicenseAquisition：： GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) 。</span><span class="sxs-lookup"><span data-stu-id="8d553-126">Also call [**IWMDRMNonSilentLicenseAquisition::GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) if you do not have the URL of the license server already.</span></span>
5.  <span data-ttu-id="8d553-127">將挑戰傳送至 URL 所指定的網頁。</span><span class="sxs-lookup"><span data-stu-id="8d553-127">Send the challenge to the Web page specified by the URL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d553-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d553-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d553-129">**取得授權**</span><span class="sxs-lookup"><span data-stu-id="8d553-129">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="8d553-130">**使用媒體基礎事件模型**</span><span class="sxs-lookup"><span data-stu-id="8d553-130">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




