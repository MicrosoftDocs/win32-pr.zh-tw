---
title: 'IWMDRMLicenseQuery SetActionAllowedQueryParams 方法 (Wmdrmsdk .h) '
description: 使用 QueryActionAllowed 方法時，SetActionAllowedQueryParams 方法會設定環境特定的資訊，以取得更精確的查詢結果。
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- SetActionAllowedQueryParams 方法 windows Media 格式
- SetActionAllowedQueryParams 方法 windows Media Format，IWMDRMLicenseQuery 介面
- IWMDRMLicenseQuery 介面 windows Media Format，SetActionAllowedQueryParams 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987019"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a><span data-ttu-id="bb943-106">IWMDRMLicenseQuery：： SetActionAllowedQueryParams 方法</span><span class="sxs-lookup"><span data-stu-id="bb943-106">IWMDRMLicenseQuery::SetActionAllowedQueryParams method</span></span>

<span data-ttu-id="bb943-107">使用 [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md)方法時， **SetActionAllowedQueryParams** 方法會設定環境特定的資訊，以取得更精確的查詢結果。</span><span class="sxs-lookup"><span data-stu-id="bb943-107">The **SetActionAllowedQueryParams** method sets environment-specific information for more accurate query results when using the [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb943-108">語法</span><span class="sxs-lookup"><span data-stu-id="bb943-108">Syntax</span></span>


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a><span data-ttu-id="bb943-109">參數</span><span class="sxs-lookup"><span data-stu-id="bb943-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb943-110">*fIsMF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb943-110">*fIsMF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb943-111">指定是否使用 Microsoft 媒體基礎 SDK 的物件來呈現內容。</span><span class="sxs-lookup"><span data-stu-id="bb943-111">Specifies whether the content will be rendered by using the objects of the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="bb943-112">**FALSE** 表示由 Windows MEDIA 格式 SDK 的物件呈現。</span><span class="sxs-lookup"><span data-stu-id="bb943-112">**FALSE** indicates rendering by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="bb943-113">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="bb943-113">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="bb943-114">*dwAppSecLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb943-114">*dwAppSecLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb943-115">查詢應用程式的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="bb943-115">Security level of the querying application.</span></span> <span data-ttu-id="bb943-116">只有在使用 Windows Media 格式 SDK 的物件時，此值才很重要，在此情況下， *fIsMF* 應該設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bb943-116">This value is only important if the objects of the Windows Media Format SDK will be used, in which case *fIsMF* should be set to **FALSE**.</span></span> <span data-ttu-id="bb943-117">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="bb943-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="bb943-118">*fHasSerialNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb943-118">*fHasSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb943-119">指定複製作業的目標裝置是否具有序號。</span><span class="sxs-lookup"><span data-stu-id="bb943-119">Specifies whether the target device for a copy operation has a serial number.</span></span> <span data-ttu-id="bb943-120">這個參數是選擇性的，只適用于複製作業的查詢。</span><span class="sxs-lookup"><span data-stu-id="bb943-120">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> <dt>

<span data-ttu-id="bb943-121">*bstrDeviceCert* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb943-121">*bstrDeviceCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb943-122">使用適用于可攜式裝置的 Windows Media DRM 時，目標裝置的裝置憑證。</span><span class="sxs-lookup"><span data-stu-id="bb943-122">Device certificate of the target device when using Windows Media DRM for Portable Devices.</span></span> <span data-ttu-id="bb943-123">這個參數是選擇性的，只適用于複製作業的查詢。</span><span class="sxs-lookup"><span data-stu-id="bb943-123">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb943-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb943-124">Return value</span></span>

<span data-ttu-id="bb943-125">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bb943-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bb943-126">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="bb943-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bb943-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bb943-127">Return code</span></span>                                                                          | <span data-ttu-id="bb943-128">Description</span><span class="sxs-lookup"><span data-stu-id="bb943-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bb943-129"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bb943-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bb943-130">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="bb943-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb943-131">備註</span><span class="sxs-lookup"><span data-stu-id="bb943-131">Remarks</span></span>

<span data-ttu-id="bb943-132">無。</span><span class="sxs-lookup"><span data-stu-id="bb943-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb943-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb943-133">Requirements</span></span>



| <span data-ttu-id="bb943-134">需求</span><span class="sxs-lookup"><span data-stu-id="bb943-134">Requirement</span></span> | <span data-ttu-id="bb943-135">值</span><span class="sxs-lookup"><span data-stu-id="bb943-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb943-136">標頭</span><span class="sxs-lookup"><span data-stu-id="bb943-136">Header</span></span><br/>  | <dl> <span data-ttu-id="bb943-137"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb943-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb943-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="bb943-138">Library</span></span><br/> | <dl> <span data-ttu-id="bb943-139"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb943-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb943-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb943-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb943-141">**IWMDRMLicenseQuery 介面**</span><span class="sxs-lookup"><span data-stu-id="bb943-141">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="bb943-142">**查詢詳細的許可權資訊**</span><span class="sxs-lookup"><span data-stu-id="bb943-142">**Querying for Detailed Rights Information**</span></span>](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





