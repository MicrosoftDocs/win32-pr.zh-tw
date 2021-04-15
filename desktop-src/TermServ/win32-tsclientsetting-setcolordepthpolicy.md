---
title: Win32_TSClientSetting 類別的 SetColorDepthPolicy 方法
description: SetColorDepthPolicy 方法會設定類別的 ColorDepthPolicy 屬性。
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- SetColorDepthPolicy 方法遠端桌面服務
- SetColorDepthPolicy 方法遠端桌面服務，Win32_TSClientSetting 類別
- Win32_TSClientSetting 類別遠端桌面服務，SetColorDepthPolicy 方法
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d47280ce303e7eeba401e0eb34c7f7fa5a7bec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384537"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="8e252-106">Win32 TSClientSetting 類別的 SetColorDepthPolicy 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8e252-106">SetColorDepthPolicy method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="8e252-107">**SetColorDepthPolicy** 方法會設定類別的 **ColorDepthPolicy** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8e252-107">The **SetColorDepthPolicy** method sets the **ColorDepthPolicy** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e252-108">語法</span><span class="sxs-lookup"><span data-stu-id="8e252-108">Syntax</span></span>


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="8e252-109">參數</span><span class="sxs-lookup"><span data-stu-id="8e252-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e252-110">*ColorDepthPolicy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e252-110">*ColorDepthPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e252-111">旗標停用或啟用 **SetColorDepthPolicy** 屬性，指定是否要覆寫使用者的最大色彩設定。</span><span class="sxs-lookup"><span data-stu-id="8e252-111">Flag disabling or enabling the **SetColorDepthPolicy** property, which specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="8e252-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="8e252-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="8e252-113">啟用屬性。</span><span class="sxs-lookup"><span data-stu-id="8e252-113">Enable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="8e252-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="8e252-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="8e252-115">停用屬性。</span><span class="sxs-lookup"><span data-stu-id="8e252-115">Disable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e252-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e252-116">Return value</span></span>

<span data-ttu-id="8e252-117">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8e252-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8e252-118">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="8e252-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="8e252-119">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8e252-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e252-120">備註</span><span class="sxs-lookup"><span data-stu-id="8e252-120">Remarks</span></span>

<span data-ttu-id="8e252-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="8e252-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8e252-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8e252-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8e252-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="8e252-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8e252-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="8e252-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e252-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e252-125">Requirements</span></span>



| <span data-ttu-id="8e252-126">需求</span><span class="sxs-lookup"><span data-stu-id="8e252-126">Requirement</span></span> | <span data-ttu-id="8e252-127">值</span><span class="sxs-lookup"><span data-stu-id="8e252-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e252-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e252-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8e252-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e252-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e252-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e252-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8e252-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e252-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e252-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e252-132">Namespace</span></span><br/>                | <span data-ttu-id="8e252-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="8e252-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8e252-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8e252-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e252-135"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e252-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e252-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8e252-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e252-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e252-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e252-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e252-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e252-139">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="8e252-139">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

