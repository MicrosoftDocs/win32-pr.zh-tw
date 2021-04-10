---
title: 查詢詳細的許可權資訊
description: 查詢詳細的許可權資訊
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- Windows Media 格式 SDK，查詢詳細許可權
- Windows Media Format SDK，詳細的許可權查詢
- 數位版權管理 (DRM) ，查詢詳細權利
- DRM (數位版權管理) ，查詢詳細權利
- 數位版權管理 (DRM) ，詳細的許可權查詢
- DRM (數位版權管理) ，詳細的許可權查詢
- DRM 用戶端擴充 Api，查詢詳細許可權
- 用戶端擴充 Api，查詢詳細許可權
- DRM 用戶端擴充 Api、詳細的許可權查詢
- 用戶端擴充 Api、詳細的許可權查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183605"
---
# <a name="querying-for-detailed-rights-information"></a><span data-ttu-id="a1e65-113">查詢詳細的許可權資訊</span><span class="sxs-lookup"><span data-stu-id="a1e65-113">Querying for Detailed Rights Information</span></span>

<span data-ttu-id="a1e65-114">藉由使用 [**IWMDRMLicenseQuery：： QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) 方法，您可以取得金鑰識別碼授權所授與之許可權的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a1e65-114">By using the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method, you can obtain detailed information about the rights granted by licenses for a key ID.</span></span> <span data-ttu-id="a1e65-115">從這個方法取得的資訊，會從套用至指定金鑰識別碼的本機授權存放區中的所有授權進行匯總。</span><span class="sxs-lookup"><span data-stu-id="a1e65-115">The information that you get from this method is aggregated from all licenses in the local license store that apply to the specified key ID.</span></span>

<span data-ttu-id="a1e65-116">**QueryLicenseState** 使用 [**DRM \_ 授權 \_ 狀態 \_ 資料**](drmdrm-license-state-data.md) 結構來顯示指定金鑰識別碼的所有授權相關匯總資訊。</span><span class="sxs-lookup"><span data-stu-id="a1e65-116">**QueryLicenseState** uses the [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure to display aggregate information about all the licenses for the specified key ID.</span></span> <span data-ttu-id="a1e65-117">此使用方式與 Windows Media 格式 SDK 中的其他物件不同。</span><span class="sxs-lookup"><span data-stu-id="a1e65-117">This usage is different than by other objects in the Windows Media Format SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1e65-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a1e65-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1e65-119">**從本機授權存放中的授權取得資訊**</span><span class="sxs-lookup"><span data-stu-id="a1e65-119">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




