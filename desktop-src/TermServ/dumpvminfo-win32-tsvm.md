---
title: Win32_TSVm 類別的 DumpVmInfo 方法
description: 此成員適用于內部測試，不應在您的程式碼中使用。
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- DumpVmInfo 方法遠端桌面服務
- DumpVmInfo 方法遠端桌面服務，Win32_TSVm 類別
- Win32_TSVm 類別遠端桌面服務，DumpVmInfo 方法
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d02a1d4ea07bd045da2850a4d7ccb0069977a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686600"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a><span data-ttu-id="69852-106">Win32 TSVm 類別的 DumpVmInfo 方法 \_</span><span class="sxs-lookup"><span data-stu-id="69852-106">DumpVmInfo method of the Win32\_TSVm class</span></span>

<span data-ttu-id="69852-107">此成員適用于內部測試，不應在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="69852-107">This member is for internal testing purposes, and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="69852-108">語法</span><span class="sxs-lookup"><span data-stu-id="69852-108">Syntax</span></span>


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a><span data-ttu-id="69852-109">參數</span><span class="sxs-lookup"><span data-stu-id="69852-109">Parameters</span></span>

<span data-ttu-id="69852-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="69852-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69852-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="69852-111">Return value</span></span>

<span data-ttu-id="69852-112">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="69852-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="69852-113">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="69852-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="69852-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="69852-114">Requirements</span></span>



| <span data-ttu-id="69852-115">需求</span><span class="sxs-lookup"><span data-stu-id="69852-115">Requirement</span></span> | <span data-ttu-id="69852-116">值</span><span class="sxs-lookup"><span data-stu-id="69852-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="69852-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69852-117">Minimum supported client</span></span><br/> | <span data-ttu-id="69852-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="69852-118">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="69852-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69852-119">Minimum supported server</span></span><br/> | <span data-ttu-id="69852-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69852-120">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="69852-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="69852-121">Namespace</span></span><br/>                | <span data-ttu-id="69852-122">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="69852-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="69852-123">MOF</span><span class="sxs-lookup"><span data-stu-id="69852-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69852-124"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="69852-124"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="69852-125">DLL</span><span class="sxs-lookup"><span data-stu-id="69852-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69852-126"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69852-126"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69852-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69852-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69852-128">**Win32 \_ TSVm**</span><span class="sxs-lookup"><span data-stu-id="69852-128">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





