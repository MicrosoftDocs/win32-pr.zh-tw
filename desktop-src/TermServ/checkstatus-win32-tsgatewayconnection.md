---
title: Win32_TSGatewayConnection 類別的 CheckStatus 方法
description: 檢查遠端桌面閘道 (RD 閘道) 的伺服器連線到另一部電腦的狀態，並判斷目的電腦是否設定為負載平衡。
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- CheckStatus 方法遠端桌面服務
- CheckStatus 方法遠端桌面服務，Win32_TSGatewayConnection 類別
- Win32_TSGatewayConnection 類別遠端桌面服務，CheckStatus 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966098"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="fd7ab-106">Win32 TSGatewayConnection 類別的 CheckStatus 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fd7ab-106">CheckStatus method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="fd7ab-107">檢查遠端桌面閘道 (RD 閘道) 的伺服器連線到另一部電腦的狀態，並判斷目的電腦是否設定為負載平衡。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-107">Checks the status of a Remote Desktop Gateway (RD Gateway) server connection to another computer, and determines whether the target computer is configured for load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7ab-108">語法</span><span class="sxs-lookup"><span data-stu-id="fd7ab-108">Syntax</span></span>


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a><span data-ttu-id="fd7ab-109">參數</span><span class="sxs-lookup"><span data-stu-id="fd7ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd7ab-110">*ServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd7ab-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7ab-111">檢查連接之來源 RD 閘道伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-111">The name of the source RD Gateway server from which the connection is checked.</span></span>

</dd> <dt>

<span data-ttu-id="fd7ab-112">*終結* \[ 點在\]</span><span class="sxs-lookup"><span data-stu-id="fd7ab-112">*EndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7ab-113">目標伺服器的名稱 (從來源伺服器檢查存取的端點) 。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-113">The name of the target server (the endpoint) to which access is checked from the source server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd7ab-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd7ab-114">Return value</span></span>

<span data-ttu-id="fd7ab-115">這個方法會傳回下列可能的傳回值。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-115">This method returns the following possible return values.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="fd7ab-116">0</span><span class="sxs-lookup"><span data-stu-id="fd7ab-116">0</span></span>

<span data-ttu-id="fd7ab-117">連接狀態為 [正常]。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-117">The connection status is OK.</span></span> <span data-ttu-id="fd7ab-118">端點可連線，並設定為可進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-118">The endpoint is reachable and is configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fd7ab-119">1</span><span class="sxs-lookup"><span data-stu-id="fd7ab-119">1</span></span>

<span data-ttu-id="fd7ab-120">連接狀態為 unknown。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-120">The connection status is unknown.</span></span> <span data-ttu-id="fd7ab-121">最有可能發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-121">Most likely, an exception occurred.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fd7ab-122">0x80075c34</span><span class="sxs-lookup"><span data-stu-id="fd7ab-122">0x80075c34</span></span>

<span data-ttu-id="fd7ab-123">端點無法連線，或未設定為用於負載平衡。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-123">The endpoint is either not reachable, or it is not configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fd7ab-124">0x80075c32</span><span class="sxs-lookup"><span data-stu-id="fd7ab-124">0x80075c32</span></span>

<span data-ttu-id="fd7ab-125">發生狀態錯誤。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-125">A status error occurred.</span></span> <span data-ttu-id="fd7ab-126">端點可連線，但未在目的電腦上啟動 RPC/HTTP 負載平衡服務 (RPCHTTPLBS) 服務。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-126">The endpoint is reachable, but the RPC/HTTP Load Balancing Service (RPCHTTPLBS) service is not started on the target computer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd7ab-127">備註</span><span class="sxs-lookup"><span data-stu-id="fd7ab-127">Remarks</span></span>

<span data-ttu-id="fd7ab-128">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fd7ab-129">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fd7ab-130">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fd7ab-131">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="fd7ab-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd7ab-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd7ab-132">Requirements</span></span>



| <span data-ttu-id="fd7ab-133">需求</span><span class="sxs-lookup"><span data-stu-id="fd7ab-133">Requirement</span></span> | <span data-ttu-id="fd7ab-134">值</span><span class="sxs-lookup"><span data-stu-id="fd7ab-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7ab-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd7ab-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7ab-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="fd7ab-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fd7ab-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd7ab-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7ab-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd7ab-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fd7ab-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="fd7ab-139">Namespace</span></span><br/>                | <span data-ttu-id="fd7ab-140">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="fd7ab-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fd7ab-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fd7ab-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd7ab-142"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd7ab-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd7ab-143">DLL</span><span class="sxs-lookup"><span data-stu-id="fd7ab-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd7ab-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd7ab-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fd7ab-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd7ab-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7ab-146">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="fd7ab-146">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

