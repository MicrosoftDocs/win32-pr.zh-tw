---
description: 清除應用程式相容性快取。
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: BaseFlushAppcompatCache 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BaseFlushAppcompatCache
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-appcompat-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-appcompat-l1-1-1.dll
ms.openlocfilehash: 6118c78784bb96b9f25e008cd2221112eeb646f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110309"
---
# <a name="baseflushappcompatcache-function"></a><span data-ttu-id="ee7f2-103">BaseFlushAppcompatCache 函式</span><span class="sxs-lookup"><span data-stu-id="ee7f2-103">BaseFlushAppcompatCache function</span></span>

<span data-ttu-id="ee7f2-104">清除應用程式相容性快取。</span><span class="sxs-lookup"><span data-stu-id="ee7f2-104">Flushes the application compatibility cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee7f2-105">Syntax</span></span>


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a><span data-ttu-id="ee7f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee7f2-106">Parameters</span></span>

<span data-ttu-id="ee7f2-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="ee7f2-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee7f2-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee7f2-108">Return value</span></span>

<span data-ttu-id="ee7f2-109">如果成功，函數會傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ee7f2-109">The function returns **TRUE** if it succeeds and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee7f2-110">備註</span><span class="sxs-lookup"><span data-stu-id="ee7f2-110">Remarks</span></span>

<span data-ttu-id="ee7f2-111">呼叫端必須是系統管理員。</span><span class="sxs-lookup"><span data-stu-id="ee7f2-111">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee7f2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee7f2-112">Requirements</span></span>



| <span data-ttu-id="ee7f2-113">需求</span><span class="sxs-lookup"><span data-stu-id="ee7f2-113">Requirement</span></span> | <span data-ttu-id="ee7f2-114">值</span><span class="sxs-lookup"><span data-stu-id="ee7f2-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7f2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee7f2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ee7f2-116">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee7f2-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ee7f2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee7f2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ee7f2-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee7f2-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee7f2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ee7f2-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee7f2-120"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee7f2-120"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee7f2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee7f2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee7f2-122">**ShimFlushCache**</span><span class="sxs-lookup"><span data-stu-id="ee7f2-122">**ShimFlushCache**</span></span>](shimflushcache.md)
</dt> </dl>

 

 




