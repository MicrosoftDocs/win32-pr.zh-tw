---
title: Win32_TSGatewayServerSettings 類別的 EnableCentralCAP 方法
description: 控制 CentralCAPEnabled 屬性，此屬性會控制 (RD \ 160; 的遠端桌面服務連線授權原則。遠端桌面閘道 (RD 閘道) server 的 Cap) 。
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- EnableCentralCAP 方法遠端桌面服務
- EnableCentralCAP 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，EnableCentralCAP 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933e91a89f9a5afdcd2ae85fa6cb097ef0c29cd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385293"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="77e48-106">Win32 TSGatewayServerSettings 類別的 EnableCentralCAP 方法 \_</span><span class="sxs-lookup"><span data-stu-id="77e48-106">EnableCentralCAP method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="77e48-107">控制 **CentralCAPEnabled** 屬性，此屬性會控制遠端桌面閘道 (RD 閘道) 伺服器的遠端桌面服務連線授權原則 (RD cap) 。</span><span class="sxs-lookup"><span data-stu-id="77e48-107">Controls the **CentralCAPEnabled** property, which controls the Remote Desktop Services connection authorization policies (RD CAPs) for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e48-108">語法</span><span class="sxs-lookup"><span data-stu-id="77e48-108">Syntax</span></span>


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="77e48-109">參數</span><span class="sxs-lookup"><span data-stu-id="77e48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77e48-110">*CentralCAPEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77e48-110">*CentralCAPEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e48-111">如果設定為 **True**，將會使用來自中央 RD CAP 伺服器的 RD cap。</span><span class="sxs-lookup"><span data-stu-id="77e48-111">If set to **True**, RD CAPs from central RD CAP servers will be used.</span></span> <span data-ttu-id="77e48-112">如果設定為 **False**，則只會使用來自本機伺服器的原則。</span><span class="sxs-lookup"><span data-stu-id="77e48-112">If set to **False**, only policies from the local server will be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77e48-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="77e48-113">Return value</span></span>

<span data-ttu-id="77e48-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="77e48-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="77e48-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="77e48-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="77e48-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="77e48-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="77e48-117">備註</span><span class="sxs-lookup"><span data-stu-id="77e48-117">Remarks</span></span>

<span data-ttu-id="77e48-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="77e48-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="77e48-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="77e48-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="77e48-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="77e48-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="77e48-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="77e48-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="77e48-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="77e48-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="77e48-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="77e48-123">Requirements</span></span>



| <span data-ttu-id="77e48-124">需求</span><span class="sxs-lookup"><span data-stu-id="77e48-124">Requirement</span></span> | <span data-ttu-id="77e48-125">值</span><span class="sxs-lookup"><span data-stu-id="77e48-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="77e48-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77e48-126">Minimum supported client</span></span><br/> | <span data-ttu-id="77e48-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="77e48-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="77e48-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77e48-128">Minimum supported server</span></span><br/> | <span data-ttu-id="77e48-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77e48-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="77e48-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="77e48-130">Namespace</span></span><br/>                | <span data-ttu-id="77e48-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="77e48-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="77e48-132">MOF</span><span class="sxs-lookup"><span data-stu-id="77e48-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77e48-133"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="77e48-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="77e48-134">DLL</span><span class="sxs-lookup"><span data-stu-id="77e48-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77e48-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77e48-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="77e48-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77e48-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e48-137">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="77e48-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

