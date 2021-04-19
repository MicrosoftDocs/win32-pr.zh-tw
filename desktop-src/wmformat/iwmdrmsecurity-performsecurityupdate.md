---
title: 'IWMDRMSecurity PerformSecurityUpdate 方法 (Wmdrmsdk .h) '
description: PerformSecurityUpdate 方法會在本機電腦上起始對 DRM 子系統的安全性更新。
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- PerformSecurityUpdate 方法 windows Media 格式
- PerformSecurityUpdate 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，PerformSecurityUpdate 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981330"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a><span data-ttu-id="f4130-106">IWMDRMSecurity：:P erformSecurityUpdate 方法</span><span class="sxs-lookup"><span data-stu-id="f4130-106">IWMDRMSecurity::PerformSecurityUpdate method</span></span>

<span data-ttu-id="f4130-107">**PerformSecurityUpdate** 方法會在本機電腦上起始對 DRM 子系統的安全性更新。</span><span class="sxs-lookup"><span data-stu-id="f4130-107">The **PerformSecurityUpdate** method initiates a security update to the DRM subsystem on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4130-108">語法</span><span class="sxs-lookup"><span data-stu-id="f4130-108">Syntax</span></span>


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="f4130-109">參數</span><span class="sxs-lookup"><span data-stu-id="f4130-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4130-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4130-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4130-111">更新選項，以下列其中一個旗標表示。</span><span class="sxs-lookup"><span data-stu-id="f4130-111">Update option expressed as one of the following flags.</span></span>



| <span data-ttu-id="f4130-112">旗標</span><span class="sxs-lookup"><span data-stu-id="f4130-112">Flag</span></span>                                          | <span data-ttu-id="f4130-113">描述</span><span class="sxs-lookup"><span data-stu-id="f4130-113">Description</span></span>                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4130-114">WMDRM \_ 安全性 \_ 執行 \_ INDIV</span><span class="sxs-lookup"><span data-stu-id="f4130-114">WMDRM\_SECURITY\_PERFORM\_INDIV</span></span>               | <span data-ttu-id="f4130-115">只有在用戶端的版本已過期時，才會將 DRM 元件設為個人化。</span><span class="sxs-lookup"><span data-stu-id="f4130-115">Causes the DRM component to be individualized only if the version of the client is out of date.</span></span> |
| <span data-ttu-id="f4130-116">WMDRM \_ 安全性 \_ 執行 \_ 撤銷 \_ 更新</span><span class="sxs-lookup"><span data-stu-id="f4130-116">WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH</span></span> | <span data-ttu-id="f4130-117">會更新用戶端電腦上的撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="f4130-117">Causes the revocation lists on the client computer to be updated.</span></span>                               |
| <span data-ttu-id="f4130-118">WMDRM \_ 安全性 \_ 執行 \_ 強制 \_ INDIV</span><span class="sxs-lookup"><span data-stu-id="f4130-118">WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV</span></span>        | <span data-ttu-id="f4130-119">即使用戶端的版本是最新的，也會使 DRM 元件成為個人化。</span><span class="sxs-lookup"><span data-stu-id="f4130-119">Causes the DRM component to be individualized even if the version of the client is up to date.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f4130-120">*ppunkCancelationCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f4130-120">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4130-121">變數的位址，此變數會接收可用於取消此作業之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f4130-121">Address of a variable that receives a pointer to an object that can be used to cancel this operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4130-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4130-122">Return value</span></span>

<span data-ttu-id="f4130-123">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f4130-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f4130-124">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f4130-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f4130-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f4130-125">Return code</span></span>                                                                          | <span data-ttu-id="f4130-126">Description</span><span class="sxs-lookup"><span data-stu-id="f4130-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f4130-127"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f4130-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f4130-128">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f4130-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4130-129">備註</span><span class="sxs-lookup"><span data-stu-id="f4130-129">Remarks</span></span>

<span data-ttu-id="f4130-130">這個方法會以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="f4130-130">This method executes asynchronously.</span></span> <span data-ttu-id="f4130-131">它會在呼叫後立即傳回，然後根據 *dwFlags* 參數中所設定的旗標產生事件。</span><span class="sxs-lookup"><span data-stu-id="f4130-131">It returns immediately after being called and then generates events depending on the flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="f4130-132">針對設定為 [WMDRM 安全性] 的 [ (旗標] 旗標設定為 [WMDRM \_ 安全性] \_ 執行 \_ INDIV 或 WMDRM \_ 安全性 \_ 執行 \_ 強制 \_ INDIV) ，在處理完成時，會產生一連串 **MEWMDRMIndividualizationProgress** 事件，後面接著 **MEWMDRMIndividualizationCompleted** 事件。</span><span class="sxs-lookup"><span data-stu-id="f4130-132">For individualization (flag set to WMDRM\_SECURITY\_PERFORM\_INDIV or WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV), a series of **MEWMDRMIndividualizationProgress** events is generated followed by an **MEWMDRMIndividualizationCompleted** event when processing is complete.</span></span> <span data-ttu-id="f4130-133">藉由呼叫 **IMFMediaEvent：： GetValue** 取得的每個 **MEWMDRMIndividualizationProgress** 事件的值都是 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="f4130-133">The value of each of the **MEWMDRMIndividualizationProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="f4130-134">您可以呼叫所抓取 **IUnknown** 介面的 **QueryInterface** 方法，以取得 [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)介面的實例。</span><span class="sxs-lookup"><span data-stu-id="f4130-134">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span>

<span data-ttu-id="f4130-135">若要重新整理撤銷清單 (旗標設為 [WMDRM \_ 安全性 \_ 執行撤銷重新整理) ] \_ \_ 時，會在處理完成時產生 **MEWMDRMREvocationDownloadCompleted** 事件。</span><span class="sxs-lookup"><span data-stu-id="f4130-135">For refreshing the revocation lists (flag set to WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH), an **MEWMDRMREvocationDownloadCompleted** event is generated when processing is complete.</span></span>

> [!Note]  
> <span data-ttu-id="f4130-136">當 **PerformSecurityUpdate** 完成個人化時，唯一會反映新的個人化狀態的現有物件就是繼承自 **IWMDRMSecurity** 的物件。</span><span class="sxs-lookup"><span data-stu-id="f4130-136">When **PerformSecurityUpdate** completes individualization, the only existing objects that will reflect the new individualized state are those that inherit from **IWMDRMSecurity**.</span></span> <span data-ttu-id="f4130-137">所有其他現有的物件將不會更新。</span><span class="sxs-lookup"><span data-stu-id="f4130-137">All other existing objects will not be updated.</span></span> <span data-ttu-id="f4130-138">您必須釋放並重新建立任何其他物件，使其反映新的個別狀態。</span><span class="sxs-lookup"><span data-stu-id="f4130-138">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

 

<span data-ttu-id="f4130-139">如需使用 Windows Media DRM 用戶端擴充 Api 的非同步方法的詳細資訊，請參閱 [使用媒體基礎事件模型](using-the-media-foundation-model.md)。</span><span class="sxs-lookup"><span data-stu-id="f4130-139">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4130-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4130-140">Requirements</span></span>



| <span data-ttu-id="f4130-141">需求</span><span class="sxs-lookup"><span data-stu-id="f4130-141">Requirement</span></span> | <span data-ttu-id="f4130-142">值</span><span class="sxs-lookup"><span data-stu-id="f4130-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4130-143">標頭</span><span class="sxs-lookup"><span data-stu-id="f4130-143">Header</span></span><br/>  | <dl> <span data-ttu-id="f4130-144"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4130-144"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4130-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="f4130-145">Library</span></span><br/> | <dl> <span data-ttu-id="f4130-146"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4130-146"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4130-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4130-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4130-148">**自動化元件撤銷和更新**</span><span class="sxs-lookup"><span data-stu-id="f4130-148">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="f4130-149">**DRM 的個人化範例**</span><span class="sxs-lookup"><span data-stu-id="f4130-149">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="f4130-150">**IWMDRMSecurity 介面**</span><span class="sxs-lookup"><span data-stu-id="f4130-150">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="f4130-151">**執行 DRM 的個人化**</span><span class="sxs-lookup"><span data-stu-id="f4130-151">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> </dl>

 

 





