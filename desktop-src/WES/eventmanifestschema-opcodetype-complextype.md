---
title: OpcodeType 複雜類型
description: 定義應用程式元件內的作業。
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- OpcodeType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106025"
---
# <a name="opcodetype-complex-type"></a><span data-ttu-id="c1185-104">OpcodeType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="c1185-104">OpcodeType Complex Type</span></span>

<span data-ttu-id="c1185-105">定義應用程式元件內的作業。</span><span class="sxs-lookup"><span data-stu-id="c1185-105">Defines an operation within a component of the application.</span></span> <span data-ttu-id="c1185-106">搭配工作使用，以識別正在記錄事件的應用程式區段。</span><span class="sxs-lookup"><span data-stu-id="c1185-106">Used in conjunction with a task to identify the section of the application that is logging the event.</span></span>

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="mofValue"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="c1185-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c1185-107">Attributes</span></span>



| <span data-ttu-id="c1185-108">名稱</span><span class="sxs-lookup"><span data-stu-id="c1185-108">Name</span></span>     | <span data-ttu-id="c1185-109">類型</span><span class="sxs-lookup"><span data-stu-id="c1185-109">Type</span></span>                                                              | <span data-ttu-id="c1185-110">Description</span><span class="sxs-lookup"><span data-stu-id="c1185-110">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1185-111">message</span><span class="sxs-lookup"><span data-stu-id="c1185-111">message</span></span>  | [<span data-ttu-id="c1185-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="c1185-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="c1185-113">Opcode 的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c1185-113">The localized display name for the opcode.</span></span> <span data-ttu-id="c1185-114">訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="c1185-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                     |
| <span data-ttu-id="c1185-115">mofValue</span><span class="sxs-lookup"><span data-stu-id="c1185-115">mofValue</span></span> | [<span data-ttu-id="c1185-116">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="c1185-116">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="c1185-117">已保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="c1185-117">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c1185-118">NAME</span><span class="sxs-lookup"><span data-stu-id="c1185-118">name</span></span>     | <span data-ttu-id="c1185-119">**QName**</span><span class="sxs-lookup"><span data-stu-id="c1185-119">**QName**</span></span>                                                         | <span data-ttu-id="c1185-120">Opcode 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1185-120">The name of the opcode.</span></span> <span data-ttu-id="c1185-121">這個名稱在此提供者的範圍內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c1185-121">This name must be unique within the scope of this provider.</span></span> <br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="c1185-122">符號</span><span class="sxs-lookup"><span data-stu-id="c1185-122">symbol</span></span>   | [<span data-ttu-id="c1185-123">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="c1185-123">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="c1185-124">用來參考應用程式中之 opcode 的符號。</span><span class="sxs-lookup"><span data-stu-id="c1185-124">The symbol to use to reference the opcode in your application.</span></span> <span data-ttu-id="c1185-125">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，為編譯器產生的標頭檔中的 opcode 建立常數。</span><span class="sxs-lookup"><span data-stu-id="c1185-125">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the opcode in the header file that the compiler generates.</span></span> <span data-ttu-id="c1185-126">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="c1185-126">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="c1185-127">value</span><span class="sxs-lookup"><span data-stu-id="c1185-127">value</span></span>    | [<span data-ttu-id="c1185-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="c1185-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="c1185-129">Opcode 值。</span><span class="sxs-lookup"><span data-stu-id="c1185-129">The opcode value.</span></span> <span data-ttu-id="c1185-130">您可以指定範圍10和239的值。</span><span class="sxs-lookup"><span data-stu-id="c1185-130">You can specify values in the range 10 and 239.</span></span> <span data-ttu-id="c1185-131">如需預先定義之 opcode 值的清單，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c1185-131">For a list of predefined opcode values, see Remarks.</span></span><br/>                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="c1185-132">備註</span><span class="sxs-lookup"><span data-stu-id="c1185-132">Remarks</span></span>

<span data-ttu-id="c1185-133">以下是您可以使用的預先定義 opcode 值。</span><span class="sxs-lookup"><span data-stu-id="c1185-133">The following are the predefined opcode values that you can use.</span></span> <span data-ttu-id="c1185-134">這些值是在包含于 Windows SDK 的 Winmeta.xml 檔案中定義。</span><span class="sxs-lookup"><span data-stu-id="c1185-134">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="c1185-135">Name</span><span class="sxs-lookup"><span data-stu-id="c1185-135">Name</span></span>          | <span data-ttu-id="c1185-136">值</span><span class="sxs-lookup"><span data-stu-id="c1185-136">Value</span></span> | <span data-ttu-id="c1185-137">符號</span><span class="sxs-lookup"><span data-stu-id="c1185-137">Symbol</span></span>                      | <span data-ttu-id="c1185-138">描述</span><span class="sxs-lookup"><span data-stu-id="c1185-138">Description</span></span>                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1185-139">win： Info</span><span class="sxs-lookup"><span data-stu-id="c1185-139">win:Info</span></span>      | <span data-ttu-id="c1185-140">0</span><span class="sxs-lookup"><span data-stu-id="c1185-140">0</span></span>     | <span data-ttu-id="c1185-141">NEW-WINEVENT \_ OPCODE \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="c1185-141">WINEVENT\_OPCODE\_INFO</span></span>      | <span data-ttu-id="c1185-142">資訊事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-142">An informational event.</span></span>                                                                                |
| <span data-ttu-id="c1185-143">win：開始</span><span class="sxs-lookup"><span data-stu-id="c1185-143">win:Start</span></span>     | <span data-ttu-id="c1185-144">1</span><span class="sxs-lookup"><span data-stu-id="c1185-144">1</span></span>     | <span data-ttu-id="c1185-145">NEW-WINEVENT \_ OPCODE \_ 開始</span><span class="sxs-lookup"><span data-stu-id="c1185-145">WINEVENT\_OPCODE\_START</span></span>     | <span data-ttu-id="c1185-146">表示啟動活動的事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-146">An event that represents starting an activity.</span></span>                                                         |
| <span data-ttu-id="c1185-147">win：停止</span><span class="sxs-lookup"><span data-stu-id="c1185-147">win:Stop</span></span>      | <span data-ttu-id="c1185-148">2</span><span class="sxs-lookup"><span data-stu-id="c1185-148">2</span></span>     | <span data-ttu-id="c1185-149">NEW-WINEVENT 作業 \_ 碼 \_ 停止</span><span class="sxs-lookup"><span data-stu-id="c1185-149">WINEVENT\_OPCODE\_STOP</span></span>      | <span data-ttu-id="c1185-150">表示停止活動的事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-150">An event that represents stopping an activity.</span></span> <span data-ttu-id="c1185-151">事件對應到最後一個不成對的開始事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-151">The event corresponds to the last unpaired start event.</span></span> |
| <span data-ttu-id="c1185-152">win： DC \_ 啟動</span><span class="sxs-lookup"><span data-stu-id="c1185-152">win:DC\_Start</span></span> | <span data-ttu-id="c1185-153">3</span><span class="sxs-lookup"><span data-stu-id="c1185-153">3</span></span>     | <span data-ttu-id="c1185-154">NEW-WINEVENT \_ OPCODE \_ DC \_ 啟動</span><span class="sxs-lookup"><span data-stu-id="c1185-154">WINEVENT\_OPCODE\_DC\_START</span></span> | <span data-ttu-id="c1185-155">表示開始之資料收集的事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-155">An event that represents data collection starting.</span></span> <span data-ttu-id="c1185-156">這些是取消事件種類。</span><span class="sxs-lookup"><span data-stu-id="c1185-156">These are rundown event types.</span></span>                      |
| <span data-ttu-id="c1185-157">win： DC \_ 停止</span><span class="sxs-lookup"><span data-stu-id="c1185-157">win:DC\_Stop</span></span>  | <span data-ttu-id="c1185-158">4</span><span class="sxs-lookup"><span data-stu-id="c1185-158">4</span></span>     | <span data-ttu-id="c1185-159">NEW-WINEVENT 作業 \_ 碼 \_ DC \_ 停止</span><span class="sxs-lookup"><span data-stu-id="c1185-159">WINEVENT\_OPCODE\_DC\_STOP</span></span>  | <span data-ttu-id="c1185-160">表示資料收集停止的事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-160">An event that represents data collection stopping.</span></span> <span data-ttu-id="c1185-161">這些是取消事件種類。</span><span class="sxs-lookup"><span data-stu-id="c1185-161">These are rundown event types.</span></span>                      |
| <span data-ttu-id="c1185-162">win：擴充功能</span><span class="sxs-lookup"><span data-stu-id="c1185-162">win:Extension</span></span> | <span data-ttu-id="c1185-163">5</span><span class="sxs-lookup"><span data-stu-id="c1185-163">5</span></span>     | <span data-ttu-id="c1185-164">NEW-WINEVENT \_ OPCODE \_ 延伸模組</span><span class="sxs-lookup"><span data-stu-id="c1185-164">WINEVENT\_OPCODE\_EXTENSION</span></span> | <span data-ttu-id="c1185-165">擴充事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-165">An extension event.</span></span>                                                                                    |
| <span data-ttu-id="c1185-166">win：回復</span><span class="sxs-lookup"><span data-stu-id="c1185-166">win:Reply</span></span>     | <span data-ttu-id="c1185-167">6</span><span class="sxs-lookup"><span data-stu-id="c1185-167">6</span></span>     | <span data-ttu-id="c1185-168">NEW-WINEVENT \_ OPCODE \_ 回復</span><span class="sxs-lookup"><span data-stu-id="c1185-168">WINEVENT\_OPCODE\_REPLY</span></span>     | <span data-ttu-id="c1185-169">回復事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-169">A reply event.</span></span>                                                                                         |
| <span data-ttu-id="c1185-170">win： Resume</span><span class="sxs-lookup"><span data-stu-id="c1185-170">win:Resume</span></span>    | <span data-ttu-id="c1185-171">7</span><span class="sxs-lookup"><span data-stu-id="c1185-171">7</span></span>     | <span data-ttu-id="c1185-172">NEW-WINEVENT \_ OPCODE \_ RESUME</span><span class="sxs-lookup"><span data-stu-id="c1185-172">WINEVENT\_OPCODE\_RESUME</span></span>    | <span data-ttu-id="c1185-173">表示在暫止後繼續之活動的事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-173">An event that represents an activity resuming after being suspended.</span></span>                                   |
| <span data-ttu-id="c1185-174">win：暫停</span><span class="sxs-lookup"><span data-stu-id="c1185-174">win:Suspend</span></span>   | <span data-ttu-id="c1185-175">8</span><span class="sxs-lookup"><span data-stu-id="c1185-175">8</span></span>     | <span data-ttu-id="c1185-176">NEW-WINEVENT \_ OPCODE \_ 暫止</span><span class="sxs-lookup"><span data-stu-id="c1185-176">WINEVENT\_OPCODE\_SUSPEND</span></span>   | <span data-ttu-id="c1185-177">表示暫止的活動暫止另一個活動完成的事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-177">An event that represents the activity being suspended pending another activity's completion.</span></span>           |
| <span data-ttu-id="c1185-178">win：傳送</span><span class="sxs-lookup"><span data-stu-id="c1185-178">win:Send</span></span>      | <span data-ttu-id="c1185-179">9</span><span class="sxs-lookup"><span data-stu-id="c1185-179">9</span></span>     | <span data-ttu-id="c1185-180">NEW-WINEVENT \_ OPCODE \_ 傳送</span><span class="sxs-lookup"><span data-stu-id="c1185-180">WINEVENT\_OPCODE\_SEND</span></span>      | <span data-ttu-id="c1185-181">表示將活動傳送至另一個元件的事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-181">An event that represents transferring activity to another component.</span></span>                                   |
| <span data-ttu-id="c1185-182">win：接收</span><span class="sxs-lookup"><span data-stu-id="c1185-182">win:Receive</span></span>   | <span data-ttu-id="c1185-183">240</span><span class="sxs-lookup"><span data-stu-id="c1185-183">240</span></span>   | <span data-ttu-id="c1185-184">NEW-WINEVENT \_ OPCODE \_ 接收</span><span class="sxs-lookup"><span data-stu-id="c1185-184">WINEVENT\_OPCODE\_RECEIVE</span></span>   | <span data-ttu-id="c1185-185">表示接收來自另一個元件之活動傳送的事件。</span><span class="sxs-lookup"><span data-stu-id="c1185-185">An event that represents receiving an activity transfer from another component.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="c1185-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1185-186">Requirements</span></span>



| <span data-ttu-id="c1185-187">需求</span><span class="sxs-lookup"><span data-stu-id="c1185-187">Requirement</span></span> | <span data-ttu-id="c1185-188">值</span><span class="sxs-lookup"><span data-stu-id="c1185-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1185-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1185-189">Minimum supported client</span></span><br/> | <span data-ttu-id="c1185-190">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1185-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1185-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1185-191">Minimum supported server</span></span><br/> | <span data-ttu-id="c1185-192">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1185-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





