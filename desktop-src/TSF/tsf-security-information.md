---
title: 安全性考慮文字服務架構
description: 安全性考慮文字服務架構
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- 文字服務架構 (TSF) ，安全性
- TSF (文字服務架構) ，安全性
- 文字服務，安全性
- 啟用 TSF 的應用程式，安全性
- TSF 的安全性
- 文字服務架構 (TSF) 、最佳作法
- TSF (文字服務架構) ，最佳作法
- 啟用 TSF 的應用程式，最佳作法
- 文字服務、最佳作法
- TSF 的最佳作法
- 文字服務架構 (TSF) ，錯誤檢查
- TSF (文字服務架構) ，錯誤檢查
- 啟用 TSF 的應用程式，錯誤檢查
- 文字服務，錯誤檢查
- 錯誤檢查
- 文字服務架構 (TSF) 、數位簽章
- TSF (文字服務架構) 、數位簽章
- 文字服務、數位簽章
- 啟用 TSF 的應用程式，數位簽章
- 數位簽章
- 文字服務架構 (TSF) 、LoadLibrary 呼叫
- TSF (文字服務架構) ，LoadLibrary 呼叫
- 文字服務，LoadLibrary 呼叫
- 啟用 TSF 的應用程式，LoadLibrary 呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d71966106cde0f59d39442f7e2bf9b2a216cd94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969105"
---
# <a name="security-considerations-text-services-framework"></a><span data-ttu-id="bfbd5-127">安全性考慮：文字服務架構</span><span class="sxs-lookup"><span data-stu-id="bfbd5-127">Security Considerations: Text Services Framework</span></span>

## <a name="best-practices-for-developing-with-tsf"></a><span data-ttu-id="bfbd5-128">使用 TSF 進行開發的最佳作法</span><span class="sxs-lookup"><span data-stu-id="bfbd5-128">Best Practices for Developing with TSF</span></span>

-   <span data-ttu-id="bfbd5-129">**數位簽章：** 文字服務提供者應該提供數位簽章給其二進位可執行檔。</span><span class="sxs-lookup"><span data-stu-id="bfbd5-129">**Digital Signatures:** Text service providers should provide digital signatures with their binary executables.</span></span> <span data-ttu-id="bfbd5-130">註冊的文字服務可以存取系統執行緒，而且可能會公開其他無法存取的資訊。</span><span class="sxs-lookup"><span data-stu-id="bfbd5-130">A registered text service has access to system threads and could expose information that would otherwise not be accessible.</span></span> <span data-ttu-id="bfbd5-131">為了協助確保穩定且安全的作業，使用者應該先驗證文字服務的數位簽章，然後才允許文字服務載入。</span><span class="sxs-lookup"><span data-stu-id="bfbd5-131">To help ensure stable and secure operation, the user should verify the digital signature of a text service before the text service is allowed to load.</span></span> <span data-ttu-id="bfbd5-132">請參閱程式 [代碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) ，以取得建立數位簽章的適當程式。</span><span class="sxs-lookup"><span data-stu-id="bfbd5-132">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) for the proper procedure to create a digital signature.</span></span>
-   <span data-ttu-id="bfbd5-133">**檢查錯誤：** 應檢查每個方法或函數呼叫是否成功。</span><span class="sxs-lookup"><span data-stu-id="bfbd5-133">**Error Checking:** Each method or function call should be checked for success.</span></span> <span data-ttu-id="bfbd5-134">如果發生失敗，則應該略過其餘的方法或函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="bfbd5-134">In the event of failure, the remaining method or function calls should be skipped.</span></span> <span data-ttu-id="bfbd5-135">本檔中的大部分程式碼範例都有限制的錯誤檢查，或是完全不會發生的問題，以避免遮蔽所要說明的點。</span><span class="sxs-lookup"><span data-stu-id="bfbd5-135">Most of the code examples in this documentation have limited error checking, or none at all, to avoid obscuring the point to be illustrated.</span></span> <span data-ttu-id="bfbd5-136">您不應該將範例直接從檔貼入生產程式碼;相反地，您應該新增自己的錯誤檢查來增強範例。</span><span class="sxs-lookup"><span data-stu-id="bfbd5-136">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

-   <span data-ttu-id="bfbd5-137">**LoadLibrary 呼叫：** 若要取得任何 [TSF](text-services-framework-functions.md)函式的指標，您將需要使用 [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)。</span><span class="sxs-lookup"><span data-stu-id="bfbd5-137">**LoadLibrary Calls:** To obtain a pointer to any of the [TSF functions](text-services-framework-functions.md), you will need to use [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="bfbd5-138">不過，請務必遵循 **LoadLibrary** 檔中所提供的格式設定 DLL 路徑名稱的程式。</span><span class="sxs-lookup"><span data-stu-id="bfbd5-138">However, it is important to follow procedures for formatting the DLL path name, as given in **LoadLibrary** documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfbd5-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="bfbd5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfbd5-140">安全性最佳作法</span><span class="sxs-lookup"><span data-stu-id="bfbd5-140">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

<span data-ttu-id="bfbd5-141">[程式碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bfbd5-141">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bfbd5-142">TSF 函式</span><span class="sxs-lookup"><span data-stu-id="bfbd5-142">TSF functions</span></span>](text-services-framework-functions.md)
</dt> <dt>

[<span data-ttu-id="bfbd5-143">LoadLibrary</span><span class="sxs-lookup"><span data-stu-id="bfbd5-143">LoadLibrary</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="bfbd5-144">GetProcAddress</span><span class="sxs-lookup"><span data-stu-id="bfbd5-144">GetProcAddress</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 