---
title: 'WM_DDE_EXECUTE 訊息 (的) '
description: 動態資料交換 (DDE) 用戶端應用程式會將 WM \_ DDE \_ 執行訊息張貼至 dde 伺服器應用程式，以將字串傳送至要以一連串命令的形式處理的伺服器。
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- WM_DDE_EXECUTE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384785"
---
# <a name="wm_dde_execute-message"></a><span data-ttu-id="c13c8-104">WM \_ DDE \_ 執行訊息</span><span class="sxs-lookup"><span data-stu-id="c13c8-104">WM\_DDE\_EXECUTE message</span></span>

<span data-ttu-id="c13c8-105">動態資料交換 (DDE) 用戶端應用程式會將 **WM \_ DDE \_ 執行** 訊息張貼至 dde 伺服器應用程式，以將字串傳送至要以一連串命令的形式處理的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c13c8-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_EXECUTE** message to a DDE server application to send a string to the server to be processed as a series of commands.</span></span> <span data-ttu-id="c13c8-106">伺服器應用程式預期會在回應中公佈一則 [**WM 的 \_ DDE \_ ACK**](wm-dde-ack.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="c13c8-106">The server application is expected to post a [**WM\_DDE\_ACK**](wm-dde-ack.md) message in response.</span></span>

<span data-ttu-id="c13c8-107">若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="c13c8-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a><span data-ttu-id="c13c8-108">參數</span><span class="sxs-lookup"><span data-stu-id="c13c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c13c8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c13c8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c13c8-110">張貼訊息之用戶端視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c13c8-110">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="c13c8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c13c8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c13c8-112">包含參考 ANSI 或 Unicode 命令字串的全域記憶體物件，視交談中涉及的 windows 類型而定。</span><span class="sxs-lookup"><span data-stu-id="c13c8-112">Contains a global memory object that references an ANSI or Unicode command string, depending on the types of windows involved in the conversation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c13c8-113">備註</span><span class="sxs-lookup"><span data-stu-id="c13c8-113">Remarks</span></span>

<span data-ttu-id="c13c8-114">命令字串是以 null 終止的字串，其中包含一個或多個以單一括弧括住的 opcode 字串 (\[ \]) 。</span><span class="sxs-lookup"><span data-stu-id="c13c8-114">The command string is a null-terminated string consisting of one or more opcode strings enclosed in single brackets (\[ \]).</span></span> <span data-ttu-id="c13c8-115">每個 opcode 字串都有下列語法，其中 *參數* 清單是選擇性的：</span><span class="sxs-lookup"><span data-stu-id="c13c8-115">Each opcode string has the following syntax, where the *parameters* list is optional:</span></span>

<span data-ttu-id="c13c8-116">*opcode 參數*</span><span class="sxs-lookup"><span data-stu-id="c13c8-116">*opcode parameters*</span></span>

<span data-ttu-id="c13c8-117">*Opcode* 是任何應用程式定義的單一 token。</span><span class="sxs-lookup"><span data-stu-id="c13c8-117">The *opcode* is any application-defined single token.</span></span> <span data-ttu-id="c13c8-118">它不能包含空格、逗號、括弧、方括弧或引號。</span><span class="sxs-lookup"><span data-stu-id="c13c8-118">It cannot include spaces, commas, parentheses, brackets, or quotation marks.</span></span>

<span data-ttu-id="c13c8-119">[ *參數* ] 清單可以包含任何應用程式定義的值或值。</span><span class="sxs-lookup"><span data-stu-id="c13c8-119">The *parameters* list can contain any application-defined value or values.</span></span> <span data-ttu-id="c13c8-120">多個參數會以逗號分隔，而整個參數清單會以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="c13c8-120">Multiple parameters are separated by commas, and the entire parameter list is enclosed in parentheses.</span></span> <span data-ttu-id="c13c8-121">參數不能包含逗號或括弧，除非在加上引號的字串內。</span><span class="sxs-lookup"><span data-stu-id="c13c8-121">Parameters cannot include commas or parentheses except inside a quoted string.</span></span> <span data-ttu-id="c13c8-122">如果括弧或括弧字元要出現在加上引號的字串中，則不需要加倍，如同舊規則下的案例。</span><span class="sxs-lookup"><span data-stu-id="c13c8-122">If a bracket or parenthesis character is to appear in a quoted string, it need not be doubled, as was the case under the old rules.</span></span>

<span data-ttu-id="c13c8-123">以下是有效的命令字串：</span><span class="sxs-lookup"><span data-stu-id="c13c8-123">The following are valid command strings:</span></span>


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



<span data-ttu-id="c13c8-124">請注意，在舊規則下，括弧和括弧必須加倍，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c13c8-124">Note that, under the old rules, parentheses and brackets had to be doubled, as follows:</span></span>


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



<span data-ttu-id="c13c8-125">伺服器應該能夠以任一形式剖析命令。</span><span class="sxs-lookup"><span data-stu-id="c13c8-125">Servers should be able to parse commands in either form.</span></span>

<span data-ttu-id="c13c8-126">只有當用戶端和伺服器視窗的控制碼造成 [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) 函數傳回 **TRUE** 時，才應該使用 Unicode 執行字串。</span><span class="sxs-lookup"><span data-stu-id="c13c8-126">Unicode execute strings should be used only when both the client and server window handles cause the [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) function to return **TRUE**.</span></span>

### <a name="posting"></a><span data-ttu-id="c13c8-127">張貼</span><span class="sxs-lookup"><span data-stu-id="c13c8-127">Posting</span></span>

<span data-ttu-id="c13c8-128">用戶端應用程式會藉由呼叫 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函數來配置全域記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="c13c8-128">The client application allocates the global memory object by calling the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span>

<span data-ttu-id="c13c8-129">當您處理伺服器張貼至 **wm dde \_ \_ 執行** 訊息的「 [**wm \_ dde \_**](wm-dde-ack.md)通知」訊息時，用戶端應用程式必須刪除 **wm \_ dde \_ ack** 訊息所傳回的物件。</span><span class="sxs-lookup"><span data-stu-id="c13c8-129">When processing the [**WM\_DDE\_ACK**](wm-dde-ack.md) message that the server posts in reply to a **WM\_DDE\_EXECUTE** message, the client application must delete the object returned by the **WM\_DDE\_ACK** message.</span></span>

### <a name="receiving"></a><span data-ttu-id="c13c8-130">接收</span><span class="sxs-lookup"><span data-stu-id="c13c8-130">Receiving</span></span>

<span data-ttu-id="c13c8-131">伺服器應用程式會張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，以回應正面或負面。</span><span class="sxs-lookup"><span data-stu-id="c13c8-131">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="c13c8-132">伺服器應重複使用全域記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="c13c8-132">The server should reuse the global memory object.</span></span>

<span data-ttu-id="c13c8-133">除非子通訊協定另有指定，否則伺服器不應張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，直到執行命令字串指定的所有動作都完成為止。</span><span class="sxs-lookup"><span data-stu-id="c13c8-133">Unless specified otherwise by a sub-protocol, the server should not post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message until all the actions specified by the execute command string are completed.</span></span> <span data-ttu-id="c13c8-134">這項規則的唯一例外狀況是當字串導致伺服器終止交談時。</span><span class="sxs-lookup"><span data-stu-id="c13c8-134">The one exception to this rule is when the string causes the server to terminate the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c13c8-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="c13c8-135">Requirements</span></span>



| <span data-ttu-id="c13c8-136">需求</span><span class="sxs-lookup"><span data-stu-id="c13c8-136">Requirement</span></span> | <span data-ttu-id="c13c8-137">值</span><span class="sxs-lookup"><span data-stu-id="c13c8-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c13c8-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c13c8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c13c8-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c13c8-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c13c8-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c13c8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c13c8-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c13c8-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c13c8-142">標頭</span><span class="sxs-lookup"><span data-stu-id="c13c8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c13c8-143"><dt> (包含 Windows. h) </dt></span><span class="sxs-lookup"><span data-stu-id="c13c8-143"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c13c8-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c13c8-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="c13c8-145">**參考**</span><span class="sxs-lookup"><span data-stu-id="c13c8-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c13c8-146">**IsWindowUnicode**</span><span class="sxs-lookup"><span data-stu-id="c13c8-146">**IsWindowUnicode**</span></span>](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[<span data-ttu-id="c13c8-147">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="c13c8-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="c13c8-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="c13c8-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="c13c8-149">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="c13c8-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="c13c8-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="c13c8-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="c13c8-151">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="c13c8-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="c13c8-152">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="c13c8-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="c13c8-153">**概念**</span><span class="sxs-lookup"><span data-stu-id="c13c8-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c13c8-154">關於動態資料交換</span><span class="sxs-lookup"><span data-stu-id="c13c8-154">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

