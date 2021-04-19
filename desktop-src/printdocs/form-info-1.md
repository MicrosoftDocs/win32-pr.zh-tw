---
description: FORM_INFO_1 結構包含列印表單的相關資訊。 此資訊包括列印表單來源、其名稱、其尺寸，以及其可列印範圍的尺寸。
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: 'FORM_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987009"
---
# <a name="form_info_1-structure"></a><span data-ttu-id="ed124-104">FORM_INFO_1 結構</span><span class="sxs-lookup"><span data-stu-id="ed124-104">FORM_INFO_1 structure</span></span>

<span data-ttu-id="ed124-105">**FORM_INFO_1** 結構包含列印表單的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ed124-105">The **FORM_INFO_1** structure contains information about a print form.</span></span> <span data-ttu-id="ed124-106">此資訊包括列印表單的原始來源、其名稱、其尺寸，以及其可列印範圍的尺寸。</span><span class="sxs-lookup"><span data-stu-id="ed124-106">The information includes the print form's origin, its name, its dimensions, and the dimensions of its printable area.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed124-107">語法</span><span class="sxs-lookup"><span data-stu-id="ed124-107">Syntax</span></span>


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a><span data-ttu-id="ed124-108">成員</span><span class="sxs-lookup"><span data-stu-id="ed124-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed124-109">**旗標**</span><span class="sxs-lookup"><span data-stu-id="ed124-109">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ed124-110">表單內容。</span><span class="sxs-lookup"><span data-stu-id="ed124-110">The form properties.</span></span> <span data-ttu-id="ed124-111">以下是定義的值。</span><span class="sxs-lookup"><span data-stu-id="ed124-111">The following values are defined.</span></span>



| <span data-ttu-id="ed124-112">值</span><span class="sxs-lookup"><span data-stu-id="ed124-112">Value</span></span>         | <span data-ttu-id="ed124-113">意義</span><span class="sxs-lookup"><span data-stu-id="ed124-113">Meaning</span></span>                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed124-114">FORM_USER</span><span class="sxs-lookup"><span data-stu-id="ed124-114">FORM_USER</span></span>    | <span data-ttu-id="ed124-115">如果設定此位旗標，使用者就會定義表單。</span><span class="sxs-lookup"><span data-stu-id="ed124-115">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="ed124-116">具有此旗標集合的表單是在登錄中定義。</span><span class="sxs-lookup"><span data-stu-id="ed124-116">Forms with this flag set are defined in the registry.</span></span>        |
| <span data-ttu-id="ed124-117">FORM_BUILTIN</span><span class="sxs-lookup"><span data-stu-id="ed124-117">FORM_BUILTIN</span></span> | <span data-ttu-id="ed124-118">如果設定此位旗標，則表單是多工緩衝處理器的一部分。</span><span class="sxs-lookup"><span data-stu-id="ed124-118">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="ed124-119">具有此旗標設定的表單定義不會出現在登錄中。</span><span class="sxs-lookup"><span data-stu-id="ed124-119">Form definitions with this flag set do not appear in the registry.</span></span> |
| <span data-ttu-id="ed124-120">FORM_PRINTER</span><span class="sxs-lookup"><span data-stu-id="ed124-120">FORM_PRINTER</span></span> | <span data-ttu-id="ed124-121">如果設定了這個位旗標，表單就會與特定的印表機相關聯，而且其定義會出現在登錄中。</span><span class="sxs-lookup"><span data-stu-id="ed124-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>          |



 

</dd> <dt>

<span data-ttu-id="ed124-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="ed124-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="ed124-123">指定表單名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="ed124-123">Pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="ed124-124">表單名稱不能超過31個字元。</span><span class="sxs-lookup"><span data-stu-id="ed124-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="ed124-125">**大小**</span><span class="sxs-lookup"><span data-stu-id="ed124-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="ed124-126">表單的寬度和高度（以千為單位）。</span><span class="sxs-lookup"><span data-stu-id="ed124-126">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> <dt>

<span data-ttu-id="ed124-127">**ImageableArea**</span><span class="sxs-lookup"><span data-stu-id="ed124-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="ed124-128">表單的寬度和高度（以千為單位）。</span><span class="sxs-lookup"><span data-stu-id="ed124-128">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed124-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed124-129">Requirements</span></span>



| <span data-ttu-id="ed124-130">需求</span><span class="sxs-lookup"><span data-stu-id="ed124-130">Requirement</span></span> | <span data-ttu-id="ed124-131">值</span><span class="sxs-lookup"><span data-stu-id="ed124-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed124-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed124-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ed124-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed124-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ed124-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed124-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ed124-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed124-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ed124-136">標頭</span><span class="sxs-lookup"><span data-stu-id="ed124-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed124-137"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ed124-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ed124-138">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="ed124-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ed124-139">**_FORM_INFO_1W** (Unicode) 和 **_FORM_INFO_1A** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="ed124-139">**_FORM_INFO_1W** (Unicode) and **_FORM_INFO_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="ed124-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed124-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed124-141">列印</span><span class="sxs-lookup"><span data-stu-id="ed124-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ed124-142">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="ed124-142">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ed124-143">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="ed124-143">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="ed124-144">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="ed124-144">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="ed124-145">**SetForm**</span><span class="sxs-lookup"><span data-stu-id="ed124-145">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




