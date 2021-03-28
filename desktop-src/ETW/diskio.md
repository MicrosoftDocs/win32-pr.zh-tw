---
description: 這個類別是磁片 i/o 事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: DiskIo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 97f9907e4da51675bb1a5f562931e471ee0e133e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943251"
---
# <a name="diskio-class"></a><span data-ttu-id="87fe2-104">DiskIo 類別</span><span class="sxs-lookup"><span data-stu-id="87fe2-104">DiskIo class</span></span>

<span data-ttu-id="87fe2-105">這個類別是磁片 i/o 事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="87fe2-105">This class is the parent class for disk I/O events.</span></span>

<span data-ttu-id="87fe2-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="87fe2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="87fe2-107">語法</span><span class="sxs-lookup"><span data-stu-id="87fe2-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="87fe2-108">成員</span><span class="sxs-lookup"><span data-stu-id="87fe2-108">Members</span></span>

<span data-ttu-id="87fe2-109">**DiskIo** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="87fe2-109">The **DiskIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="87fe2-110">備註</span><span class="sxs-lookup"><span data-stu-id="87fe2-110">Remarks</span></span>

<span data-ttu-id="87fe2-111">若要在 NT 核心記錄會話中啟用磁片 i/o 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 磁片 \_ IO** 旗標。</span><span class="sxs-lookup"><span data-stu-id="87fe2-111">To enable disk I/0 events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="87fe2-112">您也可以指定下列一或多個旗標：</span><span class="sxs-lookup"><span data-stu-id="87fe2-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="87fe2-113">**事件 \_ 追蹤 \_ 旗標 \_ 磁片 \_ IO \_ 初始化**</span><span class="sxs-lookup"><span data-stu-id="87fe2-113">**EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT**</span></span>
-   <span data-ttu-id="87fe2-114">**事件 \_ 追蹤 \_ 旗標 \_ 驅動程式**</span><span class="sxs-lookup"><span data-stu-id="87fe2-114">**EVENT\_TRACE\_FLAG\_DRIVER**</span></span>

<span data-ttu-id="87fe2-115">事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**DiskIoGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來為磁片 i/o 事件執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="87fe2-115">Event trace consumers can implement special processing for disk I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**DiskIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="87fe2-116">使用下列事件種類來識別使用事件時的實際磁片 i/o 事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-116">Use the following event types to identify the actual disk I/O event when consuming events.</span></span>



| <span data-ttu-id="87fe2-117">事件類型</span><span class="sxs-lookup"><span data-stu-id="87fe2-117">Event type</span></span>                                                                      | <span data-ttu-id="87fe2-118">描述</span><span class="sxs-lookup"><span data-stu-id="87fe2-118">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87fe2-119">**活動 \_追蹤 \_ 類型 \_ IO \_ 讀取** (事件種類值為 10) </span><span class="sxs-lookup"><span data-stu-id="87fe2-119">**EVENT\_TRACE\_TYPE\_IO\_READ**(Event type value is 10)</span></span><br/>             | <span data-ttu-id="87fe2-120">讀取事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-120">Read event.</span></span> <span data-ttu-id="87fe2-121">[**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-121">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                              |
| <span data-ttu-id="87fe2-122">**活動 \_追蹤 \_ 類型 \_ IO \_ 寫入** (事件種類值為 11) </span><span class="sxs-lookup"><span data-stu-id="87fe2-122">**EVENT\_TRACE\_TYPE\_IO\_WRITE**(Event type value is 11)</span></span><br/>            | <span data-ttu-id="87fe2-123">寫入事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-123">Write event.</span></span> <span data-ttu-id="87fe2-124">[**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-124">The [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) MOF class defines the event data for this event.</span></span>                                             |
| <span data-ttu-id="87fe2-125">**活動 \_追蹤 \_ 類型 \_ IO \_ READ \_ INIT** (事件種類值為 12) </span><span class="sxs-lookup"><span data-stu-id="87fe2-125">**EVENT\_TRACE\_TYPE\_IO\_READ\_INIT**(Event type value is 12)</span></span><br/>       | <span data-ttu-id="87fe2-126">初始化讀取事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-126">Initialize read event.</span></span> <span data-ttu-id="87fe2-127">[**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-127">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="87fe2-128">**活動 \_追蹤 \_ 類型 \_ IO \_ WRITE \_ INIT** (事件種類值為 13) </span><span class="sxs-lookup"><span data-stu-id="87fe2-128">**EVENT\_TRACE\_TYPE\_IO\_WRITE\_INIT**(Event type value is 13)</span></span><br/>      | <span data-ttu-id="87fe2-129">初始化寫入事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-129">Initialize write event.</span></span> <span data-ttu-id="87fe2-130">[**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-130">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="87fe2-131">**活動 \_追蹤 \_ 類型 \_ IO \_ FLUSH** (事件種類值為 14) </span><span class="sxs-lookup"><span data-stu-id="87fe2-131">**EVENT\_TRACE\_TYPE\_IO\_FLUSH**(Event type value is 14)</span></span><br/>            | <span data-ttu-id="87fe2-132">初始化寫入事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-132">Initialize write event.</span></span> <span data-ttu-id="87fe2-133">[**DiskIo \_ TypeGroup3**](diskio-typegroup3.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-133">The [**DiskIo\_TypeGroup3**](diskio-typegroup3.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="87fe2-134">**活動 \_追蹤 \_ 類型 \_ IO \_ FLUSH \_ INIT** (事件種類值為 15) </span><span class="sxs-lookup"><span data-stu-id="87fe2-134">**EVENT\_TRACE\_TYPE\_IO\_FLUSH\_INIT**(Event type value is 15)</span></span><br/>      | <span data-ttu-id="87fe2-135">初始化 flush 事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-135">Initialize flush event.</span></span> <span data-ttu-id="87fe2-136">[**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-136">The [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="87fe2-137">**活動 \_追蹤 \_ 類型 \_ IO 重新 \_ 導向 \_ INIT** (事件種類值為 16) </span><span class="sxs-lookup"><span data-stu-id="87fe2-137">**EVENT\_TRACE\_TYPE\_IO\_REDIRECTED\_INIT**(Event type value is 16)</span></span><br/> | <span data-ttu-id="87fe2-138">初始化重新導向的事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-138">Initialize redirected event.</span></span> <span data-ttu-id="87fe2-139">重新導向的 IO 事件可用來將磁片 Io 對應到 Windows Imaging 格式 (WIM) 到 WIM 內的檔案名。</span><span class="sxs-lookup"><span data-stu-id="87fe2-139">Redirected IO events are used to map disk IOs to a Windows Imaging Format (WIM) to the filename within the WIM.</span></span>                  |
| <span data-ttu-id="87fe2-140">事件種類值為52</span><span class="sxs-lookup"><span data-stu-id="87fe2-140">Event type value is 52</span></span><br/>                                               | <span data-ttu-id="87fe2-141">驅動程式完成要求事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-141">Driver complete request event.</span></span> <span data-ttu-id="87fe2-142">[**DriverCompleteRequest**](drivercompleterequest.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-142">The [**DriverCompleteRequest**](drivercompleterequest.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="87fe2-143">事件種類值為53</span><span class="sxs-lookup"><span data-stu-id="87fe2-143">Event type value is 53</span></span><br/>                                               | <span data-ttu-id="87fe2-144">驅動程式完成要求傳回事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-144">Driver complete request return event.</span></span> <span data-ttu-id="87fe2-145">[**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-145">The [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="87fe2-146">事件種類值為37</span><span class="sxs-lookup"><span data-stu-id="87fe2-146">Event type value is 37</span></span><br/>                                               | <span data-ttu-id="87fe2-147">驅動程式完成常式事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-147">Driver completion routine event.</span></span> <span data-ttu-id="87fe2-148">[**DriverCompletionRoutine**](drivercompletionroutine.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-148">The [**DriverCompletionRoutine**](drivercompletionroutine.md) MOF class defines the event data for this event.</span></span>              |
| <span data-ttu-id="87fe2-149">事件種類值為34</span><span class="sxs-lookup"><span data-stu-id="87fe2-149">Event type value is 34</span></span><br/>                                               | <span data-ttu-id="87fe2-150">驅動程式主要函式呼叫事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-150">Driver major function call event.</span></span> <span data-ttu-id="87fe2-151">[**DriverMajorFunctionCall**](drivermajorfunctioncall.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-151">The [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) MOF class defines the event data for this event.</span></span>             |
| <span data-ttu-id="87fe2-152">事件種類值為35</span><span class="sxs-lookup"><span data-stu-id="87fe2-152">Event type value is 35</span></span><br/>                                               | <span data-ttu-id="87fe2-153">驅動程式主要函式呼叫傳回事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-153">Driver major function call return event.</span></span> <span data-ttu-id="87fe2-154">[**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="87fe2-154">The [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="87fe2-155">磁片 i/o 提供者無法識別磁片 i/o 事件期間所讀取或寫入的檔案。</span><span class="sxs-lookup"><span data-stu-id="87fe2-155">The disk I/0 provider cannot identify which file is read or written during a disk I/O event.</span></span> <span data-ttu-id="87fe2-156">若要抓取與磁片 i/o 事件相關聯的檔案名，請啟用 file I/0 事件提供者。</span><span class="sxs-lookup"><span data-stu-id="87fe2-156">To retrieve the name of the file associated with the disk I/O event, enable the file I/0 event provider.</span></span>

<span data-ttu-id="87fe2-157">系統會在 i/o 完成時間記錄磁片 i/o 事件。</span><span class="sxs-lookup"><span data-stu-id="87fe2-157">Disk I/O events are recorded at the I/O completion time.</span></span> <span data-ttu-id="87fe2-158">若要判斷 i/o 作業的開始時間，請使用初始化事件，例如事件 \_ 追蹤 \_ 類型 \_ IO \_ READ \_ INIT。</span><span class="sxs-lookup"><span data-stu-id="87fe2-158">To determine when the I/O operation began, use the initialization events, for example, EVENT\_TRACE\_TYPE\_IO\_READ\_INIT.</span></span>

## <a name="requirements"></a><span data-ttu-id="87fe2-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="87fe2-159">Requirements</span></span>



| <span data-ttu-id="87fe2-160">需求</span><span class="sxs-lookup"><span data-stu-id="87fe2-160">Requirement</span></span> | <span data-ttu-id="87fe2-161">值</span><span class="sxs-lookup"><span data-stu-id="87fe2-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87fe2-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87fe2-162">Minimum supported client</span></span><br/> | <span data-ttu-id="87fe2-163">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87fe2-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="87fe2-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87fe2-164">Minimum supported server</span></span><br/> | <span data-ttu-id="87fe2-165">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87fe2-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87fe2-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87fe2-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87fe2-167">**DiskIo \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="87fe2-167">**DiskIo\_TypeGroup1**</span></span>](diskio-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="87fe2-168">**DiskIo \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="87fe2-168">**DiskIo\_TypeGroup2**</span></span>](diskio-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="87fe2-169">**DiskIo \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="87fe2-169">**DiskIo\_TypeGroup3**</span></span>](diskio-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="87fe2-170">**DriverCompleteRequest**</span><span class="sxs-lookup"><span data-stu-id="87fe2-170">**DriverCompleteRequest**</span></span>](drivercompleterequest.md)
</dt> <dt>

[<span data-ttu-id="87fe2-171">**DriverCompleteRequestReturn**</span><span class="sxs-lookup"><span data-stu-id="87fe2-171">**DriverCompleteRequestReturn**</span></span>](drivercompleterequestreturn.md)
</dt> <dt>

[<span data-ttu-id="87fe2-172">**DriverCompletionRoutine**</span><span class="sxs-lookup"><span data-stu-id="87fe2-172">**DriverCompletionRoutine**</span></span>](drivercompletionroutine.md)
</dt> <dt>

[<span data-ttu-id="87fe2-173">**DriverMajorFunctionCall**</span><span class="sxs-lookup"><span data-stu-id="87fe2-173">**DriverMajorFunctionCall**</span></span>](drivermajorfunctioncall.md)
</dt> <dt>

[<span data-ttu-id="87fe2-174">**DriverMajorFunctionReturn**</span><span class="sxs-lookup"><span data-stu-id="87fe2-174">**DriverMajorFunctionReturn**</span></span>](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
