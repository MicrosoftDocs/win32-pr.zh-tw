---
description: 印表機 \_ 資訊 \_ 1 結構會指定一般印表機資訊。
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: 'PRINTER_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975759"
---
# <a name="printer_info_1-structure"></a><span data-ttu-id="fe976-103">印表機 \_ 資訊 \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="fe976-103">PRINTER\_INFO\_1 structure</span></span>

<span data-ttu-id="fe976-104">**印表機 \_ 資訊 \_ 1** 結構會指定一般印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="fe976-104">The **PRINTER\_INFO\_1** structure specifies general printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe976-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe976-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="fe976-106">成員</span><span class="sxs-lookup"><span data-stu-id="fe976-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe976-107">**旗標**</span><span class="sxs-lookup"><span data-stu-id="fe976-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="fe976-108">指定傳回之資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fe976-108">Specifies information about the returned data.</span></span> <span data-ttu-id="fe976-109">以下是這個成員的值。</span><span class="sxs-lookup"><span data-stu-id="fe976-109">Following are the values for this member.</span></span>



| <span data-ttu-id="fe976-110">值</span><span class="sxs-lookup"><span data-stu-id="fe976-110">Value</span></span>                    | <span data-ttu-id="fe976-111">意義</span><span class="sxs-lookup"><span data-stu-id="fe976-111">Meaning</span></span>                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe976-112">印表機 \_ 列舉 \_ 展開</span><span class="sxs-lookup"><span data-stu-id="fe976-112">PRINTER\_ENUM\_EXPAND</span></span>    | <span data-ttu-id="fe976-113">如果已啟用預設展開，列印提供者可以將此旗標設定為呼叫應用程式的提示，以進一步列舉此物件。</span><span class="sxs-lookup"><span data-stu-id="fe976-113">A print provider can set this flag as a hint to a calling application to enumerate this object further if default expansion is enabled.</span></span> <span data-ttu-id="fe976-114">例如，列舉網域時，列印提供者可能會藉由設定此旗標來指出使用者的網域。</span><span class="sxs-lookup"><span data-stu-id="fe976-114">For example, when domains are enumerated, a print provider might indicate the user's domain by setting this flag.</span></span> |
| <span data-ttu-id="fe976-115">印表機 \_ 列舉 \_ 容器</span><span class="sxs-lookup"><span data-stu-id="fe976-115">PRINTER\_ENUM\_CONTAINER</span></span> | <span data-ttu-id="fe976-116">如果設定此旗標，印表機物件可能會包含可列舉的物件。</span><span class="sxs-lookup"><span data-stu-id="fe976-116">If this flag is set, the printer object may contain enumerable objects.</span></span> <span data-ttu-id="fe976-117">例如，物件可能是包含印表機的列印伺服器。</span><span class="sxs-lookup"><span data-stu-id="fe976-117">For example, the object may be a print server that contains printers.</span></span>                                                                                                             |
| <span data-ttu-id="fe976-118">印表機 \_ 列舉 \_ ICON1</span><span class="sxs-lookup"><span data-stu-id="fe976-118">PRINTER\_ENUM\_ICON1</span></span>     | <span data-ttu-id="fe976-119">表示在適當的情況下，應用程式應該會顯示將物件識別為最上層網路名稱（例如 Microsoft Windows Network）的圖示。</span><span class="sxs-lookup"><span data-stu-id="fe976-119">Indicates that, where appropriate, an application should display an icon identifying the object as a top-level network name, such as Microsoft Windows Network.</span></span>                                                                                           |
| <span data-ttu-id="fe976-120">印表機 \_ 列舉 \_ ICON2</span><span class="sxs-lookup"><span data-stu-id="fe976-120">PRINTER\_ENUM\_ICON2</span></span>     | <span data-ttu-id="fe976-121">表示在適當的情況下，應用程式應該會顯示將物件識別為網路網域的圖示。</span><span class="sxs-lookup"><span data-stu-id="fe976-121">Indicates that, where appropriate, an application should display an icon that identifies the object as a network domain.</span></span>                                                                                                                                  |
| <span data-ttu-id="fe976-122">印表機 \_ 列舉 \_ ICON3</span><span class="sxs-lookup"><span data-stu-id="fe976-122">PRINTER\_ENUM\_ICON3</span></span>     | <span data-ttu-id="fe976-123">表示在適當的情況下，應用程式應該會顯示將物件識別為列印伺服器的圖示。</span><span class="sxs-lookup"><span data-stu-id="fe976-123">Indicates that, where appropriate, an application should display an icon that identifies the object as a print server.</span></span>                                                                                                                                    |
| <span data-ttu-id="fe976-124">印表機 \_ 列舉 \_ ICON4</span><span class="sxs-lookup"><span data-stu-id="fe976-124">PRINTER\_ENUM\_ICON4</span></span>     | <span data-ttu-id="fe976-125">保留的。</span><span class="sxs-lookup"><span data-stu-id="fe976-125">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fe976-126">印表機 \_ 列舉 \_ ICON5</span><span class="sxs-lookup"><span data-stu-id="fe976-126">PRINTER\_ENUM\_ICON5</span></span>     | <span data-ttu-id="fe976-127">保留的。</span><span class="sxs-lookup"><span data-stu-id="fe976-127">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fe976-128">印表機 \_ 列舉 \_ ICON6</span><span class="sxs-lookup"><span data-stu-id="fe976-128">PRINTER\_ENUM\_ICON6</span></span>     | <span data-ttu-id="fe976-129">保留的。</span><span class="sxs-lookup"><span data-stu-id="fe976-129">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fe976-130">印表機 \_ 列舉 \_ ICON7</span><span class="sxs-lookup"><span data-stu-id="fe976-130">PRINTER\_ENUM\_ICON7</span></span>     | <span data-ttu-id="fe976-131">保留的。</span><span class="sxs-lookup"><span data-stu-id="fe976-131">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fe976-132">印表機 \_ 列舉 \_ ICON8</span><span class="sxs-lookup"><span data-stu-id="fe976-132">PRINTER\_ENUM\_ICON8</span></span>     | <span data-ttu-id="fe976-133">表示在適當的情況下，應用程式應該會顯示將物件識別為印表機的圖示。</span><span class="sxs-lookup"><span data-stu-id="fe976-133">Indicates that, where appropriate, an application should display an icon that identifies the object as a printer.</span></span>                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="fe976-134">**pDescription**</span><span class="sxs-lookup"><span data-stu-id="fe976-134">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="fe976-135">描述結構內容之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="fe976-135">Pointer to a null-terminated string that describes the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe976-136">**pName**</span><span class="sxs-lookup"><span data-stu-id="fe976-136">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="fe976-137">以 null 結束的字串指標，該字串會命名結構的內容。</span><span class="sxs-lookup"><span data-stu-id="fe976-137">Pointer to a null-terminated string that names the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe976-138">**pComment**</span><span class="sxs-lookup"><span data-stu-id="fe976-138">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="fe976-139">以 null 結束的字串指標，其中包含描述結構的其他資料。</span><span class="sxs-lookup"><span data-stu-id="fe976-139">Pointer to a null-terminated string that contains additional data describing the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe976-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe976-140">Requirements</span></span>



| <span data-ttu-id="fe976-141">需求</span><span class="sxs-lookup"><span data-stu-id="fe976-141">Requirement</span></span> | <span data-ttu-id="fe976-142">值</span><span class="sxs-lookup"><span data-stu-id="fe976-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe976-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe976-143">Minimum supported client</span></span><br/> | <span data-ttu-id="fe976-144">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe976-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fe976-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe976-145">Minimum supported server</span></span><br/> | <span data-ttu-id="fe976-146">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe976-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe976-147">標頭</span><span class="sxs-lookup"><span data-stu-id="fe976-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe976-148"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fe976-148"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fe976-149">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="fe976-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fe976-150">**\_ 印表機 \_ 資訊 \_ 1W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 1a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="fe976-150">**\_PRINTER\_INFO\_1W** (Unicode) and **\_PRINTER\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="fe976-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe976-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe976-152">列印</span><span class="sxs-lookup"><span data-stu-id="fe976-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fe976-153">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="fe976-153">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="fe976-154">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="fe976-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="fe976-155">**>enumprinters**</span><span class="sxs-lookup"><span data-stu-id="fe976-155">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="fe976-156">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fe976-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="fe976-157">**印表機 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="fe976-157">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="fe976-158">**印表機 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="fe976-158">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




