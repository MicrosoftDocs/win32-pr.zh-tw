---
title: Win32_TSGatewayRADIUSServer 類別的 Remove 方法
description: 移除目前的遠端驗證撥入消費者服務 (RADIUS) 伺服器。
ms.assetid: 915f6d38-ba6a-4994-8bb9-bfddb9aa6ff8
ms.tgt_platform: multiple
keywords:
- 移除方法遠端桌面服務
- 移除方法遠端桌面服務、Win32_TSGatewayRADIUSServer 介面
- Win32_TSGatewayRADIUSServer 介面遠端桌面服務，Remove 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Remove
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a91fc4a3ba8bf638dcffd76e3bf3517795674fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317419"
---
# <a name="remove-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="6a8c7-106">移除 Win32 \_ TSGatewayRADIUSServer 類別的方法</span><span class="sxs-lookup"><span data-stu-id="6a8c7-106">Remove method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="6a8c7-107">移除目前的遠端驗證撥入消費者服務 (RADIUS) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="6a8c7-107">Removes the current Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a8c7-108">語法</span><span class="sxs-lookup"><span data-stu-id="6a8c7-108">Syntax</span></span>


```mof
uint32 Remove();
```



## <a name="parameters"></a><span data-ttu-id="6a8c7-109">參數</span><span class="sxs-lookup"><span data-stu-id="6a8c7-109">Parameters</span></span>

<span data-ttu-id="6a8c7-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6a8c7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a8c7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a8c7-111">Return value</span></span>

<span data-ttu-id="6a8c7-112">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6a8c7-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6a8c7-113">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="6a8c7-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6a8c7-114">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="6a8c7-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a8c7-115">備註</span><span class="sxs-lookup"><span data-stu-id="6a8c7-115">Remarks</span></span>

<span data-ttu-id="6a8c7-116">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="6a8c7-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6a8c7-117">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6a8c7-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6a8c7-118">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6a8c7-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6a8c7-119">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6a8c7-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6a8c7-120">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="6a8c7-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a8c7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a8c7-121">Requirements</span></span>



| <span data-ttu-id="6a8c7-122">需求</span><span class="sxs-lookup"><span data-stu-id="6a8c7-122">Requirement</span></span> | <span data-ttu-id="6a8c7-123">值</span><span class="sxs-lookup"><span data-stu-id="6a8c7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a8c7-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a8c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6a8c7-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="6a8c7-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6a8c7-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a8c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6a8c7-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a8c7-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6a8c7-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="6a8c7-128">Namespace</span></span><br/>                | <span data-ttu-id="6a8c7-129">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="6a8c7-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6a8c7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6a8c7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a8c7-131"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a8c7-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a8c7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6a8c7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a8c7-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a8c7-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6a8c7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a8c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a8c7-135">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="6a8c7-135">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

