---
title: Win32_TSGatewayRADIUSServer 類別的 Add 方法
description: 新增遠端驗證撥入消費者服務 (RADIUS) 伺服器。
ms.assetid: 78f74bb6-8f70-4bc1-8e4d-1670a3ae3f31
ms.tgt_platform: multiple
keywords:
- 新增方法遠端桌面服務
- 新增方法遠端桌面服務、Win32_TSGatewayRADIUSServer 介面
- Win32_TSGatewayRADIUSServer 介面遠端桌面服務，Add 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Add
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6869c55a6704944c34c68af065875cad92e8385c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965322"
---
# <a name="add-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="1fa05-106">Win32 TSGatewayRADIUSServer 類別的 Add 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1fa05-106">Add method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="1fa05-107">新增遠端驗證撥入消費者服務 (RADIUS) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="1fa05-107">Adds a new Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa05-108">語法</span><span class="sxs-lookup"><span data-stu-id="1fa05-108">Syntax</span></span>


```mof
uint32 Add(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="1fa05-109">參數</span><span class="sxs-lookup"><span data-stu-id="1fa05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fa05-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1fa05-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa05-111">RADIUS 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa05-111">RADIUS server name.</span></span>

</dd> <dt>

<span data-ttu-id="1fa05-112">*SharedSecret* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1fa05-112">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa05-113">RADIUS 伺服器的共用密碼。</span><span class="sxs-lookup"><span data-stu-id="1fa05-113">Shared secret for the RADIUS server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fa05-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fa05-114">Return value</span></span>

<span data-ttu-id="1fa05-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1fa05-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1fa05-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="1fa05-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1fa05-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="1fa05-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1fa05-118">備註</span><span class="sxs-lookup"><span data-stu-id="1fa05-118">Remarks</span></span>

<span data-ttu-id="1fa05-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="1fa05-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1fa05-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1fa05-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1fa05-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1fa05-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1fa05-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1fa05-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1fa05-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="1fa05-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa05-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fa05-124">Requirements</span></span>



| <span data-ttu-id="1fa05-125">需求</span><span class="sxs-lookup"><span data-stu-id="1fa05-125">Requirement</span></span> | <span data-ttu-id="1fa05-126">值</span><span class="sxs-lookup"><span data-stu-id="1fa05-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa05-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fa05-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa05-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="1fa05-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1fa05-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fa05-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa05-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fa05-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1fa05-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="1fa05-131">Namespace</span></span><br/>                | <span data-ttu-id="1fa05-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="1fa05-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1fa05-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1fa05-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fa05-134"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fa05-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fa05-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa05-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fa05-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa05-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1fa05-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fa05-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa05-138">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="1fa05-138">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

