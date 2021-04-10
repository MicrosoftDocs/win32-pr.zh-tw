---
title: Win32_TSGatewayRADIUSServer 類別的 Update 方法
description: 更新目前的遠端驗證撥入消費者服務 (RADIUS) 伺服器。
ms.assetid: 38a15768-66eb-40d6-a079-16555f2bf96a
ms.tgt_platform: multiple
keywords:
- Update 方法遠端桌面服務
- Update 方法遠端桌面服務，Win32_TSGatewayRADIUSServer 類別
- Win32_TSGatewayRADIUSServer 類別遠端桌面服務，Update 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be4faf0c87e49a507ac300d7e8b32f218ed006ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685709"
---
# <a name="update-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="1eea1-106">Win32 TSGatewayRADIUSServer 類別的 Update 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1eea1-106">Update method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="1eea1-107">更新目前的遠端驗證撥入消費者服務 (RADIUS) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="1eea1-107">Updates the current Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eea1-108">語法</span><span class="sxs-lookup"><span data-stu-id="1eea1-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="1eea1-109">參數</span><span class="sxs-lookup"><span data-stu-id="1eea1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eea1-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1eea1-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eea1-111">RADIUS 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1eea1-111">RADIUS server name.</span></span>

</dd> <dt>

<span data-ttu-id="1eea1-112">*SharedSecret* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1eea1-112">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eea1-113">RADIUS 伺服器的共用密碼。</span><span class="sxs-lookup"><span data-stu-id="1eea1-113">Shared secret for the RADIUS server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eea1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1eea1-114">Return value</span></span>

<span data-ttu-id="1eea1-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1eea1-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1eea1-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="1eea1-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1eea1-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="1eea1-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1eea1-118">備註</span><span class="sxs-lookup"><span data-stu-id="1eea1-118">Remarks</span></span>

<span data-ttu-id="1eea1-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="1eea1-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1eea1-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1eea1-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1eea1-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1eea1-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1eea1-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1eea1-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1eea1-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="1eea1-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1eea1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1eea1-124">Requirements</span></span>



| <span data-ttu-id="1eea1-125">需求</span><span class="sxs-lookup"><span data-stu-id="1eea1-125">Requirement</span></span> | <span data-ttu-id="1eea1-126">值</span><span class="sxs-lookup"><span data-stu-id="1eea1-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eea1-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1eea1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1eea1-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="1eea1-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1eea1-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1eea1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1eea1-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1eea1-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1eea1-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="1eea1-131">Namespace</span></span><br/>                | <span data-ttu-id="1eea1-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="1eea1-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1eea1-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1eea1-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eea1-134"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="1eea1-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eea1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1eea1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eea1-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eea1-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1eea1-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1eea1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eea1-138">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="1eea1-138">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

