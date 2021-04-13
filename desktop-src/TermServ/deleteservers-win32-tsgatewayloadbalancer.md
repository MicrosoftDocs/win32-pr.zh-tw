---
title: Win32_TSGatewayLoadBalancer 類別的 DeleteServers 方法
description: 從伺服器屬性刪除伺服器。
ms.assetid: 5ef44725-82b6-464a-abab-a68cc8799669
ms.tgt_platform: multiple
keywords:
- DeleteServers 方法遠端桌面服務
- DeleteServers 方法遠端桌面服務，Win32_TSGatewayLoadBalancer 類別
- Win32_TSGatewayLoadBalancer 類別遠端桌面服務，DeleteServers 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b889f37b783853fbca0b9cb399a83959e2522d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384066"
---
# <a name="deleteservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="90068-106">Win32 TSGatewayLoadBalancer 類別的 DeleteServers 方法 \_</span><span class="sxs-lookup"><span data-stu-id="90068-106">DeleteServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="90068-107">從 **伺服器** 屬性刪除伺服器。</span><span class="sxs-lookup"><span data-stu-id="90068-107">Deletes servers from the **Servers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="90068-108">語法</span><span class="sxs-lookup"><span data-stu-id="90068-108">Syntax</span></span>


```mof
uint32 DeleteServers(
  [in] string Servers
);
```



## <a name="parameters"></a><span data-ttu-id="90068-109">參數</span><span class="sxs-lookup"><span data-stu-id="90068-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90068-110">*伺服器* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90068-110">*Servers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90068-111">要從 [ **伺服器** ] 屬性中刪除的 RD 閘道負載平衡伺服器清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="90068-111">Semicolon-separated list of RD Gateway load-balancing servers to delete from the **Servers** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90068-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="90068-112">Return value</span></span>

<span data-ttu-id="90068-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="90068-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="90068-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="90068-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="90068-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="90068-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="90068-116">備註</span><span class="sxs-lookup"><span data-stu-id="90068-116">Remarks</span></span>

<span data-ttu-id="90068-117">如果 *伺服器* 參數中有多部伺服器，而且其中一個伺服器無法處理，則不會處理任何伺服器。</span><span class="sxs-lookup"><span data-stu-id="90068-117">If multiple servers are in the *Servers* parameter and one of the servers cannot be processed, none of the servers will be processed.</span></span>

<span data-ttu-id="90068-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="90068-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="90068-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="90068-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="90068-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="90068-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="90068-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="90068-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="90068-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="90068-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="90068-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="90068-123">Requirements</span></span>



| <span data-ttu-id="90068-124">需求</span><span class="sxs-lookup"><span data-stu-id="90068-124">Requirement</span></span> | <span data-ttu-id="90068-125">值</span><span class="sxs-lookup"><span data-stu-id="90068-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="90068-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90068-126">Minimum supported client</span></span><br/> | <span data-ttu-id="90068-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="90068-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="90068-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90068-128">Minimum supported server</span></span><br/> | <span data-ttu-id="90068-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90068-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="90068-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="90068-130">Namespace</span></span><br/>                | <span data-ttu-id="90068-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="90068-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="90068-132">MOF</span><span class="sxs-lookup"><span data-stu-id="90068-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90068-133"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="90068-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="90068-134">DLL</span><span class="sxs-lookup"><span data-stu-id="90068-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90068-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90068-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="90068-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90068-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90068-137">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="90068-137">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

