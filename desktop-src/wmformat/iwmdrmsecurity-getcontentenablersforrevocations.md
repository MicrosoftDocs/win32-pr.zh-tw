---
title: 'IWMDRMSecurity GetContentEnablersForRevocations 方法 (Wmdrmsdk .h) '
description: GetContentEnablersForRevocations 方法會抓取內容啟用程式介面，以根據已撤銷的憑證來更新元件。
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- GetContentEnablersForRevocations 方法 windows Media 格式
- GetContentEnablersForRevocations 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetContentEnablersForRevocations 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001884"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a><span data-ttu-id="68fda-106">IWMDRMSecurity：： GetContentEnablersForRevocations 方法</span><span class="sxs-lookup"><span data-stu-id="68fda-106">IWMDRMSecurity::GetContentEnablersForRevocations method</span></span>

<span data-ttu-id="68fda-107">**GetContentEnablersForRevocations** 方法會抓取內容啟用程式介面，以根據已撤銷的憑證來更新元件。</span><span class="sxs-lookup"><span data-stu-id="68fda-107">The **GetContentEnablersForRevocations** method retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="68fda-108">語法</span><span class="sxs-lookup"><span data-stu-id="68fda-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="68fda-109">參數</span><span class="sxs-lookup"><span data-stu-id="68fda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68fda-110">*rgpbCerts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68fda-110">*rgpbCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68fda-111">用來取出內容啟用程式的憑證陣列。</span><span class="sxs-lookup"><span data-stu-id="68fda-111">Array of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="68fda-112">陣列中的元素數目必須由 *cCerts* 指定。</span><span class="sxs-lookup"><span data-stu-id="68fda-112">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="68fda-113">*rgpdwCertSizes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68fda-113">*rgpdwCertSizes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68fda-114">陣列，包含 *rgpbCerts* 陣列中的憑證大小。</span><span class="sxs-lookup"><span data-stu-id="68fda-114">Array containing the sizes of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="68fda-115">陣列中的元素數目必須由 *cCerts* 指定。</span><span class="sxs-lookup"><span data-stu-id="68fda-115">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="68fda-116">*rgpguidCerts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68fda-116">*rgpguidCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68fda-117">陣列，包含 *rgpbCerts* 陣列中的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="68fda-117">Array containing the types of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="68fda-118">陣列中的元素數目必須由 *cCerts* 指定。</span><span class="sxs-lookup"><span data-stu-id="68fda-118">The number of elements in the array must be specified by *cCerts*.</span></span> <span data-ttu-id="68fda-119">針對陣列的每個元素，請使用下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="68fda-119">For each element of the array, use one of the following values.</span></span>



| <span data-ttu-id="68fda-120">GUID 常數</span><span class="sxs-lookup"><span data-stu-id="68fda-120">GUID constant</span></span>                 | <span data-ttu-id="68fda-121">Description</span><span class="sxs-lookup"><span data-stu-id="68fda-121">Description</span></span>                                                    |
|-------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="68fda-122">WMDRM \_ REVOCATIONTYPE \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="68fda-122">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="68fda-123">指定應用程式憑證。</span><span class="sxs-lookup"><span data-stu-id="68fda-123">Specifies an application certificate.</span></span>                          |
| <span data-ttu-id="68fda-124">WMDRM \_ REVOCATIONTYPE \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="68fda-124">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="68fda-125">指定裝置憑證。</span><span class="sxs-lookup"><span data-stu-id="68fda-125">Specifies a device certificate.</span></span>                                |
| <span data-ttu-id="68fda-126">WMDRM \_ REVOCATIONTYPE \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="68fda-126">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="68fda-127">指定網路裝置憑證的 Windows Media DRM。</span><span class="sxs-lookup"><span data-stu-id="68fda-127">Specifies a Windows Media DRM for Network Devices certificate.</span></span> |



 

</dd> <dt>

<span data-ttu-id="68fda-128">*cCerts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68fda-128">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68fda-129">要取出內容啟用程式的憑證數目。</span><span class="sxs-lookup"><span data-stu-id="68fda-129">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="68fda-130">這是 *rgpbCerts* 陣列、 *RgpdwCertSizes* 陣列和 *rgpguidCerts* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="68fda-130">This is the number of elements in the *rgpbCerts* array, the *rgpdwCertSizes* array, and the *rgpguidCerts* array.</span></span>

</dd> <dt>

<span data-ttu-id="68fda-131">*hResultHint* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68fda-131">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68fda-132">因為撤銷憑證而失敗的作業所收到的傳回值。</span><span class="sxs-lookup"><span data-stu-id="68fda-132">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="68fda-133">如果您未呼叫來回應失敗的方法呼叫，請將設定為 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="68fda-133">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="68fda-134">*prgContentEnablers* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="68fda-134">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68fda-135">接收新建立之 **IMFContentEnabler** 介面位址的陣列。</span><span class="sxs-lookup"><span data-stu-id="68fda-135">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="68fda-136">設定為 **Null** ，以取得 *pcContentEnablers* 參數中的內容啟用程式數目。</span><span class="sxs-lookup"><span data-stu-id="68fda-136">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="68fda-137">*pcContentEnablers* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="68fda-137">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="68fda-138">*PrgContentEnablers* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="68fda-138">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="68fda-139">如果 *prgContentEnablers* 為 **Null**，則此值會設定為輸出上所需的內容啟用程式數目。</span><span class="sxs-lookup"><span data-stu-id="68fda-139">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68fda-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="68fda-140">Return value</span></span>

<span data-ttu-id="68fda-141">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="68fda-141">The method returns an **HRESULT**.</span></span> <span data-ttu-id="68fda-142">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="68fda-142">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="68fda-143">傳回碼</span><span class="sxs-lookup"><span data-stu-id="68fda-143">Return code</span></span>                                                                          | <span data-ttu-id="68fda-144">Description</span><span class="sxs-lookup"><span data-stu-id="68fda-144">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="68fda-145"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="68fda-145"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="68fda-146">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="68fda-146">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68fda-147">備註</span><span class="sxs-lookup"><span data-stu-id="68fda-147">Remarks</span></span>

<span data-ttu-id="68fda-148">如果您使用 **IMFContentEnabler** 介面更新撤銷的元件，您必須明確地說明使用者的流程。</span><span class="sxs-lookup"><span data-stu-id="68fda-148">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="68fda-149">因為更新程式會將用戶端電腦的資訊傳送到 Microsoft 網站，所以必須進行這種澄清。</span><span class="sxs-lookup"><span data-stu-id="68fda-149">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="68fda-150">當您呼叫 **IMFContentEnabler：： AutomaticEnable** 時，內容啟用程式會以 Microsoft 網站上的更新服務位址啟動預設的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="68fda-150">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="68fda-151">識別已撤銷元件的唯一識別碼會傳送至 update 服務。</span><span class="sxs-lookup"><span data-stu-id="68fda-151">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="68fda-152">接著，服務會將瀏覽器重新導向至網頁，讓使用者可以從該網頁下載並安裝新的已撤銷元件版本。</span><span class="sxs-lookup"><span data-stu-id="68fda-152">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="68fda-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="68fda-153">Requirements</span></span>



| <span data-ttu-id="68fda-154">需求</span><span class="sxs-lookup"><span data-stu-id="68fda-154">Requirement</span></span> | <span data-ttu-id="68fda-155">值</span><span class="sxs-lookup"><span data-stu-id="68fda-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68fda-156">標頭</span><span class="sxs-lookup"><span data-stu-id="68fda-156">Header</span></span><br/>  | <dl> <span data-ttu-id="68fda-157"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="68fda-157"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="68fda-158">程式庫</span><span class="sxs-lookup"><span data-stu-id="68fda-158">Library</span></span><br/> | <dl> <span data-ttu-id="68fda-159"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="68fda-159"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68fda-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68fda-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68fda-161">**自動化元件撤銷和更新**</span><span class="sxs-lookup"><span data-stu-id="68fda-161">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="68fda-162">**IWMDRMSecurity 介面**</span><span class="sxs-lookup"><span data-stu-id="68fda-162">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





