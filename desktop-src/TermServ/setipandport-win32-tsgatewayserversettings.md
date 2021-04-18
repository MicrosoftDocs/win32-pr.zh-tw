---
title: Win32_TSGatewayServerSettings 類別的 SetIPAndPort 方法
description: 設定指定傳輸的接聽 IP 位址和埠號碼。
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- SetIPAndPort 方法遠端桌面服務
- SetIPAndPort 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，SetIPAndPort 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508515"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="4b06a-106">Win32 TSGatewayServerSettings 類別的 SetIPAndPort 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4b06a-106">SetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="4b06a-107">設定指定傳輸的接聽 IP 位址和埠號碼。</span><span class="sxs-lookup"><span data-stu-id="4b06a-107">Sets the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b06a-108">語法</span><span class="sxs-lookup"><span data-stu-id="4b06a-108">Syntax</span></span>


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
);
```



## <a name="parameters"></a><span data-ttu-id="4b06a-109">參數</span><span class="sxs-lookup"><span data-stu-id="4b06a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b06a-110">*TransportType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b06a-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b06a-111">指定傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="4b06a-111">Specifies the transport type.</span></span> <span data-ttu-id="4b06a-112">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="4b06a-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="4b06a-113">0</span><span class="sxs-lookup"><span data-stu-id="4b06a-113">0</span></span>
</dt> <dd>

<span data-ttu-id="4b06a-114">RPC over HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="4b06a-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="4b06a-115">1</span><span class="sxs-lookup"><span data-stu-id="4b06a-115">1</span></span>
</dt> <dd>

<span data-ttu-id="4b06a-116">HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="4b06a-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="4b06a-117">2</span><span class="sxs-lookup"><span data-stu-id="4b06a-117">2</span></span>
</dt> <dd>

<span data-ttu-id="4b06a-118">UDP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="4b06a-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4b06a-119">*IPAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b06a-119">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b06a-120">以八位格式指定接聽的 IP 位址 (例如 "192.168.1.1" ) 。</span><span class="sxs-lookup"><span data-stu-id="4b06a-120">Specifies the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="4b06a-121">*埠* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b06a-121">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b06a-122">指定接聽埠號碼。</span><span class="sxs-lookup"><span data-stu-id="4b06a-122">Specifies the listening port number.</span></span>

</dd> <dt>

<span data-ttu-id="4b06a-123">*OverrideExisting* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b06a-123">*OverrideExisting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b06a-124">指出是否要覆寫 HTTP 的現有 IP/埠系結。</span><span class="sxs-lookup"><span data-stu-id="4b06a-124">Indicates whether to override the existing IP/Port binding for HTTP.</span></span> <span data-ttu-id="4b06a-125">只有在 *TransportType* 參數包含 0 (RPC over HTTP) 或 1 (HTTP) 時，才會使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="4b06a-125">This parameter is only used if the *TransportType* parameter contains 0 (RPC over HTTP) or 1 (HTTP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b06a-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b06a-126">Return value</span></span>

<span data-ttu-id="4b06a-127">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="4b06a-127">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4b06a-128">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="4b06a-128">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4b06a-129">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="4b06a-129">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b06a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b06a-130">Requirements</span></span>



| <span data-ttu-id="4b06a-131">需求</span><span class="sxs-lookup"><span data-stu-id="4b06a-131">Requirement</span></span> | <span data-ttu-id="4b06a-132">值</span><span class="sxs-lookup"><span data-stu-id="4b06a-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b06a-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b06a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4b06a-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="4b06a-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4b06a-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b06a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4b06a-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b06a-136">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="4b06a-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="4b06a-137">Namespace</span></span><br/>                | <span data-ttu-id="4b06a-138">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="4b06a-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4b06a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4b06a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b06a-140"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b06a-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b06a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4b06a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b06a-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b06a-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4b06a-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b06a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b06a-144">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="4b06a-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





