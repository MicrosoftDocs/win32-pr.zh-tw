---
description: NLA 用戶端可以用整個系統來記錄網路設定資訊，讓未來的查詢傳回指定的設定資訊，而不論網路是否為作用中。
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: 使用 NLA 註冊服務實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976825"
---
# <a name="registering-a-service-instance-with-nla"></a><span data-ttu-id="44bfc-103">使用 NLA 註冊服務實例</span><span class="sxs-lookup"><span data-stu-id="44bfc-103">Registering a Service Instance with NLA</span></span>

<span data-ttu-id="44bfc-104">NLA 用戶端可以用整個系統來記錄網路設定資訊，讓未來的查詢傳回指定的設定資訊，而不論網路是否為作用中。</span><span class="sxs-lookup"><span data-stu-id="44bfc-104">NLA clients can record network configuration information on a system-wide basis, enabling future queries to return the specified configuration information regardless of whether the network is active.</span></span> <span data-ttu-id="44bfc-105">這項功能可讓 NLA 用戶端影響跨多個應用程式的一致網路資訊使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="44bfc-105">This capability allows NLA clients to affect a consistent network information user experience across multiple applications.</span></span>

## <a name="parameters"></a><span data-ttu-id="44bfc-106">參數</span><span class="sxs-lookup"><span data-stu-id="44bfc-106">Parameters</span></span>

<span data-ttu-id="44bfc-107">若要向網路定位知悉服務供應商註冊服務實例，請使用 [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) 函數。</span><span class="sxs-lookup"><span data-stu-id="44bfc-107">To register a service instance with the Network Location Awareness service provider, use the [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function.</span></span> <span data-ttu-id="44bfc-108">為了適當地註冊服務實例，必須使用適當的資訊來設定 **WSASetService** 函式的某些參數，如本節所述。</span><span class="sxs-lookup"><span data-stu-id="44bfc-108">In order to properly register a service instance certain parameters of the **WSASetService** function must be set with the appropriate information, as explained in this section.</span></span> <span data-ttu-id="44bfc-109">如需快速參考， **WSASetService** 函式具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="44bfc-109">For quick reference, the **WSASetService** function has the following syntax:</span></span>

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

<span data-ttu-id="44bfc-110">針對 *lpqsRegInfo* 參數，請提供來自 nla sp 查詢結果的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構，或依照在 [查詢 NLA](querying-nla-2.md)中所指定的 nla sp 查詢需求來遵循。</span><span class="sxs-lookup"><span data-stu-id="44bfc-110">For the *lpqsRegInfo* parameter, provide a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure from either an NLA SP query result, or constructed adhering to the requirements of an NLA SP query, as specified in [Querying NLA](querying-nla-2.md).</span></span>

<span data-ttu-id="44bfc-111">*EssOperation* 參數支援的作業如下：</span><span class="sxs-lookup"><span data-stu-id="44bfc-111">Operations supported for the *essOperation* parameter are the following:</span></span>

<dl> <dt>

<span data-ttu-id="44bfc-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE \_ 註冊</span><span class="sxs-lookup"><span data-stu-id="44bfc-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE\_REGISTER</span></span>
</dt> <dd>

<span data-ttu-id="44bfc-113">在 *lpqsRegInfo* 中提供的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構中所定義的網路，會藉由將網路實例儲存在目前使用者的登錄區中（允許模擬），為使用中的使用者提供持續性。</span><span class="sxs-lookup"><span data-stu-id="44bfc-113">The network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is made persistent for the active user by storing the network instance in the registry hive for the current user, which allows impersonation.</span></span>

</dd> <dt>

<span data-ttu-id="44bfc-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="44bfc-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE\_DELETE</span></span>
</dt> <dd>

<span data-ttu-id="44bfc-115">如果 *lpqsRegInfo* 中提供的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構中所定義的網路是永久性的，則會將它移除。</span><span class="sxs-lookup"><span data-stu-id="44bfc-115">If the network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is persistent, it will be removed.</span></span>

</dd> </dl>

<span data-ttu-id="44bfc-116">您可以使用下列選項來修改 *essOperation* 參數中指定的作業，這些選項可以使用二進位或邏輯來指定：</span><span class="sxs-lookup"><span data-stu-id="44bfc-116">The operation specified in the *essOperation* parameter can be modified by the following options, which can be specified with binary OR logic:</span></span>

<dl> <dt>

<span data-ttu-id="44bfc-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA \_ 易記 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="44bfc-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA\_FRIENDLY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="44bfc-118">搭配 RNRSERVICE REGISTER 使用時 \_ ，會檢查 *lpqsRegInfo* 中定義之網路的 *lpszComment* 欄位是否有效，並持續儲存。</span><span class="sxs-lookup"><span data-stu-id="44bfc-118">When used with RNRSERVICE\_REGISTER, the *lpszComment* field of the network defined in *lpqsRegInfo* is checked for validity and stored persistently.</span></span> <span data-ttu-id="44bfc-119">搭配 RNRSERVICE DELETE 使用 \_ 和定義的網路具有易記名稱時，會移除易記名稱，但不會保留網路專案的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="44bfc-119">When used with RNRSERVICE\_DELETE and the defined network has a friendly name, the friendly name is removed but the network entry is left intact.</span></span>

</dd> <dt>

<span data-ttu-id="44bfc-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA \_ ALLUSERS \_ NETWORK</span><span class="sxs-lookup"><span data-stu-id="44bfc-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA\_ALLUSERS\_NETWORK</span></span>
</dt> <dd>

<span data-ttu-id="44bfc-121">與 RNRSERVICE REGISTER 搭配使用時 \_ ，專案會持續儲存在 HKEY \_ 本機電腦下 \_ ，讓它可在本機電腦上的所有使用者進行查詢時使用。</span><span class="sxs-lookup"><span data-stu-id="44bfc-121">When used with RNRSERVICE\_REGISTER, the entry is stored persistently under HKEY\_LOCAL\_MACHINE, making it available during queries to all users on the local computer.</span></span> <span data-ttu-id="44bfc-122">與 RNRSERVICE DELETE 一起使用時 \_ ，會從 HKEY 本機電腦中移除指定的網路 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="44bfc-122">When used with RNRSERVICE\_DELETE, the specified network is removed from HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="44bfc-123">如果指定的網路不存在，就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="44bfc-123">An error is returned if the specified network is not present.</span></span> <span data-ttu-id="44bfc-124">若要從目前使用者的登錄 hive 刪除網路，則不得指定此旗標。</span><span class="sxs-lookup"><span data-stu-id="44bfc-124">In order to delete a network from the registry hive of the current user, this flag must not be specified.</span></span> <span data-ttu-id="44bfc-125">此旗標只在本機系統管理員的安全性內容中有效。</span><span class="sxs-lookup"><span data-stu-id="44bfc-125">This flag is only valid in the security context of a local system administrator.</span></span>

</dd> </dl>

<span data-ttu-id="44bfc-126">NLA 支援下列 [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) 函式呼叫的錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="44bfc-126">NLA supports the following error codes for [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function calls:</span></span>

| <span data-ttu-id="44bfc-127">錯誤</span><span class="sxs-lookup"><span data-stu-id="44bfc-127">Error</span></span>             | <span data-ttu-id="44bfc-128">意義</span><span class="sxs-lookup"><span data-stu-id="44bfc-128">Meaning</span></span>                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44bfc-129">WSANOTINITIALISED</span><span class="sxs-lookup"><span data-stu-id="44bfc-129">WSANOTINITIALISED</span></span> | <span data-ttu-id="44bfc-130">未執行成功呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 函式來初始化 NLA。</span><span class="sxs-lookup"><span data-stu-id="44bfc-130">A successful call to the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function to initialize NLA was not performed.</span></span>                                                                  |
| <span data-ttu-id="44bfc-131">WSAEACCESS</span><span class="sxs-lookup"><span data-stu-id="44bfc-131">WSAEACCESS</span></span>        | <span data-ttu-id="44bfc-132">NLA \_ ALLUSERS \_ NETWORK 是在 *dwControlFlags* 中指定，而不是在本機系統管理員的安全性內容中。</span><span class="sxs-lookup"><span data-stu-id="44bfc-132">NLA\_ALLUSERS\_NETWORK was specified in *dwControlFlags* while not in the security context of a local system administrator.</span></span>                                                |
| <span data-ttu-id="44bfc-133">WSAEALREADY</span><span class="sxs-lookup"><span data-stu-id="44bfc-133">WSAEALREADY</span></span>       | <span data-ttu-id="44bfc-134">已依要求的方式持續儲存指定的網路，且 *dwControlFlags* 中未指定任何旗標來表示現有專案的更新。</span><span class="sxs-lookup"><span data-stu-id="44bfc-134">The specified network is already persistently stored in the requested manner, and no flags were specified in *dwControlFlags* to indicate an update to the existing entry.</span></span> |
| <span data-ttu-id="44bfc-135">WSAEAFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="44bfc-135">WSAEAFNOSUPPORT</span></span>   | <span data-ttu-id="44bfc-136">指定的通訊協定系列不支援。</span><span class="sxs-lookup"><span data-stu-id="44bfc-136">A protocol family was specified for which there is no support.</span></span> <span data-ttu-id="44bfc-137">NLA 只支援 IP 通訊協定系列。</span><span class="sxs-lookup"><span data-stu-id="44bfc-137">Only IP protocol families are supported in NLA.</span></span>                                                             |
| <span data-ttu-id="44bfc-138">WSAEPFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="44bfc-138">WSAEPFNOSUPPORT</span></span>   | <span data-ttu-id="44bfc-139">指定了不支援的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="44bfc-139">A protocol was specified for which there is no support.</span></span> <span data-ttu-id="44bfc-140">NLA 只支援 IP 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="44bfc-140">Only IP protocol is supported in NLA.</span></span>                                                                              |



 

 

 



