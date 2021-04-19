---
description: 印表機 \_ 資訊 \_ 6 會指定印表機的狀態值。
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: 'PRINTER_INFO_6 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984723"
---
# <a name="printer_info_6-structure"></a><span data-ttu-id="ed061-103">印表機 \_ 資訊 \_ 6 結構</span><span class="sxs-lookup"><span data-stu-id="ed061-103">PRINTER\_INFO\_6 structure</span></span>

<span data-ttu-id="ed061-104">**印表機 \_ 資訊 \_ 6** 會指定印表機的狀態值。</span><span class="sxs-lookup"><span data-stu-id="ed061-104">The **PRINTER\_INFO\_6** specifies the status value of a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed061-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed061-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="ed061-106">成員</span><span class="sxs-lookup"><span data-stu-id="ed061-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed061-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="ed061-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="ed061-108">印表機狀態。</span><span class="sxs-lookup"><span data-stu-id="ed061-108">The printer status.</span></span> <span data-ttu-id="ed061-109">這個成員可以是下列值的任何合理組合。</span><span class="sxs-lookup"><span data-stu-id="ed061-109">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="ed061-110">值</span><span class="sxs-lookup"><span data-stu-id="ed061-110">Value</span></span>                               | <span data-ttu-id="ed061-111">意義</span><span class="sxs-lookup"><span data-stu-id="ed061-111">Meaning</span></span>                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed061-112">印表機 \_ 狀態 \_ 忙碌中</span><span class="sxs-lookup"><span data-stu-id="ed061-112">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="ed061-113">印表機忙碌中。</span><span class="sxs-lookup"><span data-stu-id="ed061-113">The printer is busy.</span></span>                                                                                          |
| <span data-ttu-id="ed061-114">印表機 \_ 狀態 \_ 門 \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="ed061-114">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="ed061-115">印表機門已開啟。</span><span class="sxs-lookup"><span data-stu-id="ed061-115">The printer door is open.</span></span>                                                                                     |
| <span data-ttu-id="ed061-116">印表機 \_ 狀態 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="ed061-116">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="ed061-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="ed061-117">Not used.</span></span>                                                                                                     |
| <span data-ttu-id="ed061-118">印表機 \_ 狀態 \_ 初始化</span><span class="sxs-lookup"><span data-stu-id="ed061-118">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="ed061-119">印表機初始化中。</span><span class="sxs-lookup"><span data-stu-id="ed061-119">The printer is initializing.</span></span>                                                                                  |
| <span data-ttu-id="ed061-120">印表機 \_ 狀態 \_ IO 使用中 \_</span><span class="sxs-lookup"><span data-stu-id="ed061-120">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="ed061-121">印表機處於作用中的輸入/輸出狀態</span><span class="sxs-lookup"><span data-stu-id="ed061-121">The printer is in an active input/output state</span></span>                                                                |
| <span data-ttu-id="ed061-122">印表機 \_ 狀態 \_ 手動 \_ 饋送</span><span class="sxs-lookup"><span data-stu-id="ed061-122">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="ed061-123">印表機處於手動摘要狀態。</span><span class="sxs-lookup"><span data-stu-id="ed061-123">The printer is in a manual feed state.</span></span>                                                                        |
| <span data-ttu-id="ed061-124">印表機 \_ 狀態 \_ 無 \_ 墨粉</span><span class="sxs-lookup"><span data-stu-id="ed061-124">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="ed061-125">印表機的碳粉已用完。</span><span class="sxs-lookup"><span data-stu-id="ed061-125">The printer is out of toner.</span></span>                                                                                  |
| <span data-ttu-id="ed061-126">印表機 \_ 狀態 \_ 無法 \_ 使用</span><span class="sxs-lookup"><span data-stu-id="ed061-126">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="ed061-127">印表機無法列印。</span><span class="sxs-lookup"><span data-stu-id="ed061-127">The printer is not available for printing.</span></span>                                                                    |
| <span data-ttu-id="ed061-128">印表機 \_ 狀態 \_ 離線</span><span class="sxs-lookup"><span data-stu-id="ed061-128">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="ed061-129">印表機為離線。</span><span class="sxs-lookup"><span data-stu-id="ed061-129">The printer is offline.</span></span>                                                                                       |
| <span data-ttu-id="ed061-130">印表機 \_ 狀態 \_ \_ 記憶體不足 \_</span><span class="sxs-lookup"><span data-stu-id="ed061-130">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="ed061-131">印表機的記憶體用盡。</span><span class="sxs-lookup"><span data-stu-id="ed061-131">The printer has run out of memory.</span></span>                                                                            |
| <span data-ttu-id="ed061-132">印表機 \_ 狀態 \_ 輸出 \_ 紙匣已 \_ 滿</span><span class="sxs-lookup"><span data-stu-id="ed061-132">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="ed061-133">印表機的輸出紙匣已滿。</span><span class="sxs-lookup"><span data-stu-id="ed061-133">The printer's output bin is full.</span></span>                                                                             |
| <span data-ttu-id="ed061-134">印表機 \_ 狀態 \_ 頁面 \_</span><span class="sxs-lookup"><span data-stu-id="ed061-134">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="ed061-135">印表機無法列印目前的頁面。</span><span class="sxs-lookup"><span data-stu-id="ed061-135">The printer cannot print the current page.</span></span>                                                                    |
| <span data-ttu-id="ed061-136">印表機 \_ 狀態 \_ 紙 \_ 紙</span><span class="sxs-lookup"><span data-stu-id="ed061-136">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="ed061-137">印表機中的紙張已卡住</span><span class="sxs-lookup"><span data-stu-id="ed061-137">Paper is jammed in the printer</span></span>                                                                                |
| <span data-ttu-id="ed061-138">印表機 \_ 狀態 \_ 紙張 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="ed061-138">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="ed061-139">印表機紙張用完。</span><span class="sxs-lookup"><span data-stu-id="ed061-139">The printer is out of paper.</span></span>                                                                                  |
| <span data-ttu-id="ed061-140">印表機 \_ 狀態 \_ 紙張 \_ 問題</span><span class="sxs-lookup"><span data-stu-id="ed061-140">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="ed061-141">印表機有紙張問題。</span><span class="sxs-lookup"><span data-stu-id="ed061-141">The printer has a paper problem.</span></span>                                                                              |
| <span data-ttu-id="ed061-142">印表機 \_ 狀態已 \_ 暫停</span><span class="sxs-lookup"><span data-stu-id="ed061-142">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="ed061-143">印表機已暫停。</span><span class="sxs-lookup"><span data-stu-id="ed061-143">The printer is paused.</span></span>                                                                                        |
| <span data-ttu-id="ed061-144">印表機 \_ 狀態 \_ 暫止 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="ed061-144">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="ed061-145">因為呼叫 [**DeletePrinter**](deleteprinter.md) 函式，所以印表機暫止刪除。</span><span class="sxs-lookup"><span data-stu-id="ed061-145">The printer is pending deletion as a result of a call to the [**DeletePrinter**](deleteprinter.md) function.</span></span> |
| <span data-ttu-id="ed061-146">印表機 \_ 狀態 \_ \_ 省電</span><span class="sxs-lookup"><span data-stu-id="ed061-146">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="ed061-147">印表機處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="ed061-147">The printer is in power save mode.</span></span>                                                                            |
| <span data-ttu-id="ed061-148">印表機 \_ 狀態 \_ 列印</span><span class="sxs-lookup"><span data-stu-id="ed061-148">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="ed061-149">印表機正在列印。</span><span class="sxs-lookup"><span data-stu-id="ed061-149">The printer is printing.</span></span>                                                                                      |
| <span data-ttu-id="ed061-150">印表機 \_ 狀態 \_ 處理</span><span class="sxs-lookup"><span data-stu-id="ed061-150">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="ed061-151">印表機正在處理來自 [**SetPrinter**](setprinter.md) 函式的命令。</span><span class="sxs-lookup"><span data-stu-id="ed061-151">The printer is processing a command from the [**SetPrinter**](setprinter.md) function.</span></span>                       |
| <span data-ttu-id="ed061-152">印表機 \_ 狀態 \_ 伺服器 \_ 不明</span><span class="sxs-lookup"><span data-stu-id="ed061-152">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="ed061-153">印表機狀態不明。</span><span class="sxs-lookup"><span data-stu-id="ed061-153">The printer status is unknown.</span></span>                                                                                |
| <span data-ttu-id="ed061-154">印表機 \_ 狀態 \_ 墨粉 \_ 低</span><span class="sxs-lookup"><span data-stu-id="ed061-154">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="ed061-155">印表機碳粉不足。</span><span class="sxs-lookup"><span data-stu-id="ed061-155">The printer is low on toner.</span></span>                                                                                  |
| <span data-ttu-id="ed061-156">印表機 \_ 狀態 \_ 使用者 \_ 介入</span><span class="sxs-lookup"><span data-stu-id="ed061-156">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="ed061-157">印表機有錯誤，需要使用者進行一些動作。</span><span class="sxs-lookup"><span data-stu-id="ed061-157">The printer has an error that requires the user to do something.</span></span>                                              |
| <span data-ttu-id="ed061-158">印表機 \_ 狀態 \_ 等候中</span><span class="sxs-lookup"><span data-stu-id="ed061-158">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="ed061-159">印表機正在等候。</span><span class="sxs-lookup"><span data-stu-id="ed061-159">The printer is waiting.</span></span>                                                                                       |
| <span data-ttu-id="ed061-160">印表機 \_ 狀態 \_ 預熱 \_</span><span class="sxs-lookup"><span data-stu-id="ed061-160">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="ed061-161">印表機準備中。</span><span class="sxs-lookup"><span data-stu-id="ed061-161">The printer is warming up.</span></span>                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed061-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed061-162">Requirements</span></span>



| <span data-ttu-id="ed061-163">需求</span><span class="sxs-lookup"><span data-stu-id="ed061-163">Requirement</span></span> | <span data-ttu-id="ed061-164">值</span><span class="sxs-lookup"><span data-stu-id="ed061-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed061-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed061-165">Minimum supported client</span></span><br/> | <span data-ttu-id="ed061-166">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed061-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ed061-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed061-167">Minimum supported server</span></span><br/> | <span data-ttu-id="ed061-168">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed061-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ed061-169">標頭</span><span class="sxs-lookup"><span data-stu-id="ed061-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed061-170"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ed061-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ed061-171">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="ed061-171">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ed061-172">**\_ 印表機 \_ 資訊 \_ 6W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 6a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="ed061-172">**\_PRINTER\_INFO\_6W** (Unicode) and **\_PRINTER\_INFO\_6A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="ed061-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed061-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed061-174">列印</span><span class="sxs-lookup"><span data-stu-id="ed061-174">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ed061-175">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="ed061-175">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ed061-176">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="ed061-176">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="ed061-177">**印表機 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ed061-177">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="ed061-178">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ed061-178">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="ed061-179">**印表機 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ed061-179">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="ed061-180">**印表機 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="ed061-180">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="ed061-181">**印表機 \_ 資訊 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="ed061-181">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> </dl>

 

 




