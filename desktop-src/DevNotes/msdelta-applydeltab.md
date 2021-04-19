---
description: 使用以緩衝區形式提供的差異和來源 (，) 建立目標資料的新複本。 輸出資料會在 MSDelta 配置的緩衝區中傳回。
title: ApplyDeltaB 函式
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000920"
---
# <a name="applydeltab-function"></a><span data-ttu-id="ea3a9-104">ApplyDeltaB 函式</span><span class="sxs-lookup"><span data-stu-id="ea3a9-104">ApplyDeltaB function</span></span>

<span data-ttu-id="ea3a9-105">使用以緩衝區形式提供的差異和來源 (，) 建立目標資料的新複本。</span><span class="sxs-lookup"><span data-stu-id="ea3a9-105">Uses the delta and source (provided as buffers) to create a new copy of the target data.</span></span> <span data-ttu-id="ea3a9-106">輸出資料會在 MSDelta 配置的緩衝區中傳回。</span><span class="sxs-lookup"><span data-stu-id="ea3a9-106">The output data is returned in an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="ea3a9-107">完成此函式之後，您必須呼叫 [DeltaFree](msdelta-deltafree.md) 來釋放輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ea3a9-107">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

> [!NOTE]
> <span data-ttu-id="ea3a9-108">如果指定的 delta 是使用 [PatchAPI](patchapi.md)所建立，且已設定 [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) 旗標，則 MSDelta 會呼叫 PatchAPI 以套用差異。</span><span class="sxs-lookup"><span data-stu-id="ea3a9-108">If the specified delta was created using [PatchAPI](patchapi.md), and the [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) flag is set, MSDelta will call PatchAPI to apply the delta.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea3a9-109">語法</span><span class="sxs-lookup"><span data-stu-id="ea3a9-109">Syntax</span></span>

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a><span data-ttu-id="ea3a9-110">參數</span><span class="sxs-lookup"><span data-stu-id="ea3a9-110">Parameters</span></span>

<span data-ttu-id="ea3a9-111">*ApplyFlags*</span><span class="sxs-lookup"><span data-stu-id="ea3a9-111">*ApplyFlags*</span></span>

<span data-ttu-id="ea3a9-112">在請 [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) 或 [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags)。</span><span class="sxs-lookup"><span data-stu-id="ea3a9-112">[in] Either [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) or [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span></span>

<span data-ttu-id="ea3a9-113">*來源*</span><span class="sxs-lookup"><span data-stu-id="ea3a9-113">*Source*</span></span>

<span data-ttu-id="ea3a9-114">在 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構，包含包含來源資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="ea3a9-114">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="ea3a9-115">*差異*</span><span class="sxs-lookup"><span data-stu-id="ea3a9-115">*Delta*</span></span>

<span data-ttu-id="ea3a9-116">在包含差異資料之緩衝區指標的 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構。</span><span class="sxs-lookup"><span data-stu-id="ea3a9-116">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the delta data.</span></span>

<span data-ttu-id="ea3a9-117">*lpTarget*</span><span class="sxs-lookup"><span data-stu-id="ea3a9-117">*lpTarget*</span></span>

<span data-ttu-id="ea3a9-118">擴展要寫入目標的 [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="ea3a9-118">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the target is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea3a9-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea3a9-119">Return value</span></span>

<span data-ttu-id="ea3a9-120">如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ea3a9-120">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="ea3a9-121">當函數傳回 **FALSE** 時，您可以呼叫 [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 來取得對應的 Win32 系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ea3a9-121">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea3a9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea3a9-122">Requirements</span></span>

| <span data-ttu-id="ea3a9-123">需求</span><span class="sxs-lookup"><span data-stu-id="ea3a9-123">Requirement</span></span> | <span data-ttu-id="ea3a9-124">值</span><span class="sxs-lookup"><span data-stu-id="ea3a9-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3a9-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ea3a9-125">Header</span></span> | <span data-ttu-id="ea3a9-126">msdelta。h</span><span class="sxs-lookup"><span data-stu-id="ea3a9-126">msdelta.h</span></span> |
| <span data-ttu-id="ea3a9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ea3a9-127">DLL</span></span> | <span data-ttu-id="ea3a9-128">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="ea3a9-128">msdelta.dll</span></span> |
| <span data-ttu-id="ea3a9-129">Unicode</span><span class="sxs-lookup"><span data-stu-id="ea3a9-129">Unicode</span></span> | <span data-ttu-id="ea3a9-130">不適用</span><span class="sxs-lookup"><span data-stu-id="ea3a9-130">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="ea3a9-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea3a9-131">See also</span></span>

[<span data-ttu-id="ea3a9-132">MSDelta</span><span class="sxs-lookup"><span data-stu-id="ea3a9-132">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="ea3a9-133">DeltaFree</span><span class="sxs-lookup"><span data-stu-id="ea3a9-133">DeltaFree</span></span>](msdelta-deltafree.md)
