---
description: 如果呼叫程式是在載入器標注中叫用，則此函式會強制結束通話程式。 否則，它不會有任何作用。
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: LdrFastFailInLoaderCallout 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986175"
---
# <a name="ldrfastfailinloadercallout-function"></a><span data-ttu-id="5052a-104">LdrFastFailInLoaderCallout 函式</span><span class="sxs-lookup"><span data-stu-id="5052a-104">LdrFastFailInLoaderCallout function</span></span>

<span data-ttu-id="5052a-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="5052a-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5052a-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="5052a-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5052a-107">如果呼叫程式是在載入器標注中叫用，則此函式會強制結束通話程式。</span><span class="sxs-lookup"><span data-stu-id="5052a-107">This function forcefully terminates the calling program if it is invoked inside a loader callout.</span></span> <span data-ttu-id="5052a-108">否則，它不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="5052a-108">Otherwise, it has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="5052a-109">語法</span><span class="sxs-lookup"><span data-stu-id="5052a-109">Syntax</span></span>


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a><span data-ttu-id="5052a-110">參數</span><span class="sxs-lookup"><span data-stu-id="5052a-110">Parameters</span></span>

<span data-ttu-id="5052a-111">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="5052a-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5052a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5052a-112">Return value</span></span>

<span data-ttu-id="5052a-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5052a-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5052a-114">備註</span><span class="sxs-lookup"><span data-stu-id="5052a-114">Remarks</span></span>

<span data-ttu-id="5052a-115">此常式不會攔截所有可能的鎖死案例;載入器標注中的執行緒可能會取得鎖定，而載入器標注以外的某個執行緒則會保留相同的鎖定，並呼叫載入器。</span><span class="sxs-lookup"><span data-stu-id="5052a-115">This routine does not catch all potential deadlock cases; it is possible for a thread inside a loader callout to acquire a lock while some thread outside a loader callout holds the same lock and makes a call into the loader.</span></span> <span data-ttu-id="5052a-116">換句話說，載入器鎖定和用戶端鎖定之間可能會有鎖定順序反轉。</span><span class="sxs-lookup"><span data-stu-id="5052a-116">In other words, there can be a lock order inversion between the loader lock and a client lock.</span></span>

## <a name="requirements"></a><span data-ttu-id="5052a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5052a-117">Requirements</span></span>



| <span data-ttu-id="5052a-118">需求</span><span class="sxs-lookup"><span data-stu-id="5052a-118">Requirement</span></span> | <span data-ttu-id="5052a-119">值</span><span class="sxs-lookup"><span data-stu-id="5052a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5052a-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="5052a-120">Library</span></span><br/> | <dl> <span data-ttu-id="5052a-121"><dt>Ntdll.dll .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5052a-121"><dt>NTDll.lib</dt></span></span> </dl> |
| <span data-ttu-id="5052a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5052a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5052a-123"><dt>NTDll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5052a-123"><dt>NTDll.dll</dt></span></span> </dl> |



 

 




