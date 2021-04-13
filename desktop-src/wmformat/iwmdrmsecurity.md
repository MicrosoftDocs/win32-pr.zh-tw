---
title: IWMDRMSecurity 介面
description: IWMDRMSecurity 介面會管理用戶端電腦和數位版權管理 (DRM) 子系統的各種安全性相關資訊。若要取得這個介面的實例，請呼叫 IWMDRMProvider CreateObject。
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- IWMDRMSecurity 介面 windows 媒體格式
- IWMDRMSecurity 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312753"
---
# <a name="iwmdrmsecurity-interface"></a><span data-ttu-id="0ff80-105">IWMDRMSecurity 介面</span><span class="sxs-lookup"><span data-stu-id="0ff80-105">IWMDRMSecurity interface</span></span>

<span data-ttu-id="0ff80-106">**IWMDRMSecurity** 介面會管理用戶端電腦和數位版權管理 (DRM) 子系統的各種安全性相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ff80-106">The **IWMDRMSecurity** interface manages a variety of security-related information for the client computer and digital rights management (DRM) subsystem.</span></span>

<span data-ttu-id="0ff80-107">若要取得這個介面的實例，請呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)。</span><span class="sxs-lookup"><span data-stu-id="0ff80-107">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="0ff80-108">將 **IID \_ IWMDRMSecurity** 傳遞為 *riid* 參數。</span><span class="sxs-lookup"><span data-stu-id="0ff80-108">Pass **IID\_IWMDRMSecurity** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="0ff80-109">成員</span><span class="sxs-lookup"><span data-stu-id="0ff80-109">Members</span></span>

<span data-ttu-id="0ff80-110">**IWMDRMSecurity** 介面繼承自 [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)。</span><span class="sxs-lookup"><span data-stu-id="0ff80-110">The **IWMDRMSecurity** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="0ff80-111">**IWMDRMSecurity** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0ff80-111">**IWMDRMSecurity** also has these types of members:</span></span>

-   [<span data-ttu-id="0ff80-112">方法</span><span class="sxs-lookup"><span data-stu-id="0ff80-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0ff80-113">方法</span><span class="sxs-lookup"><span data-stu-id="0ff80-113">Methods</span></span>

<span data-ttu-id="0ff80-114">**IWMDRMSecurity** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0ff80-114">The **IWMDRMSecurity** interface has these methods.</span></span>



| <span data-ttu-id="0ff80-115">方法</span><span class="sxs-lookup"><span data-stu-id="0ff80-115">Method</span></span>                                                                                      | <span data-ttu-id="0ff80-116">描述</span><span class="sxs-lookup"><span data-stu-id="0ff80-116">Description</span></span>                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ff80-117">**CheckCertForRevocation**</span><span class="sxs-lookup"><span data-stu-id="0ff80-117">**CheckCertForRevocation**</span></span>](iwmdrmsecurity-checkcertforrevocation.md)                     | <span data-ttu-id="0ff80-118">判斷憑證是否已撤銷。</span><span class="sxs-lookup"><span data-stu-id="0ff80-118">Determines whether a certificate has been revoked.</span></span><br/>                                                    |
| [<span data-ttu-id="0ff80-119">**GetContentEnablersForRevocations**</span><span class="sxs-lookup"><span data-stu-id="0ff80-119">**GetContentEnablersForRevocations**</span></span>](iwmdrmsecurity-getcontentenablersforrevocations.md) | <span data-ttu-id="0ff80-120">抓取內容啟用程式介面，以根據已撤銷的憑證來更新元件。</span><span class="sxs-lookup"><span data-stu-id="0ff80-120">Retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span><br/> |
| [<span data-ttu-id="0ff80-121">**GetContentEnablersFromHashes**</span><span class="sxs-lookup"><span data-stu-id="0ff80-121">**GetContentEnablersFromHashes**</span></span>](iwmdrmsecurity-getcontentenablersfromhashes.md)         | <span data-ttu-id="0ff80-122">抓取可根據雜湊憑證來更新元件的內容啟用程式介面。</span><span class="sxs-lookup"><span data-stu-id="0ff80-122">Retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span><br/>  |
| [<span data-ttu-id="0ff80-123">**GetMachineCertificate**</span><span class="sxs-lookup"><span data-stu-id="0ff80-123">**GetMachineCertificate**</span></span>](iwmdrmsecurity-getmachinecertificate.md)                       | <span data-ttu-id="0ff80-124">抓取用戶端電腦上 DRM 子系統的電腦憑證。</span><span class="sxs-lookup"><span data-stu-id="0ff80-124">Retrieves the machine certificate of the DRM subsystem on the client computer.</span></span><br/>                        |
| [<span data-ttu-id="0ff80-125">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="0ff80-125">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)                               | <span data-ttu-id="0ff80-126">從本機存放區抓取憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="0ff80-126">Retrieves a certificate revocation list from the local store.</span></span><br/>                                         |
| [<span data-ttu-id="0ff80-127">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="0ff80-127">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)                 | <span data-ttu-id="0ff80-128">抓取本機存放區中憑證撤銷清單的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0ff80-128">Retrieves the version number of a certificate revocation list in the local store.</span></span><br/>                     |
| [<span data-ttu-id="0ff80-129">**GetSecurityVersion**</span><span class="sxs-lookup"><span data-stu-id="0ff80-129">**GetSecurityVersion**</span></span>](iwmdrmsecurity-getsecurityversion.md)                             | <span data-ttu-id="0ff80-130">抓取用戶端電腦上的 DRM 子系統版本。</span><span class="sxs-lookup"><span data-stu-id="0ff80-130">Retrieves the version of the DRM subsystem on the client computer.</span></span><br/>                                    |
| [<span data-ttu-id="0ff80-131">**PerformSecurityUpdate**</span><span class="sxs-lookup"><span data-stu-id="0ff80-131">**PerformSecurityUpdate**</span></span>](iwmdrmsecurity-performsecurityupdate.md)                       | <span data-ttu-id="0ff80-132">在用戶端電腦上起始對 DRM 子系統的安全性更新。</span><span class="sxs-lookup"><span data-stu-id="0ff80-132">Initiates a security update to the DRM subsystem on the client computer.</span></span><br/>                              |
| [<span data-ttu-id="0ff80-133">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="0ff80-133">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)                               | <span data-ttu-id="0ff80-134">在本機存放區中設定憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="0ff80-134">Sets a certificate revocation list in the local store.</span></span><br/>                                                |



 

## <a name="see-also"></a><span data-ttu-id="0ff80-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ff80-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff80-136">**DRM 的個人化範例**</span><span class="sxs-lookup"><span data-stu-id="0ff80-136">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="0ff80-137">**介面**</span><span class="sxs-lookup"><span data-stu-id="0ff80-137">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0ff80-138">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="0ff80-138">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





