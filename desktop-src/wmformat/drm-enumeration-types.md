---
title: Microsoft Windows Media DRM 用戶端列舉類型
description: 列舉類型
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- Windows Media Format SDK，列舉類型
- 數位版權管理 (DRM) ，列舉類型
- DRM (數位版權管理) 、列舉類型
- DRM 用戶端擴充 Api，列舉類型
- 用戶端擴充 Api，列舉類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159342367035767d213d57987d93d23eb321a6c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024457"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="40b09-108">Microsoft Windows Media DRM 用戶端列舉類型</span><span class="sxs-lookup"><span data-stu-id="40b09-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="40b09-109">下表說明 Microsoft Windows Media DRM 用戶端擴充 Api 所支援的列舉。</span><span class="sxs-lookup"><span data-stu-id="40b09-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="40b09-110">列舉型別</span><span class="sxs-lookup"><span data-stu-id="40b09-110">Enumeration</span></span>                                                                      | <span data-ttu-id="40b09-111">描述</span><span class="sxs-lookup"><span data-stu-id="40b09-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40b09-112">**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="40b09-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="40b09-113">由 [**IWMDRMLicenseQuery：： QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) 介面用來指定不允許動作的原因。</span><span class="sxs-lookup"><span data-stu-id="40b09-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="40b09-114">**DRM \_ ATTR \_ 資料類型**</span><span class="sxs-lookup"><span data-stu-id="40b09-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="40b09-115">定義用於 DRM 屬性和屬性的資料類型。</span><span class="sxs-lookup"><span data-stu-id="40b09-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="40b09-116">**DRM \_ 加密 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="40b09-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="40b09-117">定義可以用來加密內容的密碼編譯演算法類型。</span><span class="sxs-lookup"><span data-stu-id="40b09-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="40b09-118">**DRM \_ HTTP \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="40b09-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="40b09-119">針對 DRM 要求定義 HTTP 狀態的範圍。</span><span class="sxs-lookup"><span data-stu-id="40b09-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="40b09-120">**DRM 的 \_ 個人化 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="40b09-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="40b09-121">定義 DRM 個人化的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="40b09-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="40b09-122">**DRM \_ 授權 \_ 狀態 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="40b09-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="40b09-123">指定 [**DRM \_ 授權 \_ 狀態 \_ 資料**](drmdrm-license-state-data.md) 結構所描述的授許可權制類型。</span><span class="sxs-lookup"><span data-stu-id="40b09-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="40b09-124">**MSDRM \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="40b09-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="40b09-125">定義 DRM 子系統的狀態條件。</span><span class="sxs-lookup"><span data-stu-id="40b09-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="40b09-126">**WMDRMNET \_ 原則 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="40b09-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="40b09-127">列出適用于網路裝置作業的 Windows Media DRM 可用的原則類型。</span><span class="sxs-lookup"><span data-stu-id="40b09-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="40b09-128">**WMT \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="40b09-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="40b09-129">定義可在 DRM 授權中指定的許可權。</span><span class="sxs-lookup"><span data-stu-id="40b09-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="40b09-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="40b09-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b09-131">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="40b09-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




