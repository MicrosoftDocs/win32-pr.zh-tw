---
description: FileIo 類別-這個類別是檔案 i/o 事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: FileIo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716528902a115e23eae5b49ef572b87a71d11e25
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106526"
---
# <a name="fileio-class"></a><span data-ttu-id="8a49b-104">FileIo 類別</span><span class="sxs-lookup"><span data-stu-id="8a49b-104">FileIo class</span></span>

<span data-ttu-id="8a49b-105">這個類別是檔案 i/o 事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="8a49b-105">This class is the parent class for file I/O events.</span></span>

<span data-ttu-id="8a49b-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="8a49b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a49b-107">語法</span><span class="sxs-lookup"><span data-stu-id="8a49b-107">Syntax</span></span>

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="8a49b-108">成員</span><span class="sxs-lookup"><span data-stu-id="8a49b-108">Members</span></span>

<span data-ttu-id="8a49b-109">**FileIo** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="8a49b-109">The **FileIo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a49b-110">備註</span><span class="sxs-lookup"><span data-stu-id="8a49b-110">Remarks</span></span>

<span data-ttu-id="8a49b-111">若要在 NT 核心記錄會話中啟用檔案 IO 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標磁片檔案 \_ \_ \_ IO** 旗標。</span><span class="sxs-lookup"><span data-stu-id="8a49b-111">To enable the File IO events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="8a49b-112">您也可以指定下列一或多個旗標：</span><span class="sxs-lookup"><span data-stu-id="8a49b-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="8a49b-113">**事件 \_ 追蹤 \_ 旗標檔案 \_ \_ IO**</span><span class="sxs-lookup"><span data-stu-id="8a49b-113">**EVENT\_TRACE\_FLAG\_FILE\_IO**</span></span>
-   <span data-ttu-id="8a49b-114">**事件 \_ 追蹤 \_ 旗標檔案 \_ \_ IO \_ 初始化**</span><span class="sxs-lookup"><span data-stu-id="8a49b-114">**EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT**</span></span>

<span data-ttu-id="8a49b-115">事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**FileIoGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來執行檔案 i/o 事件的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="8a49b-115">Event trace consumers can implement special processing for file I/O events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**FileIoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="8a49b-116">使用下列事件種類來識別使用事件時的實際事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-116">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="8a49b-117">事件類型</span><span class="sxs-lookup"><span data-stu-id="8a49b-117">Event type</span></span>             | <span data-ttu-id="8a49b-118">描述</span><span class="sxs-lookup"><span data-stu-id="8a49b-118">Description</span></span>                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a49b-119">事件種類值為0</span><span class="sxs-lookup"><span data-stu-id="8a49b-119">Event type value is 0</span></span>  | <span data-ttu-id="8a49b-120">檔案名事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-120">File name event.</span></span> <span data-ttu-id="8a49b-121">[**FileIo \_ 名稱**](fileio-name.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-121">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                               |
| <span data-ttu-id="8a49b-122">事件種類值為32</span><span class="sxs-lookup"><span data-stu-id="8a49b-122">Event type value is 32</span></span> | <span data-ttu-id="8a49b-123">File create 事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-123">File create event.</span></span> <span data-ttu-id="8a49b-124">[**FileIo \_ 名稱**](fileio-name.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-124">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="8a49b-125">事件種類值為35</span><span class="sxs-lookup"><span data-stu-id="8a49b-125">Event type value is 35</span></span> | <span data-ttu-id="8a49b-126">檔案刪除事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-126">File delete event.</span></span> <span data-ttu-id="8a49b-127">[**FileIo \_ 名稱**](fileio-name.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-127">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="8a49b-128">事件種類值為36</span><span class="sxs-lookup"><span data-stu-id="8a49b-128">Event type value is 36</span></span> | <span data-ttu-id="8a49b-129">File 取消事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-129">File rundown event.</span></span> <span data-ttu-id="8a49b-130">列舉在追蹤會話結束時，電腦上所有開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="8a49b-130">Enumerates all open files on the computer at the end of the trace session.</span></span> <span data-ttu-id="8a49b-131">[**FileIo \_ 名稱**](fileio-name.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-131">The [**FileIo\_Name**](fileio-name.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="8a49b-132">事件種類值為64</span><span class="sxs-lookup"><span data-stu-id="8a49b-132">Event type value is 64</span></span> | <span data-ttu-id="8a49b-133">File create 事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-133">File create event.</span></span> <span data-ttu-id="8a49b-134">[**FileIo \_ Create**](fileio-create.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-134">The [**FileIo\_Create**](fileio-create.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="8a49b-135">事件種類值為72</span><span class="sxs-lookup"><span data-stu-id="8a49b-135">Event type value is 72</span></span> | <span data-ttu-id="8a49b-136">目錄列舉事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-136">Directory enumeration event.</span></span> <span data-ttu-id="8a49b-137">[**FileIo \_ DirEnum**](fileio-direnum.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-137">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                             |
| <span data-ttu-id="8a49b-138">事件種類值為77</span><span class="sxs-lookup"><span data-stu-id="8a49b-138">Event type value is 77</span></span> | <span data-ttu-id="8a49b-139">目錄通知事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-139">Directory notification event.</span></span> <span data-ttu-id="8a49b-140">[**FileIo \_ DirEnum**](fileio-direnum.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-140">The [**FileIo\_DirEnum**](fileio-direnum.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="8a49b-141">事件種類值為69</span><span class="sxs-lookup"><span data-stu-id="8a49b-141">Event type value is 69</span></span> | <span data-ttu-id="8a49b-142">設定資訊事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-142">Set information event.</span></span> <span data-ttu-id="8a49b-143">[**FileIo \_ 資訊**](fileio-info.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-143">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                         |
| <span data-ttu-id="8a49b-144">事件種類值為70</span><span class="sxs-lookup"><span data-stu-id="8a49b-144">Event type value is 70</span></span> | <span data-ttu-id="8a49b-145">刪除檔案事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-145">Delete file event.</span></span> <span data-ttu-id="8a49b-146">[**FileIo \_ 資訊**](fileio-info.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-146">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="8a49b-147">事件種類值為71</span><span class="sxs-lookup"><span data-stu-id="8a49b-147">Event type value is 71</span></span> | <span data-ttu-id="8a49b-148">重新命名檔案事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-148">Rename file event.</span></span> <span data-ttu-id="8a49b-149">[**FileIo \_ 資訊**](fileio-info.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-149">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                             |
| <span data-ttu-id="8a49b-150">事件種類值為74</span><span class="sxs-lookup"><span data-stu-id="8a49b-150">Event type value is 74</span></span> | <span data-ttu-id="8a49b-151">查詢檔案資訊事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-151">Query file information event.</span></span> <span data-ttu-id="8a49b-152">[**FileIo \_ 資訊**](fileio-info.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-152">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="8a49b-153">事件種類值為75</span><span class="sxs-lookup"><span data-stu-id="8a49b-153">Event type value is 75</span></span> | <span data-ttu-id="8a49b-154">檔案系統控制事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-154">File system control event.</span></span> <span data-ttu-id="8a49b-155">[**FileIo \_ 資訊**](fileio-info.md)MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-155">The [**FileIo\_Info**](fileio-info.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="8a49b-156">事件種類值為76</span><span class="sxs-lookup"><span data-stu-id="8a49b-156">Event type value is 76</span></span> | <span data-ttu-id="8a49b-157">作業結束事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-157">End of operation event.</span></span> <span data-ttu-id="8a49b-158">[**FileIo \_ OpEnd**](fileio-opend.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-158">The [**FileIo\_OpEnd**](fileio-opend.md) MOF class defines the event data for this event.</span></span>                                                                      |
| <span data-ttu-id="8a49b-159">事件種類值為67</span><span class="sxs-lookup"><span data-stu-id="8a49b-159">Event type value is 67</span></span> | <span data-ttu-id="8a49b-160">File read 事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-160">File read event.</span></span> <span data-ttu-id="8a49b-161">[**FileIo \_ ReadWrite**](fileio-readwrite.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-161">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                     |
| <span data-ttu-id="8a49b-162">事件種類值為68</span><span class="sxs-lookup"><span data-stu-id="8a49b-162">Event type value is 68</span></span> | <span data-ttu-id="8a49b-163">檔案寫入事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-163">File write event.</span></span> <span data-ttu-id="8a49b-164">[**FileIo \_ ReadWrite**](fileio-readwrite.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-164">The [**FileIo\_ReadWrite**](fileio-readwrite.md) MOF class defines the event data for this event.</span></span>                                                                    |
| <span data-ttu-id="8a49b-165">事件種類值為65</span><span class="sxs-lookup"><span data-stu-id="8a49b-165">Event type value is 65</span></span> | <span data-ttu-id="8a49b-166">清除事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-166">Clean up event.</span></span> <span data-ttu-id="8a49b-167">釋放檔案的最後一個控制碼時，就會產生此事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-167">The event is generated when the last handle to the file is released.</span></span> <span data-ttu-id="8a49b-168">[**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-168">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="8a49b-169">事件種類值為66</span><span class="sxs-lookup"><span data-stu-id="8a49b-169">Event type value is 66</span></span> | <span data-ttu-id="8a49b-170">關閉事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-170">Close event.</span></span> <span data-ttu-id="8a49b-171">釋放檔案物件時，就會產生此事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-171">The event is generated when the file object is freed.</span></span> <span data-ttu-id="8a49b-172">[**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-172">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>                     |
| <span data-ttu-id="8a49b-173">事件種類值為73</span><span class="sxs-lookup"><span data-stu-id="8a49b-173">Event type value is 73</span></span> | <span data-ttu-id="8a49b-174">Flush 事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-174">Flush event.</span></span> <span data-ttu-id="8a49b-175">當檔案緩衝區完全排清到磁片時，就會產生此事件。</span><span class="sxs-lookup"><span data-stu-id="8a49b-175">This event is generated when the file buffers are fully flushed to disk.</span></span> <span data-ttu-id="8a49b-176">[**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF 類別會定義此事件的事件資料。</span><span class="sxs-lookup"><span data-stu-id="8a49b-176">The [**FileIo\_SimpleOp**](fileio-simpleop.md) MOF class defines the event data for this event.</span></span>  |



 

<span data-ttu-id="8a49b-177">檔案 IO 事件是在作業開始時記錄。</span><span class="sxs-lookup"><span data-stu-id="8a49b-177">File IO events are logged at the beginning of the operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a49b-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a49b-178">Requirements</span></span>



| <span data-ttu-id="8a49b-179">需求</span><span class="sxs-lookup"><span data-stu-id="8a49b-179">Requirement</span></span> | <span data-ttu-id="8a49b-180">值</span><span class="sxs-lookup"><span data-stu-id="8a49b-180">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a49b-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a49b-181">Minimum supported client</span></span><br/> | <span data-ttu-id="8a49b-182">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a49b-182">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8a49b-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a49b-183">Minimum supported server</span></span><br/> | <span data-ttu-id="8a49b-184">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a49b-184">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a49b-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a49b-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a49b-186">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="8a49b-186">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="8a49b-187">**FileIo \_ V0**</span><span class="sxs-lookup"><span data-stu-id="8a49b-187">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> <dt>

[<span data-ttu-id="8a49b-188">**FileIo \_ V1**</span><span class="sxs-lookup"><span data-stu-id="8a49b-188">**FileIo\_V1**</span></span>](fileio-v1.md)
</dt> </dl>

 

 
