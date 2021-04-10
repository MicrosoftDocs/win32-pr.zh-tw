---
title: Win32_TSClientSetting 類別的 SetColorDepth 方法
description: SetColorDepth 方法會設定類別的 ColorDepth 屬性。
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- SetColorDepth 方法遠端桌面服務
- SetColorDepth 方法遠端桌面服務，Win32_TSClientSetting 類別
- Win32_TSClientSetting 類別遠端桌面服務，SetColorDepth 方法
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934963"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="5332a-106">Win32 TSClientSetting 類別的 SetColorDepth 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5332a-106">SetColorDepth method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="5332a-107">**SetColorDepth** 方法會設定類別的 **ColorDepth** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5332a-107">The **SetColorDepth** method sets the **ColorDepth** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="5332a-108">語法</span><span class="sxs-lookup"><span data-stu-id="5332a-108">Syntax</span></span>


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a><span data-ttu-id="5332a-109">參數</span><span class="sxs-lookup"><span data-stu-id="5332a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5332a-110">*ColorDepth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5332a-110">*ColorDepth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5332a-111">**ColorDepth** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="5332a-111">The new value for the **ColorDepth** property.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="5332a-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="5332a-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="5332a-113">每圖元8位</span><span class="sxs-lookup"><span data-stu-id="5332a-113">8 bits per pixel</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="5332a-114"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="5332a-114"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="5332a-115">每圖元15個位</span><span class="sxs-lookup"><span data-stu-id="5332a-115">15 bits per pixel</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="5332a-116"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="5332a-116"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="5332a-117">每圖元16個位</span><span class="sxs-lookup"><span data-stu-id="5332a-117">16 bits per pixel</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="5332a-118"><span id="4"></span>**億**</span><span class="sxs-lookup"><span data-stu-id="5332a-118"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="5332a-119">每圖元24個位</span><span class="sxs-lookup"><span data-stu-id="5332a-119">24 bits per pixel</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="5332a-120"><span id="5"></span>**.5**</span><span class="sxs-lookup"><span data-stu-id="5332a-120"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="5332a-121">每圖元32位</span><span class="sxs-lookup"><span data-stu-id="5332a-121">32 bits per pixel</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5332a-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="5332a-122">Return value</span></span>

<span data-ttu-id="5332a-123">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5332a-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5332a-124">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="5332a-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="5332a-125">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5332a-125">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="5332a-126">備註</span><span class="sxs-lookup"><span data-stu-id="5332a-126">Remarks</span></span>

<span data-ttu-id="5332a-127">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="5332a-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5332a-128">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5332a-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5332a-129">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="5332a-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5332a-130">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="5332a-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5332a-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="5332a-131">Requirements</span></span>



| <span data-ttu-id="5332a-132">需求</span><span class="sxs-lookup"><span data-stu-id="5332a-132">Requirement</span></span> | <span data-ttu-id="5332a-133">值</span><span class="sxs-lookup"><span data-stu-id="5332a-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5332a-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5332a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5332a-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5332a-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5332a-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5332a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5332a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5332a-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5332a-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="5332a-138">Namespace</span></span><br/>                | <span data-ttu-id="5332a-139">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="5332a-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5332a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5332a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5332a-141"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="5332a-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5332a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5332a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5332a-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5332a-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5332a-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5332a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5332a-145">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="5332a-145">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

