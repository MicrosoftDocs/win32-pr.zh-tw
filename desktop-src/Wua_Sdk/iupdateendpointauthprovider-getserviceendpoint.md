---
description: 要求用來連接到服務的端點。
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'IUpdateEndpointProvider：： GetServiceEndpoint 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967155"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a><span data-ttu-id="cf6f9-103">IUpdateEndpointProvider：： GetServiceEndpoint 方法</span><span class="sxs-lookup"><span data-stu-id="cf6f9-103">IUpdateEndpointProvider::GetServiceEndpoint method</span></span>

<span data-ttu-id="cf6f9-104">要求用來連接到服務的端點。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-104">Requests an endpoint that is used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf6f9-105">語法</span><span class="sxs-lookup"><span data-stu-id="cf6f9-105">Syntax</span></span>


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a><span data-ttu-id="cf6f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="cf6f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf6f9-107">*ServiceId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf6f9-107">*ServiceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf6f9-108">識別要更新的服務。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="cf6f9-109">*endpointType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf6f9-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf6f9-110">識別服務所執行的端點類型。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-110">Identifies the type of endpoint implemented by the service.</span></span>

<span data-ttu-id="cf6f9-111">[**UpdateEndpointType**](updateendpointtype.md)列舉會定義下列常數。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-111">The [**UpdateEndpointType**](updateendpointtype.md) enumeration defines the following constants.</span></span>

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span data-ttu-id="cf6f9-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span><span class="sxs-lookup"><span data-stu-id="cf6f9-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>


</dt> <dd>

<span data-ttu-id="cf6f9-113">用來連接到更新服務的用戶端伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-113">A client-server endpoint that is used to connect to the update service.</span></span>

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span data-ttu-id="cf6f9-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span><span class="sxs-lookup"><span data-stu-id="cf6f9-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>


</dt> <dd>

<span data-ttu-id="cf6f9-115">當用戶端報告掃描、下載及安裝回更新服務的結果時，所使用的報表端點</span><span class="sxs-lookup"><span data-stu-id="cf6f9-115">A Reporting endpoint that is used used when the client reports the results of scans, downloads, and installs back to the update service</span></span>

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span data-ttu-id="cf6f9-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span><span class="sxs-lookup"><span data-stu-id="cf6f9-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>


</dt> <dd>

<span data-ttu-id="cf6f9-117">當用戶端電腦連線到更新服務以查看是否有新版本的 Windows Update 代理程式用戶端軟體時，所使用的 Self-Update 端點。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-117">A Self-Update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span data-ttu-id="cf6f9-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span><span class="sxs-lookup"><span data-stu-id="cf6f9-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>


</dt> <dd>

<span data-ttu-id="cf6f9-119">當用戶端電腦聯絡規定服務，以處理適用于目的電腦的特定更新時，所使用的法規端點。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-119">A Regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span data-ttu-id="cf6f9-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span><span class="sxs-lookup"><span data-stu-id="cf6f9-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>


</dt> <dd>

<span data-ttu-id="cf6f9-121">Simple-Targeting endoint，只用于 (公司環境中的 WSUS 伺服器) 的私人服務。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-121">A Simple-Targeting endoint that is used only with private services (WSUS servers in corporate environments).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cf6f9-122">*proxySettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf6f9-122">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf6f9-123">識別連接到 proxy 伺服器時所使用的設定。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-123">Identifies the settings that are used when connecting to a proxy server.</span></span>

</dd> <dt>

<span data-ttu-id="cf6f9-124">*hUserToken* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf6f9-124">*hUserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf6f9-125">包含表示使用者的 token 控制碼物件。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-125">Contains a token handle object that represents the user.</span></span> <span data-ttu-id="cf6f9-126">端點提供者會使用此權杖來決定要使用的 proxy 設定和認證。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-126">The endpoint provider uses this token to determine which proxy settings and credentials to use.</span></span>

</dd> <dt>

<span data-ttu-id="cf6f9-127">*fRefreshOnline* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf6f9-127">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf6f9-128">表示氣象 WUA 要求新的權杖。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-128">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="cf6f9-129">True 表示要求新的權杖。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-129">True indicates that a new token is requested.</span></span> <span data-ttu-id="cf6f9-130">False 表示要求新的或快取的標記。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-130">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="cf6f9-131">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-131">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="cf6f9-132">*pbstrEndpointLoc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf6f9-132">*pbstrEndpointLoc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf6f9-133">指定用來與服務通訊的 URL。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-133">Specify the URL used to communicate with the service.</span></span> <span data-ttu-id="cf6f9-134">例如，針對 cleint 伺服器端點，這會是用戶端伺服器服務的 URL。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-134">For example, for a cleint-server endpoint this would be the URL to the client server service.</span></span> <span data-ttu-id="cf6f9-135">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-135">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf6f9-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf6f9-136">Return value</span></span>

<span data-ttu-id="cf6f9-137">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-137">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="cf6f9-138">否則，會傳回 COM 或 Windows 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-138">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf6f9-139">備註</span><span class="sxs-lookup"><span data-stu-id="cf6f9-139">Remarks</span></span>

<span data-ttu-id="cf6f9-140">WUA 通常會在第一次呼叫此方法時，將 *fRefreshOnline* 參數設定為 false，然後如果連接錯誤時 WUA，則會在再次呼叫方法時將該參數設定為 true。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-140">WUA typically sets the *fRefreshOnline* parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="cf6f9-141">不過，此方法的執行可以從安全性權杖服務 (STS) 要求新的權杖，或隨時提供快取的權杖。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-141">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

<span data-ttu-id="cf6f9-142">如果端點不需要驗證，則呼叫端只能使用 *pbstrEndpointLoc* 參數所指定的 URL 連接到服務。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-142">If the endpoint does not need authentication, then the caller can connect to the service using only the URL specified by the *pbstrEndpointLoc* parameter.</span></span>

<span data-ttu-id="cf6f9-143">如果端點需要驗證，則呼叫端可以使用 *pbstrEndpointLoc* 參數所指定的 URL，以及其他參數所提供的資料。</span><span class="sxs-lookup"><span data-stu-id="cf6f9-143">If the endpoint does need authentication, then the caller can use the URL specified by the *pbstrEndpointLoc* parameter and the data provided by the other parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf6f9-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf6f9-144">Requirements</span></span>



| <span data-ttu-id="cf6f9-145">需求</span><span class="sxs-lookup"><span data-stu-id="cf6f9-145">Requirement</span></span> | <span data-ttu-id="cf6f9-146">值</span><span class="sxs-lookup"><span data-stu-id="cf6f9-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6f9-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf6f9-147">Minimum supported client</span></span><br/> | <span data-ttu-id="cf6f9-148">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf6f9-148">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="cf6f9-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf6f9-149">Minimum supported server</span></span><br/> | <span data-ttu-id="cf6f9-150">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="cf6f9-150">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="cf6f9-151">標頭</span><span class="sxs-lookup"><span data-stu-id="cf6f9-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf6f9-152"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf6f9-152"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf6f9-153">Idl</span><span class="sxs-lookup"><span data-stu-id="cf6f9-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cf6f9-154"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf6f9-154"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="cf6f9-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf6f9-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf6f9-156"><dt>UpdateEndpointAuth .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf6f9-156"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf6f9-157">DLL</span><span class="sxs-lookup"><span data-stu-id="cf6f9-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf6f9-158"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf6f9-158"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf6f9-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf6f9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf6f9-160">**IUpdateEndpointProvider**</span><span class="sxs-lookup"><span data-stu-id="cf6f9-160">**IUpdateEndpointProvider**</span></span>](iupdateendpointprovider.md)
</dt> </dl>

 

 




