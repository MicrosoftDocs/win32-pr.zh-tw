---
title: Win32_SessionDirectoryVMMPlugin 類別的 GetCurrentVMMPlugin 方法
description: 取得已啟用的最高優先順序外掛程式。
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- GetCurrentVMMPlugin 方法遠端桌面服務
- GetCurrentVMMPlugin 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，GetCurrentVMMPlugin 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844315"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="794d3-106">Win32 SessionDirectoryVMMPlugin 類別的 GetCurrentVMMPlugin 方法 \_</span><span class="sxs-lookup"><span data-stu-id="794d3-106">GetCurrentVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="794d3-107">取得已啟用的最高優先順序外掛程式。</span><span class="sxs-lookup"><span data-stu-id="794d3-107">Gets the highest priority plug-in that is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="794d3-108">語法</span><span class="sxs-lookup"><span data-stu-id="794d3-108">Syntax</span></span>


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="794d3-109">參數</span><span class="sxs-lookup"><span data-stu-id="794d3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="794d3-110">*sName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="794d3-110">*sName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="794d3-111">外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="794d3-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="794d3-112">*sProvider* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="794d3-112">*sProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="794d3-113">外掛程式提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="794d3-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="794d3-114">*sServiceLocation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="794d3-114">*sServiceLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="794d3-115">外掛程式應聯絡的服務位置。</span><span class="sxs-lookup"><span data-stu-id="794d3-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="794d3-116">*sClassID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="794d3-116">*sClassID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="794d3-117">外掛程式的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="794d3-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="794d3-118">*優先順序* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="794d3-118">*Priority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="794d3-119">外掛程式的優先順序。</span><span class="sxs-lookup"><span data-stu-id="794d3-119">The priority of the plug-in.</span></span> <span data-ttu-id="794d3-120">值愈高，外掛程式的優先順序愈高。</span><span class="sxs-lookup"><span data-stu-id="794d3-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="794d3-121">*已啟用* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="794d3-121">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="794d3-122">指出外掛程式是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="794d3-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="794d3-123">如果外掛程式已啟用則 **為 True** ，否則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="794d3-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="794d3-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="794d3-124">Return value</span></span>

<span data-ttu-id="794d3-125">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="794d3-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="794d3-126">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="794d3-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="794d3-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="794d3-127">Requirements</span></span>



| <span data-ttu-id="794d3-128">需求</span><span class="sxs-lookup"><span data-stu-id="794d3-128">Requirement</span></span> | <span data-ttu-id="794d3-129">值</span><span class="sxs-lookup"><span data-stu-id="794d3-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="794d3-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="794d3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="794d3-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="794d3-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="794d3-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="794d3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="794d3-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="794d3-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="794d3-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="794d3-134">Namespace</span></span><br/>                | <span data-ttu-id="794d3-135">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="794d3-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="794d3-136">MOF</span><span class="sxs-lookup"><span data-stu-id="794d3-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="794d3-137"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="794d3-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="794d3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="794d3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="794d3-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="794d3-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="794d3-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="794d3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="794d3-141">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="794d3-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





