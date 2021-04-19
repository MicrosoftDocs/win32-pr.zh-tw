---
description: IsValidDevmode 函數會驗證 DEVMODE 結構的內容是否有效。
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: 'IsValidDevmode 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975300"
---
# <a name="isvaliddevmode-function"></a><span data-ttu-id="a20dc-103">IsValidDevmode 函式</span><span class="sxs-lookup"><span data-stu-id="a20dc-103">IsValidDevmode function</span></span>

<span data-ttu-id="a20dc-104">**IsValidDevmode** 函數會驗證 DEVMODE 結構的內容是否有效。</span><span class="sxs-lookup"><span data-stu-id="a20dc-104">The **IsValidDevmode** function verifies that the contents of a DEVMODE structure are valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="a20dc-105">語法</span><span class="sxs-lookup"><span data-stu-id="a20dc-105">Syntax</span></span>


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a><span data-ttu-id="a20dc-106">參數</span><span class="sxs-lookup"><span data-stu-id="a20dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a20dc-107">*pDevmode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a20dc-107">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a20dc-108">要驗證的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 指標。</span><span class="sxs-lookup"><span data-stu-id="a20dc-108">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to validate.</span></span>

</dd> <dt>

<span data-ttu-id="a20dc-109">*DevmodeSize*</span><span class="sxs-lookup"><span data-stu-id="a20dc-109">*DevmodeSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a20dc-110">輸入位元組緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a20dc-110">The size in bytes of the input byte buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a20dc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a20dc-111">Return value</span></span>

<span data-ttu-id="a20dc-112">如果 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)在結構上有效，**則為 TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a20dc-112">**TRUE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is structurally valid.</span></span> <span data-ttu-id="a20dc-113">如果發現次要錯誤，函數會修正這些錯誤並傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a20dc-113">If minor errors are found the function will fix them and return **TRUE**.</span></span>

<span data-ttu-id="a20dc-114">如果 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)有一或多個明顯的結構化問題，則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a20dc-114">**FALSE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) has one or more significant structural problems.</span></span> <span data-ttu-id="a20dc-115">例如，其 **dmSize** 成員未對齊，或指定的緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="a20dc-115">For example, its **dmSize** member is misaligned or specifies a buffer that is too small.</span></span> <span data-ttu-id="a20dc-116">此外，如果 **pDevmode** 為 **Null**，則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a20dc-116">Also, **FALSE** if **pDevmode** is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a20dc-117">備註</span><span class="sxs-lookup"><span data-stu-id="a20dc-117">Remarks</span></span>

<span data-ttu-id="a20dc-118">不會檢查 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 的私用印表機驅動程式欄位，只會檢查公用欄位。</span><span class="sxs-lookup"><span data-stu-id="a20dc-118">No private printer driver fields of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) are checked, only the public fields.</span></span>

<span data-ttu-id="a20dc-119"> + 只有當呼叫者可以保證輸入緩衝區大小至少為該大小時，才應該使用 dmSize **dmDriverExtra** 進行 **DevmodeSize** 。</span><span class="sxs-lookup"><span data-stu-id="a20dc-119">Callers should use **dmSize**+**dmDriverExtra** for **DevmodeSize** only if they can guarantee that the input buffer size is at least that big.</span></span> <span data-ttu-id="a20dc-120">由於 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 通常是不受信任的資料，因此 **dmSize** 和 **dmDriverExtra** 位移之輸入緩衝區中的值也不受信任。</span><span class="sxs-lookup"><span data-stu-id="a20dc-120">Since the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is generally untrusted data, the values that are in the input buffer at the **dmSize** and **dmDriverExtra** offsets are also untrusted.</span></span>

<span data-ttu-id="a20dc-121">此函式可在 Least-Privileged 使用者帳戶 (LUA) 內容中執行。</span><span class="sxs-lookup"><span data-stu-id="a20dc-121">This function is executable in Least-Privileged User Account (LUA) context.</span></span>

## <a name="requirements"></a><span data-ttu-id="a20dc-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a20dc-122">Requirements</span></span>



| <span data-ttu-id="a20dc-123">需求</span><span class="sxs-lookup"><span data-stu-id="a20dc-123">Requirement</span></span> | <span data-ttu-id="a20dc-124">值</span><span class="sxs-lookup"><span data-stu-id="a20dc-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a20dc-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a20dc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a20dc-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a20dc-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a20dc-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a20dc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a20dc-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a20dc-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a20dc-129">標頭</span><span class="sxs-lookup"><span data-stu-id="a20dc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a20dc-130"><dt>Winspool.drv。h</dt></span><span class="sxs-lookup"><span data-stu-id="a20dc-130"><dt>Winspool.h</dt></span></span> </dl>   |
| <span data-ttu-id="a20dc-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="a20dc-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="a20dc-132"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a20dc-132"><dt>Winspool.lib</dt></span></span> </dl> |
| <span data-ttu-id="a20dc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a20dc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a20dc-134"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="a20dc-134"><dt>Winspool.drv</dt></span></span> </dl> |
| <span data-ttu-id="a20dc-135">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a20dc-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a20dc-136">**IsValidDevmodeW** (Unicode) 和 **IsValidDevmodeA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a20dc-136">**IsValidDevmodeW** (Unicode) and **IsValidDevmodeA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a20dc-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a20dc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a20dc-138">列印</span><span class="sxs-lookup"><span data-stu-id="a20dc-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a20dc-139">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="a20dc-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a20dc-140">**版**</span><span class="sxs-lookup"><span data-stu-id="a20dc-140">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




