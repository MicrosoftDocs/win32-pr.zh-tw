---
title: 將中繼資料新增至轉換的檔案
description: 將中繼資料新增至轉換的檔案
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Windows Media Player，轉換流程
- Windows Media Player 外掛程式，轉換
- 外掛程式，轉換
- 轉換外掛程式，將中繼資料新增至轉換的檔案
- 將中繼資料新增至轉換的檔案
- 中繼資料，新增至轉換的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682466"
---
# <a name="adding-metadata-to-converted-files"></a><span data-ttu-id="6bec4-109">將中繼資料新增至轉換的檔案</span><span class="sxs-lookup"><span data-stu-id="6bec4-109">Adding Metadata to Converted Files</span></span>

<span data-ttu-id="6bec4-110">轉換的檔案必須包含特定的中繼資料，以確保良好的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="6bec4-110">Converted files must contain certain metadata to ensure a good user experience.</span></span> <span data-ttu-id="6bec4-111">轉換後的檔案至少必須包含 [Windows Media 中繼資料使用指導方針](/previous-versions/ms867702(v=msdn.10))中所列的主要屬性。</span><span class="sxs-lookup"><span data-stu-id="6bec4-111">At a minimum, converted files must contain the primary attributes listed in the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

<span data-ttu-id="6bec4-112">針對音樂檔案，將 **WM/MediaClassPrimaryID** 的值設定為 D1607DBC-E323-4BE2-86A1-48A42A28441E。</span><span class="sxs-lookup"><span data-stu-id="6bec4-112">For music files, set the value for **WM/MediaClassPrimaryID** to D1607DBC-E323-4BE2-86A1-48A42A28441E.</span></span>

<span data-ttu-id="6bec4-113">針對語音信箱檔案，將 **WM/MediaClassPrimaryID** 的值設定為01CD0F29-DA4E-4157-897B-6275D50C4F11，也就是音訊檔案的主要類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="6bec4-113">For voicemail files, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11, which is the primary class GUID for audio files.</span></span> <span data-ttu-id="6bec4-114">將 **WM/MediaClassSecondaryID** 的值設定為193c8824-4d52-4178-90bd-305240b04636。</span><span class="sxs-lookup"><span data-stu-id="6bec4-114">Set the value for **WM/MediaClassSecondaryID** to 193c8824-4d52-4178-90bd-305240b04636.</span></span>

<span data-ttu-id="6bec4-115">針對語音筆記，將 **WM/MediaClassPrimaryID** 的值設定為01CD0F29-DA4E-4157-897B-6275D50C4F11。</span><span class="sxs-lookup"><span data-stu-id="6bec4-115">For voice notes, set the value for **WM/MediaClassPrimaryID** to 01CD0F29-DA4E-4157-897B-6275D50C4F11.</span></span> <span data-ttu-id="6bec4-116">將 **WM/MediaClassSecondaryID** 的值設定為3A172A13-2BD9-4831-835B-114F6A95943F。</span><span class="sxs-lookup"><span data-stu-id="6bec4-116">Set the value for **WM/MediaClassSecondaryID** to 3A172A13-2BD9-4831-835B-114F6A95943F.</span></span>

<span data-ttu-id="6bec4-117">將 [ **WM/ContentDistributor** ] 的值設定為提供內容之音樂服務的機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="6bec4-117">Set the value for **WM/ContentDistributor** to the key name for the music service that provided the content.</span></span>

<span data-ttu-id="6bec4-118">將 [ **WM/UniqueFileIdentifier** ] 的值設定為 [內容識別碼]。</span><span class="sxs-lookup"><span data-stu-id="6bec4-118">Set the value for **WM/UniqueFileIdentifier** to the content ID.</span></span> <span data-ttu-id="6bec4-119">這可讓您在未來取得特定的內容專案。</span><span class="sxs-lookup"><span data-stu-id="6bec4-119">This will enable you to retrieve specific content items at a future time.</span></span>

<span data-ttu-id="6bec4-120">設定 **WM/WMShadowFileSourceFileType** 的值。</span><span class="sxs-lookup"><span data-stu-id="6bec4-120">Set a value for **WM/WMShadowFileSourceFileType**.</span></span>

<span data-ttu-id="6bec4-121">針對受保護的內容，請使用 Windows Media Format SDK 將 **DRM \_ DRMHeader \_ ContentID** 屬性設定為內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="6bec4-121">For protected content, use the Windows Media Format SDK to set the **DRM\_DRMHeader\_ContentID** attribute to the content ID.</span></span>

<span data-ttu-id="6bec4-122">針對受保護的內容，請設定 **WM/WMShadowFileSourceDRMType** 的值。</span><span class="sxs-lookup"><span data-stu-id="6bec4-122">For protected content, set a value for **WM/WMShadowFileSourceDRMType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bec4-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="6bec4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bec4-124">**關於轉換外掛程式**</span><span class="sxs-lookup"><span data-stu-id="6bec4-124">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="6bec4-125">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="6bec4-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 