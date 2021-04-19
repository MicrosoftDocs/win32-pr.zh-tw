---
description: PORT \_ INFO \_ 3 結構會指定印表機埠的狀態值。
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: 'PORT_INFO_3 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992042"
---
# <a name="port_info_3-structure"></a><span data-ttu-id="791c3-103">埠 \_ 資訊 \_ 3 結構</span><span class="sxs-lookup"><span data-stu-id="791c3-103">PORT\_INFO\_3 structure</span></span>

<span data-ttu-id="791c3-104">**PORT \_ INFO \_ 3** 結構會指定印表機埠的狀態值。</span><span class="sxs-lookup"><span data-stu-id="791c3-104">The **PORT\_INFO\_3** structure specifies the status value of a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="791c3-105">語法</span><span class="sxs-lookup"><span data-stu-id="791c3-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a><span data-ttu-id="791c3-106">成員</span><span class="sxs-lookup"><span data-stu-id="791c3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="791c3-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="791c3-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="791c3-108">新的埠狀態值。</span><span class="sxs-lookup"><span data-stu-id="791c3-108">The new port status value.</span></span> <span data-ttu-id="791c3-109">只有當 **pszStatus** 成員是 **Null** 時，才會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="791c3-109">This value is used only if the **pszStatus** member is **NULL**.</span></span>

<span data-ttu-id="791c3-110">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="791c3-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="791c3-111">值</span><span class="sxs-lookup"><span data-stu-id="791c3-111">Value</span></span>                            | <span data-ttu-id="791c3-112">意義</span><span class="sxs-lookup"><span data-stu-id="791c3-112">Meaning</span></span>                                             |
|----------------------------------|-----------------------------------------------------|
| <span data-ttu-id="791c3-113">0</span><span class="sxs-lookup"><span data-stu-id="791c3-113">0</span></span>                                | <span data-ttu-id="791c3-114">清除印表機埠狀態。</span><span class="sxs-lookup"><span data-stu-id="791c3-114">Clears the printer port status.</span></span>                     |
| <span data-ttu-id="791c3-115">\_離線埠狀態 \_</span><span class="sxs-lookup"><span data-stu-id="791c3-115">PORT\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="791c3-116">埠的印表機已離線。</span><span class="sxs-lookup"><span data-stu-id="791c3-116">The port's printer is offline.</span></span>                      |
| <span data-ttu-id="791c3-117">埠 \_ 狀態 \_ 紙 \_ 紙</span><span class="sxs-lookup"><span data-stu-id="791c3-117">PORT\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="791c3-118">埠的印表機有紙紙。</span><span class="sxs-lookup"><span data-stu-id="791c3-118">The port's printer has a paper jam.</span></span>                 |
| <span data-ttu-id="791c3-119">埠 \_ 狀態 \_ 紙張 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="791c3-119">PORT\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="791c3-120">埠的印表機缺紙。</span><span class="sxs-lookup"><span data-stu-id="791c3-120">The port's printer is out of paper.</span></span>                 |
| <span data-ttu-id="791c3-121">埠 \_ 狀態 \_ 輸出 \_ BIN 已 \_ 滿</span><span class="sxs-lookup"><span data-stu-id="791c3-121">PORT\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="791c3-122">埠的 printer's 輸出 bin 已滿。</span><span class="sxs-lookup"><span data-stu-id="791c3-122">The port's printer's output bin is full.</span></span>            |
| <span data-ttu-id="791c3-123">埠 \_ 狀態 \_ 紙張 \_ 問題</span><span class="sxs-lookup"><span data-stu-id="791c3-123">PORT\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="791c3-124">埠的印表機有紙張問題。</span><span class="sxs-lookup"><span data-stu-id="791c3-124">The port's printer has a paper problem.</span></span>             |
| <span data-ttu-id="791c3-125">\_ \_ 無 \_ 墨粉的埠狀態</span><span class="sxs-lookup"><span data-stu-id="791c3-125">PORT\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="791c3-126">埠的印表機已缺墨粉。</span><span class="sxs-lookup"><span data-stu-id="791c3-126">The port's printer is out of toner.</span></span>                 |
| <span data-ttu-id="791c3-127">埠 \_ 狀態 \_ 門 \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="791c3-127">PORT\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="791c3-128">埠的印表機門已開啟。</span><span class="sxs-lookup"><span data-stu-id="791c3-128">The door of the port's printer is open.</span></span>             |
| <span data-ttu-id="791c3-129">埠 \_ 狀態 \_ 使用者 \_ 介入</span><span class="sxs-lookup"><span data-stu-id="791c3-129">PORT\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="791c3-130">埠的印表機需要使用者介入。</span><span class="sxs-lookup"><span data-stu-id="791c3-130">The port's printer requires user intervention.</span></span>      |
| <span data-ttu-id="791c3-131">埠 \_ 狀態 \_ \_ 記憶體不足 \_</span><span class="sxs-lookup"><span data-stu-id="791c3-131">PORT\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="791c3-132">埠的印表機記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="791c3-132">The port's printer is out of memory.</span></span>                |
| <span data-ttu-id="791c3-133">埠 \_ 狀態 \_ 墨粉 \_ 低</span><span class="sxs-lookup"><span data-stu-id="791c3-133">PORT\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="791c3-134">埠的印表機碳粉不足。</span><span class="sxs-lookup"><span data-stu-id="791c3-134">The port's printer is low on toner.</span></span>                 |
| <span data-ttu-id="791c3-135">埠 \_ 狀態 \_ 預熱 \_</span><span class="sxs-lookup"><span data-stu-id="791c3-135">PORT\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="791c3-136">埠的印表機正在準備。</span><span class="sxs-lookup"><span data-stu-id="791c3-136">The port's printer is warming up.</span></span>                   |
| <span data-ttu-id="791c3-137">埠 \_ 狀態省 \_ 電 \_</span><span class="sxs-lookup"><span data-stu-id="791c3-137">PORT\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="791c3-138">埠的印表機會處於電源節省模式。</span><span class="sxs-lookup"><span data-stu-id="791c3-138">The port's printer is in a power-conservation mode.</span></span> |



 

</dd> <dt>

<span data-ttu-id="791c3-139">**pszStatus**</span><span class="sxs-lookup"><span data-stu-id="791c3-139">**pszStatus**</span></span>
</dt> <dd>

<span data-ttu-id="791c3-140">要設定的新印表機埠狀態值字串指標。</span><span class="sxs-lookup"><span data-stu-id="791c3-140">Pointer to a new printer port status value string to set.</span></span> <span data-ttu-id="791c3-141">如果針對 **dwStatus** 所列的值沒有適當的狀態值，請使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="791c3-141">Use this member if there is no suitable status value among those listed for **dwStatus**.</span></span>

</dd> <dt>

<span data-ttu-id="791c3-142">**dwSeverity**</span><span class="sxs-lookup"><span data-stu-id="791c3-142">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="791c3-143">埠狀態值的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="791c3-143">The severity of the port status value.</span></span>

<span data-ttu-id="791c3-144">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="791c3-144">This member can be one of the following values.</span></span>



| <span data-ttu-id="791c3-145">值</span><span class="sxs-lookup"><span data-stu-id="791c3-145">Value</span></span>                       | <span data-ttu-id="791c3-146">意義</span><span class="sxs-lookup"><span data-stu-id="791c3-146">Meaning</span></span>                                   |
|-----------------------------|-------------------------------------------|
| <span data-ttu-id="791c3-147">埠 \_ 狀態 \_ 類型 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="791c3-147">PORT\_STATUS\_TYPE\_ERROR</span></span>   | <span data-ttu-id="791c3-148">埠狀態值表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="791c3-148">The port status value indicates an error.</span></span> |
| <span data-ttu-id="791c3-149">埠 \_ 狀態 \_ 類型 \_ 警告</span><span class="sxs-lookup"><span data-stu-id="791c3-149">PORT\_STATUS\_TYPE\_WARNING</span></span> | <span data-ttu-id="791c3-150">埠狀態值是警告。</span><span class="sxs-lookup"><span data-stu-id="791c3-150">The port status value is a warning.</span></span>       |
| <span data-ttu-id="791c3-151">埠 \_ 狀態 \_ 類型 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="791c3-151">PORT\_STATUS\_TYPE\_INFO</span></span>    | <span data-ttu-id="791c3-152">埠狀態值為 [資訊]。</span><span class="sxs-lookup"><span data-stu-id="791c3-152">The port status value is informational.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="791c3-153">備註</span><span class="sxs-lookup"><span data-stu-id="791c3-153">Remarks</span></span>

<span data-ttu-id="791c3-154">當您設定 [印表機埠狀態值] 的 [嚴重性值埠 \_ 狀態 \_ 類型] \_ 錯誤時，列印多工緩衝處理器會停止將作業傳送至埠。</span><span class="sxs-lookup"><span data-stu-id="791c3-154">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="791c3-155">列印多工緩衝處理器不會繼續將作業傳送到埠，直到進行另一個 [**SetPort**](setport.md) 呼叫以清除狀態為止。</span><span class="sxs-lookup"><span data-stu-id="791c3-155">The print spooler does not resume sending jobs to the port until another [**SetPort**](setport.md) call is made to clear the status.</span></span>

## <a name="requirements"></a><span data-ttu-id="791c3-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="791c3-156">Requirements</span></span>



| <span data-ttu-id="791c3-157">需求</span><span class="sxs-lookup"><span data-stu-id="791c3-157">Requirement</span></span> | <span data-ttu-id="791c3-158">值</span><span class="sxs-lookup"><span data-stu-id="791c3-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="791c3-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="791c3-159">Minimum supported client</span></span><br/> | <span data-ttu-id="791c3-160">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="791c3-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="791c3-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="791c3-161">Minimum supported server</span></span><br/> | <span data-ttu-id="791c3-162">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="791c3-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="791c3-163">標頭</span><span class="sxs-lookup"><span data-stu-id="791c3-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="791c3-164"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="791c3-164"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="791c3-165">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="791c3-165">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="791c3-166">**\_ 埠 \_ 資訊 \_ 3w 法** (Unicode) 和 **\_ 埠 \_ 資訊 \_ 3a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="791c3-166">**\_PORT\_INFO\_3W** (Unicode) and **\_PORT\_INFO\_3A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="791c3-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="791c3-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="791c3-168">列印</span><span class="sxs-lookup"><span data-stu-id="791c3-168">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="791c3-169">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="791c3-169">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="791c3-170">**SetPort**</span><span class="sxs-lookup"><span data-stu-id="791c3-170">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




