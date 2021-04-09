---
title: Win32_SessionDirectoryVMMPlugin 類別的 SetEnabled 方法
description: 啟用或停用外掛程式。
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- SetEnabled 方法遠端桌面服務
- SetEnabled 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，SetEnabled 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7089a21f143b6f3b27fe9fe58563e6777bf2f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686483"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="22655-106">Win32 SessionDirectoryVMMPlugin 類別的 SetEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="22655-106">SetEnabled method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="22655-107">啟用或停用外掛程式。</span><span class="sxs-lookup"><span data-stu-id="22655-107">Enables or disables the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="22655-108">語法</span><span class="sxs-lookup"><span data-stu-id="22655-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="22655-109">參數</span><span class="sxs-lookup"><span data-stu-id="22655-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22655-110">*已啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22655-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22655-111">指出外掛程式是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="22655-111">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="22655-112">如果外掛程式已啟用則 **為 True** ，否則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="22655-112">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22655-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="22655-113">Return value</span></span>

<span data-ttu-id="22655-114">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="22655-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="22655-115">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="22655-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="22655-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="22655-116">Requirements</span></span>



| <span data-ttu-id="22655-117">需求</span><span class="sxs-lookup"><span data-stu-id="22655-117">Requirement</span></span> | <span data-ttu-id="22655-118">值</span><span class="sxs-lookup"><span data-stu-id="22655-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22655-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22655-119">Minimum supported client</span></span><br/> | <span data-ttu-id="22655-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="22655-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="22655-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22655-121">Minimum supported server</span></span><br/> | <span data-ttu-id="22655-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="22655-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="22655-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="22655-123">Namespace</span></span><br/>                | <span data-ttu-id="22655-124">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="22655-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="22655-125">MOF</span><span class="sxs-lookup"><span data-stu-id="22655-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22655-126"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="22655-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="22655-127">DLL</span><span class="sxs-lookup"><span data-stu-id="22655-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22655-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22655-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22655-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22655-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22655-130">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="22655-130">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





