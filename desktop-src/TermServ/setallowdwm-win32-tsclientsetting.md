---
title: Win32_TSClientSetting 類別的 SetAllowDwm 方法
description: 設定 AllowDwm 屬性。
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- SetAllowDwm 方法遠端桌面服務
- SetAllowDwm 方法遠端桌面服務，Win32_TSClientSetting 類別
- Win32_TSClientSetting 類別遠端桌面服務，SetAllowDwm 方法
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39441ba3244f206b057ba47c3cb6f765b5e80604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967731"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="ba7fa-106">Win32 TSClientSetting 類別的 SetAllowDwm 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ba7fa-106">SetAllowDwm method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="ba7fa-107">設定 **AllowDwm** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ba7fa-107">Sets the **AllowDwm** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7fa-108">語法</span><span class="sxs-lookup"><span data-stu-id="ba7fa-108">Syntax</span></span>


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a><span data-ttu-id="ba7fa-109">參數</span><span class="sxs-lookup"><span data-stu-id="ba7fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba7fa-110">*AllowDwm* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ba7fa-110">*AllowDwm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba7fa-111">新的 **AllowDwm** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="ba7fa-111">The new **AllowDwm** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba7fa-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba7fa-112">Return value</span></span>

<span data-ttu-id="ba7fa-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ba7fa-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ba7fa-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="ba7fa-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="ba7fa-115">如果伺服器已覆寫使用者的連接設定，此方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ba7fa-115">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba7fa-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba7fa-116">Requirements</span></span>



| <span data-ttu-id="ba7fa-117">需求</span><span class="sxs-lookup"><span data-stu-id="ba7fa-117">Requirement</span></span> | <span data-ttu-id="ba7fa-118">值</span><span class="sxs-lookup"><span data-stu-id="ba7fa-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7fa-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba7fa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ba7fa-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="ba7fa-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ba7fa-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba7fa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ba7fa-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba7fa-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ba7fa-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ba7fa-123">End of client support</span></span><br/>    | <span data-ttu-id="ba7fa-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="ba7fa-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ba7fa-125">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ba7fa-125">End of server support</span></span><br/>    | <span data-ttu-id="ba7fa-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba7fa-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ba7fa-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="ba7fa-127">Namespace</span></span><br/>                | <span data-ttu-id="ba7fa-128">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="ba7fa-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ba7fa-129">MOF</span><span class="sxs-lookup"><span data-stu-id="ba7fa-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba7fa-130"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba7fa-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba7fa-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ba7fa-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba7fa-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba7fa-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba7fa-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba7fa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7fa-134">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="ba7fa-134">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





