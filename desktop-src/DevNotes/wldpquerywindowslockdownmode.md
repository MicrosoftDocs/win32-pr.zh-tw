---
description: 抓取目前的 Windows 安全模式。 Windows 可以處於鎖定模式、已解除鎖定的一般模式或試用模式。
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: 'WldpQueryWindowsLockdownMode 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190986"
---
# <a name="wldpquerywindowslockdownmode-function"></a><span data-ttu-id="d2677-104">WldpQueryWindowsLockdownMode 函式</span><span class="sxs-lookup"><span data-stu-id="d2677-104">WldpQueryWindowsLockdownMode function</span></span>

<span data-ttu-id="d2677-105">抓取目前的 Windows 安全模式。</span><span class="sxs-lookup"><span data-stu-id="d2677-105">Retrieves the current Windows secure mode.</span></span> <span data-ttu-id="d2677-106">Windows 可以處於鎖定模式、已解除鎖定的一般模式或試用模式。</span><span class="sxs-lookup"><span data-stu-id="d2677-106">Windows can be in locked mode, unlocked normal mode, or trial mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2677-107">語法</span><span class="sxs-lookup"><span data-stu-id="d2677-107">Syntax</span></span>


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a><span data-ttu-id="d2677-108">參數</span><span class="sxs-lookup"><span data-stu-id="d2677-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2677-109">*lockdownMode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d2677-109">*lockdownMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2677-110">成功時，會傳回 [**PWLDP 的 \_ WINDOWS \_ 鎖定 \_ 模式**](wldp-windows-lockdown-mode.md) ，指出目前 Windows 10 裝置的安全模式。</span><span class="sxs-lookup"><span data-stu-id="d2677-110">On success, returns a [**PWLDP\_WINDOWS\_LOCKDOWN\_MODE**](wldp-windows-lockdown-mode.md) that indicates the secure mode for the current Windows 10 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2677-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2677-111">Return value</span></span>

<span data-ttu-id="d2677-112">**如果成功，則 \_ 此** 方法會傳回，否則會傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="d2677-112">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2677-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2677-113">Requirements</span></span>



| <span data-ttu-id="d2677-114">需求</span><span class="sxs-lookup"><span data-stu-id="d2677-114">Requirement</span></span> | <span data-ttu-id="d2677-115">值</span><span class="sxs-lookup"><span data-stu-id="d2677-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d2677-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2677-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d2677-117">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2677-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d2677-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2677-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d2677-119">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2677-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d2677-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d2677-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2677-121"><dt>Wldp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2677-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2677-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d2677-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2677-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2677-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




