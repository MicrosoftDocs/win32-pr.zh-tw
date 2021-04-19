---
title: 'NAP 類型常數 (NapTypes .h) '
description: 已定義下列 NAP 常數。
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968193"
---
# <a name="nap-type-constants"></a><span data-ttu-id="24a74-103">NAP 類型常數</span><span class="sxs-lookup"><span data-stu-id="24a74-103">NAP Type Constants</span></span>

> [!Note]  
> <span data-ttu-id="24a74-104">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="24a74-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="24a74-105">已定義下列 NAP 常數。</span><span class="sxs-lookup"><span data-stu-id="24a74-105">The following NAP constants are defined.</span></span>

<span data-ttu-id="24a74-106">下列 NAP 常數定義于 NapTypes 中：</span><span class="sxs-lookup"><span data-stu-id="24a74-106">The following NAP constants are defined in NapTypes.h:</span></span>

<dl> <dt>

<span data-ttu-id="24a74-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span><span class="sxs-lookup"><span data-stu-id="24a74-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-108">0x64</span><span class="sxs-lookup"><span data-stu-id="24a74-108">0x64</span></span>
</dt> <dt>



<span data-ttu-id="24a74-109">[**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)類型長度值的最大數目 (TLV) 與 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)封包相關聯的物件。</span><span class="sxs-lookup"><span data-stu-id="24a74-109">The maximum number of [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) objects associated with an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span><span class="sxs-lookup"><span data-stu-id="24a74-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-111">0xFA0</span><span class="sxs-lookup"><span data-stu-id="24a74-111">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="24a74-112">與健全狀況聲明相關聯之 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) 物件的大小上限（以位元組為單位） ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) 封包。</span><span class="sxs-lookup"><span data-stu-id="24a74-112">The maximum size, in bytes, of a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) object associated with a statement of health ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span><span class="sxs-lookup"><span data-stu-id="24a74-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-114">0xC</span><span class="sxs-lookup"><span data-stu-id="24a74-114">0xC</span></span>
</dt> <dt>



<span data-ttu-id="24a74-115">[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)封包的大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="24a74-115">The minimum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span><span class="sxs-lookup"><span data-stu-id="24a74-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-117">0xFA0</span><span class="sxs-lookup"><span data-stu-id="24a74-117">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="24a74-118">[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)封包的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="24a74-118">The maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="24a74-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-120">maxSoHAttributeSize/sizeof (DWORD) </span><span class="sxs-lookup"><span data-stu-id="24a74-120">maxSoHAttributeSize / sizeof(DWORD)</span></span>
</dt> <dt>



<span data-ttu-id="24a74-121">與 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)相關聯的 DWORD 值的最大數目。</span><span class="sxs-lookup"><span data-stu-id="24a74-121">The maximum number of DWORD values associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="24a74-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-123">maxSoHAttributeSize/0x4</span><span class="sxs-lookup"><span data-stu-id="24a74-123">maxSoHAttributeSize / 0x4</span></span>
</dt> <dt>



<span data-ttu-id="24a74-124">與 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)相關聯的 IPv4 位址數目上限。</span><span class="sxs-lookup"><span data-stu-id="24a74-124">The maximum number of IPv4 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="24a74-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-126">maxSoHAttributeSize/0x10</span><span class="sxs-lookup"><span data-stu-id="24a74-126">maxSoHAttributeSize / 0x10</span></span>
</dt> <dt>



<span data-ttu-id="24a74-127">與 [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)相關聯的 IPv6 位址數目上限。</span><span class="sxs-lookup"><span data-stu-id="24a74-127">The maximum number of IPv6 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span><span class="sxs-lookup"><span data-stu-id="24a74-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-129">0x400</span><span class="sxs-lookup"><span data-stu-id="24a74-129">0x400</span></span>
</dt> <dt>



<span data-ttu-id="24a74-130">[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構所指定之字串的最大長度。</span><span class="sxs-lookup"><span data-stu-id="24a74-130">The maximum length of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span><span class="sxs-lookup"><span data-stu-id="24a74-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-132"> (maxStringLength + 1) \* sizeof (WCHAR) </span><span class="sxs-lookup"><span data-stu-id="24a74-132">(maxStringLength + 1) \* sizeof(WCHAR)</span></span>
</dt> <dt>



<span data-ttu-id="24a74-133">[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構所指定之字串的最大長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="24a74-133">The maximum length, in bytes, of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="24a74-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-135">0x14</span><span class="sxs-lookup"><span data-stu-id="24a74-135">0x14</span></span>
</dt> <dt>



<span data-ttu-id="24a74-136">系統健全狀況實體的最大數目，例如 Shv 和 Sha。</span><span class="sxs-lookup"><span data-stu-id="24a74-136">The maximum number of system health entities, such as SHVs and SHAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="24a74-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-138">\[範圍 (0、maxSystemHealthEntityCount) \]</span><span class="sxs-lookup"><span data-stu-id="24a74-138">\[range(0, maxSystemHealthEntityCount)\]</span></span> 
</dt> <dt>



<span data-ttu-id="24a74-139">系統健康狀態實體數目的可能值範圍。</span><span class="sxs-lookup"><span data-stu-id="24a74-139">The range of possible values for the number of system health entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span><span class="sxs-lookup"><span data-stu-id="24a74-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-141">0x14</span><span class="sxs-lookup"><span data-stu-id="24a74-141">0x14</span></span>
</dt> <dt>



<span data-ttu-id="24a74-142">強制實體的最大數目，例如 Qec。</span><span class="sxs-lookup"><span data-stu-id="24a74-142">The maximum number of enforcement entities, such as QECs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span><span class="sxs-lookup"><span data-stu-id="24a74-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-144">\[範圍 (0、maxEnforcerCount) \]</span><span class="sxs-lookup"><span data-stu-id="24a74-144">\[range(0, maxEnforcerCount)\]</span></span>
</dt> <dt>



<span data-ttu-id="24a74-145">強制實體數目的可能值範圍。</span><span class="sxs-lookup"><span data-stu-id="24a74-145">The range of possible values for the number of enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span><span class="sxs-lookup"><span data-stu-id="24a74-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-147">0xC8</span><span class="sxs-lookup"><span data-stu-id="24a74-147">0xC8</span></span>
</dt> <dt>



<span data-ttu-id="24a74-148">[**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata)結構的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="24a74-148">The maximum size, in bytes, of a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span><span class="sxs-lookup"><span data-stu-id="24a74-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-150">0x14</span><span class="sxs-lookup"><span data-stu-id="24a74-150">0x14</span></span>
</dt> <dt>



<span data-ttu-id="24a74-151">與強制實體相關聯之 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 物件的最大數目。</span><span class="sxs-lookup"><span data-stu-id="24a74-151">The maximum number of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) objects associated with an enforcement entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span><span class="sxs-lookup"><span data-stu-id="24a74-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span><span class="sxs-lookup"><span data-stu-id="24a74-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span></span>
</dt> <dt>



<span data-ttu-id="24a74-154">所有系統健全狀況和強制實體的最大快取 SoH 連接數目。</span><span class="sxs-lookup"><span data-stu-id="24a74-154">The maximum number of cached SoH connections for all system health and enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="24a74-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-156">0x1</span><span class="sxs-lookup"><span data-stu-id="24a74-156">0x1</span></span>
</dt> <dt>



<span data-ttu-id="24a74-157">指定 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)是因為新的要求而非快取的要求所致。</span><span class="sxs-lookup"><span data-stu-id="24a74-157">Specifies that an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)is due to a new request, not a cached request.</span></span> <span data-ttu-id="24a74-158">[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)物件上的 NAP 代理程式會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="24a74-158">This flag is used by the NAP agent on an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span><span class="sxs-lookup"><span data-stu-id="24a74-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-160">0x1</span><span class="sxs-lookup"><span data-stu-id="24a74-160">0x1</span></span>
</dt> <dt>



<span data-ttu-id="24a74-161">指定需要進行修正。</span><span class="sxs-lookup"><span data-stu-id="24a74-161">Specifies that fix-up is required.</span></span> <span data-ttu-id="24a74-162">此旗標是由 SHA 使用。</span><span class="sxs-lookup"><span data-stu-id="24a74-162">This flag is used by a SHA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span><span class="sxs-lookup"><span data-stu-id="24a74-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-164">0x5</span><span class="sxs-lookup"><span data-stu-id="24a74-164">0x5</span></span>
</dt> <dt>



<span data-ttu-id="24a74-165">[**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping)結構中所包含的失敗類別目錄數目。</span><span class="sxs-lookup"><span data-stu-id="24a74-165">The number of failure categories contained within a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span><span class="sxs-lookup"><span data-stu-id="24a74-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-167">0x1</span><span class="sxs-lookup"><span data-stu-id="24a74-167">0x1</span></span>
</dt> <dt>



<span data-ttu-id="24a74-168">元件是隔離強制用戶端 (QEC) ，可在連線驗證期間，在頻內傳送 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包。</span><span class="sxs-lookup"><span data-stu-id="24a74-168">The component is a quarantine enforcement client (QEC) that sends an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet in-band during connection authentication.</span></span>

> [!Note]  
> <span data-ttu-id="24a74-169">Sha 和 Shv 不會使用此值。</span><span class="sxs-lookup"><span data-stu-id="24a74-169">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span><span class="sxs-lookup"><span data-stu-id="24a74-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-171">0x2</span><span class="sxs-lookup"><span data-stu-id="24a74-171">0x2</span></span>
</dt> <dt>



<span data-ttu-id="24a74-172">元件是一種 QEC，它會執行 [**INapCertRelyingParty**](inapcertrelyingparty.md) ，而且必須與健康情況憑證伺服器互動 (HCS) 才能取得健康情況憑證。</span><span class="sxs-lookup"><span data-stu-id="24a74-172">The component is a QEC that implements [**INapCertRelyingParty**](inapcertrelyingparty.md) and must interact with the Health Certificate Server (HCS) in order to obtain a health certificate.</span></span>

> [!Note]  
> <span data-ttu-id="24a74-173">Sha 和 Shv 不會使用此值。</span><span class="sxs-lookup"><span data-stu-id="24a74-173">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> </dl>

<span data-ttu-id="24a74-174">下列 NAP 常數定義于 NapEnforcementClient 中。</span><span class="sxs-lookup"><span data-stu-id="24a74-174">The following NAP constants are defined in NapEnforcementClient.h.</span></span>

<dl> <dt>

<span data-ttu-id="24a74-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="24a74-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-176">0x0FA0</span><span class="sxs-lookup"><span data-stu-id="24a74-176">0x0FA0</span></span>
</dt> <dt>



<span data-ttu-id="24a74-177">SoH 封包的預設最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="24a74-177">The default maximum size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="24a74-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-179">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="24a74-179">0xFFFF</span></span>
</dt> <dt>



<span data-ttu-id="24a74-180">SoH 封包的最大可能大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="24a74-180">The maximum possible size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="24a74-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-182">0x012C</span><span class="sxs-lookup"><span data-stu-id="24a74-182">0x012C</span></span>
</dt> <dt>



<span data-ttu-id="24a74-183">SoH 封包最小可能的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="24a74-183">The smallest possible maximum size, in bytes, of an SoH packet.</span></span> <span data-ttu-id="24a74-184">SoH 封包的實際大小可能小於 **minProtocolMaxSize**。</span><span class="sxs-lookup"><span data-stu-id="24a74-184">The actual size of the SoH packet may be smaller than **minProtocolMaxSize**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24a74-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="24a74-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24a74-186">範圍 (minProtocolMaxSize、maxProtocolMaxSize) </span><span class="sxs-lookup"><span data-stu-id="24a74-186">range(minProtocolMaxSize, maxProtocolMaxSize)</span></span>
</dt> <dt>



<span data-ttu-id="24a74-187">SoH 封包大小上限的可能值範圍。</span><span class="sxs-lookup"><span data-stu-id="24a74-187">The range of possible values for the maximum size of a SoH packet.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24a74-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="24a74-188">Requirements</span></span>



| <span data-ttu-id="24a74-189">需求</span><span class="sxs-lookup"><span data-stu-id="24a74-189">Requirement</span></span> | <span data-ttu-id="24a74-190">值</span><span class="sxs-lookup"><span data-stu-id="24a74-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a74-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24a74-191">Minimum supported client</span></span><br/> | <span data-ttu-id="24a74-192">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24a74-192">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="24a74-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24a74-193">Minimum supported server</span></span><br/> | <span data-ttu-id="24a74-194">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24a74-194">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="24a74-195">標頭</span><span class="sxs-lookup"><span data-stu-id="24a74-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="24a74-196"><dt>NapTypes .h;</dt><dt>NapEnforcementClient .h</dt></span><span class="sxs-lookup"><span data-stu-id="24a74-196"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a74-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24a74-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a74-198">**NAP 常數**</span><span class="sxs-lookup"><span data-stu-id="24a74-198">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





