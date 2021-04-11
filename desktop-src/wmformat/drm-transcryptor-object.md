---
title: DRM Transcryptor 物件
description: DRM Transcryptor 物件
ms.assetid: 50c041b3-6621-4618-843f-6ef9b8e741ab
keywords:
- Windows Media Format SDK，DRM transcryptor 物件
- Advanced Systems Format (ASF) ，DRM transcryptor 物件
- ASF (Advanced Systems Format) ，DRM transcryptor 物件
- 物件，DRM transcryptor 物件
- DRM transcryptor 物件
- Windows Media 格式 SDK，transcryptor 物件
- Advanced Systems Format (ASF) ，transcryptor 物件
- ASF (Advanced Systems Format) ，transcryptor 物件
- 物件，transcryptor 物件
- transcryptor 物件
- 數位版權管理 (DRM) ，transcryptor 物件
- DRM (數位版權管理) ，transcryptor 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46213dd7ebfbe48ff22039c201dbff3aab462f5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092546"
---
# <a name="drm-transcryptor-object"></a><span data-ttu-id="e84af-115">DRM Transcryptor 物件</span><span class="sxs-lookup"><span data-stu-id="e84af-115">DRM Transcryptor Object</span></span>

<span data-ttu-id="e84af-116">DRM transcryptor 物件會將受 DRM 保護的 ASF 檔案轉換成準備傳送到網路裝置的資料流程，而網路裝置會使用 Windows Media DRM 10 作為網路裝置。</span><span class="sxs-lookup"><span data-stu-id="e84af-116">The DRM transcryptor object converts DRM-protected ASF files into data streams ready to be sent to network devices that use Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="e84af-117">DRM transcryptor 物件是由 [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) 函數所建立，它會將指標設定為 [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) 介面。</span><span class="sxs-lookup"><span data-stu-id="e84af-117">The DRM transcryptor object is created by the [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) function, which sets a pointer to the [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) interface.</span></span> <span data-ttu-id="e84af-118">**IUnknown** 和 **IWMDRMTranscryptor** 是此物件唯一支援的介面。</span><span class="sxs-lookup"><span data-stu-id="e84af-118">**IUnknown** and **IWMDRMTranscryptor** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e84af-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="e84af-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e84af-120">**物件**</span><span class="sxs-lookup"><span data-stu-id="e84af-120">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




