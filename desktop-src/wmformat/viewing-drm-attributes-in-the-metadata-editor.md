---
title: 在中繼資料編輯器中查看 DRM 屬性
description: 在中繼資料編輯器中查看 DRM 屬性
ms.assetid: e25fb8c8-8f4d-40fd-aa6f-675921e0ccdd
keywords:
- Windows Media Format SDK，DRM 屬性查看
- 數位版權管理 (DRM) ，屬性查看
- DRM (數位版權管理) ，屬性查看
- Windows Media Format SDK，中繼資料編輯器
- 數位版權管理 (DRM) ，中繼資料編輯器
- DRM (數位版權管理) ，中繼資料編輯器
- Windows Media Format SDK，IWMDRMEditor 介面
- 數位版權管理 (DRM) ，IWMDRMEditor 介面
- DRM (數位版權管理) 、IWMDRMEditor 介面
- 中繼資料編輯器，DRM 屬性查看
- 中繼資料編輯器，IWMDRMEditor 介面
- IWMDRMEditor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8541444ad7704ecc340476929f1205f11ccd61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314316"
---
# <a name="viewing-drm-attributes-in-the-metadata-editor"></a><span data-ttu-id="4a057-115">在中繼資料編輯器中查看 DRM 屬性</span><span class="sxs-lookup"><span data-stu-id="4a057-115">Viewing DRM Attributes in the Metadata Editor</span></span>

<span data-ttu-id="4a057-116">中繼資料編輯器會公開 IWMDRMEditor 介面，此介面可讓編輯應用程式檢查受保護 ASF 檔案中 DRM 標頭的某些屬性，以及內容授權中的屬性（如果有的話），即使應用程式沒有 DRM 特定的靜態程式庫，也就是完全啟用 DRM 播放程式和寫入器應用程式所需的 (wmstubdrm .lib) 。</span><span class="sxs-lookup"><span data-stu-id="4a057-116">The Metadata Editor exposes the IWMDRMEditor interface, which enables editing applications to examine certain attributes of a DRM header in a protected ASF file, and attributes in the content license, if one is present, even if the application doesn't have the DRM-specific static library (wmstubdrm.lib) that is required for fully-enabled DRM player and writer applications.</span></span>

> [!Note]  
> <span data-ttu-id="4a057-117">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="4a057-117">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4a057-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a057-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a057-119">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="4a057-119">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="4a057-120">**IWMDRMEditor 介面**</span><span class="sxs-lookup"><span data-stu-id="4a057-120">**IWMDRMEditor Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




