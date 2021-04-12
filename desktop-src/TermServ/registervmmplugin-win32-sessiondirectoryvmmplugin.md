---
title: Win32_SessionDirectoryVMMPlugin 類別的 RegisterVMMPlugin 方法
description: 註冊新的 VMM 外掛程式。
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- RegisterVMMPlugin 方法遠端桌面服務
- RegisterVMMPlugin 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，RegisterVMMPlugin 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384278"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="ae835-106">Win32 SessionDirectoryVMMPlugin 類別的 RegisterVMMPlugin 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ae835-106">RegisterVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="ae835-107">註冊新的 VMM 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="ae835-107">Registers a new VMM plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae835-108">語法</span><span class="sxs-lookup"><span data-stu-id="ae835-108">Syntax</span></span>


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a><span data-ttu-id="ae835-109">參數</span><span class="sxs-lookup"><span data-stu-id="ae835-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae835-110">*sName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae835-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae835-111">外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae835-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="ae835-112">*sProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae835-112">*sProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae835-113">外掛程式提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae835-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="ae835-114">*sServiceLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae835-114">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae835-115">外掛程式應聯絡的服務位置。</span><span class="sxs-lookup"><span data-stu-id="ae835-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="ae835-116">*sClassID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae835-116">*sClassID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae835-117">外掛程式的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae835-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="ae835-118">*優先順序* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae835-118">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae835-119">外掛程式的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ae835-119">The priority of the plug-in.</span></span> <span data-ttu-id="ae835-120">值愈高，外掛程式的優先順序愈高。</span><span class="sxs-lookup"><span data-stu-id="ae835-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="ae835-121">*已啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae835-121">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae835-122">指出外掛程式是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="ae835-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="ae835-123">如果外掛程式已啟用則 **為 True** ，否則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="ae835-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae835-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae835-124">Return value</span></span>

<span data-ttu-id="ae835-125">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ae835-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ae835-126">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="ae835-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae835-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae835-127">Requirements</span></span>



| <span data-ttu-id="ae835-128">需求</span><span class="sxs-lookup"><span data-stu-id="ae835-128">Requirement</span></span> | <span data-ttu-id="ae835-129">值</span><span class="sxs-lookup"><span data-stu-id="ae835-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae835-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae835-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ae835-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="ae835-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ae835-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae835-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ae835-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae835-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="ae835-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="ae835-134">Namespace</span></span><br/>                | <span data-ttu-id="ae835-135">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="ae835-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="ae835-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ae835-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae835-137"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae835-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae835-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ae835-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae835-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae835-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae835-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae835-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae835-141">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="ae835-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





