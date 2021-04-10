---
description: WiaAddDevice 函式會叫用掃描器和相機安裝精靈 UI。 它相當於執行 &\# 0034; rundll32.exe sti \_ci.dll AddDevice&\# 0034; 從命令提示字元。
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: 'WiaAddDevice 函式 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690552"
---
# <a name="wiaadddevice-function"></a><span data-ttu-id="fd876-104">WiaAddDevice 函式</span><span class="sxs-lookup"><span data-stu-id="fd876-104">WiaAddDevice function</span></span>

<span data-ttu-id="fd876-105">**WiaAddDevice** 函式會叫用掃描器和相機安裝精靈 UI。</span><span class="sxs-lookup"><span data-stu-id="fd876-105">The **WiaAddDevice** function invokes the Scanner and Camera Installation Wizard UI.</span></span> <span data-ttu-id="fd876-106">這相當於從命令提示字元執行 "rundll32.exe sti \_ci.dll AddDevice"。</span><span class="sxs-lookup"><span data-stu-id="fd876-106">It is equivalent to running "rundll32.exe sti\_ci.dll AddDevice" from the command prompt.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd876-107">語法</span><span class="sxs-lookup"><span data-stu-id="fd876-107">Syntax</span></span>


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a><span data-ttu-id="fd876-108">參數</span><span class="sxs-lookup"><span data-stu-id="fd876-108">Parameters</span></span>

<span data-ttu-id="fd876-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="fd876-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd876-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd876-110">Return value</span></span>

<span data-ttu-id="fd876-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fd876-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd876-112">備註</span><span class="sxs-lookup"><span data-stu-id="fd876-112">Remarks</span></span>

<span data-ttu-id="fd876-113">此函式應以系統管理員認證來呼叫。</span><span class="sxs-lookup"><span data-stu-id="fd876-113">This function should be called with administrator credentials.</span></span> <span data-ttu-id="fd876-114">在 [使用者帳戶控制] 下執行 (LUA) 時，應提高處理常式的許可權。</span><span class="sxs-lookup"><span data-stu-id="fd876-114">When running under User Account Control (LUA), the process should be elevated.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd876-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd876-115">Requirements</span></span>



| <span data-ttu-id="fd876-116">需求</span><span class="sxs-lookup"><span data-stu-id="fd876-116">Requirement</span></span> | <span data-ttu-id="fd876-117">值</span><span class="sxs-lookup"><span data-stu-id="fd876-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd876-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd876-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fd876-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd876-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fd876-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd876-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fd876-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd876-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fd876-122">標頭</span><span class="sxs-lookup"><span data-stu-id="fd876-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd876-123"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="fd876-123"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="fd876-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="fd876-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd876-125"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd876-125"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd876-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd876-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd876-127">**InstallWiaDevice**</span><span class="sxs-lookup"><span data-stu-id="fd876-127">**InstallWiaDevice**</span></span>](-wia-installwiadevice.md)
</dt> </dl>

 

 




