---
title: Win32_TerminalServiceSetting 類別的 SetFallbackPrintDriverType 方法
description: SetFallbackPrintDriverType 方法會設定類別的 FallbackPrintDriverType 屬性。
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- SetFallbackPrintDriverType 方法遠端桌面服務
- SetFallbackPrintDriverType 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetFallbackPrintDriverType 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025418"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="7368a-106">Win32 TerminalServiceSetting 類別的 SetFallbackPrintDriverType 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7368a-106">SetFallbackPrintDriverType method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="7368a-107">**SetFallbackPrintDriverType** 方法會設定類別的 **FallbackPrintDriverType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7368a-107">The **SetFallbackPrintDriverType** method sets the **FallbackPrintDriverType** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="7368a-108">語法</span><span class="sxs-lookup"><span data-stu-id="7368a-108">Syntax</span></span>


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a><span data-ttu-id="7368a-109">參數</span><span class="sxs-lookup"><span data-stu-id="7368a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7368a-110">*FallbackPrintDriverType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7368a-110">*FallbackPrintDriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7368a-111">設定 **FallbackPrintDriverType** 屬性，以允許或拒絕新的遠端桌面服務連接。</span><span class="sxs-lookup"><span data-stu-id="7368a-111">Sets the **FallbackPrintDriverType** property which allows or denies new Remote Desktop Services connections.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="7368a-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="7368a-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="7368a-113">無備用驅動程式。</span><span class="sxs-lookup"><span data-stu-id="7368a-113">No fallback drivers.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="7368a-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="7368a-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="7368a-115">最佳猜測。</span><span class="sxs-lookup"><span data-stu-id="7368a-115">Best guess.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="7368a-116"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="7368a-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="7368a-117">最佳猜測。</span><span class="sxs-lookup"><span data-stu-id="7368a-117">Best guess.</span></span> <span data-ttu-id="7368a-118">如果找不到相符項，則會切換回 Hewlett-Packard 印表機控制語言 (PCL) 。</span><span class="sxs-lookup"><span data-stu-id="7368a-118">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="7368a-119"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="7368a-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="7368a-120">最佳猜測。</span><span class="sxs-lookup"><span data-stu-id="7368a-120">Best guess.</span></span> <span data-ttu-id="7368a-121">如果找不到相符的結果，則會改回 Postscript (PS) 。</span><span class="sxs-lookup"><span data-stu-id="7368a-121">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="7368a-122"><span id="4"></span>**億**</span><span class="sxs-lookup"><span data-stu-id="7368a-122"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="7368a-123">最佳猜測。</span><span class="sxs-lookup"><span data-stu-id="7368a-123">Best guess.</span></span> <span data-ttu-id="7368a-124">如果找不到相符的，則會顯示 PS 和 PCL 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="7368a-124">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7368a-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="7368a-125">Return value</span></span>

<span data-ttu-id="7368a-126">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7368a-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7368a-127">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="7368a-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="7368a-128">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7368a-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="7368a-129">備註</span><span class="sxs-lookup"><span data-stu-id="7368a-129">Remarks</span></span>

<span data-ttu-id="7368a-130">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="7368a-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7368a-131">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7368a-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7368a-132">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="7368a-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7368a-133">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="7368a-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7368a-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="7368a-134">Requirements</span></span>



| <span data-ttu-id="7368a-135">需求</span><span class="sxs-lookup"><span data-stu-id="7368a-135">Requirement</span></span> | <span data-ttu-id="7368a-136">值</span><span class="sxs-lookup"><span data-stu-id="7368a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7368a-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7368a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7368a-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7368a-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7368a-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7368a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7368a-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7368a-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7368a-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="7368a-141">Namespace</span></span><br/>                | <span data-ttu-id="7368a-142">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="7368a-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7368a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7368a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7368a-144"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="7368a-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7368a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7368a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7368a-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7368a-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7368a-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7368a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7368a-148">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="7368a-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

