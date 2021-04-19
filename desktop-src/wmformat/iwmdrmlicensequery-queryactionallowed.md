---
title: 'IWMDRMLicenseQuery QueryActionAllowed 方法 (Wmdrmsdk .h) '
description: QueryActionAllowed 方法會在本機授權存放區上執行查詢，以抓取適用于指定金鑰識別碼的一或多個 DRM 動作的授權狀態。
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- QueryActionAllowed 方法 windows Media 格式
- QueryActionAllowed 方法 windows Media Format，IWMDRMLicenseQuery 介面
- IWMDRMLicenseQuery 介面 windows Media Format，QueryActionAllowed 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989655"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a><span data-ttu-id="2e247-106">IWMDRMLicenseQuery：： QueryActionAllowed 方法</span><span class="sxs-lookup"><span data-stu-id="2e247-106">IWMDRMLicenseQuery::QueryActionAllowed method</span></span>

<span data-ttu-id="2e247-107">**QueryActionAllowed** 方法會在本機授權存放區上執行查詢，以抓取適用于指定金鑰識別碼的一或多個 DRM 動作的授權狀態。</span><span class="sxs-lookup"><span data-stu-id="2e247-107">The **QueryActionAllowed** method performs a query on the local license store to retrieve the license status for one or more DRM actions that apply to a specified Key ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e247-108">語法</span><span class="sxs-lookup"><span data-stu-id="2e247-108">Syntax</span></span>


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="2e247-109">參數</span><span class="sxs-lookup"><span data-stu-id="2e247-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e247-110">*bstrKID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e247-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e247-111">要查詢的索引鍵識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e247-111">Key ID for which to query.</span></span> <span data-ttu-id="2e247-112">只會評估適用于此金鑰識別碼的授權。</span><span class="sxs-lookup"><span data-stu-id="2e247-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="2e247-113">*bstrMinReqIndivVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e247-113">*bstrMinReqIndivVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e247-114">在 ASF 檔案的標頭中指定的最小安全性版本。</span><span class="sxs-lookup"><span data-stu-id="2e247-114">The minimum security version specified in the header of the ASF file.</span></span> <span data-ttu-id="2e247-115">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="2e247-115">This parameter is optional.</span></span> <span data-ttu-id="2e247-116">傳遞 **Null** 以執行沒有此資訊的查詢。</span><span class="sxs-lookup"><span data-stu-id="2e247-116">Pass **NULL** to perform the query without this information.</span></span>

</dd> <dt>

<span data-ttu-id="2e247-117">*cActionsToQuery* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e247-117">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e247-118">要查詢的動作數目。</span><span class="sxs-lookup"><span data-stu-id="2e247-118">The number of actions for which to query.</span></span> <span data-ttu-id="2e247-119">必須將此值設定為針對 *rgbstrActionsToQuery* 和 *rgdwQueryResult* 參數傳遞之陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="2e247-119">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgdwQueryResult* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="2e247-120">*\[ rgbstrActionsToQuery \]*\[in\]</span><span class="sxs-lookup"><span data-stu-id="2e247-120">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e247-121">要查詢的一或多個許可權的陣列。</span><span class="sxs-lookup"><span data-stu-id="2e247-121">Array of one or more rights for which to query.</span></span> <span data-ttu-id="2e247-122">此陣列必須包含 *cActionsToQuery* 所指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="2e247-122">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="2e247-123">每個元素都必須設定為下列其中一個常數：</span><span class="sxs-lookup"><span data-stu-id="2e247-123">Each element must be set to one of the following constants:</span></span>



| <span data-ttu-id="2e247-124">常數</span><span class="sxs-lookup"><span data-stu-id="2e247-124">Constant</span></span>                                         | <span data-ttu-id="2e247-125">描述</span><span class="sxs-lookup"><span data-stu-id="2e247-125">Description</span></span>                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2e247-126">g \_ wszWMDRM \_ ActionAllowed \_ 播放</span><span class="sxs-lookup"><span data-stu-id="2e247-126">g\_wszWMDRM\_ActionAllowed\_Playback</span></span>             | <span data-ttu-id="2e247-127">包含在查詢中播放內容的許可權。</span><span class="sxs-lookup"><span data-stu-id="2e247-127">Include to query for the right to play the content.</span></span>                              |
| <span data-ttu-id="2e247-128">g \_ wszWMDRM \_ ActionAllowed \_ Copy</span><span class="sxs-lookup"><span data-stu-id="2e247-128">g\_wszWMDRM\_ActionAllowed\_Copy</span></span>                 | <span data-ttu-id="2e247-129">包含以查詢將內容複寫到外部裝置或媒體的許可權。</span><span class="sxs-lookup"><span data-stu-id="2e247-129">Include to query for the right to copy the content to external devices or media.</span></span> |
| <span data-ttu-id="2e247-130">g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn</span><span class="sxs-lookup"><span data-stu-id="2e247-130">g\_wszWMDRM\_ActionAllowed\_PlaylistBurn</span></span>         | <span data-ttu-id="2e247-131">包含在查詢中，將內容複寫到 CD 做為播放清單的一部分。</span><span class="sxs-lookup"><span data-stu-id="2e247-131">Include to query for the right to copy the content to CD as part of a playlist.</span></span>  |
| <span data-ttu-id="2e247-132">g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage</span><span class="sxs-lookup"><span data-stu-id="2e247-132">g\_wszWMDRM\_ActionAllowed\_CreateThumbnailImage</span></span> | <span data-ttu-id="2e247-133">包含以查詢從內容建立縮圖影像的許可權。</span><span class="sxs-lookup"><span data-stu-id="2e247-133">Include to query for the right to create a thumbnail image from the content.</span></span>     |
| <span data-ttu-id="2e247-134">g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="2e247-134">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>             | <span data-ttu-id="2e247-135">包含在查詢中將內容複寫到 CD 的許可權。</span><span class="sxs-lookup"><span data-stu-id="2e247-135">Include to query for the right to copy the content to CD.</span></span>                        |



 

</dd> <dt>

<span data-ttu-id="2e247-136">*\[ rgdwQueryResult \]*\[out\]</span><span class="sxs-lookup"><span data-stu-id="2e247-136">*rgdwQueryResult\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e247-137">一或多個 DWORD 變數的陣列，這些變數會接收 *rgbstrActionsToQuery* 所指定許可權的查詢結果。</span><span class="sxs-lookup"><span data-stu-id="2e247-137">Array of one or more DWORD variables that receive the results of the query for the rights specified by *rgbstrActionsToQuery*.</span></span> <span data-ttu-id="2e247-138">如果允許某項動作，則對應的元素會設定為零。</span><span class="sxs-lookup"><span data-stu-id="2e247-138">If an action is allowed, the corresponding element is set to zero.</span></span> <span data-ttu-id="2e247-139">如果不允許某個動作，則會使用位 OR 運算，將專案設定為一或多個 [**DRM \_ 動作 \_ 允許的 \_ 查詢 \_ 結果**](drm-action-allowed-query-results.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="2e247-139">If an action is not allowed, the element is set to one or more values of the [**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**](drm-action-allowed-query-results.md) enumeration combined by using the bitwise OR operation.</span></span> <span data-ttu-id="2e247-140">此陣列必須包含 *cActionsToQuery* 所指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="2e247-140">This array must contain as many elements as specified by *cActionsToQuery*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e247-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e247-141">Return value</span></span>

<span data-ttu-id="2e247-142">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="2e247-142">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2e247-143">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="2e247-143">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2e247-144">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2e247-144">Return code</span></span>                                                                          | <span data-ttu-id="2e247-145">Description</span><span class="sxs-lookup"><span data-stu-id="2e247-145">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2e247-146"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2e247-146"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2e247-147">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="2e247-147">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2e247-148">備註</span><span class="sxs-lookup"><span data-stu-id="2e247-148">Remarks</span></span>

<span data-ttu-id="2e247-149">查詢播放和複製許可權時，您會先設定環境參數，以取得更精確的結果。</span><span class="sxs-lookup"><span data-stu-id="2e247-149">When querying for play and copy rights, you will get more accurate results by first setting environmental parameters.</span></span> <span data-ttu-id="2e247-150">使用 [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) 方法來設定環境參數。</span><span class="sxs-lookup"><span data-stu-id="2e247-150">Use the [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) method to set the environmental parameters.</span></span> <span data-ttu-id="2e247-151">燒錄許可權的查詢結果不會受到環境參數的影響;您可以安全地使用預設值。</span><span class="sxs-lookup"><span data-stu-id="2e247-151">The results of queries for the burn right are unaffected by the environmental parameters; you can safely use the defaults.</span></span>

<span data-ttu-id="2e247-152">**QueryActionAllowed** 方法所傳回的結果是從本機授權存放區中的零或多個授權匯總而來。</span><span class="sxs-lookup"><span data-stu-id="2e247-152">The results returned by the **QueryActionAllowed** method are aggregated from zero or more licenses in the local license store.</span></span> <span data-ttu-id="2e247-153">如果遇到啟用的結果，此方法可能無法搜尋套用至金鑰識別碼的所有授權。</span><span class="sxs-lookup"><span data-stu-id="2e247-153">The method may not search all of the licenses that apply to the Key ID if it encounters an enabled result.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e247-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e247-154">Requirements</span></span>



| <span data-ttu-id="2e247-155">需求</span><span class="sxs-lookup"><span data-stu-id="2e247-155">Requirement</span></span> | <span data-ttu-id="2e247-156">值</span><span class="sxs-lookup"><span data-stu-id="2e247-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e247-157">標頭</span><span class="sxs-lookup"><span data-stu-id="2e247-157">Header</span></span><br/>  | <dl> <span data-ttu-id="2e247-158"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e247-158"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e247-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="2e247-159">Library</span></span><br/> | <dl> <span data-ttu-id="2e247-160"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e247-160"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e247-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e247-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e247-162">**IWMDRMLicenseQuery 介面**</span><span class="sxs-lookup"><span data-stu-id="2e247-162">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="2e247-163">**查詢簡單的許可權資訊**</span><span class="sxs-lookup"><span data-stu-id="2e247-163">**Querying for Simple Rights Information**</span></span>](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





