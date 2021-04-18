---
title: 使用撤銷清單
description: 使用撤銷清單
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Windows Media Format SDK，撤銷清單
- Advanced Systems Format (ASF) ，撤銷清單
- ASF (Advanced Systems Format) ，撤銷清單
- 撤銷清單
- 數位版權管理 (DRM) ，撤銷清單
- DRM (數位版權管理) ，撤銷清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f4eca82dd82c9225406a85034ff2a6df227fce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507776"
---
# <a name="working-with-revocation-lists"></a><span data-ttu-id="0eb25-109">使用撤銷清單</span><span class="sxs-lookup"><span data-stu-id="0eb25-109">Working with Revocation Lists</span></span>

<span data-ttu-id="0eb25-110">為了回應安全性缺口，並確保已知被破壞或遭入侵的播放機應用程式無法播放或使用受保護的檔案，每個發行的授權都包含一個撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="0eb25-110">To respond to security breaches and to ensure that player applications known to be broken or compromised cannot play or use protected files, each license that is issued contains a revocation list.</span></span> <span data-ttu-id="0eb25-111">撤銷清單包含所有已知已中斷或損毀的播放程式應用程式憑證。</span><span class="sxs-lookup"><span data-stu-id="0eb25-111">A revocation list contains the application certificates of all those player applications known to be broken or corrupted.</span></span> <span data-ttu-id="0eb25-112">收到新的授權時，播放機應用程式的 DRM 元件會檢查是否有撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="0eb25-112">When a new license is received, the DRM component of the player application checks for a revocation list.</span></span> <span data-ttu-id="0eb25-113">如果發現比目前電腦上的新版本還要新，則會儲存較新的清單。</span><span class="sxs-lookup"><span data-stu-id="0eb25-113">If one is found that is newer than the one currently on the computer, the newer list is stored.</span></span> <span data-ttu-id="0eb25-114">當取用者下次播放受保護的 ASF 檔案時，DRM 元件會將播放程式應用程式與撤銷清單進行比較。</span><span class="sxs-lookup"><span data-stu-id="0eb25-114">The next time the consumer plays a protected ASF file, the DRM component compares the player application to the revocation list.</span></span> <span data-ttu-id="0eb25-115">如果播放機應用程式已遭撤銷，DRM 元件會將錯誤訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="0eb25-115">If the player application is revoked, the DRM component sends an error message to the application.</span></span>

<span data-ttu-id="0eb25-116">在下列案例中，播放程式應用程式可能會收到撤銷錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="0eb25-116">Player applications can receive a revocation error message in the following scenarios:</span></span>

-   <span data-ttu-id="0eb25-117">當應用程式針對受保護的檔案呼叫 [**IWMDRMReader：： AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) 方法之後，就會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="0eb25-117">The error message is received after the application calls the [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) method for a protected file.</span></span> <span data-ttu-id="0eb25-118">呼叫會失敗，並已撤銷 **HRESULT** 程式碼 NS \_ E \_ DRM \_ APPCERT \_ ，該程式碼會提供給 **OnStatus** 回呼函式 WMT \_ 取得 \_ 授權狀態。</span><span class="sxs-lookup"><span data-stu-id="0eb25-118">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the **OnStatus** callback function with WMT\_ACQUIRE\_LICENSE status.</span></span> <span data-ttu-id="0eb25-119">如果忽略此 **HRESULT** 程式碼，將會繼續發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="0eb25-119">If this **HRESULT** code is ignored, errors will continue to occur.</span></span>
-   <span data-ttu-id="0eb25-120">當應用程式建立啟用 DRM 的讀取器，並針對受保護的檔案呼叫 [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) 方法時，就會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="0eb25-120">The error message is received when the application creates the DRM-enabled reader and calls the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method for a protected file.</span></span> <span data-ttu-id="0eb25-121">呼叫會失敗，並已撤銷 **HRESULT** 程式碼 NS \_ E \_ DRM \_ APPCERT \_ ，此程式碼會提供給 [**IWMStatusCallback：： ONSTATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法，並已 \_ 開啟 WMT 狀態。</span><span class="sxs-lookup"><span data-stu-id="0eb25-121">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method with WMT\_OPENED status.</span></span> <span data-ttu-id="0eb25-122">當播放程式應用程式收到此錯誤訊息時，應用程式應該通知終端使用者，並提供方法將功能還原至其播放程式。</span><span class="sxs-lookup"><span data-stu-id="0eb25-122">When a player application receives this error message, the application should notify end users and provide a way for them to restore functionality to their player.</span></span> <span data-ttu-id="0eb25-123">例如，應用程式可以開啟 URL，讓使用者可以下載遭入侵應用程式的升級。</span><span class="sxs-lookup"><span data-stu-id="0eb25-123">For example, the application can open a URL where end users can download an upgrade for the compromised application.</span></span>

<span data-ttu-id="0eb25-124">**注意** 此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="0eb25-124">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0eb25-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="0eb25-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0eb25-126">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="0eb25-126">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="0eb25-127">**處理授權取得事件**</span><span class="sxs-lookup"><span data-stu-id="0eb25-127">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> </dl>

 

 




