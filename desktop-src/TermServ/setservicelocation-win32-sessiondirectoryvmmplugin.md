---
title: Win32_SessionDirectoryVMMPlugin 類別的 SetServiceLocation 方法
description: 設定外掛程式的服務位置。
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- SetServiceLocation 方法遠端桌面服務
- SetServiceLocation 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，SetServiceLocation 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508832"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="11eac-106">Win32 SessionDirectoryVMMPlugin 類別的 SetServiceLocation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="11eac-106">SetServiceLocation method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="11eac-107">設定外掛程式的服務位置。</span><span class="sxs-lookup"><span data-stu-id="11eac-107">Sets the service location for the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="11eac-108">語法</span><span class="sxs-lookup"><span data-stu-id="11eac-108">Syntax</span></span>


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="11eac-109">參數</span><span class="sxs-lookup"><span data-stu-id="11eac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11eac-110">*sServiceLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11eac-110">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11eac-111">外掛程式應聯絡的服務位置。</span><span class="sxs-lookup"><span data-stu-id="11eac-111">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11eac-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="11eac-112">Return value</span></span>

<span data-ttu-id="11eac-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="11eac-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="11eac-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="11eac-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="11eac-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="11eac-115">Requirements</span></span>



| <span data-ttu-id="11eac-116">需求</span><span class="sxs-lookup"><span data-stu-id="11eac-116">Requirement</span></span> | <span data-ttu-id="11eac-117">值</span><span class="sxs-lookup"><span data-stu-id="11eac-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11eac-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11eac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="11eac-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="11eac-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="11eac-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11eac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="11eac-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="11eac-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="11eac-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="11eac-122">Namespace</span></span><br/>                | <span data-ttu-id="11eac-123">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="11eac-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="11eac-124">MOF</span><span class="sxs-lookup"><span data-stu-id="11eac-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11eac-125"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="11eac-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="11eac-126">DLL</span><span class="sxs-lookup"><span data-stu-id="11eac-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11eac-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11eac-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11eac-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11eac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11eac-129">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="11eac-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





