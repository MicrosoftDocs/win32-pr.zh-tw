---
title: ORPC_DBG_BUFFER 結構
description: ORPC \_ DBG \_ 緩衝區結構是用來將 RPC 資料封送處理至 IOrpcDebugNotify 介面之方法的緩衝區格式。
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- ORPC_DBG_BUFFER 結構 COM
- PORPC_DBG_BUFFER 結構指標 COM
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969764"
---
# <a name="orpc_dbg_buffer-structure"></a><span data-ttu-id="954c8-105">ORPC \_ DBG \_ 緩衝區結構</span><span class="sxs-lookup"><span data-stu-id="954c8-105">ORPC\_DBG\_BUFFER structure</span></span>

<span data-ttu-id="954c8-106">**ORPC \_ DBG \_ 緩衝區** 結構是用來將 RPC 資料封送處理至 [**IOrpcDebugNotify**](iorpcdebugnotify.md)介面之方法的緩衝區格式。</span><span class="sxs-lookup"><span data-stu-id="954c8-106">The **ORPC\_DBG\_BUFFER** structure is the buffer format used to marshalled RPC data to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="954c8-107">語法</span><span class="sxs-lookup"><span data-stu-id="954c8-107">Syntax</span></span>


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a><span data-ttu-id="954c8-108">成員</span><span class="sxs-lookup"><span data-stu-id="954c8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="954c8-109">**alwaysOrSometimes**</span><span class="sxs-lookup"><span data-stu-id="954c8-109">**alwaysOrSometimes**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-110">控制偵錯工具產生的值。</span><span class="sxs-lookup"><span data-stu-id="954c8-110">A value that controls debugger spawning.</span></span> <span data-ttu-id="954c8-111">**alwaysOrSometimes** 可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="954c8-111">**alwaysOrSometimes** can be one of the following values:</span></span>



| <span data-ttu-id="954c8-112">值</span><span class="sxs-lookup"><span data-stu-id="954c8-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="954c8-113">意義</span><span class="sxs-lookup"><span data-stu-id="954c8-113">Meaning</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <span data-ttu-id="954c8-114"><dt>**ORPC \_DEBUG \_ ALWAYS**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="954c8-114"><dt>**ORPC\_DEBUG\_ALWAYS**</dt> <dt>0x00000000</dt></span></span> </dl>                              | <span data-ttu-id="954c8-115">如果設定，COM 一律會在接收者上引發用戶端或伺服器通知。</span><span class="sxs-lookup"><span data-stu-id="954c8-115">If set, COM will always raise the client or server notification on the receiver.</span></span><br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <span data-ttu-id="954c8-116"><dt>**ORPC \_\_如果 \_ \_ 已啟用**</dt>攔截，則進行調試 <dt></dt></span><span class="sxs-lookup"><span data-stu-id="954c8-116"><dt>**ORPC\_DEBUG\_IF\_HOOK\_ENABLED**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="954c8-117">如果設定，則只有在 **fTrace** 設為 **TRUE** 的情況下，藉由呼叫 DllDebugObjectRPCHook 中的 [](dlldebugobjectrpchook.md)來啟用 com 偵錯工具，com 才會在接收者上引發用戶端或伺服器通知。</span><span class="sxs-lookup"><span data-stu-id="954c8-117">If set, COM will only raise the client or server notification on the receiver if COM debugging has been enabled by calling [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in that process with **fTrace** set to **TRUE**.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="954c8-118">**>vermajor**</span><span class="sxs-lookup"><span data-stu-id="954c8-118">**verMajor**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-119">資料格式規格的主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="954c8-119">The major version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="954c8-120">**>verminor**</span><span class="sxs-lookup"><span data-stu-id="954c8-120">**verMinor**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-121">資料格式規格的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="954c8-121">The minor version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="954c8-122">**cbRemaining**</span><span class="sxs-lookup"><span data-stu-id="954c8-122">**cbRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-123">在此結構中遵循的位元組數目（包含 **cbRemaining**）。</span><span class="sxs-lookup"><span data-stu-id="954c8-123">The number of bytes, inclusive of **cbRemaining**, that follow in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="954c8-124">**guidSemantic**</span><span class="sxs-lookup"><span data-stu-id="954c8-124">**guidSemantic**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-125">GUID，可判斷下列等位的成員。</span><span class="sxs-lookup"><span data-stu-id="954c8-125">A GUID that determines which members of the union are present below.</span></span> <span data-ttu-id="954c8-126">**guidSemantic** 可以採用下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="954c8-126">**guidSemantic** can take one of the following values:</span></span>



| <span data-ttu-id="954c8-127">值</span><span class="sxs-lookup"><span data-stu-id="954c8-127">Value</span></span>                                                                                                           | <span data-ttu-id="954c8-128">意義</span><span class="sxs-lookup"><span data-stu-id="954c8-128">Meaning</span></span>                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="954c8-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span><span class="sxs-lookup"><span data-stu-id="954c8-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span></span> </dl> | <span data-ttu-id="954c8-130">判斷偵錯工具是否要執行單一逐步執行。</span><span class="sxs-lookup"><span data-stu-id="954c8-130">Determines if single stepping is to be performed by the debugger.</span></span> <span data-ttu-id="954c8-131">以下只會顯示聯集的 **fStopOnOtherSide** 成員。</span><span class="sxs-lookup"><span data-stu-id="954c8-131">Only the **fStopOnOtherSide** member of the union is present below.</span></span><br/>                                             |
| <dl> <span data-ttu-id="954c8-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="954c8-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="954c8-133">判斷是否要將 RPC 封送處理的資料和調試碼處理碼傳遞給接收者。</span><span class="sxs-lookup"><span data-stu-id="954c8-133">Determines if RPC marshalled data and debugging opcodes are passed to the receiver.</span></span> <span data-ttu-id="954c8-134">Union 的所有成員都存在於下方，但 **fStopOnOtherSide** 除外。</span><span class="sxs-lookup"><span data-stu-id="954c8-134">All of the members of the union are present below with the exception of **fStopOnOtherSide**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="954c8-135">**fStopOnOtherSide**</span><span class="sxs-lookup"><span data-stu-id="954c8-135">**fStopOnOtherSide**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-136">若 **為 TRUE**，則偵錯工具會執行單一逐步執行，並在到達另一端時，從伺服器跳過並繼續執行。</span><span class="sxs-lookup"><span data-stu-id="954c8-136">If **TRUE**, single stepping is performed by the debugger and it should step out of the server and continue execution once the other side is reached.</span></span> <span data-ttu-id="954c8-137">否則，不會執行單一逐步執行，而且偵錯工具會在另一端停止執行。</span><span class="sxs-lookup"><span data-stu-id="954c8-137">Otherwise, single stepping is not performed and debugger execution stops on the other side.</span></span>

</dd> <dt>

<span data-ttu-id="954c8-138">**wDebuggingOpCode**</span><span class="sxs-lookup"><span data-stu-id="954c8-138">**wDebuggingOpCode**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-139">值，允許指定一系列作業的其中一個。</span><span class="sxs-lookup"><span data-stu-id="954c8-139">A value that allows for one of a series of operations to be specified.</span></span> <span data-ttu-id="954c8-140">**wDebuggingOpCode** 可以採用下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="954c8-140">**wDebuggingOpCode** can take one of the following values:</span></span>



| <span data-ttu-id="954c8-141">值</span><span class="sxs-lookup"><span data-stu-id="954c8-141">Value</span></span>                                                                             | <span data-ttu-id="954c8-142">意義</span><span class="sxs-lookup"><span data-stu-id="954c8-142">Meaning</span></span>                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="954c8-143"><dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="954c8-143"><dt>0x0000</dt></span></span> </dl> | <span data-ttu-id="954c8-144">無作業。</span><span class="sxs-lookup"><span data-stu-id="954c8-144">No operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="954c8-145"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="954c8-145"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="954c8-146">如果設定，則在設定為 **TRUE** 時，單一步驟的語義與 **fStopOnOtherSide** 相同。</span><span class="sxs-lookup"><span data-stu-id="954c8-146">If set, single step semantics are identical to **fStopOnOtherSide** when set to **TRUE**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="954c8-147">**cExtent**</span><span class="sxs-lookup"><span data-stu-id="954c8-147">**cExtent**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-148">填充。</span><span class="sxs-lookup"><span data-stu-id="954c8-148">Padding.</span></span> <span data-ttu-id="954c8-149">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="954c8-149">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="954c8-150">**padding**</span><span class="sxs-lookup"><span data-stu-id="954c8-150">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-151">填充。</span><span class="sxs-lookup"><span data-stu-id="954c8-151">Padding.</span></span> <span data-ttu-id="954c8-152">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="954c8-152">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="954c8-153">**Cb**</span><span class="sxs-lookup"><span data-stu-id="954c8-153">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-154">**RgbData** 中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="954c8-154">The size, in bytes of the data in **rgbData**.</span></span>

</dd> <dt>

<span data-ttu-id="954c8-155">**guidExtent**</span><span class="sxs-lookup"><span data-stu-id="954c8-155">**guidExtent**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-156">判斷 **rgbData** 中之資料類型的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="954c8-156">A **GUID** that determines the type of data in **rgbData**.</span></span> <span data-ttu-id="954c8-157">**guidExtent** 可以採用下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="954c8-157">**guidExtent** can take one of the following values:</span></span>



| <span data-ttu-id="954c8-158">值</span><span class="sxs-lookup"><span data-stu-id="954c8-158">Value</span></span>                                                                                                           | <span data-ttu-id="954c8-159">意義</span><span class="sxs-lookup"><span data-stu-id="954c8-159">Meaning</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="954c8-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="954c8-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="954c8-161">**rgbData** 是已封送處理的介面指標。</span><span class="sxs-lookup"><span data-stu-id="954c8-161">**rgbData** is a marshalled interface pointer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="954c8-162">**rgbData**</span><span class="sxs-lookup"><span data-stu-id="954c8-162">**rgbData**</span></span>
</dt> <dd>

<span data-ttu-id="954c8-163">**位元組** 緩衝區，用來在用戶端與伺服器偵錯工具之間傳遞 RPC 封送處理的 COM 資料。</span><span class="sxs-lookup"><span data-stu-id="954c8-163">A **BYTE** buffer used to pass RPC marshalled COM data between the client and server debuggers.</span></span> <span data-ttu-id="954c8-164">**RgbData** 的內容取決於 **GuidExtent** 中的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="954c8-164">The contents of **rgbData** are determined by the **GUID** in **guidExtent**.</span></span>



| <span data-ttu-id="954c8-165">guidExtent 值</span><span class="sxs-lookup"><span data-stu-id="954c8-165">guidExtent Value</span></span>                     | <span data-ttu-id="954c8-166">rgbData 內容</span><span class="sxs-lookup"><span data-stu-id="954c8-166">rgbData contents</span></span>                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="954c8-167">53199051-57EB-11ce-A964-00AA006C3706</span><span class="sxs-lookup"><span data-stu-id="954c8-167">53199051-57EB-11ce-A964-00AA006C3706</span></span> | <span data-ttu-id="954c8-168">呼叫 [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)所產生的封送處理介面指標。</span><span class="sxs-lookup"><span data-stu-id="954c8-168">A marshalled interface pointer that results from calling [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span></span> <span data-ttu-id="954c8-169">已封送處理的指標會使用 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)轉換成其對應的介面指標。</span><span class="sxs-lookup"><span data-stu-id="954c8-169">The marshalled pointer is converted into its corresponding interface pointer using [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="954c8-170">備註</span><span class="sxs-lookup"><span data-stu-id="954c8-170">Remarks</span></span>

<span data-ttu-id="954c8-171">這個結構的成員具有1位元組的對齊方式，而且一律以位元組由小到大的順序傳輸。</span><span class="sxs-lookup"><span data-stu-id="954c8-171">This members of this structure have 1-byte alignment and are always transmitted in little-endian byte order.</span></span>

## <a name="requirements"></a><span data-ttu-id="954c8-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="954c8-172">Requirements</span></span>



| <span data-ttu-id="954c8-173">需求</span><span class="sxs-lookup"><span data-stu-id="954c8-173">Requirement</span></span> | <span data-ttu-id="954c8-174">值</span><span class="sxs-lookup"><span data-stu-id="954c8-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="954c8-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="954c8-175">Minimum supported client</span></span><br/> | <span data-ttu-id="954c8-176">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="954c8-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="954c8-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="954c8-177">Minimum supported server</span></span><br/> | <span data-ttu-id="954c8-178">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="954c8-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="954c8-179">標頭</span><span class="sxs-lookup"><span data-stu-id="954c8-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="954c8-180"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="954c8-180"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="954c8-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="954c8-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="954c8-182">**ORPC \_ DBG \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="954c8-182">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="954c8-183">**ORPC \_ INIT 引數 \_**</span><span class="sxs-lookup"><span data-stu-id="954c8-183">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="954c8-184">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="954c8-184">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="954c8-185">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="954c8-185">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





