---
title: IWMDRMLicenseQuery 介面
description: IWMDRMLicenseQuery 介面可讓應用程式查詢受保護檔案的許可權和授權狀態。
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- IWMDRMLicenseQuery 介面 windows 媒體格式
- IWMDRMLicenseQuery 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682711"
---
# <a name="iwmdrmlicensequery-interface"></a><span data-ttu-id="be6d2-105">IWMDRMLicenseQuery 介面</span><span class="sxs-lookup"><span data-stu-id="be6d2-105">IWMDRMLicenseQuery interface</span></span>

<span data-ttu-id="be6d2-106">**IWMDRMLicenseQuery** 介面可讓應用程式查詢受保護檔案的許可權和授權狀態。</span><span class="sxs-lookup"><span data-stu-id="be6d2-106">The **IWMDRMLicenseQuery** interface enables applications to query the rights and license state for a protected file.</span></span> <span data-ttu-id="be6d2-107">此介面會使用金鑰識別碼在本機授權存放區上執行查詢。</span><span class="sxs-lookup"><span data-stu-id="be6d2-107">This interface uses the Key ID to perform queries on the local license store.</span></span>

<span data-ttu-id="be6d2-108">若要取得這個介面的實例，請呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)。</span><span class="sxs-lookup"><span data-stu-id="be6d2-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="be6d2-109">將 **IID \_ IWMDRMLicenseQuery** 傳遞為 *riid* 參數。</span><span class="sxs-lookup"><span data-stu-id="be6d2-109">Pass **IID\_IWMDRMLicenseQuery** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="be6d2-110">成員</span><span class="sxs-lookup"><span data-stu-id="be6d2-110">Members</span></span>

<span data-ttu-id="be6d2-111">**IWMDRMLicenseQuery** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="be6d2-111">The **IWMDRMLicenseQuery** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be6d2-112">**IWMDRMLicenseQuery** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="be6d2-112">**IWMDRMLicenseQuery** also has these types of members:</span></span>

-   [<span data-ttu-id="be6d2-113">方法</span><span class="sxs-lookup"><span data-stu-id="be6d2-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be6d2-114">方法</span><span class="sxs-lookup"><span data-stu-id="be6d2-114">Methods</span></span>

<span data-ttu-id="be6d2-115">**IWMDRMLicenseQuery** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="be6d2-115">The **IWMDRMLicenseQuery** interface has these methods.</span></span>



| <span data-ttu-id="be6d2-116">方法</span><span class="sxs-lookup"><span data-stu-id="be6d2-116">Method</span></span>                                                                                | <span data-ttu-id="be6d2-117">描述</span><span class="sxs-lookup"><span data-stu-id="be6d2-117">Description</span></span>                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be6d2-118">**QueryActionAllowed**</span><span class="sxs-lookup"><span data-stu-id="be6d2-118">**QueryActionAllowed**</span></span>](iwmdrmlicensequery-queryactionallowed.md)                   | <span data-ttu-id="be6d2-119">查詢本機授權存放區，以取得依金鑰識別碼執行動作的許可權。</span><span class="sxs-lookup"><span data-stu-id="be6d2-119">Queries the local license store for permissions to perform actions by Key ID.</span></span><br/>         |
| [<span data-ttu-id="be6d2-120">**QueryLicenseState**</span><span class="sxs-lookup"><span data-stu-id="be6d2-120">**QueryLicenseState**</span></span>](iwmdrmlicensequery-querylicensestate.md)                     | <span data-ttu-id="be6d2-121">依金鑰識別碼和特定權利查詢本機授權存放區中的授權狀態資料。</span><span class="sxs-lookup"><span data-stu-id="be6d2-121">Queries the local license store for license state data by Key ID and specific rights.</span></span><br/> |
| [<span data-ttu-id="be6d2-122">**SetActionAllowedQueryParams**</span><span class="sxs-lookup"><span data-stu-id="be6d2-122">**SetActionAllowedQueryParams**</span></span>](iwmdrmlicensequery-setactionallowedqueryparams.md) | <span data-ttu-id="be6d2-123">設定環境參數以改善授權查詢的精確度。</span><span class="sxs-lookup"><span data-stu-id="be6d2-123">Sets environmental parameters to improve the accuracy of license queries.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="be6d2-124">備註</span><span class="sxs-lookup"><span data-stu-id="be6d2-124">Remarks</span></span>

<span data-ttu-id="be6d2-125">**IWMDRMLicenseQuery** 方法不會提供個別授權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="be6d2-125">The methods of **IWMDRMLicenseQuery** do not provide information about individual licenses.</span></span> <span data-ttu-id="be6d2-126">相反地，在傳回查詢結果之前，DRM 子系統會匯總授權資料。</span><span class="sxs-lookup"><span data-stu-id="be6d2-126">Instead, the license data is aggregated by the DRM subsystem before the query results are returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="be6d2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be6d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6d2-128">**介面**</span><span class="sxs-lookup"><span data-stu-id="be6d2-128">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

