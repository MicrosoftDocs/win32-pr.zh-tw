---
title: 加密和匯入媒體範例
description: 加密和匯入媒體範例
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows Media Format SDK，DRM 匯入
- Windows Media Format SDK，匯入
- Windows Media Format SDK，加密媒體範例
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- 數位版權管理 (DRM) ，加密媒體範例
- DRM (數位版權管理) ，加密媒體範例
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- DRM 用戶端擴充 Api，加密媒體範例
- 用戶端擴充 Api，加密媒體範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374427"
---
# <a name="encrypting-and-importing-media-samples"></a><span data-ttu-id="f7159-114">加密和匯入媒體範例</span><span class="sxs-lookup"><span data-stu-id="f7159-114">Encrypting and Importing Media Samples</span></span>

<span data-ttu-id="f7159-115">針對使用 Windows Media DRM 進行加密的每個媒體範例，您必須產生嚴格大於前一個的 salt 值， (單純增加) 。</span><span class="sxs-lookup"><span data-stu-id="f7159-115">For each media sample that you encrypt using Windows Media DRM, you must generate a salt value that is strictly bigger than the previous one (monotonically increasing).</span></span> <span data-ttu-id="f7159-116">使用新的 salt 值建立暫時性加密金鑰，方法是將 SHA-1 加密演算法套用至與 salt 值串連的初始化向量。</span><span class="sxs-lookup"><span data-stu-id="f7159-116">Use the new salt value to create a transitory encryption key by applying the SHA-1 encryption algorithm to the initialization vector concatenated with the salt value.</span></span>

<span data-ttu-id="f7159-117">接下來，使用所產生的暫時性金鑰，根據 RC4 演算法來加密範例。</span><span class="sxs-lookup"><span data-stu-id="f7159-117">Next, encrypt the sample according to the RC4 algorithm using the generated transitory key.</span></span> <span data-ttu-id="f7159-118">將範例傳遞給 SDK 之前，您的應用程式必須藉由設定擴充屬性來建立 salt 值與範例之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="f7159-118">Before the sample is passed to the SDK, your application must associate the salt value with the sample by setting an extension attribute.</span></span>

<span data-ttu-id="f7159-119">以下是加密媒體範例的步驟：</span><span class="sxs-lookup"><span data-stu-id="f7159-119">Here are the steps for encrypting media samples:</span></span>

1.  <span data-ttu-id="f7159-120">呼叫範例物件的 **QueryInterface** 方法，以取得 [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) 介面。</span><span class="sxs-lookup"><span data-stu-id="f7159-120">Call the **QueryInterface** method of the sample object to get the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface.</span></span>
2.  <span data-ttu-id="f7159-121">遞增 salt 值。</span><span class="sxs-lookup"><span data-stu-id="f7159-121">Increment the salt value.</span></span>
3.  <span data-ttu-id="f7159-122">使用 RC1 加密演算法來加密範例。</span><span class="sxs-lookup"><span data-stu-id="f7159-122">Encrypt the sample using an RC1 encryption algorithm.</span></span> <span data-ttu-id="f7159-123">針對加密，您會串連初始化向量和 salt 值來建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="f7159-123">For the encryption you create a key by concatenating the initialization vector and the salt value.</span></span>
4.  <span data-ttu-id="f7159-124">藉由呼叫 [**INSSBuffer：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty)將 salt 值提供給 SDK。</span><span class="sxs-lookup"><span data-stu-id="f7159-124">Provide the salt value to the SDK by calling [**INSSBuffer::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7159-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7159-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7159-126">**DRM 匯入**</span><span class="sxs-lookup"><span data-stu-id="f7159-126">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="f7159-127">**媒體範例加密範例**</span><span class="sxs-lookup"><span data-stu-id="f7159-127">**Media Sample Encryption Example**</span></span>](media-sample-encryption-example.md)
</dt> </dl>

 

 




