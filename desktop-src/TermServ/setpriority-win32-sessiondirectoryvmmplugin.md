---
title: Win32_SessionDirectoryVMMPlugin 類別的 SetPriority 方法
description: 設定外掛程式的優先順序。
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- SetPriority 方法遠端桌面服務
- SetPriority 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，SetPriority 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d20dbc4af332d0c658f819f8e47f5b3eb4e95b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935059"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="ce44f-106">Win32 SessionDirectoryVMMPlugin 類別的 SetPriority 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ce44f-106">SetPriority method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="ce44f-107">設定外掛程式的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ce44f-107">Sets the priority of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce44f-108">語法</span><span class="sxs-lookup"><span data-stu-id="ce44f-108">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="ce44f-109">參數</span><span class="sxs-lookup"><span data-stu-id="ce44f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce44f-110">*優先順序* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce44f-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-111">外掛程式的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ce44f-111">The priority of the plug-in.</span></span> <span data-ttu-id="ce44f-112">值愈高，外掛程式的優先順序愈高。</span><span class="sxs-lookup"><span data-stu-id="ce44f-112">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="ce44f-113">優先權預設為零。</span><span class="sxs-lookup"><span data-stu-id="ce44f-113">The priority is zero by default.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce44f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce44f-114">Return value</span></span>

<span data-ttu-id="ce44f-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ce44f-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ce44f-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="ce44f-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce44f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce44f-117">Requirements</span></span>



| <span data-ttu-id="ce44f-118">需求</span><span class="sxs-lookup"><span data-stu-id="ce44f-118">Requirement</span></span> | <span data-ttu-id="ce44f-119">值</span><span class="sxs-lookup"><span data-stu-id="ce44f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce44f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce44f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ce44f-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="ce44f-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ce44f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce44f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ce44f-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce44f-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="ce44f-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="ce44f-124">Namespace</span></span><br/>                | <span data-ttu-id="ce44f-125">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="ce44f-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="ce44f-126">MOF</span><span class="sxs-lookup"><span data-stu-id="ce44f-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce44f-127"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce44f-127"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce44f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ce44f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce44f-129"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce44f-129"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce44f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce44f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce44f-131">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="ce44f-131">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





