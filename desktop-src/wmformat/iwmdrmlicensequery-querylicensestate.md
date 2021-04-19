---
title: 'IWMDRMLicenseQuery QueryLicenseState 方法 (Wmdrmsdk .h) '
description: QueryLicenseState 方法會查詢本機授權存放區，以取得適用于一或多個特定許可權之金鑰識別碼的授權資訊。
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- QueryLicenseState 方法 windows Media 格式
- QueryLicenseState 方法 windows Media Format，IWMDRMLicenseQuery 介面
- IWMDRMLicenseQuery 介面 windows Media Format，QueryLicenseState 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977629"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a><span data-ttu-id="8e5a8-106">IWMDRMLicenseQuery：： QueryLicenseState 方法</span><span class="sxs-lookup"><span data-stu-id="8e5a8-106">IWMDRMLicenseQuery::QueryLicenseState method</span></span>

<span data-ttu-id="8e5a8-107">**QueryLicenseState** 方法會查詢本機授權存放區，以取得適用于一或多個特定許可權之金鑰識別碼的授權資訊。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-107">The **QueryLicenseState** method queries the local license store for license information that applies to a Key ID for one or more specific rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5a8-108">語法</span><span class="sxs-lookup"><span data-stu-id="8e5a8-108">Syntax</span></span>


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a><span data-ttu-id="8e5a8-109">參數</span><span class="sxs-lookup"><span data-stu-id="8e5a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e5a8-110">*bstrKID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e5a8-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5a8-111">要查詢的索引鍵識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-111">Key ID for which to query.</span></span> <span data-ttu-id="8e5a8-112">只會評估適用于此金鑰識別碼的授權。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="8e5a8-113">*cActionsToQuery* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e5a8-113">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5a8-114">要查詢的動作數目。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-114">The number of actions for which to query.</span></span> <span data-ttu-id="8e5a8-115">必須將此值設定為針對 *rgbstrActionsToQuery* 和 *rgResultStateData* 參數傳遞之陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-115">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgResultStateData* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="8e5a8-116">*\[ rgbstrActionsToQuery \]*\[in\]</span><span class="sxs-lookup"><span data-stu-id="8e5a8-116">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5a8-117">要查詢的一或多個許可權的陣列。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-117">Array of one or more rights for which to query.</span></span> <span data-ttu-id="8e5a8-118">此陣列必須包含 *cActionsToQuery* 所指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-118">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="8e5a8-119">每個元素都必須設定為下列其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-119">Each element must be set to one of the following constants.</span></span>



| <span data-ttu-id="8e5a8-120">常數</span><span class="sxs-lookup"><span data-stu-id="8e5a8-120">Constant</span></span>                                        | <span data-ttu-id="8e5a8-121">描述</span><span class="sxs-lookup"><span data-stu-id="8e5a8-121">Description</span></span>                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5a8-122">g \_ wszWMDRM \_ LicenseState \_ 備份</span><span class="sxs-lookup"><span data-stu-id="8e5a8-122">g\_wszWMDRM\_LicenseState\_Backup</span></span>               | <span data-ttu-id="8e5a8-123">包含以查詢有關備份和還原授權之許可權的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-123">Include to query for the details about the right to back up and restore the license.</span></span>                                                               |
| <span data-ttu-id="8e5a8-124">g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="8e5a8-124">g\_wszWMDRM\_LicenseState\_CollaborativePlay</span></span>    | <span data-ttu-id="8e5a8-125">包含，以查詢與使用者群組共用內容的許可權詳細資料，作為共同作業播放案例的一部分。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-125">Include to query for the details about the right to share the content with a group of users as part of a collaborative playback scenario.</span></span>          |
| <span data-ttu-id="8e5a8-126">g \_ wszWMDRM \_ LicenseState \_ Copy</span><span class="sxs-lookup"><span data-stu-id="8e5a8-126">g\_wszWMDRM\_LicenseState\_Copy</span></span>                 | <span data-ttu-id="8e5a8-127">包含以查詢將內容複寫到外部裝置或媒體的許可權詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-127">Include to query for the details about the right to copy the content to external devices or media.</span></span>                                                 |
| <span data-ttu-id="8e5a8-128">g \_ wszWMDRM \_ LicenseState \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="8e5a8-128">g\_wszWMDRM\_LicenseState\_CopyToCD</span></span>             | <span data-ttu-id="8e5a8-129">[包含] 以查詢將內容複寫到 CD 的右邊詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-129">Include to query for the details about the right to copy the content to CD.</span></span>                                                                        |
| <span data-ttu-id="8e5a8-130">g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="8e5a8-130">g\_wszWMDRM\_LicenseState\_CopyToNonSDMIDevice</span></span>  | <span data-ttu-id="8e5a8-131">包含，以查詢將內容複寫到不支援 (SDMI) 之安全數位媒體計畫之裝置的許可權詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-131">Include to query for the details about the right to copy the content to a device that does not support the secure digital media initiative (SDMI).</span></span> |
| <span data-ttu-id="8e5a8-132">g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="8e5a8-132">g\_wszWMDRM\_LicenseState\_CopyToSDMIDevice</span></span>     | <span data-ttu-id="8e5a8-133">包含以查詢有關將內容複寫到支援 SDMI 之裝置的許可權詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-133">Include to query for the details about the right to copy the content to a device that supports the SDMI.</span></span>                                           |
| <span data-ttu-id="8e5a8-134">g \_ wszWMDRM \_ LicenseState \_ CreateThumbnailImage</span><span class="sxs-lookup"><span data-stu-id="8e5a8-134">g\_wszWMDRM\_LicenseState\_CreateThumbnailImage</span></span> | <span data-ttu-id="8e5a8-135">包含以查詢從內容建立縮圖影像右邊的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-135">Include to query for the details about the right to create a thumbnail image from the content.</span></span>                                                     |
| <span data-ttu-id="8e5a8-136">g \_ wszWMDRM \_ LicenseState \_ 播放</span><span class="sxs-lookup"><span data-stu-id="8e5a8-136">g\_wszWMDRM\_LicenseState\_Playback</span></span>             | <span data-ttu-id="8e5a8-137">包含以查詢有關播放內容之右邊的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-137">Include to query for the details about the right to play the content.</span></span>                                                                              |
| <span data-ttu-id="8e5a8-138">g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn</span><span class="sxs-lookup"><span data-stu-id="8e5a8-138">g\_wszWMDRM\_LicenseState\_PlaylistBurn</span></span>         | <span data-ttu-id="8e5a8-139">包含，以查詢將內容複寫到 CD 做為播放清單一部分的右邊詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-139">Include to query for the details about the right to copy the content to CD as part of a playlist.</span></span>                                                  |



 

</dd> <dt>

<span data-ttu-id="8e5a8-140">*\[ rgResultStateData \]*\[out\]</span><span class="sxs-lookup"><span data-stu-id="8e5a8-140">*rgResultStateData\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5a8-141">一或多個 [**DRM \_ 授權 \_ 狀態 \_ 資料**](drmdrm-license-state-data.md) 結構的陣列，此結構會接收適用于 *rgbstrActionsToQuery* 參數的對應元素右側的授權狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-141">Array of one or more [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structures that receive the license state information that applies to the right in the corresponding element of the *rgbstrActionsToQuery* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e5a8-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e5a8-142">Return value</span></span>

<span data-ttu-id="8e5a8-143">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-143">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8e5a8-144">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-144">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8e5a8-145">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8e5a8-145">Return code</span></span>                                                                          | <span data-ttu-id="8e5a8-146">Description</span><span class="sxs-lookup"><span data-stu-id="8e5a8-146">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8e5a8-147"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8e5a8-147"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8e5a8-148">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-148">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8e5a8-149">備註</span><span class="sxs-lookup"><span data-stu-id="8e5a8-149">Remarks</span></span>

<span data-ttu-id="8e5a8-150">將會搜尋並評估套用至指定金鑰識別碼的所有授權。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-150">All licenses that apply to the specified Key ID will be searched and evaluated.</span></span> <span data-ttu-id="8e5a8-151">結果會進行匯總，因此每個 **DRM \_ 授權 \_ 狀態 \_ 資料** 結構可能包含來自多個授權的資訊。</span><span class="sxs-lookup"><span data-stu-id="8e5a8-151">The results are aggregated, so each **DRM\_LICENSE\_STATE\_DATA** structure may contain information from multiple licenses.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e5a8-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e5a8-152">Requirements</span></span>



| <span data-ttu-id="8e5a8-153">需求</span><span class="sxs-lookup"><span data-stu-id="8e5a8-153">Requirement</span></span> | <span data-ttu-id="8e5a8-154">值</span><span class="sxs-lookup"><span data-stu-id="8e5a8-154">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5a8-155">標頭</span><span class="sxs-lookup"><span data-stu-id="8e5a8-155">Header</span></span><br/>  | <dl> <span data-ttu-id="8e5a8-156"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="8e5a8-156"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e5a8-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="8e5a8-157">Library</span></span><br/> | <dl> <span data-ttu-id="8e5a8-158"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e5a8-158"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e5a8-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e5a8-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5a8-160">**IWMDRMLicenseQuery 介面**</span><span class="sxs-lookup"><span data-stu-id="8e5a8-160">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> </dl>

 

 





