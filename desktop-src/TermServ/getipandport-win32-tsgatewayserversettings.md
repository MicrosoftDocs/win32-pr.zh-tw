---
title: Win32_TSGatewayServerSettings 類別的 GetIPAndPort 方法
description: 取得指定傳輸的接聽 IP 位址和埠號碼。
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- GetIPAndPort 方法遠端桌面服務
- GetIPAndPort 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，GetIPAndPort 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317160"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="56dac-106">Win32 TSGatewayServerSettings 類別的 GetIPAndPort 方法 \_</span><span class="sxs-lookup"><span data-stu-id="56dac-106">GetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="56dac-107">取得指定傳輸的接聽 IP 位址和埠號碼。</span><span class="sxs-lookup"><span data-stu-id="56dac-107">Obtains the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="56dac-108">語法</span><span class="sxs-lookup"><span data-stu-id="56dac-108">Syntax</span></span>


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
);
```



## <a name="parameters"></a><span data-ttu-id="56dac-109">參數</span><span class="sxs-lookup"><span data-stu-id="56dac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56dac-110">*TransportType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56dac-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56dac-111">指定傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="56dac-111">Specifies the transport type.</span></span> <span data-ttu-id="56dac-112">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="56dac-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="56dac-113">0</span><span class="sxs-lookup"><span data-stu-id="56dac-113">0</span></span>
</dt> <dd>

<span data-ttu-id="56dac-114">RPC over HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="56dac-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="56dac-115">1</span><span class="sxs-lookup"><span data-stu-id="56dac-115">1</span></span>
</dt> <dd>

<span data-ttu-id="56dac-116">HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="56dac-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="56dac-117">2</span><span class="sxs-lookup"><span data-stu-id="56dac-117">2</span></span>
</dt> <dd>

<span data-ttu-id="56dac-118">UDP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="56dac-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="56dac-119">*IPAddress* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="56dac-119">*IPAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56dac-120">接收接聽 IP 位址的字串，以八位格式 (例如 "192.168.1.1" ) 。</span><span class="sxs-lookup"><span data-stu-id="56dac-120">A string that receives the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="56dac-121">*埠* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="56dac-121">*Port* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56dac-122">指定接聽埠號碼。</span><span class="sxs-lookup"><span data-stu-id="56dac-122">Specifies the listening port number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56dac-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="56dac-123">Return value</span></span>

<span data-ttu-id="56dac-124">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="56dac-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="56dac-125">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="56dac-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="56dac-126">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="56dac-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56dac-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="56dac-127">Requirements</span></span>



| <span data-ttu-id="56dac-128">需求</span><span class="sxs-lookup"><span data-stu-id="56dac-128">Requirement</span></span> | <span data-ttu-id="56dac-129">值</span><span class="sxs-lookup"><span data-stu-id="56dac-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="56dac-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56dac-130">Minimum supported client</span></span><br/> | <span data-ttu-id="56dac-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="56dac-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="56dac-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56dac-132">Minimum supported server</span></span><br/> | <span data-ttu-id="56dac-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="56dac-133">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="56dac-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="56dac-134">Namespace</span></span><br/>                | <span data-ttu-id="56dac-135">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="56dac-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="56dac-136">MOF</span><span class="sxs-lookup"><span data-stu-id="56dac-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56dac-137"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="56dac-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="56dac-138">DLL</span><span class="sxs-lookup"><span data-stu-id="56dac-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56dac-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56dac-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="56dac-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56dac-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56dac-141">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="56dac-141">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





