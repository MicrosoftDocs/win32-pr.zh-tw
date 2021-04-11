---
title: Win32_TSGatewayServerSettings 類別的 IsTransportEnabled 方法
description: 判斷指定的傳輸是否已啟用。
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- IsTransportEnabled 方法遠端桌面服務
- IsTransportEnabled 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，IsTransportEnabled 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da152499138f6c1aba1ff6477c719aa0e787deee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094471"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="ec56e-106">Win32 TSGatewayServerSettings 類別的 IsTransportEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ec56e-106">IsTransportEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="ec56e-107">判斷指定的傳輸是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="ec56e-107">Determines whether the specified transport is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec56e-108">語法</span><span class="sxs-lookup"><span data-stu-id="ec56e-108">Syntax</span></span>


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="ec56e-109">參數</span><span class="sxs-lookup"><span data-stu-id="ec56e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec56e-110">*TransportType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec56e-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec56e-111">指定傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="ec56e-111">Specifies the transport type.</span></span> <span data-ttu-id="ec56e-112">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="ec56e-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="ec56e-113">0</span><span class="sxs-lookup"><span data-stu-id="ec56e-113">0</span></span>
</dt> <dd>

<span data-ttu-id="ec56e-114">RPC over HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="ec56e-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="ec56e-115">1</span><span class="sxs-lookup"><span data-stu-id="ec56e-115">1</span></span>
</dt> <dd>

<span data-ttu-id="ec56e-116">HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="ec56e-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="ec56e-117">2</span><span class="sxs-lookup"><span data-stu-id="ec56e-117">2</span></span>
</dt> <dd>

<span data-ttu-id="ec56e-118">UDP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="ec56e-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ec56e-119">*已啟用* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ec56e-119">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec56e-120">**布林** 值，指出是否已啟用傳輸。</span><span class="sxs-lookup"><span data-stu-id="ec56e-120">A **boolean** value that indicates whether the transport is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec56e-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec56e-121">Return value</span></span>

<span data-ttu-id="ec56e-122">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="ec56e-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ec56e-123">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="ec56e-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ec56e-124">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="ec56e-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec56e-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec56e-125">Requirements</span></span>



| <span data-ttu-id="ec56e-126">需求</span><span class="sxs-lookup"><span data-stu-id="ec56e-126">Requirement</span></span> | <span data-ttu-id="ec56e-127">值</span><span class="sxs-lookup"><span data-stu-id="ec56e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec56e-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec56e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ec56e-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="ec56e-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ec56e-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec56e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ec56e-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec56e-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="ec56e-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec56e-132">Namespace</span></span><br/>                | <span data-ttu-id="ec56e-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="ec56e-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ec56e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ec56e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec56e-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec56e-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec56e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ec56e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec56e-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec56e-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ec56e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec56e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec56e-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="ec56e-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





