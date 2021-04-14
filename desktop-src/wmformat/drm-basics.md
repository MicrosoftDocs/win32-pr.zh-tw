---
title: DRM 基本概念
description: DRM 基本概念
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows Media Format SDK，DRM 基本概念
- 數位版權管理 (DRM) ，關於
- DRM (數位版權管理) ，關於
- 數位版權管理 (DRM) ，保護內容
- DRM (數位版權管理) ，保護內容
- 數位版權管理 (DRM) ，封裝內容
- DRM (數位版權管理) ，封裝內容
- 數位版權管理 (DRM) ，讀取受保護的內容
- DRM (數位版權管理) ，讀取受保護的內容
- 保護內容
- 封裝內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372625"
---
# <a name="drm-basics"></a><span data-ttu-id="c7690-114">DRM 基本概念</span><span class="sxs-lookup"><span data-stu-id="c7690-114">DRM Basics</span></span>

<span data-ttu-id="c7690-115">Windows Media DRM 技術從 Windows Media Format SDK 的觀點來看相當簡單。</span><span class="sxs-lookup"><span data-stu-id="c7690-115">The Windows Media DRM technologies are fairly simple from the perspective of the Windows Media Format SDK.</span></span> <span data-ttu-id="c7690-116">SDK 的元件可以用來保護內容，以及播放受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="c7690-116">Components of the SDK can be used to protect content and to play protected content.</span></span>

## <a name="protecting-content"></a><span data-ttu-id="c7690-117">保護內容</span><span class="sxs-lookup"><span data-stu-id="c7690-117">Protecting Content</span></span>

<span data-ttu-id="c7690-118">保護內容 (也稱為封裝內容) 涉及加密檔案的資料區段，並在檔案標頭中包含一些可讓播放程式解密內容的資訊。</span><span class="sxs-lookup"><span data-stu-id="c7690-118">Protecting content (also called packaging content) involves encrypting the data section of the file and including some information in the file header that enables players to decrypt the content.</span></span>

<span data-ttu-id="c7690-119">若要加密內容，您需要索引鍵，這是用來植入加密演算法的值。</span><span class="sxs-lookup"><span data-stu-id="c7690-119">To encrypt the content, you need a key, which is a value used to seed the encryption algorithms.</span></span> <span data-ttu-id="c7690-120">金鑰是由兩個部分所組成：金鑰種子 (或私密金鑰) ，以及 (或公開金鑰) 的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7690-120">A key is made up of two pieces: a key seed (or private key), and a key identifier (or public key).</span></span> <span data-ttu-id="c7690-121">金鑰種子是您用來編碼內容的秘密值。</span><span class="sxs-lookup"><span data-stu-id="c7690-121">The key seed is the secret value with which you encode content.</span></span> <span data-ttu-id="c7690-122">金鑰識別碼是受保護檔案標頭中包含的公用值。</span><span class="sxs-lookup"><span data-stu-id="c7690-122">The key identifier is a public value that is included in the header of a protected file.</span></span>

<span data-ttu-id="c7690-123">當檔案受到保護時，就無法在沒有授權的情況下解密。</span><span class="sxs-lookup"><span data-stu-id="c7690-123">When a file is protected, it cannot be decrypted without a license.</span></span> <span data-ttu-id="c7690-124">授權包含指定受保護內容之使用條款的資訊。</span><span class="sxs-lookup"><span data-stu-id="c7690-124">A license includes information that specifies the terms of use for the protected content.</span></span> <span data-ttu-id="c7690-125">授權條款是由內容擁有者決定，而且可以自訂以符合各種需求。</span><span class="sxs-lookup"><span data-stu-id="c7690-125">The terms of a license are decided by the content owner and can be customized to meet a variety of needs.</span></span> <span data-ttu-id="c7690-126">封裝檔案的過程中，有一部分是包含網頁的 URL，使用者可以在其中取得存取內容的授權。</span><span class="sxs-lookup"><span data-stu-id="c7690-126">Part of the process of packaging a file is to include the URL of a Web page where users can acquire a license to access the content.</span></span>

## <a name="reading-protected-content"></a><span data-ttu-id="c7690-127">讀取受保護的內容</span><span class="sxs-lookup"><span data-stu-id="c7690-127">Reading Protected Content</span></span>

<span data-ttu-id="c7690-128">若要讀取受保護的內容，內容的授權必須位於用戶端電腦上。</span><span class="sxs-lookup"><span data-stu-id="c7690-128">To read protected content, a license for the content must reside on the client computer.</span></span> <span data-ttu-id="c7690-129">某些授許可權制是由 Windows Media Format SDK 的 DRM 元件在內部檢查，有些則必須由您的應用程式強制執行。</span><span class="sxs-lookup"><span data-stu-id="c7690-129">Some license restrictions are checked internally by the DRM components of the Windows Media Format SDK, while others must be enforced by your application.</span></span>

<span data-ttu-id="c7690-130">您可以使用 Windows Media Format SDK 的物件來協助使用者取得內容的授權，以及執行其他系統管理工作，例如更新 DRM 元件和備份授權。</span><span class="sxs-lookup"><span data-stu-id="c7690-130">You can use the objects of the Windows Media Format SDK to assist the user in acquiring licenses for content and to perform other administrative tasks, such as updating DRM components and backing up licenses.</span></span>

> [!Note]  
> <span data-ttu-id="c7690-131">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="c7690-131">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c7690-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7690-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7690-133">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="c7690-133">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="c7690-134">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="c7690-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




