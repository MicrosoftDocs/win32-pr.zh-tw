---
description: NMEVENTDATA 結構包含事件條件的相關資訊，該條件會傳遞給網路監視器，以在專家檢視器中插入一行。
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: 'NMEVENTDATA 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848247"
---
# <a name="nmeventdata-structure"></a><span data-ttu-id="2f060-103">NMEVENTDATA 結構</span><span class="sxs-lookup"><span data-stu-id="2f060-103">NMEVENTDATA structure</span></span>

<span data-ttu-id="2f060-104">**NMEVENTDATA** 結構包含事件條件的相關資訊，該條件會傳遞給網路監視器，以在專家檢視器中插入一行。</span><span class="sxs-lookup"><span data-stu-id="2f060-104">The **NMEVENTDATA** structure contains information about an event condition that is passed to Network Monitor to insert a line in the expert viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f060-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f060-105">Syntax</span></span>


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a><span data-ttu-id="2f060-106">成員</span><span class="sxs-lookup"><span data-stu-id="2f060-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2f060-107">**版本**</span><span class="sxs-lookup"><span data-stu-id="2f060-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-108">**NMEVENTDATA** 結構的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="2f060-108">Version number of the **NMEVENTDATA** structure.</span></span> <span data-ttu-id="2f060-109">版本號碼必須為零。</span><span class="sxs-lookup"><span data-stu-id="2f060-109">The version number must be zero.</span></span> <span data-ttu-id="2f060-110">網路監視器的未來版本可能會支援較高的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="2f060-110">Future versions of Network Monitor may support a higher version number.</span></span>

</dd> <dt>

<span data-ttu-id="2f060-111">**EventIdent**</span><span class="sxs-lookup"><span data-stu-id="2f060-111">**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-112">事件的識別項。</span><span class="sxs-lookup"><span data-stu-id="2f060-112">Identifier of the event.</span></span> <span data-ttu-id="2f060-113">**EventIdent** 對每個專家都是唯一的，並參考 [事件參考頁面](event-reference-page.md)。</span><span class="sxs-lookup"><span data-stu-id="2f060-113">**EventIdent** is unique to each expert, and references an [event reference page](event-reference-page.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f060-114">**旗標**</span><span class="sxs-lookup"><span data-stu-id="2f060-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-115">一組旗標，描述傳送事件資料的物件，以及事件的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="2f060-115">A set of flags that describes who sends the event data, and how the event is displayed.</span></span>



| <span data-ttu-id="2f060-116">值</span><span class="sxs-lookup"><span data-stu-id="2f060-116">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="2f060-117">意義</span><span class="sxs-lookup"><span data-stu-id="2f060-117">Meaning</span></span>                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <span data-ttu-id="2f060-118"><dt>**事件 \_ 旗標 \_ 專家**</dt></span><span class="sxs-lookup"><span data-stu-id="2f060-118"><dt>**EVENT\_FLAG\_EXPERT**</dt></span></span> </dl>                                                                         | <span data-ttu-id="2f060-119">活動來自專家。</span><span class="sxs-lookup"><span data-stu-id="2f060-119">The event came from an expert.</span></span> <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <span data-ttu-id="2f060-120"><dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 嚴重性**</dt></span><span class="sxs-lookup"><span data-stu-id="2f060-120"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SEVERITY**</dt></span></span> </dl>                 | <span data-ttu-id="2f060-121">不要顯示事件的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="2f060-121">Do not display the severity level for the event.</span></span> <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <span data-ttu-id="2f060-122"><dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 來源**</dt></span><span class="sxs-lookup"><span data-stu-id="2f060-122"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SOURCE**</dt></span></span> </dl>                       | <span data-ttu-id="2f060-123">不要顯示事件的來源名稱。</span><span class="sxs-lookup"><span data-stu-id="2f060-123">Do not display the source name for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <span data-ttu-id="2f060-124"><dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 事件 \_ 名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="2f060-124"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_EVENT\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="2f060-125">不要顯示事件的事件名稱。</span><span class="sxs-lookup"><span data-stu-id="2f060-125">Do not display the event name for the event.</span></span> <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <span data-ttu-id="2f060-126"><dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 描述**</dt></span><span class="sxs-lookup"><span data-stu-id="2f060-126"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_DESCRIPTION**</dt></span></span> </dl>        | <span data-ttu-id="2f060-127">不要顯示事件的描述。</span><span class="sxs-lookup"><span data-stu-id="2f060-127">Do not display the description for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <span data-ttu-id="2f060-128"><dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 電腦**</dt></span><span class="sxs-lookup"><span data-stu-id="2f060-128"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_MACHINE**</dt></span></span> </dl>                    | <span data-ttu-id="2f060-129">不要顯示事件的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="2f060-129">Do not display the machine name for the event.</span></span> <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <span data-ttu-id="2f060-130"><dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 時間**</dt></span><span class="sxs-lookup"><span data-stu-id="2f060-130"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_TIME**</dt></span></span> </dl>                             | <span data-ttu-id="2f060-131">不顯示事件的時間</span><span class="sxs-lookup"><span data-stu-id="2f060-131">Do not display the time for the event</span></span> <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <span data-ttu-id="2f060-132"><dt>**NMEVENTFLAG \_ 不 \_ \_ 顯示 \_ 固定 \_ 的資料行**</dt></span><span class="sxs-lookup"><span data-stu-id="2f060-132"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_FIXED\_COLUMNS**</dt></span></span> </dl> | <span data-ttu-id="2f060-133">不要顯示 [嚴重性]、[來源]、[事件名稱]、[描述]、[電腦] 或 [時間] 欄。</span><span class="sxs-lookup"><span data-stu-id="2f060-133">Do not display the Severity, Source, Event Name, Description, Machine, or Time columns.</span></span> <span data-ttu-id="2f060-134">這不是單一旗標，但它是前六個旗標的聯集。</span><span class="sxs-lookup"><span data-stu-id="2f060-134">This is not a single flag, but it is a union of the previous six flags.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="2f060-135">**嚴重性**</span><span class="sxs-lookup"><span data-stu-id="2f060-135">**Severity**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-136">事件的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="2f060-136">Severity level of the event.</span></span> <span data-ttu-id="2f060-137">嚴重性層級可以具有下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="2f060-137">The severity level can have one of the following values:</span></span>

<span data-ttu-id="2f060-138">NMEVENT \_ 嚴重性 \_ 資訊 NMEVENT \_ 嚴重性 \_ 警告 NMEVENT \_ 嚴重性 \_ 強烈 \_ 警告 NMEVENT \_ 嚴重性 \_ 錯誤 NMEVENT \_ 嚴重性 \_ 嚴重 \_ 錯誤 NMEVENT \_ 嚴重性 \_ 嚴重 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="2f060-138">NMEVENT\_SEVERITY\_INFORMATIONAL NMEVENT\_SEVERITY\_WARNING NMEVENT\_SEVERITY\_STRONG\_WARNING NMEVENT\_SEVERITY\_ERROR NMEVENT\_SEVERITY\_SEVERE\_ERROR NMEVENT\_SEVERITY\_CRITICAL\_ERROR</span></span>

</dd> <dt>

<span data-ttu-id="2f060-139">**NumColumns**</span><span class="sxs-lookup"><span data-stu-id="2f060-139">**NumColumns**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-140">目前結構中所指定的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="2f060-140">Number of columns designated in the current structure.</span></span>

</dd> <dt>

<span data-ttu-id="2f060-141">**szSourceName**</span><span class="sxs-lookup"><span data-stu-id="2f060-141">**szSourceName**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-142">顯示之專家的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f060-142">Name of the expert that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="2f060-143">**szEventName**</span><span class="sxs-lookup"><span data-stu-id="2f060-143">**szEventName**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-144">顯示之事件的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f060-144">Name of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="2f060-145">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="2f060-145">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-146">所顯示事件的描述。</span><span class="sxs-lookup"><span data-stu-id="2f060-146">Description of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="2f060-147">**szMachine**</span><span class="sxs-lookup"><span data-stu-id="2f060-147">**szMachine**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-148">已淘汰，應為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f060-148">Obsolete, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2f060-149">**理由**</span><span class="sxs-lookup"><span data-stu-id="2f060-149">**Justification**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-150">事件檢視器的第二個視窗中顯示的資訊。</span><span class="sxs-lookup"><span data-stu-id="2f060-150">Information displayed in the second window of the Event Viewer.</span></span> <span data-ttu-id="2f060-151">**理由** 成員可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f060-151">The **Justification** member may be **NULL**.</span></span> <span data-ttu-id="2f060-152">如果是 **Null**，則不會顯示第二個視窗。</span><span class="sxs-lookup"><span data-stu-id="2f060-152">If it is **NULL**, the second window is not be visible.</span></span>

</dd> <dt>

<span data-ttu-id="2f060-153">**szUrl**</span><span class="sxs-lookup"><span data-stu-id="2f060-153">**szUrl**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-154">保護此成員必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f060-154">Reserved; this member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2f060-155">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="2f060-155">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-156">發生事件條件的時間。</span><span class="sxs-lookup"><span data-stu-id="2f060-156">Time at which the event condition occurs.</span></span> <span data-ttu-id="2f060-157">時間是相對於捕捉的開頭來測量。</span><span class="sxs-lookup"><span data-stu-id="2f060-157">The time is measured relative to the beginning of the capture.</span></span>

</dd> <dt>

<span data-ttu-id="2f060-158">**資料行**</span><span class="sxs-lookup"><span data-stu-id="2f060-158">**Column**</span></span>
</dt> <dd>

<span data-ttu-id="2f060-159">出現在事件檢視器上方窗格中的資料行結構資料表。</span><span class="sxs-lookup"><span data-stu-id="2f060-159">Table of column structures that appears in the top pane of the Event Viewer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f060-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f060-160">Requirements</span></span>



| <span data-ttu-id="2f060-161">需求</span><span class="sxs-lookup"><span data-stu-id="2f060-161">Requirement</span></span> | <span data-ttu-id="2f060-162">值</span><span class="sxs-lookup"><span data-stu-id="2f060-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2f060-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f060-163">Minimum supported client</span></span><br/> | <span data-ttu-id="2f060-164">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f060-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2f060-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f060-165">Minimum supported server</span></span><br/> | <span data-ttu-id="2f060-166">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f060-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2f060-167">標頭</span><span class="sxs-lookup"><span data-stu-id="2f060-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f060-168"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="2f060-168"><dt>Netmon.h</dt></span></span> </dl> |



 

 




