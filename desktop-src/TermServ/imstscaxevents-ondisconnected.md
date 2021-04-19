---
title: IMsTscAxEvents OnDisconnected 方法
description: 當用戶端控制項從遠端桌面工作階段主機的 (RD 工作階段主機) 伺服器中斷連線時呼叫。
ms.assetid: f01086e7-61d1-41df-ba0a-4eecfa57d492
ms.tgt_platform: multiple
keywords:
- OnDisconnected 方法遠端桌面服務
- OnDisconnected 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnDisconnected 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 372ad98c73b1b0e90753891e01e46c61a78c23dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968358"
---
# <a name="imstscaxeventsondisconnected-method"></a><span data-ttu-id="2c4cd-106">IMsTscAxEvents：： OnDisconnected 方法</span><span class="sxs-lookup"><span data-stu-id="2c4cd-106">IMsTscAxEvents::OnDisconnected method</span></span>

<span data-ttu-id="2c4cd-107">當用戶端控制項從遠端桌面工作階段主機的 (RD 工作階段主機) 伺服器中斷連線時呼叫。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-107">Called when the client control has been disconnected from the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c4cd-108">語法</span><span class="sxs-lookup"><span data-stu-id="2c4cd-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long discReason
);
```



## <a name="parameters"></a><span data-ttu-id="2c4cd-109">參數</span><span class="sxs-lookup"><span data-stu-id="2c4cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c4cd-110">*discReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c4cd-110">*discReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4cd-111">指定中斷連接的原因。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-111">Specifies the reason for the disconnection.</span></span> <span data-ttu-id="2c4cd-112">以下是錯誤碼清單。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-112">The following is a list of error codes.</span></span> <span data-ttu-id="2c4cd-113">其中某些錯誤碼定義于 Wincred 中。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-113">Some of these error codes are defined in Wincred.h.</span></span>

<dt>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>

<span data-ttu-id="2c4cd-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-115">通訊端已關閉。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-115">Socket closed.</span></span>

</dd> <dt>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>

<span data-ttu-id="2c4cd-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-117">伺服器遠端中斷連接。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-117">Remote disconnection by server.</span></span> <span data-ttu-id="2c4cd-118">這不是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-118">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>

<span data-ttu-id="2c4cd-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-120">解壓縮錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-120">Decompression error.</span></span>

</dd> <dt>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>

<span data-ttu-id="2c4cd-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-122">連線逾時。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-122">Connection timed out.</span></span>

</dd> <dt>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>

<span data-ttu-id="2c4cd-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-124">解密錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-124">Decryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>

<span data-ttu-id="2c4cd-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-126">DNS 名稱查閱失敗。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-126">DNS name lookup failure.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>

<span data-ttu-id="2c4cd-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-128">DNS 查閱失敗。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-128">DNS lookup failed.</span></span>

</dd> <dt>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>

<span data-ttu-id="2c4cd-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-130">加密錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-130">Encryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>

<span data-ttu-id="2c4cd-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-132">Windows 通訊端 [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) 呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-132">Windows Sockets [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>

<span data-ttu-id="2c4cd-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-134">找不到主機錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-134">Host not found error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>

<span data-ttu-id="2c4cd-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-136">內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-136">Internal error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>

<span data-ttu-id="2c4cd-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-138">內部安全性錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-138">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>

<span data-ttu-id="2c4cd-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-140">內部安全性錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-140">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>

<span data-ttu-id="2c4cd-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-142">指定的加密方法無效。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-142">The encryption method specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>

<span data-ttu-id="2c4cd-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-144">指定的 IP 位址不正確。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-144">Bad IP address specified.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>

<span data-ttu-id="2c4cd-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-146">伺服器安全性資料無效。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-146">Server security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>

<span data-ttu-id="2c4cd-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-148">安全性資料無效。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-148">Security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>

<span data-ttu-id="2c4cd-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-150">指定的 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-150">The IP address specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>

<span data-ttu-id="2c4cd-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-152">授權協商失敗。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-152">License negotiation failed.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>

<span data-ttu-id="2c4cd-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-154">授權超時。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-154">Licensing time-out.</span></span>

</dd> <dt>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>

<span data-ttu-id="2c4cd-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-156">本機中斷連接。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-156">Local disconnection.</span></span> <span data-ttu-id="2c4cd-157">這不是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-157">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>

<span data-ttu-id="2c4cd-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-159">沒有任何可用的資訊。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-159">No information is available.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>

<span data-ttu-id="2c4cd-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-161">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-161">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>

<span data-ttu-id="2c4cd-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-163">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-163">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>

<span data-ttu-id="2c4cd-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-165">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-165">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>

<span data-ttu-id="2c4cd-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-167">使用者遠端中斷連接。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-167">Remote disconnection by user.</span></span> <span data-ttu-id="2c4cd-168">這不是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-168">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>

<span data-ttu-id="2c4cd-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-170">無法解除封裝伺服器憑證。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-170">Failed to unpack server certificate.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>

<span data-ttu-id="2c4cd-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-172">Windows 通訊端 [**連接**](/windows/desktop/api/winsock2/nf-winsock2-connect) 失敗。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-172">Windows Sockets [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) failed.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>

<span data-ttu-id="2c4cd-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-174">Windows 通訊端 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-174">Windows Sockets [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>

<span data-ttu-id="2c4cd-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-176">發生超時。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-176">Time-out occurred.</span></span>

</dd> <dt>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>

<span data-ttu-id="2c4cd-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-178">內部計時器錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-178">Internal timer error.</span></span>

</dd> <dt>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>

<span data-ttu-id="2c4cd-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-180">Windows 通訊端 [**傳送**](/windows/desktop/api/winsock2/nf-winsock2-send) 呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-180">Windows Sockets [**send**](/windows/desktop/api/winsock2/nf-winsock2-send) call failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>

<span data-ttu-id="2c4cd-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL \_錯誤 \_ 帳戶 \_ 已停用** (2823 (0xB07) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL\_ERR\_ACCOUNT\_DISABLED** (2823 (0xB07))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-182">帳戶已停用。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-182">The account is disabled.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>

<span data-ttu-id="2c4cd-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL \_錯誤 \_ 帳戶已 \_ 過期** (3591 (0xE07) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL\_ERR\_ACCOUNT\_EXPIRED** (3591 (0xE07))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-184">帳戶已過期。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-184">The account is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>

<span data-ttu-id="2c4cd-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL \_錯誤 \_ 帳戶 \_ 已 \_ 鎖定** (3335 (0xD07) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL\_ERR\_ACCOUNT\_LOCKED\_OUT** (3335 (0xD07))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-186">帳戶已經鎖定。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-186">The account is locked out.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>

<span data-ttu-id="2c4cd-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL \_錯誤 \_ 帳戶 \_ 限制** (3079 (0xC07) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL\_ERR\_ACCOUNT\_RESTRICTION** (3079 (0xC07))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-188">帳戶受限。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-188">The account is restricted.</span></span>

</dd> <dt>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>

<span data-ttu-id="2c4cd-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL \_ERR 憑證已 \_ \_ 過期** (6919 (0x1B07) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL\_ERR\_CERT\_EXPIRED** (6919 (0x1B07))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-190">收到的憑證已過期。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-190">The received certificate is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>

<span data-ttu-id="2c4cd-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL \_錯誤 \_ 委派 \_ 原則** (5639 (0x1607) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL\_ERR\_DELEGATION\_POLICY** (5639 (0x1607))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-192">原則不支援將認證委派給目標伺服器。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-192">The policy does not support delegation of credentials to the target server.</span></span>

</dd> <dt>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>

<span data-ttu-id="2c4cd-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL \_伺服器 (8455 (0x2107 \_ \_ \_ 所需 \_ 的 \_ 新** 認證) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL\_ERR\_FRESH\_CRED\_REQUIRED\_BY\_SERVER** (8455 (0x2107))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-194">伺服器驗證原則不允許使用已儲存認證的連接要求。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-194">The server authentication policy does not allow connection requests using saved credentials.</span></span> <span data-ttu-id="2c4cd-195">使用者必須輸入新的認證。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-195">The user must enter new credentials.</span></span>

</dd> <dt>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>

<span data-ttu-id="2c4cd-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL \_錯誤 \_ 登入 \_ 失敗** (2055 (0x807) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL\_ERR\_LOGON\_FAILURE** (2055 (0x807))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-197">登入失敗。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-197">Login failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>

<span data-ttu-id="2c4cd-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL \_錯誤 \_ \_ 驗證 \_ 授權** 單位 (6151 (0x1807) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL\_ERR\_NO\_AUTHENTICATING\_AUTHORITY** (6151 (0x1807))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-199">無法連絡任何授權單位進行驗證。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-199">No authority could be contacted for authentication.</span></span> <span data-ttu-id="2c4cd-200">驗證方的功能變數名稱可能錯誤、無法連線到網域，或可能有信任關係失敗。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-200">The domain name of the authenticating party could be wrong, the domain could be unreachable, or there might have been a trust relationship failure.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>

<span data-ttu-id="2c4cd-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL \_錯誤 \_ (\_ \_** 2567 (0xA07) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL\_ERR\_NO\_SUCH\_USER** (2567 (0xA07))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-202">指定的使用者沒有帳戶。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-202">The specified user has no account.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>

<span data-ttu-id="2c4cd-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL \_錯誤 \_ 密碼已 \_ 過期** (3847 (0xF07) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL\_ERR\_PASSWORD\_EXPIRED** (3847 (0xF07))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-204">密碼已過期。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-204">The password is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>

<span data-ttu-id="2c4cd-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL \_錯誤 \_ 密碼 \_ 必須 \_ 變更** (4615 (0x1207) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL\_ERR\_PASSWORD\_MUST\_CHANGE** (4615 (0x1207))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-206">使用者密碼必須在第一次登入之前變更。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-206">The user password must be changed before logging on for the first time.</span></span>

</dd> <dt>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>

<span data-ttu-id="2c4cd-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL \_ERR \_ POLICY \_ NTLM \_** (5895 (0x1707) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL\_ERR\_POLICY\_NTLM\_ONLY** (5895 (0x1707))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-208">除非已達成相互驗證，否則不允許將認證委派給目標伺服器。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-208">Delegation of credentials to the target server is not allowed unless mutual authentication has been achieved.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>

<span data-ttu-id="2c4cd-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL \_錯誤 \_ 智慧卡 \_ 卡 \_ 封鎖** (8711 (0x2207) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL\_ERR\_SMARTCARD\_CARD\_BLOCKED** (8711 (0x2207))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-210">智慧卡遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-210">The smart card is blocked.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>

<span data-ttu-id="2c4cd-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL \_錯誤的 \_ 智慧卡 \_ 錯誤 \_ PIN** (7175 (0x1C07) ) </span><span class="sxs-lookup"><span data-stu-id="2c4cd-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL\_ERR\_SMARTCARD\_WRONG\_PIN** (7175 (0x1C07))</span></span>


</dt> <dd>

<span data-ttu-id="2c4cd-212">將不正確的 PIN 呈現給智慧卡。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-212">An incorrect PIN was presented to the smart card.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c4cd-213">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c4cd-213">Return value</span></span>

<span data-ttu-id="2c4cd-214">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-214">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c4cd-215">備註</span><span class="sxs-lookup"><span data-stu-id="2c4cd-215">Remarks</span></span>

<span data-ttu-id="2c4cd-216">若要取得中斷連線錯誤的描述，請呼叫 [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)方法，並將 *DiscReason* 參數和 [**IMsRdpClient**](imsrdpclient-interface.md)介面的 [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)屬性傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-216">To retrieve a description of the disconnect error, call the [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) method and pass it the *discReason* parameter and the [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) property of the [**IMsRdpClient**](imsrdpclient-interface.md) interface.</span></span>

<span data-ttu-id="2c4cd-217">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="2c4cd-217">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c4cd-218">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c4cd-218">Requirements</span></span>



| <span data-ttu-id="2c4cd-219">需求</span><span class="sxs-lookup"><span data-stu-id="2c4cd-219">Requirement</span></span> | <span data-ttu-id="2c4cd-220">值</span><span class="sxs-lookup"><span data-stu-id="2c4cd-220">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4cd-221">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c4cd-221">Minimum supported client</span></span><br/> | <span data-ttu-id="2c4cd-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c4cd-222">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2c4cd-223">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c4cd-223">Minimum supported server</span></span><br/> | <span data-ttu-id="2c4cd-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c4cd-224">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2c4cd-225">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2c4cd-225">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c4cd-226"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c4cd-226"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c4cd-227">DLL</span><span class="sxs-lookup"><span data-stu-id="2c4cd-227">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c4cd-228"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c4cd-228"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c4cd-229">IID</span><span class="sxs-lookup"><span data-stu-id="2c4cd-229">IID</span></span><br/>                      | <span data-ttu-id="2c4cd-230">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="2c4cd-230">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="2c4cd-231">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c4cd-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c4cd-232">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="2c4cd-232">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

