---
description: 在以緩衝區形式提供的來源和目標 (之間建立差異) 並傳回輸出 delta 作為 MSDelta 配置的緩衝區。
title: CreateDeltaB 函式
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977403"
---
# <a name="createdeltab-function"></a><span data-ttu-id="39528-103">CreateDeltaB 函式</span><span class="sxs-lookup"><span data-stu-id="39528-103">CreateDeltaB function</span></span>

<span data-ttu-id="39528-104">在以緩衝區形式提供的來源和目標 (之間建立差異) 並傳回輸出 delta 作為 MSDelta 配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="39528-104">Creates a delta between the source and target (provided as buffers) and returns the output delta as an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="39528-105">完成此函式之後，您必須呼叫 [DeltaFree](msdelta-deltafree.md) 來釋放輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="39528-105">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="39528-106">語法</span><span class="sxs-lookup"><span data-stu-id="39528-106">Syntax</span></span>

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a><span data-ttu-id="39528-107">參數</span><span class="sxs-lookup"><span data-stu-id="39528-107">Parameters</span></span>

<span data-ttu-id="39528-108">*FileTypeSet*</span><span class="sxs-lookup"><span data-stu-id="39528-108">*FileTypeSet*</span></span>

<span data-ttu-id="39528-109">在 [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) 值，表示要用於建立進程的檔案類型集。</span><span class="sxs-lookup"><span data-stu-id="39528-109">[in] The [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) value that indicates the file type set to be used for the create process.</span></span>

<span data-ttu-id="39528-110">*SetFlags*</span><span class="sxs-lookup"><span data-stu-id="39528-110">*SetFlags*</span></span>

<span data-ttu-id="39528-111">在一或多個 [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) 值，這個值會指定要在建立進程期間使用的旗標，以及預設旗標。</span><span class="sxs-lookup"><span data-stu-id="39528-111">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the flags to be used during the create process, in addition to the default flags.</span></span>

<span data-ttu-id="39528-112">*ResetFlags*</span><span class="sxs-lookup"><span data-stu-id="39528-112">*ResetFlags*</span></span>

<span data-ttu-id="39528-113">在一或多個 [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) 值，這個值會指定要在建立進程期間重設的預設旗標。</span><span class="sxs-lookup"><span data-stu-id="39528-113">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the default flags to be reset during the create process.</span></span>

<span data-ttu-id="39528-114">*來源*</span><span class="sxs-lookup"><span data-stu-id="39528-114">*Source*</span></span>

<span data-ttu-id="39528-115">在 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構，包含包含來源資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="39528-115">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="39528-116">*Target*</span><span class="sxs-lookup"><span data-stu-id="39528-116">*Target*</span></span>

<span data-ttu-id="39528-117">在包含目標資料之緩衝區指標的 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構。</span><span class="sxs-lookup"><span data-stu-id="39528-117">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the target data.</span></span>

<span data-ttu-id="39528-118">*SourceOptions*</span><span class="sxs-lookup"><span data-stu-id="39528-118">*SourceOptions*</span></span>

<span data-ttu-id="39528-119">[in] 保留。</span><span class="sxs-lookup"><span data-stu-id="39528-119">[in] Reserved.</span></span> <span data-ttu-id="39528-120">傳遞 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構，並將 *可編輯* 的設定為 **FALSE**、 *LpStart* 設定為 **Null** ，並將 *uSize* 設定為0。</span><span class="sxs-lookup"><span data-stu-id="39528-120">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="39528-121">*TargetOptions*</span><span class="sxs-lookup"><span data-stu-id="39528-121">*TargetOptions*</span></span>

<span data-ttu-id="39528-122">[in] 保留。</span><span class="sxs-lookup"><span data-stu-id="39528-122">[in] Reserved.</span></span> <span data-ttu-id="39528-123">傳遞 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構，並將 *可編輯* 的設定為 **FALSE**、 *LpStart* 設定為 **Null** ，並將 *uSize* 設定為0。</span><span class="sxs-lookup"><span data-stu-id="39528-123">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="39528-124">*GlobalOptions*</span><span class="sxs-lookup"><span data-stu-id="39528-124">*GlobalOptions*</span></span>

<span data-ttu-id="39528-125">[in] 保留。</span><span class="sxs-lookup"><span data-stu-id="39528-125">[in] Reserved.</span></span> <span data-ttu-id="39528-126">傳遞 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構，並將 *LpStart* 設定為 **Null** ，並將 *uSize* 設定為0。</span><span class="sxs-lookup"><span data-stu-id="39528-126">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="39528-127">*lpTargetFileTime*</span><span class="sxs-lookup"><span data-stu-id="39528-127">*lpTargetFileTime*</span></span>

<span data-ttu-id="39528-128">在套用 delta 之後，于目標檔案上設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="39528-128">[in] The time stamp set on the target file after delta apply.</span></span> <span data-ttu-id="39528-129">如果是 **Null**，則目標時間戳記將會是建立進程期間的目前時間。</span><span class="sxs-lookup"><span data-stu-id="39528-129">If **NULL**, the target timestamp will be the current time during the create process.</span></span>

<span data-ttu-id="39528-130">*HashAlgId*</span><span class="sxs-lookup"><span data-stu-id="39528-130">*HashAlgId*</span></span>

<span data-ttu-id="39528-131">在用來產生目標特徵標記的演算法 ALG_ID。</span><span class="sxs-lookup"><span data-stu-id="39528-131">[in] ALG_ID of the algorithm to be used to generate the target signature.</span></span> <span data-ttu-id="39528-132">某些特殊值為：</span><span class="sxs-lookup"><span data-stu-id="39528-132">Some special values are:</span></span>

- <span data-ttu-id="39528-133">0 = 沒有簽章</span><span class="sxs-lookup"><span data-stu-id="39528-133">0 = No signature</span></span>
- <span data-ttu-id="39528-134">32 = msdelta.dll 中定義的32位 CRC</span><span class="sxs-lookup"><span data-stu-id="39528-134">32 = 32-bit CRC defined in msdelta.dll</span></span>

<span data-ttu-id="39528-135">*lpDelta*</span><span class="sxs-lookup"><span data-stu-id="39528-135">*lpDelta*</span></span>

<span data-ttu-id="39528-136">擴展要寫入差異的 [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="39528-136">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the delta is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="39528-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="39528-137">Return value</span></span>

<span data-ttu-id="39528-138">如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="39528-138">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="39528-139">當函數傳回 **FALSE** 時，您可以呼叫 [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 來取得對應的 Win32 系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="39528-139">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="39528-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="39528-140">Requirements</span></span>

| <span data-ttu-id="39528-141">需求</span><span class="sxs-lookup"><span data-stu-id="39528-141">Requirement</span></span> | <span data-ttu-id="39528-142">值</span><span class="sxs-lookup"><span data-stu-id="39528-142">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39528-143">標頭</span><span class="sxs-lookup"><span data-stu-id="39528-143">Header</span></span> | <span data-ttu-id="39528-144">msdelta。h</span><span class="sxs-lookup"><span data-stu-id="39528-144">msdelta.h</span></span> |
| <span data-ttu-id="39528-145">DLL</span><span class="sxs-lookup"><span data-stu-id="39528-145">DLL</span></span> | <span data-ttu-id="39528-146">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="39528-146">msdelta.dll</span></span> |
| <span data-ttu-id="39528-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="39528-147">Unicode</span></span> | <span data-ttu-id="39528-148">不適用</span><span class="sxs-lookup"><span data-stu-id="39528-148">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="39528-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39528-149">See also</span></span>

[<span data-ttu-id="39528-150">MSDelta</span><span class="sxs-lookup"><span data-stu-id="39528-150">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="39528-151">DeltaFree</span><span class="sxs-lookup"><span data-stu-id="39528-151">DeltaFree</span></span>](msdelta-deltafree.md)
