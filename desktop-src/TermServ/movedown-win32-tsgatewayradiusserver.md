---
title: Win32_TSGatewayRADIUSServer 類別的 MoveDown 方法
description: 將此遠端驗證撥入消費者服務 (RADIUS) server 在優先順序下向下移動一個位置。
ms.assetid: 1b12d2a0-1463-4bd7-9b92-5df2ba799a8a
ms.tgt_platform: multiple
keywords:
- MoveDown 方法遠端桌面服務
- MoveDown 方法遠端桌面服務，Win32_TSGatewayRADIUSServer 類別
- Win32_TSGatewayRADIUSServer 類別遠端桌面服務，MoveDown 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b652eb5e9cfc36f0d41e14d9953b295d35e660be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508523"
---
# <a name="movedown-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="a8f39-106">Win32 TSGatewayRADIUSServer 類別的 MoveDown 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a8f39-106">MoveDown method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="a8f39-107">將此遠端驗證撥入消費者服務 (RADIUS) server 在優先順序下向下移動一個位置。</span><span class="sxs-lookup"><span data-stu-id="a8f39-107">Moves this Remote Authentication Dial-In User Service (RADIUS) server one position down in the priority order.</span></span> <span data-ttu-id="a8f39-108">這個方法會遞增目前 RADIUS 伺服器的 **priority** 屬性，並遞減 radius 伺服器在目前 radius 伺服器之後的 **priority** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a8f39-108">This method increments the **Priority** property of the current RADIUS server and decrements the **Priority** property of the RADIUS server that follows the current RADIUS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f39-109">語法</span><span class="sxs-lookup"><span data-stu-id="a8f39-109">Syntax</span></span>


```mof
uint32 MoveDown();
```



## <a name="parameters"></a><span data-ttu-id="a8f39-110">參數</span><span class="sxs-lookup"><span data-stu-id="a8f39-110">Parameters</span></span>

<span data-ttu-id="a8f39-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a8f39-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8f39-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8f39-112">Return value</span></span>

<span data-ttu-id="a8f39-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="a8f39-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a8f39-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="a8f39-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a8f39-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="a8f39-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f39-116">備註</span><span class="sxs-lookup"><span data-stu-id="a8f39-116">Remarks</span></span>

<span data-ttu-id="a8f39-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a8f39-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a8f39-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="a8f39-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a8f39-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a8f39-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a8f39-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="a8f39-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a8f39-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="a8f39-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f39-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8f39-122">Requirements</span></span>



| <span data-ttu-id="a8f39-123">需求</span><span class="sxs-lookup"><span data-stu-id="a8f39-123">Requirement</span></span> | <span data-ttu-id="a8f39-124">值</span><span class="sxs-lookup"><span data-stu-id="a8f39-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f39-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8f39-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f39-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="a8f39-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a8f39-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8f39-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f39-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8f39-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a8f39-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="a8f39-129">Namespace</span></span><br/>                | <span data-ttu-id="a8f39-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="a8f39-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a8f39-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a8f39-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8f39-132"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8f39-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8f39-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a8f39-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8f39-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f39-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a8f39-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8f39-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f39-136">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="a8f39-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

