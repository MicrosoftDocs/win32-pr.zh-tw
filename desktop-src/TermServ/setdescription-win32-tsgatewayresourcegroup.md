---
title: Win32_TSGatewayResourceGroup 類別的 SetDescription 方法
description: 設定資源群組的 Description 屬性。
ms.assetid: ab1280c7-ce53-4807-9537-953b597dd636
ms.tgt_platform: multiple
keywords:
- SetDescription 方法遠端桌面服務
- SetDescription 方法遠端桌面服務，Win32_TSGatewayResourceGroup 類別
- Win32_TSGatewayResourceGroup 類別遠端桌面服務，SetDescription 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d815cc5400a182f2dff3b982643d5e6bfd861002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967565"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="1c7d7-106">Win32 TSGatewayResourceGroup 類別的 SetDescription 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1c7d7-106">SetDescription method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="1c7d7-107">設定資源群組的 **Description** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1c7d7-107">Sets the **Description** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c7d7-108">語法</span><span class="sxs-lookup"><span data-stu-id="1c7d7-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="1c7d7-109">參數</span><span class="sxs-lookup"><span data-stu-id="1c7d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c7d7-110">*描述* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c7d7-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7d7-111">資源群組的描述。</span><span class="sxs-lookup"><span data-stu-id="1c7d7-111">Description of the resource group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c7d7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c7d7-112">Return value</span></span>

<span data-ttu-id="1c7d7-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1c7d7-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1c7d7-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="1c7d7-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1c7d7-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="1c7d7-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c7d7-116">備註</span><span class="sxs-lookup"><span data-stu-id="1c7d7-116">Remarks</span></span>

<span data-ttu-id="1c7d7-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="1c7d7-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1c7d7-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1c7d7-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1c7d7-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1c7d7-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1c7d7-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1c7d7-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1c7d7-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="1c7d7-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c7d7-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c7d7-122">Requirements</span></span>



| <span data-ttu-id="1c7d7-123">需求</span><span class="sxs-lookup"><span data-stu-id="1c7d7-123">Requirement</span></span> | <span data-ttu-id="1c7d7-124">值</span><span class="sxs-lookup"><span data-stu-id="1c7d7-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c7d7-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c7d7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1c7d7-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="1c7d7-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1c7d7-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c7d7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1c7d7-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c7d7-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1c7d7-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="1c7d7-129">Namespace</span></span><br/>                | <span data-ttu-id="1c7d7-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="1c7d7-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1c7d7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1c7d7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c7d7-132"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c7d7-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c7d7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1c7d7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c7d7-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c7d7-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1c7d7-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c7d7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c7d7-136">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="1c7d7-136">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

