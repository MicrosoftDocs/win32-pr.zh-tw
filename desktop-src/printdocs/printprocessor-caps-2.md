---
description: 代表印表機功能資訊。
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: 'PRINTPROCESSOR_CAPS_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984643"
---
# <a name="printprocessor_caps_2-structure"></a><span data-ttu-id="10716-103">PRINTPROCESSOR \_ CAPS \_ 2 結構</span><span class="sxs-lookup"><span data-stu-id="10716-103">PRINTPROCESSOR\_CAPS\_2 structure</span></span>

<span data-ttu-id="10716-104">代表印表機功能資訊。</span><span class="sxs-lookup"><span data-stu-id="10716-104">Represents printer capability information.</span></span>

## <a name="syntax"></a><span data-ttu-id="10716-105">語法</span><span class="sxs-lookup"><span data-stu-id="10716-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a><span data-ttu-id="10716-106">成員</span><span class="sxs-lookup"><span data-stu-id="10716-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="10716-107">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="10716-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="10716-108">值，指出結構的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="10716-108">A value that indicates the structure's version number.</span></span>

</dd> <dt>

<span data-ttu-id="10716-109">**dwNupOptions**</span><span class="sxs-lookup"><span data-stu-id="10716-109">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="10716-110">位元遮罩，代表印表機可在實體工作表的一端列印的各種檔頁面數目。</span><span class="sxs-lookup"><span data-stu-id="10716-110">A bit mask representing the various numbers of document pages the printer can print on a single side of a physical sheet.</span></span> <span data-ttu-id="10716-111">最不重要的位代表每一端的一個檔頁面，下一個位代表每一端的2個檔頁面等等。</span><span class="sxs-lookup"><span data-stu-id="10716-111">The least significant bit represents one document page per side, the next bit represents 2 document pages per side, and so on.</span></span> <span data-ttu-id="10716-112">例如，0x0000810B 指出印表機每個實體端支援1、2、4、9和16份檔頁面。</span><span class="sxs-lookup"><span data-stu-id="10716-112">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical side.</span></span>

</dd> <dt>

<span data-ttu-id="10716-113">**dwPageOrderFlags**</span><span class="sxs-lookup"><span data-stu-id="10716-113">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="10716-114">旗標值，指出列印頁面的順序。</span><span class="sxs-lookup"><span data-stu-id="10716-114">A flag value that indicates the order in which pages will be printed.</span></span> <span data-ttu-id="10716-115">它可以是 **一般 \_ 列印**、 **反向 \_ 列印** 或 **手冊 \_ 列印**。</span><span class="sxs-lookup"><span data-stu-id="10716-115">It can be **NORMAL\_PRINT**, **REVERSE\_PRINT**, or **BOOKLET\_PRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="10716-116">**dwNumberOfCopies**</span><span class="sxs-lookup"><span data-stu-id="10716-116">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="10716-117">印表機可以處理的最大複本數目。</span><span class="sxs-lookup"><span data-stu-id="10716-117">The maximum number of copies the printer can handle.</span></span>

</dd> <dt>

<span data-ttu-id="10716-118">**dwNupDirectionCaps**</span><span class="sxs-lookup"><span data-stu-id="10716-118">**dwNupDirectionCaps**</span></span>
</dt> <dd>

<span data-ttu-id="10716-119">當多個檔頁面列印在紙張紙的同一側時，可使用的模式。</span><span class="sxs-lookup"><span data-stu-id="10716-119">The available patterns when multiple document pages are printed on the same side of a sheet of paper.</span></span> <span data-ttu-id="10716-120">可能的旗標如下：</span><span class="sxs-lookup"><span data-stu-id="10716-120">The possible flags are the following:</span></span>



| <span data-ttu-id="10716-121">值</span><span class="sxs-lookup"><span data-stu-id="10716-121">Value</span></span>                     | <span data-ttu-id="10716-122">意義</span><span class="sxs-lookup"><span data-stu-id="10716-122">Meaning</span></span>                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10716-123">向 \_ \_ 下 PPCAPS \_</span><span class="sxs-lookup"><span data-stu-id="10716-123">PPCAPS\_RIGHT\_THEN\_DOWN</span></span> | <span data-ttu-id="10716-124">頁面會由右至左顯示于資料列中，每個後續的資料列在其前置項下方。</span><span class="sxs-lookup"><span data-stu-id="10716-124">Pages appear in rows from right to left, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="10716-125">\_向下 PPCAPS 到 \_ \_ 右邊</span><span class="sxs-lookup"><span data-stu-id="10716-125">PPCAPS\_DOWN\_THEN\_RIGHT</span></span> | <span data-ttu-id="10716-126">頁面會顯示在資料行中，從上到下，每個後續的資料行都在其前置項右邊。</span><span class="sxs-lookup"><span data-stu-id="10716-126">Pages appear in columns from top to bottom, each subsequent column to the right of its predecessor.</span></span> |
| <span data-ttu-id="10716-127">\_向 \_ \_ 下 PPCAPS</span><span class="sxs-lookup"><span data-stu-id="10716-127">PPCAPS\_LEFT\_THEN\_DOWN</span></span>  | <span data-ttu-id="10716-128">頁面會從左至右出現在資料列中，每個後續的資料列在其前置項下方。</span><span class="sxs-lookup"><span data-stu-id="10716-128">Pages appear in rows from left to right, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="10716-129">\_向下 PPCAPS 至 \_ \_ 左方</span><span class="sxs-lookup"><span data-stu-id="10716-129">PPCAPS\_DOWN\_THEN\_LEFT</span></span>  | <span data-ttu-id="10716-130">頁面會出現在從上到下的資料行中，每個後續的資料行都會出現在其前身的左邊。</span><span class="sxs-lookup"><span data-stu-id="10716-130">Pages appear in columns from top to bottom, each subsequent column to the left of its predecessor.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="10716-131">**dwNupBorderCaps**</span><span class="sxs-lookup"><span data-stu-id="10716-131">**dwNupBorderCaps**</span></span>
</dt> <dd>

<span data-ttu-id="10716-132">只能是 PPCAPS \_ 框線 \_ 列印，表示當多個檔頁面列印在實體工作表的一側時，可以告知印表機是否要在每個檔頁面的可成像區域周圍列印框線。</span><span class="sxs-lookup"><span data-stu-id="10716-132">Can be only PPCAPS\_BORDER\_PRINT, indicating that, when multiple document pages are being printed on a single side of a physical sheet, the printer can be told whether or not to print a border around the imageable area of each document page.</span></span>

</dd> <dt>

<span data-ttu-id="10716-133">**dwBookletHandlingCaps**</span><span class="sxs-lookup"><span data-stu-id="10716-133">**dwBookletHandlingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="10716-134">只能 PPCAPS \_ 手冊 \_ EDGE，指出印表機可以列印手冊樣式。</span><span class="sxs-lookup"><span data-stu-id="10716-134">Can only be PPCAPS\_BOOKLET\_EDGE, indicating that the printer can print booklet style.</span></span>

<span data-ttu-id="10716-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span><span class="sxs-lookup"><span data-stu-id="10716-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span></span><dd> 

| <span data-ttu-id="10716-136">值</span><span class="sxs-lookup"><span data-stu-id="10716-136">Value</span></span>                                         | <span data-ttu-id="10716-137">意義</span><span class="sxs-lookup"><span data-stu-id="10716-137">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10716-138">\_ \_ \_ \_ 反向 \_ 雙工 PPCAPS 反轉頁面</span><span class="sxs-lookup"><span data-stu-id="10716-138">PPCAPS\_REVERSE\_PAGES\_FOR\_REVERSE\_DUPLEX</span></span>  | <span data-ttu-id="10716-139">以反向順序和雙工方式進行列印時，處理器可以列印每一對頁面的順序，而不是依順序4、3、2、1來列印，而是會列印順序3、4、1、2。</span><span class="sxs-lookup"><span data-stu-id="10716-139">When printing in reverse order and duplexing, the processor can print swap the order of each pair of pages, so instead of printing in order 4,3,2,1, they will print in the order 3,4,1,2.</span></span>                                                                                                       |
| <span data-ttu-id="10716-140">PPCAPS \_ 不要 \_ 傳送 \_ 額外 \_ \_ 的頁面給 \_ 雙工</span><span class="sxs-lookup"><span data-stu-id="10716-140">PPCAPS\_DONT\_SEND\_EXTRA\_PAGES\_FOR\_DUPLEX</span></span> | <span data-ttu-id="10716-141">當雙工時，當有奇數的檔頁面時，可以通知列印處理器不要傳送額外的頁面。</span><span class="sxs-lookup"><span data-stu-id="10716-141">When duplexing, the Print Processor can be told not to send an extra page when there is an odd number of document pages.</span></span> <span data-ttu-id="10716-142">處理器會盡可能發揮最大的價值，但如果防止額外的空白頁面造成不適當的輸出，可能仍會傳送額外的頁面。</span><span class="sxs-lookup"><span data-stu-id="10716-142">The processor will honor the value as best as it can, but in cases where preventing an extra blank page would cause improper output, the extra pages may still be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="10716-143">**dwScalingCaps**</span><span class="sxs-lookup"><span data-stu-id="10716-143">**dwScalingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="10716-144">只能 PPCAPS \_ 正方形 \_ 調整，表示印表機可以調整頁面影像。</span><span class="sxs-lookup"><span data-stu-id="10716-144">Can only be PPCAPS\_SQUARE\_SCALING, indicating that the printer can scale the page image.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10716-145">備註</span><span class="sxs-lookup"><span data-stu-id="10716-145">Remarks</span></span>

<span data-ttu-id="10716-146">所有結構成員的值都是由 Windows 驅動程式套件中記載的 **GetPrintProcessorCapabilities** 函數所提供。</span><span class="sxs-lookup"><span data-stu-id="10716-146">Values for all structure members are supplied by the **GetPrintProcessorCapabilities** function which is documented in the Windows Driver Kit.</span></span>

<span data-ttu-id="10716-147">當應用程式呼叫 [**GetPrinterData**](getprinterdata.md)時，多工緩衝處理器會呼叫列印處理器的 **GetPrintProcessorCapabilities** 函式，並指定具有 **\_ PrintProcCaps**_datatype_ 格式的值名稱，其中 *datatype* 是輸入資料類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="10716-147">When an application calls [**GetPrinterData**](getprinterdata.md), the spooler calls a print processor's **GetPrintProcessorCapabilities** function and specifies a value name that has a format of **PrintProcCaps\_**_datatype_, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="10716-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="10716-148">Requirements</span></span>



| <span data-ttu-id="10716-149">需求</span><span class="sxs-lookup"><span data-stu-id="10716-149">Requirement</span></span> | <span data-ttu-id="10716-150">值</span><span class="sxs-lookup"><span data-stu-id="10716-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10716-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10716-151">Minimum supported client</span></span><br/> | <span data-ttu-id="10716-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10716-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="10716-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10716-153">Minimum supported server</span></span><br/> | <span data-ttu-id="10716-154">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10716-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="10716-155">標頭</span><span class="sxs-lookup"><span data-stu-id="10716-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="10716-156"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="10716-156"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10716-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10716-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10716-158">列印</span><span class="sxs-lookup"><span data-stu-id="10716-158">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="10716-159">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="10716-159">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="10716-160">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="10716-160">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

 




