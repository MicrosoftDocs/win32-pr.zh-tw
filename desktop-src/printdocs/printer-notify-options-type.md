---
description: 印表機 \_ 通知 \_ 選項 \_ 類型結構會指定印表機變更通知物件所要監視的印表機或作業資訊欄位集。FindFirstPrinterChangeNotification 函式的呼叫會指定印表機 \_ 通知 \_ 選項結構，其中包含印表機 \_ 通知 \_ 選項類型結構的陣列 \_ 。
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: 'PRINTER_NOTIFY_OPTIONS_TYPE 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987585"
---
# <a name="printer_notify_options_type-structure"></a><span data-ttu-id="918cc-103">印表機 \_ 通知 \_ 選項 \_ 類型結構</span><span class="sxs-lookup"><span data-stu-id="918cc-103">PRINTER\_NOTIFY\_OPTIONS\_TYPE structure</span></span>

<span data-ttu-id="918cc-104">**印表機 \_ 通知 \_ 選項 \_ 類型** 結構會指定印表機變更通知物件所要監視的印表機或作業資訊欄位集。</span><span class="sxs-lookup"><span data-stu-id="918cc-104">The **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structure specifies the set of printer or job information fields to be monitored by a printer change notification object.</span></span>

<span data-ttu-id="918cc-105">[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)函式的呼叫會指定 [**印表機 \_ 通知 \_ 選項**](printer-notify-options.md)結構，其中包含 **印表機 \_ 通知 \_ 選項 \_ 類型** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="918cc-105">A call to the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function specifies a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure, which contains an array of **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="918cc-106">語法</span><span class="sxs-lookup"><span data-stu-id="918cc-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a><span data-ttu-id="918cc-107">成員</span><span class="sxs-lookup"><span data-stu-id="918cc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="918cc-108">**型別**</span><span class="sxs-lookup"><span data-stu-id="918cc-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="918cc-109">要監看的型別。</span><span class="sxs-lookup"><span data-stu-id="918cc-109">The type to be watched.</span></span> <span data-ttu-id="918cc-110">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="918cc-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="918cc-111">值</span><span class="sxs-lookup"><span data-stu-id="918cc-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="918cc-112">意義</span><span class="sxs-lookup"><span data-stu-id="918cc-112">Meaning</span></span>                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="918cc-113"><dt>**作業 \_通知 \_ 類型**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="918cc-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="918cc-114">指出 **pFields** 陣列中指定的欄位是工作 \_ 通知 \_ 欄位 \_ \* 常數。</span><span class="sxs-lookup"><span data-stu-id="918cc-114">Indicates that the fields specified in the **pFields** array are JOB\_NOTIFY\_FIELD\_\* constants.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="918cc-115"><dt>**印表機 \_通知 \_ 類型**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="918cc-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="918cc-116">指出 **pFields** 陣列中指定的欄位是印表機 \_ 通知 \_ 欄位 \_ \* 常數。</span><span class="sxs-lookup"><span data-stu-id="918cc-116">Indicates that the fields specified in the **pFields** array are PRINTER\_NOTIFY\_FIELD\_\* constants.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="918cc-117">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="918cc-117">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="918cc-118">保留的。</span><span class="sxs-lookup"><span data-stu-id="918cc-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="918cc-119">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="918cc-119">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="918cc-120">保留的。</span><span class="sxs-lookup"><span data-stu-id="918cc-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="918cc-121">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="918cc-121">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="918cc-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="918cc-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="918cc-123">**Count**</span><span class="sxs-lookup"><span data-stu-id="918cc-123">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="918cc-124">**PFields** 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="918cc-124">The number of elements in the **pFields** array.</span></span>

</dd> <dt>

<span data-ttu-id="918cc-125">**pFields**</span><span class="sxs-lookup"><span data-stu-id="918cc-125">**pFields**</span></span>
</dt> <dd>

<span data-ttu-id="918cc-126">值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="918cc-126">A pointer to an array of values.</span></span> <span data-ttu-id="918cc-127">陣列的每個元素都會指定相關的作業或印表機資訊欄位。</span><span class="sxs-lookup"><span data-stu-id="918cc-127">Each element of the array specifies a job or printer information field of interest.</span></span> <span data-ttu-id="918cc-128">如需支援的印表機和作業資訊欄位清單，請參閱 [**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="918cc-128">For a list of supported printer and job information fields, see the [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="918cc-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="918cc-129">Requirements</span></span>



| <span data-ttu-id="918cc-130">需求</span><span class="sxs-lookup"><span data-stu-id="918cc-130">Requirement</span></span> | <span data-ttu-id="918cc-131">值</span><span class="sxs-lookup"><span data-stu-id="918cc-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="918cc-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="918cc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="918cc-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="918cc-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="918cc-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="918cc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="918cc-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="918cc-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="918cc-136">標頭</span><span class="sxs-lookup"><span data-stu-id="918cc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="918cc-137"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="918cc-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="918cc-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="918cc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="918cc-139">列印</span><span class="sxs-lookup"><span data-stu-id="918cc-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="918cc-140">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="918cc-140">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="918cc-141">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="918cc-141">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="918cc-142">**印表機 \_ 通知 \_ 資訊 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="918cc-142">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="918cc-143">**印表機 \_ 通知 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="918cc-143">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

 




