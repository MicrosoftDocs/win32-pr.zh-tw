---
title: Win32_TSGatewayServerSettings 類別的 EnableTransport 方法
description: 啟用或停用指定的傳輸。
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- EnableTransport 方法遠端桌面服務
- EnableTransport 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，EnableTransport 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a14e7ee94eb02e1358d66b9965ecc2323d5b773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991314"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="6ec52-106">Win32 TSGatewayServerSettings 類別的 EnableTransport 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6ec52-106">EnableTransport method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="6ec52-107">啟用或停用指定的傳輸。</span><span class="sxs-lookup"><span data-stu-id="6ec52-107">Enables or disables the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec52-108">語法</span><span class="sxs-lookup"><span data-stu-id="6ec52-108">Syntax</span></span>


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a><span data-ttu-id="6ec52-109">參數</span><span class="sxs-lookup"><span data-stu-id="6ec52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec52-110">*TransportType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ec52-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-111">指定傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="6ec52-111">Specifies the transport type.</span></span> <span data-ttu-id="6ec52-112">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="6ec52-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="6ec52-113">0</span><span class="sxs-lookup"><span data-stu-id="6ec52-113">0</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-114">RPC over HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="6ec52-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="6ec52-115">1</span><span class="sxs-lookup"><span data-stu-id="6ec52-115">1</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-116">HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="6ec52-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="6ec52-117">2</span><span class="sxs-lookup"><span data-stu-id="6ec52-117">2</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-118">UDP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="6ec52-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6ec52-119">*啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ec52-119">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-120">指定傳輸為啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="6ec52-120">Specifies if the transport is enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec52-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ec52-121">Return value</span></span>

<span data-ttu-id="6ec52-122">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6ec52-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6ec52-123">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="6ec52-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6ec52-124">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="6ec52-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec52-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ec52-125">Requirements</span></span>



| <span data-ttu-id="6ec52-126">需求</span><span class="sxs-lookup"><span data-stu-id="6ec52-126">Requirement</span></span> | <span data-ttu-id="6ec52-127">值</span><span class="sxs-lookup"><span data-stu-id="6ec52-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec52-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ec52-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec52-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="6ec52-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6ec52-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ec52-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec52-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ec52-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="6ec52-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="6ec52-132">Namespace</span></span><br/>                | <span data-ttu-id="6ec52-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="6ec52-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6ec52-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6ec52-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ec52-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ec52-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ec52-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6ec52-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec52-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec52-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6ec52-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ec52-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec52-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="6ec52-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





