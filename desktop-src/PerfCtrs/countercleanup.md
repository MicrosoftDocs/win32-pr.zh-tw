---
description: 移除提供者註冊。
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: CounterCleanup 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969362"
---
# <a name="countercleanup-function"></a><span data-ttu-id="f9ae3-103">CounterCleanup 函式</span><span class="sxs-lookup"><span data-stu-id="f9ae3-103">CounterCleanup function</span></span>

<span data-ttu-id="f9ae3-104">移除提供者的註冊。</span><span class="sxs-lookup"><span data-stu-id="f9ae3-104">Removes the provider's registration.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9ae3-105">語法</span><span class="sxs-lookup"><span data-stu-id="f9ae3-105">Syntax</span></span>


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a><span data-ttu-id="f9ae3-106">參數</span><span class="sxs-lookup"><span data-stu-id="f9ae3-106">Parameters</span></span>

<span data-ttu-id="f9ae3-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="f9ae3-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9ae3-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9ae3-108">Return value</span></span>

<span data-ttu-id="f9ae3-109">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f9ae3-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9ae3-110">備註</span><span class="sxs-lookup"><span data-stu-id="f9ae3-110">Remarks</span></span>

<span data-ttu-id="f9ae3-111">您的提供者會呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="f9ae3-111">Your provider calls this function.</span></span> <span data-ttu-id="f9ae3-112">此函數會呼叫 [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) 函式，以移除提供者的註冊。</span><span class="sxs-lookup"><span data-stu-id="f9ae3-112">The function calls the [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) function to remove the provider's registration.</span></span>

<span data-ttu-id="f9ae3-113">當您指定 **-o** 引數時， [**CTRPP**](ctrpp.md)工具會產生這個內嵌函數。</span><span class="sxs-lookup"><span data-stu-id="f9ae3-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="f9ae3-114">如果您指定 **-prefix** 引數 (例如 **_prefix_CounterCleanup**，則函式的名稱會包含 *前置* 詞字串。</span><span class="sxs-lookup"><span data-stu-id="f9ae3-114">The function's name includes a *prefix* string if you specify the **-prefix** argument (for example, **_prefix_CounterCleanup**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9ae3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9ae3-115">Requirements</span></span>



| <span data-ttu-id="f9ae3-116">需求</span><span class="sxs-lookup"><span data-stu-id="f9ae3-116">Requirement</span></span> | <span data-ttu-id="f9ae3-117">值</span><span class="sxs-lookup"><span data-stu-id="f9ae3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f9ae3-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9ae3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9ae3-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9ae3-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f9ae3-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9ae3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9ae3-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9ae3-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




