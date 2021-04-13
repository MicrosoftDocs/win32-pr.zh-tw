---
title: 驗證與初始化
description: 驗證與初始化
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- Windows Media Format SDK，驗證
- Windows Media Format SDK，初始化
- 數位版權管理 (DRM) ，驗證
- DRM (數位版權管理) ，驗證
- 數位版權管理 (DRM) ，初始化
- DRM (數位版權管理) ，初始化
- DRM 用戶端擴充 Api，驗證
- 用戶端擴充 Api，驗證
- DRM 用戶端擴充 Api，初始化
- 用戶端擴充 Api，初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314310"
---
# <a name="verification-and-initialization"></a><span data-ttu-id="e4a6f-113">驗證與初始化</span><span class="sxs-lookup"><span data-stu-id="e4a6f-113">Verification and Initialization</span></span>

<span data-ttu-id="e4a6f-114">您應該執行下列步驟來確認是否允許 transcryption，以及初始化將會解密內容的物件：</span><span class="sxs-lookup"><span data-stu-id="e4a6f-114">You should perform the following steps to verify that transcryption is allowed and to initialize an object that will decrypt the content:</span></span>

1.  <span data-ttu-id="e4a6f-115">如果您已經有內容的金鑰識別碼，請跳至步驟5。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-115">If you already have the Key ID for the content, skip to step 5.</span></span>
2.  <span data-ttu-id="e4a6f-116">呼叫 [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) 函式來建立中繼資料編輯器物件，並取得該物件之 [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-116">Call the [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) function to create a metadata editor object and get an instance of that object's [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) interface.</span></span>
3.  <span data-ttu-id="e4a6f-117">呼叫 **IWMMetadataEditor：： QueryInterface** 以取得 [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-117">Call **IWMMetadataEditor::QueryInterface** to get an instance of the [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) interface.</span></span>
4.  <span data-ttu-id="e4a6f-118">呼叫 [**IWMDRMEditor：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) 以取得 **DRM \_ DRMHeader \_ KeyID** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-118">Call [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) to get the **DRM\_DRMHeader\_KeyID** property.</span></span>
5.  <span data-ttu-id="e4a6f-119">藉由呼叫 [**WMDRMStartup**](wmdrmstartup.md) 函式來初始化 WINDOWS Media DRM 用戶端擴充 api。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-119">Initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>
6.  <span data-ttu-id="e4a6f-120">呼叫 [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) 函數來建立安全的提供者物件，並取得該物件之 [**IWMDRMProvider**](iwmdrmprovider.md) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-120">Call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function to create a secure provider object and get an instance of that object's [**IWMDRMProvider**](iwmdrmprovider.md) interface.</span></span>
7.  <span data-ttu-id="e4a6f-121">呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md) 來建立授權管理物件，並取得其 [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-121">Call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md) to create a license management object and get an instance of its [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span>
8.  <span data-ttu-id="e4a6f-122">呼叫 [**IWMDRMLicenseManagement：： CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)，並傳入金鑰識別碼和許可權，以控制在 transcrypted 後要對內容採取的動作。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-122">Call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing in the Key ID and the right that governs the actions to be taken with the content after it is transcrypted.</span></span> <span data-ttu-id="e4a6f-123">此呼叫將會抓取 [**IWMDRMLicense**](iwmdrmlicense.md) 介面的實例，可用來列舉任何相符的授權。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-123">This call will retrieve an instance of the [**IWMDRMLicense**](iwmdrmlicense.md) interface that can be used to enumerate through any matching licenses.</span></span>
9.  <span data-ttu-id="e4a6f-124">呼叫 [**IWMDRMLicense：： GetInclusionList**](iwmdrmlicense-getinclusionlist.md) ，以根據授權簽發者所指定 (CPS) 取得授權的內容保護系統清單。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-124">Call [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) to retrieve the list of authorized content protection systems (CPS) as specified by the license issuer.</span></span>
10. <span data-ttu-id="e4a6f-125">剖析包含清單，以確認授權允許輸出 CPS 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-125">Parse the inclusion list to confirm that the GUID of the output CPS is allowed by the license.</span></span>
11. <span data-ttu-id="e4a6f-126">如果所需的匯出 GUID 不在包含清單中，請呼叫 [**IWMDRMLicense：： GetNext**](iwmdrmlicense-getnext.md) 來取得下一個適用的授權 (如果有任何) ，然後重複步驟9和10。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-126">If the desired export GUID is not in the inclusion list, call [**IWMDRMLicense::GetNext**](iwmdrmlicense-getnext.md) to get the next applicable license (if any) and repeat steps 9 and 10.</span></span> <span data-ttu-id="e4a6f-127">如果沒有任何授權在其內含清單中具有所需的 GUID，則無法執行匯出。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-127">If no license has the desired GUID in its inclusion list, the export cannot be performed.</span></span>
12. <span data-ttu-id="e4a6f-128">呼叫 [**IWMDRMLicense：： CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) 來建立解密器物件。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-128">Call [**IWMDRMLicense::CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) to create a decryptor object.</span></span> <span data-ttu-id="e4a6f-129">傳入匯出應用程式憑證。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-129">Pass in the export application certificate.</span></span> <span data-ttu-id="e4a6f-130">此呼叫將提供指向解密程式物件之 [**IWMDRMDecrypt**](iwmdrmdecrypt.md) 介面實例的指標，以及包含種子的二進位物件。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-130">This call will provide a pointer to an instance of the decryptor object's [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface and a binary object containing the seed.</span></span> <span data-ttu-id="e4a6f-131">目前只支援 Windows Media **DRM \_ 保護 \_ 類型 \_ RC4** 常數作為 *dwFlags* 參數的引數。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-131">Only the Windows Media **DRM\_PROTECTION\_TYPE\_RC4** constant is supported as an argument to the *dwFlags* parameter at this time.</span></span>
13. <span data-ttu-id="e4a6f-132">使用 RSA OAEP 加密配置來解密初始化向量。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-132">Use the RSA OAEP encryption scheme to decrypt the initialization vector.</span></span>
14. <span data-ttu-id="e4a6f-133">當您輸入 Windows Media DRM 匯出協定時，請使用 Microsoft 提供的 ASF 剖析程式庫，找出每個承載的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4a6f-133">Use the ASF parsing library provided by Microsoft when you enter into the Windows Media DRM export agreement, to locate the offset in bytes for each payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4a6f-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4a6f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4a6f-135">**匯出壓縮的內容**</span><span class="sxs-lookup"><span data-stu-id="e4a6f-135">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




