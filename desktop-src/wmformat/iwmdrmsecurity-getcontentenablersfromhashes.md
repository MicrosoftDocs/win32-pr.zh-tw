---
title: 'IWMDRMSecurity GetContentEnablersFromHashes 方法 (Wmdrmsdk .h) '
description: GetContentEnablersFromHashes 方法會抓取內容啟用程式介面，以根據已雜湊的憑證來更新元件。
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- GetContentEnablersFromHashes 方法 windows Media 格式
- GetContentEnablersFromHashes 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetContentEnablersFromHashes 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983981"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a><span data-ttu-id="86c0a-106">IWMDRMSecurity：： GetContentEnablersFromHashes 方法</span><span class="sxs-lookup"><span data-stu-id="86c0a-106">IWMDRMSecurity::GetContentEnablersFromHashes method</span></span>

<span data-ttu-id="86c0a-107">**GetContentEnablersFromHashes** 方法會抓取內容啟用程式介面，以根據已雜湊的憑證來更新元件。</span><span class="sxs-lookup"><span data-stu-id="86c0a-107">The **GetContentEnablersFromHashes** method retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c0a-108">語法</span><span class="sxs-lookup"><span data-stu-id="86c0a-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="86c0a-109">參數</span><span class="sxs-lookup"><span data-stu-id="86c0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c0a-110">*rgpbCertHashes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86c0a-110">*rgpbCertHashes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c0a-111">憑證雜湊的陣列，用來取得的內容啟用程式。</span><span class="sxs-lookup"><span data-stu-id="86c0a-111">Array of certificate hashes to obtain content enablers for.</span></span>

</dd> <dt>

<span data-ttu-id="86c0a-112">*cCerts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86c0a-112">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c0a-113">要取出內容啟用程式的憑證數目。</span><span class="sxs-lookup"><span data-stu-id="86c0a-113">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="86c0a-114">這是 *rgpbCertHashes* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="86c0a-114">This is the number of elements in the *rgpbCertHashes* array.</span></span>

</dd> <dt>

<span data-ttu-id="86c0a-115">*hResultHint* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86c0a-115">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c0a-116">因為撤銷憑證而失敗的作業所收到的傳回值。</span><span class="sxs-lookup"><span data-stu-id="86c0a-116">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="86c0a-117">如果您未呼叫來回應失敗的方法呼叫，請將設定為 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="86c0a-117">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="86c0a-118">*prgContentEnablers* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="86c0a-118">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86c0a-119">接收新建立之 **IMFContentEnabler** 介面位址的陣列。</span><span class="sxs-lookup"><span data-stu-id="86c0a-119">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="86c0a-120">設定為 **Null** ，以取得 *pcContentEnablers* 參數中的內容啟用程式數目。</span><span class="sxs-lookup"><span data-stu-id="86c0a-120">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="86c0a-121">*pcContentEnablers* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="86c0a-121">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86c0a-122">*PrgContentEnablers* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="86c0a-122">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="86c0a-123">如果 *prgContentEnablers* 為 **Null**，則此值會設定為輸出上所需的內容啟用程式數目。</span><span class="sxs-lookup"><span data-stu-id="86c0a-123">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c0a-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="86c0a-124">Return value</span></span>

<span data-ttu-id="86c0a-125">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="86c0a-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="86c0a-126">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="86c0a-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="86c0a-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="86c0a-127">Return code</span></span>                                                                          | <span data-ttu-id="86c0a-128">Description</span><span class="sxs-lookup"><span data-stu-id="86c0a-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="86c0a-129"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="86c0a-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="86c0a-130">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="86c0a-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86c0a-131">備註</span><span class="sxs-lookup"><span data-stu-id="86c0a-131">Remarks</span></span>

<span data-ttu-id="86c0a-132">如果您使用 **IMFContentEnabler** 介面更新撤銷的元件，您必須明確地說明使用者的流程。</span><span class="sxs-lookup"><span data-stu-id="86c0a-132">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="86c0a-133">因為更新程式會將用戶端電腦的資訊傳送到 Microsoft 網站，所以必須進行這種澄清。</span><span class="sxs-lookup"><span data-stu-id="86c0a-133">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="86c0a-134">當您呼叫 **IMFContentEnabler：： AutomaticEnable** 時，內容啟用程式會以 Microsoft 網站上的更新服務位址啟動預設的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="86c0a-134">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="86c0a-135">識別已撤銷元件的唯一識別碼會傳送至 update 服務。</span><span class="sxs-lookup"><span data-stu-id="86c0a-135">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="86c0a-136">接著，服務會將瀏覽器重新導向至網頁，讓使用者可以從該網頁下載並安裝新的已撤銷元件版本。</span><span class="sxs-lookup"><span data-stu-id="86c0a-136">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c0a-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="86c0a-137">Requirements</span></span>



| <span data-ttu-id="86c0a-138">需求</span><span class="sxs-lookup"><span data-stu-id="86c0a-138">Requirement</span></span> | <span data-ttu-id="86c0a-139">值</span><span class="sxs-lookup"><span data-stu-id="86c0a-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86c0a-140">標頭</span><span class="sxs-lookup"><span data-stu-id="86c0a-140">Header</span></span><br/>  | <dl> <span data-ttu-id="86c0a-141"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="86c0a-141"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="86c0a-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="86c0a-142">Library</span></span><br/> | <dl> <span data-ttu-id="86c0a-143"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="86c0a-143"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86c0a-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86c0a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c0a-145">**IWMDRMSecurity 介面**</span><span class="sxs-lookup"><span data-stu-id="86c0a-145">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





