---
description: PRINTPROCESSOR \_ CAPS \_ 1 結構是在 .pdata 變數所指定的緩衝區中，GetPrinterData 函式所傳回之印表機功能資訊的格式。
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: 'PRINTPROCESSOR_CAPS_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975428"
---
# <a name="printprocessor_caps_1-structure"></a><span data-ttu-id="73e39-103">PRINTPROCESSOR \_ CAPS \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="73e39-103">PRINTPROCESSOR\_CAPS\_1 structure</span></span>

<span data-ttu-id="73e39-104">**PRINTPROCESSOR \_ CAPS \_ 1** 結構是在 *.pdata* 變數所指定的緩衝區中， [**GetPrinterData**](getprinterdata.md)函式所傳回之印表機功能資訊的格式。</span><span class="sxs-lookup"><span data-stu-id="73e39-104">The **PRINTPROCESSOR\_CAPS\_1** structure is the format for the printer capability information that is returned by the [**GetPrinterData**](getprinterdata.md) function in the buffer specified by the *pData* variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e39-105">語法</span><span class="sxs-lookup"><span data-stu-id="73e39-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a><span data-ttu-id="73e39-106">成員</span><span class="sxs-lookup"><span data-stu-id="73e39-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="73e39-107">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="73e39-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="73e39-108">結構的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="73e39-108">The structure's version number.</span></span> <span data-ttu-id="73e39-109">此值必須是1。</span><span class="sxs-lookup"><span data-stu-id="73e39-109">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="73e39-110">**dwNupOptions**</span><span class="sxs-lookup"><span data-stu-id="73e39-110">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="73e39-111">位元遮罩，代表印表機可在實體頁面上列印的各種檔頁面數目。</span><span class="sxs-lookup"><span data-stu-id="73e39-111">A bit mask representing the various numbers of document pages the printer can print on a physical page.</span></span> <span data-ttu-id="73e39-112">最不重要的位代表每個頁面1個檔頁面，下一個位代表每頁2份檔頁面等等。</span><span class="sxs-lookup"><span data-stu-id="73e39-112">The least significant bit represents 1 document page per page, the next bit represents 2 document pages per page, and so on.</span></span> <span data-ttu-id="73e39-113">例如，0x0000810B 表示印表機支援每個實體頁面1、2、4、9和16份檔頁面。</span><span class="sxs-lookup"><span data-stu-id="73e39-113">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical page.</span></span>

</dd> <dt>

<span data-ttu-id="73e39-114">**dwPageOrderFlags**</span><span class="sxs-lookup"><span data-stu-id="73e39-114">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="73e39-115">列印頁面的順序。</span><span class="sxs-lookup"><span data-stu-id="73e39-115">The order in which pages will be printed.</span></span> <span data-ttu-id="73e39-116">此值可以是一般 \_ 列印、反向 \_ 列印或手冊 \_ 列印。</span><span class="sxs-lookup"><span data-stu-id="73e39-116">This value can be NORMAL\_PRINT, REVERSE\_PRINT, or BOOKLET\_PRINT.</span></span>

</dd> <dt>

<span data-ttu-id="73e39-117">**dwNumberOfCopies**</span><span class="sxs-lookup"><span data-stu-id="73e39-117">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="73e39-118">印表機可以處理的最大複本數目。</span><span class="sxs-lookup"><span data-stu-id="73e39-118">The maximum number of copies the printer can handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73e39-119">備註</span><span class="sxs-lookup"><span data-stu-id="73e39-119">Remarks</span></span>

<span data-ttu-id="73e39-120">所有結構成員的值都是由 [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) 函式所提供，此函數記載于 WINDOWS 驅動程式套件 (WDK) 中。</span><span class="sxs-lookup"><span data-stu-id="73e39-120">Values for all structure members are supplied by the [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function, which is documented in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="73e39-121">當應用程式呼叫 [**GetPrinterData**](getprinterdata.md)，以 [](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) PrintProcCaps datatype 的格式指定值名稱 \_ \*\*（其中 *datatype* 是輸入資料類型的名稱）時，多工緩衝處理器會呼叫列印處理器的 GetPrintProcessorCapabilities 函式。</span><span class="sxs-lookup"><span data-stu-id="73e39-121">The spooler calls a print processor's [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function when an application calls [**GetPrinterData**](getprinterdata.md), specifying a value name with a format of PrintProcCaps\_*datatype*, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="73e39-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="73e39-122">Requirements</span></span>



| <span data-ttu-id="73e39-123">需求</span><span class="sxs-lookup"><span data-stu-id="73e39-123">Requirement</span></span> | <span data-ttu-id="73e39-124">值</span><span class="sxs-lookup"><span data-stu-id="73e39-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e39-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73e39-125">Minimum supported client</span></span><br/> | <span data-ttu-id="73e39-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73e39-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="73e39-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73e39-127">Minimum supported server</span></span><br/> | <span data-ttu-id="73e39-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73e39-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="73e39-129">標頭</span><span class="sxs-lookup"><span data-stu-id="73e39-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="73e39-130"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="73e39-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e39-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73e39-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e39-132">列印</span><span class="sxs-lookup"><span data-stu-id="73e39-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="73e39-133">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="73e39-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="73e39-134">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="73e39-134">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

