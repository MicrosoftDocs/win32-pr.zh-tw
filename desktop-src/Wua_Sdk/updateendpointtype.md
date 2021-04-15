---
description: 定義可以用來連接到服務的端點類型。
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: 'UpdateEndpointType 列舉 (UpdateEndpointAuth) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510953"
---
# <a name="updateendpointtype-enumeration"></a><span data-ttu-id="d1107-103">UpdateEndpointType 列舉</span><span class="sxs-lookup"><span data-stu-id="d1107-103">UpdateEndpointType enumeration</span></span>

<span data-ttu-id="d1107-104">定義可以用來連接到服務的端點類型。</span><span class="sxs-lookup"><span data-stu-id="d1107-104">Defines the type of endpoints that can be used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1107-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1107-105">Syntax</span></span>


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a><span data-ttu-id="d1107-106">常數</span><span class="sxs-lookup"><span data-stu-id="d1107-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d1107-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span><span class="sxs-lookup"><span data-stu-id="d1107-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="d1107-108">用來連線到更新服務的用戶端伺服器端點，例如公司環境中的 Windows Update、Microsoft Update 和 WSUS 伺服器，以尋找可能適用于電腦之更新的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1107-108">A client-server endpoint that is used to connect to the update service, such as Windows Update, Microsoft Update, and WSUS server in a corporate environment, to find information on updates that may be applicable to the computer.</span></span>

<span data-ttu-id="d1107-109">更新服務會傳回上次用戶端與伺服器同步處理後，已發行、修改或撤銷之更新的資訊。</span><span class="sxs-lookup"><span data-stu-id="d1107-109">The update service returns information on updates that have been published, revised, or withdrawn since the last time that client performed a sync with the server.</span></span>

</dd> <dt>

<span data-ttu-id="d1107-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span><span class="sxs-lookup"><span data-stu-id="d1107-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>
</dt> <dd>

<span data-ttu-id="d1107-111">當用戶端報告掃描、下載及安裝回更新服務的結果時，所使用的報告端點。</span><span class="sxs-lookup"><span data-stu-id="d1107-111">A reporting endpoint that is used when the client reports the results of scans, downloads, and installs back to the update service.</span></span>

<span data-ttu-id="d1107-112">在公用服務 (Windows Update 和 Microsoft Update) 的情況下，這是為了品質監視用途所進行。</span><span class="sxs-lookup"><span data-stu-id="d1107-112">In the case of public services (Windows Update and Microsoft Update), this is done for quality monitoring purposes.</span></span>

<span data-ttu-id="d1107-113">在私人服務（例如公司 WSUS 伺服器）的情況下，thhis 類型的端點也可讓伺服器收集有關受管理之用戶端電腦的清查和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="d1107-113">In the case of private services, such as a corporate WSUS server, thhis type of endpoint also allows the server to collect inventory and other information about the client computers under management.</span></span>

</dd> <dt>

<span data-ttu-id="d1107-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span><span class="sxs-lookup"><span data-stu-id="d1107-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="d1107-115">當用戶端電腦連線到更新服務以查看是否有新版本的 Windows Update 代理程式用戶端軟體時，所使用的自我更新端點。</span><span class="sxs-lookup"><span data-stu-id="d1107-115">A self-update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

<span data-ttu-id="d1107-116">自我更新端點會使用不同的通訊協定，然後是 Client-Server 端點，因此即使發生錯誤狀況，可能會導致正常的用戶端伺服器同步處理無法在特定用戶端電腦上運作，也可以散發自我更新。</span><span class="sxs-lookup"><span data-stu-id="d1107-116">The Self-update endpoint uses a different protocol then the Client-Server endpoint so that self-updates can be distributed even if there is an error condition that might be preventing the normal client-server sync from working on a particular client computer.</span></span>

</dd> <dt>

<span data-ttu-id="d1107-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span><span class="sxs-lookup"><span data-stu-id="d1107-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>
</dt> <dd>

<span data-ttu-id="d1107-118">當用戶端電腦聯絡規定服務，以處理適用于目的電腦的特定更新時，所使用的法規端點。</span><span class="sxs-lookup"><span data-stu-id="d1107-118">A regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

<span data-ttu-id="d1107-119">法規服務可以指出更新是否「受管制」 (也稱為「節流」 ) -換句話說，法規服務可以告訴用戶端電腦它不應該對特定的更新採取任何動作，即使該更新看似適用也一樣。</span><span class="sxs-lookup"><span data-stu-id="d1107-119">The regulation service can indicate whether the update is “regulated” (also known as “throttled”) – in other words, the regulation service can tell the client computer that it should not act on a particular update, even though that update appears to be applicable.</span></span>

</dd> <dt>

<span data-ttu-id="d1107-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span><span class="sxs-lookup"><span data-stu-id="d1107-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>
</dt> <dd>

<span data-ttu-id="d1107-121">只搭配私人服務使用的簡單目標端點， (在公司環境中) 的 WSUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="d1107-121">A simple-targeting endpoint that is used only with private services (WSUS servers in corporate environments).</span></span> <span data-ttu-id="d1107-122">在公司環境中，可以將用戶端電腦指派給特定的目標群組，而且可以核准在某些群組的電腦上安裝更新，而不是其他群組的電腦。</span><span class="sxs-lookup"><span data-stu-id="d1107-122">In a corporate environment, client computers can be assigned to particular target groups, and updates can be approved for installation on computers in some groups but not others.</span></span>

<span data-ttu-id="d1107-123">例如，WSUS 系統管理員可能會為用來測試新更新的電腦建立「測試」群組，而系統管理員可能會核准測試群組中電腦上安裝的新發行更新，而不會將它們核准用於組織中的其他電腦。</span><span class="sxs-lookup"><span data-stu-id="d1107-123">For example, the WSUS administrator may create a “Testing” group for computers that are used to test new updates, and the administrator may approve newly-released updates for installation on computers in the Testing group without approving them for installation on other computers in the organization.</span></span> <span data-ttu-id="d1107-124">簡單的目標交換可用來讓用戶端電腦向 WSUS 伺服器註冊自己，並允許伺服器告訴用戶端電腦它所在的群組。</span><span class="sxs-lookup"><span data-stu-id="d1107-124">The simple targeting exchange is used to allow a client computer to register itself with the WSUS server, and to allow the server to tell the client computer what group it is in.</span></span>

</dd> <dt>

<span data-ttu-id="d1107-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span><span class="sxs-lookup"><span data-stu-id="d1107-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="d1107-126">安全的用戶端-伺服器端點，可讓用戶端取得需要授權之應用程式的相關資訊，以便在用戶端電腦上使用這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="d1107-126">A secured-client-server endpoint that allows a client to obtain info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="d1107-127">此授權架構目前僅供 Windows 8 用來部署透過 Windows Store 取得的應用程式和更新。</span><span class="sxs-lookup"><span data-stu-id="d1107-127">This licensing framework is currently only used by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="d1107-128">Windows Update、Microsoft Update 或 WSUS 目前未使用安全的用戶端-伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="d1107-128">The secured-client-server endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> <dt>

<span data-ttu-id="d1107-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span><span class="sxs-lookup"><span data-stu-id="d1107-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span></span>
</dt> <dd>

<span data-ttu-id="d1107-130">用戶端會使用次要服務驗證端點來提供驗證，然後才能取得需要授權的應用程式資訊，以便在用戶端電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="d1107-130">The secondary-service-authentication endpoint is used by a client to provide authentication before it obtains info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="d1107-131">此授權架構目前僅供 Windows 8 用來部署透過 Windows Store 取得的應用程式和更新。</span><span class="sxs-lookup"><span data-stu-id="d1107-131">This licensing framework is currently only utilized by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="d1107-132">Windows Update、Microsoft Update 或 WSUS 目前未使用次要服務驗證端點。</span><span class="sxs-lookup"><span data-stu-id="d1107-132">The secondary-service-authentication endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1107-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1107-133">Requirements</span></span>



| <span data-ttu-id="d1107-134">需求</span><span class="sxs-lookup"><span data-stu-id="d1107-134">Requirement</span></span> | <span data-ttu-id="d1107-135">值</span><span class="sxs-lookup"><span data-stu-id="d1107-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1107-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1107-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d1107-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1107-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="d1107-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1107-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d1107-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1107-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d1107-140">標頭</span><span class="sxs-lookup"><span data-stu-id="d1107-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1107-141"><dt>UpdateEndpointAuth。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1107-141"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1107-142">Idl</span><span class="sxs-lookup"><span data-stu-id="d1107-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1107-143"><dt>UpdateEndpointAuth .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1107-143"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




