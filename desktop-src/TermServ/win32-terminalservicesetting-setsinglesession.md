---
title: Win32_TerminalServiceSetting 類別的 SetSingleSession 方法
description: SetSingleSession 方法會設定類別的 SingleSession 屬性。
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- SetSingleSession 方法遠端桌面服務
- SetSingleSession 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetSingleSession 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a6ff702020b7682938b7174c65623eba30076a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965521"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="b461c-106">Win32 TerminalServiceSetting 類別的 SetSingleSession 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b461c-106">SetSingleSession method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="b461c-107">**SetSingleSession** 方法會設定類別的 **SingleSession** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b461c-107">The **SetSingleSession** method sets the **SingleSession** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="b461c-108">語法</span><span class="sxs-lookup"><span data-stu-id="b461c-108">Syntax</span></span>


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a><span data-ttu-id="b461c-109">參數</span><span class="sxs-lookup"><span data-stu-id="b461c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b461c-110">*SingleSession* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b461c-110">*SingleSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b461c-111">旗標停用或啟用 **SingleSession** 屬性，以判斷使用者是否限制在一或多個遠端桌面服務會話中。</span><span class="sxs-lookup"><span data-stu-id="b461c-111">Flag disabling or enabling the **SingleSession** property, which determines whether users are limited to one or more Remote Desktop Services sessions.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b461c-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="b461c-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b461c-113">停用屬性。</span><span class="sxs-lookup"><span data-stu-id="b461c-113">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="b461c-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="b461c-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="b461c-115">啟用屬性。</span><span class="sxs-lookup"><span data-stu-id="b461c-115">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b461c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b461c-116">Return value</span></span>

<span data-ttu-id="b461c-117">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b461c-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b461c-118">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="b461c-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b461c-119">備註</span><span class="sxs-lookup"><span data-stu-id="b461c-119">Remarks</span></span>

<span data-ttu-id="b461c-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="b461c-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b461c-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b461c-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b461c-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b461c-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b461c-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="b461c-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b461c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b461c-124">Requirements</span></span>



| <span data-ttu-id="b461c-125">需求</span><span class="sxs-lookup"><span data-stu-id="b461c-125">Requirement</span></span> | <span data-ttu-id="b461c-126">值</span><span class="sxs-lookup"><span data-stu-id="b461c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b461c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b461c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b461c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b461c-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b461c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b461c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b461c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b461c-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b461c-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="b461c-131">Namespace</span></span><br/>                | <span data-ttu-id="b461c-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="b461c-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b461c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b461c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b461c-134"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="b461c-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b461c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b461c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b461c-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b461c-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b461c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b461c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b461c-138">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="b461c-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

