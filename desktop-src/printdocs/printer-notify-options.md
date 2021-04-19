---
description: 印表機 \_ 通知 \_ 選項結構會指定監視印表機或列印伺服器之變更通知物件的選項。
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: 'PRINTER_NOTIFY_OPTIONS 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987584"
---
# <a name="printer_notify_options-structure"></a><span data-ttu-id="90356-103">印表機 \_ 通知 \_ 選項結構</span><span class="sxs-lookup"><span data-stu-id="90356-103">PRINTER\_NOTIFY\_OPTIONS structure</span></span>

<span data-ttu-id="90356-104">**印表機 \_ 通知 \_ 選項** 結構會指定監視印表機或列印伺服器之變更通知物件的選項。</span><span class="sxs-lookup"><span data-stu-id="90356-104">The **PRINTER\_NOTIFY\_OPTIONS** structure specifies options for a change notification object that monitors a printer or print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="90356-105">語法</span><span class="sxs-lookup"><span data-stu-id="90356-105">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="90356-106">成員</span><span class="sxs-lookup"><span data-stu-id="90356-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="90356-107">**版本**</span><span class="sxs-lookup"><span data-stu-id="90356-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="90356-108">此結構的版本。</span><span class="sxs-lookup"><span data-stu-id="90356-108">The version of this structure.</span></span> <span data-ttu-id="90356-109">將這個成員設定為2。</span><span class="sxs-lookup"><span data-stu-id="90356-109">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="90356-110">**旗標**</span><span class="sxs-lookup"><span data-stu-id="90356-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="90356-111">位旗標。</span><span class="sxs-lookup"><span data-stu-id="90356-111">A bit flag.</span></span> <span data-ttu-id="90356-112">如果您在 FindNextPrinterChangeNotification 函式的呼叫中設定 [印表機通知選項重新整理] 旗標，此函式會 \_ \_ \_ 為所有受監視的印表機資訊欄位提供目前的資料。 [](findnextprinterchangenotification.md)</span><span class="sxs-lookup"><span data-stu-id="90356-112">If you set the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag in a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function, the function provides current data for all monitored printer information fields.</span></span> <span data-ttu-id="90356-113">[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)函式會忽略 **旗標** 成員。</span><span class="sxs-lookup"><span data-stu-id="90356-113">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function ignores the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="90356-114">**Count**</span><span class="sxs-lookup"><span data-stu-id="90356-114">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="90356-115">**PTypes** 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="90356-115">The number of elements in the **pTypes** array.</span></span>

</dd> <dt>

<span data-ttu-id="90356-116">**pTypes**</span><span class="sxs-lookup"><span data-stu-id="90356-116">**pTypes**</span></span>
</dt> <dd>

<span data-ttu-id="90356-117">[**印表機 \_ 通知 \_ 選項 \_ 類型**](printer-notify-options-type.md)結構的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="90356-117">A pointer to an array of [**PRINTER\_NOTIFY\_OPTIONS\_TYPE**](printer-notify-options-type.md) structures.</span></span> <span data-ttu-id="90356-118">使用這個陣列的一個專案來指定要監視的印表機資訊欄位，以及一個專案來指定要監視的作業資訊欄位。</span><span class="sxs-lookup"><span data-stu-id="90356-118">Use one element of this array to specify the printer information fields to monitor, and one element to specify the job information fields to monitor.</span></span> <span data-ttu-id="90356-119">您可以監視印表機資訊、作業資訊或兩者。</span><span class="sxs-lookup"><span data-stu-id="90356-119">You can monitor either printer information, job information, or both.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90356-120">備註</span><span class="sxs-lookup"><span data-stu-id="90356-120">Remarks</span></span>

<span data-ttu-id="90356-121">使用此結構搭配 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) 函式來指定要監視變更的印表機或作業資訊欄位集。</span><span class="sxs-lookup"><span data-stu-id="90356-121">Use this structure with the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function to specify the set of printer or job information fields to monitor for change.</span></span>

<span data-ttu-id="90356-122">使用此結構搭配 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函式，以要求所有受監視印表機和作業資訊欄位目前的資料。</span><span class="sxs-lookup"><span data-stu-id="90356-122">Use this structure with the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function to request the current data for all monitored printer and job information fields.</span></span> <span data-ttu-id="90356-123">在此情況下， **旗標** 成員會指定印表機通知選項的重新整理旗標，而函式會 \_ \_ \_ 忽略其他結構成員。</span><span class="sxs-lookup"><span data-stu-id="90356-123">In this case, the **Flags** member specifies the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag, and the function ignores the other structure members.</span></span>

## <a name="requirements"></a><span data-ttu-id="90356-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="90356-124">Requirements</span></span>



| <span data-ttu-id="90356-125">需求</span><span class="sxs-lookup"><span data-stu-id="90356-125">Requirement</span></span> | <span data-ttu-id="90356-126">值</span><span class="sxs-lookup"><span data-stu-id="90356-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90356-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90356-127">Minimum supported client</span></span><br/> | <span data-ttu-id="90356-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90356-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="90356-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90356-129">Minimum supported server</span></span><br/> | <span data-ttu-id="90356-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90356-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="90356-131">標頭</span><span class="sxs-lookup"><span data-stu-id="90356-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="90356-132"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="90356-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90356-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90356-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90356-134">列印</span><span class="sxs-lookup"><span data-stu-id="90356-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="90356-135">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="90356-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="90356-136">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="90356-136">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="90356-137">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="90356-137">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="90356-138">**印表機 \_ 通知 \_ 選項 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="90356-138">**PRINTER\_NOTIFY\_OPTIONS\_TYPE**</span></span>](printer-notify-options-type.md)
</dt> </dl>

 

 




