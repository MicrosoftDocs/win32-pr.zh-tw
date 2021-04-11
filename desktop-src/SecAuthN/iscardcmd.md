---
description: 提供建立和管理智慧卡應用程式協定資料單位 (APDU) 所需的方法。
ms.assetid: fd84bb2e-27da-4670-b8e8-56c7948b78bb
title: 'ISCardCmd 介面 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd
- ISCardCmd.Type
- ISCardCmd.get_Type
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f14291f3777dcdc8b661f96f94d987209100a365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026096"
---
# <a name="iscardcmd-interface"></a><span data-ttu-id="a8864-103">ISCardCmd 介面</span><span class="sxs-lookup"><span data-stu-id="a8864-103">ISCardCmd interface</span></span>

<span data-ttu-id="a8864-104">\[**ISCardCmd** 介面可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a8864-104">\[The **ISCardCmd** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a8864-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="a8864-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a8864-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="a8864-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a8864-107">**ISCardCmd** 介面提供了建立和管理 [*智慧卡*](../secgloss/s-gly.md)[*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 所需的方法。</span><span class="sxs-lookup"><span data-stu-id="a8864-107">The **ISCardCmd** interface provides the methods needed to construct and manage a [*smart card*](../secgloss/s-gly.md) [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="a8864-108">此介面會封裝兩個緩衝區：</span><span class="sxs-lookup"><span data-stu-id="a8864-108">This interface encapsulates two buffers:</span></span>

-   <span data-ttu-id="a8864-109">APDU 緩衝區包含將傳送到卡片的命令順序。</span><span class="sxs-lookup"><span data-stu-id="a8864-109">The APDU buffer contains the command sequence that will be sent to the card.</span></span>
-   <span data-ttu-id="a8864-110">APDUReply 緩衝區包含執行 APDU 命令之後從卡片傳回的資料 (此資料也稱為「傳回的 APDU」) 。</span><span class="sxs-lookup"><span data-stu-id="a8864-110">The APDUReply buffer contains data returned from the card after execution of the APDU command (this data is also referred to as the return APDU).</span></span>

<span data-ttu-id="a8864-111">下列範例顯示 **ISCardCmd** 介面的一般用法。</span><span class="sxs-lookup"><span data-stu-id="a8864-111">The following example shows a typical use of the **ISCardCmd** interface.</span></span> <span data-ttu-id="a8864-112">**ISCardCmd** 介面是用來建立 APDU。</span><span class="sxs-lookup"><span data-stu-id="a8864-112">The **ISCardCmd** interface is used to build an APDU.</span></span>

<span data-ttu-id="a8864-113">**將交易提交至特定卡片**</span><span class="sxs-lookup"><span data-stu-id="a8864-113">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="a8864-114">建立 [**ISCard**](iscard.md) 介面並連接至智慧卡。</span><span class="sxs-lookup"><span data-stu-id="a8864-114">Create an [**ISCard**](iscard.md) interface and connect to a smart card.</span></span>
2.  <span data-ttu-id="a8864-115">建立 **ISCardCmd** 介面。</span><span class="sxs-lookup"><span data-stu-id="a8864-115">Create an **ISCardCmd** interface.</span></span>
3.  <span data-ttu-id="a8864-116">使用 [**ISCardISO7816**](iscardiso7816.md) 介面或 **ISCardCmd** 的其中一個組建方法，建立智慧卡 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="a8864-116">Build a smart card APDU command by using the [**ISCardISO7816**](iscardiso7816.md) interface or one of **ISCardCmd** build methods.</span></span>
4.  <span data-ttu-id="a8864-117">藉由呼叫適當的 [**ISCard**](iscard.md) 介面方法，在智慧卡上執行命令。</span><span class="sxs-lookup"><span data-stu-id="a8864-117">Execute the command on the smart card by calling the appropriate [**ISCard**](iscard.md) interface method.</span></span>
5.  <span data-ttu-id="a8864-118">評估傳回的回應。</span><span class="sxs-lookup"><span data-stu-id="a8864-118">Evaluate the returned response.</span></span>
6.  <span data-ttu-id="a8864-119">視需要重複此程式。</span><span class="sxs-lookup"><span data-stu-id="a8864-119">Repeat the procedure as needed.</span></span>
7.  <span data-ttu-id="a8864-120">視需要釋放 **ISCardCmd** 介面和其他專案。</span><span class="sxs-lookup"><span data-stu-id="a8864-120">Release the **ISCardCmd** interface and others as needed.</span></span>

## <a name="members"></a><span data-ttu-id="a8864-121">成員</span><span class="sxs-lookup"><span data-stu-id="a8864-121">Members</span></span>

<span data-ttu-id="a8864-122">**ISCardCmd** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="a8864-122">The **ISCardCmd** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a8864-123">**ISCardCmd** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a8864-123">**ISCardCmd** also has these types of members:</span></span>

-   [<span data-ttu-id="a8864-124">方法</span><span class="sxs-lookup"><span data-stu-id="a8864-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="a8864-125">屬性</span><span class="sxs-lookup"><span data-stu-id="a8864-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a8864-126">方法</span><span class="sxs-lookup"><span data-stu-id="a8864-126">Methods</span></span>

<span data-ttu-id="a8864-127">**ISCardCmd** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a8864-127">The **ISCardCmd** interface has these methods.</span></span>



| <span data-ttu-id="a8864-128">方法</span><span class="sxs-lookup"><span data-stu-id="a8864-128">Method</span></span>                                       | <span data-ttu-id="a8864-129">描述</span><span class="sxs-lookup"><span data-stu-id="a8864-129">Description</span></span>                                                                                                |
|:---------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8864-130">**BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="a8864-130">**BuildCmd**</span></span>](iscardcmd-buildcmd.md)       | <span data-ttu-id="a8864-131">為傳輸到智慧卡的有效命令 APDU 進行結構化。</span><span class="sxs-lookup"><span data-stu-id="a8864-131">Constructs a valid command APDU for transmission to a smart card.</span></span><br/>                               |
| [<span data-ttu-id="a8864-132">**清楚**</span><span class="sxs-lookup"><span data-stu-id="a8864-132">**Clear**</span></span>](iscardcmd-clear.md)             | <span data-ttu-id="a8864-133">清除 APDU 和回復 APDU 訊息緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a8864-133">Clears the APDU and the reply APDU message buffers.</span></span><br/>                                             |
| [<span data-ttu-id="a8864-134">**封裝**</span><span class="sxs-lookup"><span data-stu-id="a8864-134">**Encapsulate**</span></span>](iscardcmd-encapsulate.md) | <span data-ttu-id="a8864-135">將指定的命令 APDU 封裝到另一個命令 APDU，以傳輸至智慧卡。</span><span class="sxs-lookup"><span data-stu-id="a8864-135">Encapsulates the given command APDU into another command APDU for transmission to a smart card.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a8864-136">屬性</span><span class="sxs-lookup"><span data-stu-id="a8864-136">Properties</span></span>

<span data-ttu-id="a8864-137">**ISCardCmd** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a8864-137">The **ISCardCmd** interface has these properties.</span></span>



| <span data-ttu-id="a8864-138">屬性</span><span class="sxs-lookup"><span data-stu-id="a8864-138">Property</span></span>                                                              | <span data-ttu-id="a8864-139">存取類型</span><span class="sxs-lookup"><span data-stu-id="a8864-139">Access type</span></span>           | <span data-ttu-id="a8864-140">Description</span><span class="sxs-lookup"><span data-stu-id="a8864-140">Description</span></span>                                                                                                                                                         |
|:----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8864-141">**AlternateClassId**</span><span class="sxs-lookup"><span data-stu-id="a8864-141">**AlternateClassId**</span></span>](iscardcmd-get-alternateclassid.md)<br/> | <span data-ttu-id="a8864-142">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-142">Read/write</span></span><br/> | <span data-ttu-id="a8864-143">目前的替代類別識別碼值。</span><span class="sxs-lookup"><span data-stu-id="a8864-143">Current alternate class ID value.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="a8864-144">**Apdu**</span><span class="sxs-lookup"><span data-stu-id="a8864-144">**Apdu**</span></span>](iscardcmd-get-apdu.md)<br/>                         | <span data-ttu-id="a8864-145">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-145">Read/write</span></span><br/> | <span data-ttu-id="a8864-146">原始 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="a8864-146">Raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span><br/> |
| [<span data-ttu-id="a8864-147">**ApduLength**</span><span class="sxs-lookup"><span data-stu-id="a8864-147">**ApduLength**</span></span>](iscardcmd-get-apdulength.md)<br/>             | <span data-ttu-id="a8864-148">唯讀</span><span class="sxs-lookup"><span data-stu-id="a8864-148">Read-only</span></span><br/>  | <span data-ttu-id="a8864-149">APDU 的長度。</span><span class="sxs-lookup"><span data-stu-id="a8864-149">Length of the APDU.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="a8864-150">**ApduReply**</span><span class="sxs-lookup"><span data-stu-id="a8864-150">**ApduReply**</span></span>](iscardcmd-get-apdureply.md)<br/>               | <span data-ttu-id="a8864-151">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-151">Read/write</span></span><br/> | <span data-ttu-id="a8864-152">[*回復 APDU*](../secgloss/r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a8864-152">[*Reply APDU*](../secgloss/r-gly.md).</span></span><br/>                                                                        |
| [<span data-ttu-id="a8864-153">**ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="a8864-153">**ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)<br/>   | <span data-ttu-id="a8864-154">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-154">Read/write</span></span><br/> | <span data-ttu-id="a8864-155">回復 APDU 的長度。</span><span class="sxs-lookup"><span data-stu-id="a8864-155">Length of the reply APDU.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="a8864-156">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="a8864-156">**ClassId**</span></span>](iscardcmd-get-classid.md)<br/>                   | <span data-ttu-id="a8864-157">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-157">Read/write</span></span><br/> | <span data-ttu-id="a8864-158">APDU 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8864-158">Class ID of the APDU.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="a8864-159">**資料**</span><span class="sxs-lookup"><span data-stu-id="a8864-159">**Data**</span></span>](iscardcmd-get-data.md)<br/>                         | <span data-ttu-id="a8864-160">唯讀</span><span class="sxs-lookup"><span data-stu-id="a8864-160">Read-only</span></span><br/>  | <span data-ttu-id="a8864-161">APDU 的資料欄位。</span><span class="sxs-lookup"><span data-stu-id="a8864-161">Data field of the APDU.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="a8864-162">**InstructionId**</span><span class="sxs-lookup"><span data-stu-id="a8864-162">**InstructionId**</span></span>](iscardcmd-get-instructionid.md)<br/>       | <span data-ttu-id="a8864-163">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-163">Read/write</span></span><br/> | <span data-ttu-id="a8864-164">來自 APDU 的指令識別碼位元組。</span><span class="sxs-lookup"><span data-stu-id="a8864-164">Instruction ID byte from the APDU.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="a8864-165">**LeField**</span><span class="sxs-lookup"><span data-stu-id="a8864-165">**LeField**</span></span>](iscardcmd-get-lefield.md)<br/>                   | <span data-ttu-id="a8864-166">唯讀</span><span class="sxs-lookup"><span data-stu-id="a8864-166">Read-only</span></span><br/>  | <span data-ttu-id="a8864-167">APDU 的 Le 欄位。</span><span class="sxs-lookup"><span data-stu-id="a8864-167">Le field of the APDU.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="a8864-168">**Nad**</span><span class="sxs-lookup"><span data-stu-id="a8864-168">**Nad**</span></span>](iscardcmd-put-nad.md)<br/>                           | <span data-ttu-id="a8864-169">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-169">Read/write</span></span><br/> | <span data-ttu-id="a8864-170">節點位址。</span><span class="sxs-lookup"><span data-stu-id="a8864-170">Node address.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="a8864-171">**P1**</span><span class="sxs-lookup"><span data-stu-id="a8864-171">**P1**</span></span>](iscardcmd-get-p1.md)<br/>                             | <span data-ttu-id="a8864-172">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-172">Read/write</span></span><br/> | <span data-ttu-id="a8864-173">APDU 的第一個參數位元組。</span><span class="sxs-lookup"><span data-stu-id="a8864-173">First parameter byte of the APDU.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="a8864-174">**P2**</span><span class="sxs-lookup"><span data-stu-id="a8864-174">**P2**</span></span>](iscardcmd-get-p2.md)<br/>                             | <span data-ttu-id="a8864-175">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-175">Read/write</span></span><br/> | <span data-ttu-id="a8864-176">APDU 的第二個參數位元組。</span><span class="sxs-lookup"><span data-stu-id="a8864-176">Second parameter byte of the APDU.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="a8864-177">**P3**</span><span class="sxs-lookup"><span data-stu-id="a8864-177">**P3**</span></span>](iscardcmd-get-p3.md)<br/>                             | <span data-ttu-id="a8864-178">唯讀</span><span class="sxs-lookup"><span data-stu-id="a8864-178">Read-only</span></span><br/>  | <span data-ttu-id="a8864-179">APDU 的第三個參數位元組。</span><span class="sxs-lookup"><span data-stu-id="a8864-179">Third parameter byte of the APDU.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="a8864-180">**ReplyNad**</span><span class="sxs-lookup"><span data-stu-id="a8864-180">**ReplyNad**</span></span>](iscardcmd-get-replynad.md)<br/>                 | <span data-ttu-id="a8864-181">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-181">Read/write</span></span><br/> | <span data-ttu-id="a8864-182">信用卡在回復訊息中使用的節點位址。</span><span class="sxs-lookup"><span data-stu-id="a8864-182">Node address used by the card in the reply message.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="a8864-183">**ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="a8864-183">**ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)<br/>           | <span data-ttu-id="a8864-184">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8864-184">Read/write</span></span><br/> | <span data-ttu-id="a8864-185">[*回復 APDU*](../secgloss/r-gly.md) 訊息狀態字組。</span><span class="sxs-lookup"><span data-stu-id="a8864-185">[*Reply APDU*](../secgloss/r-gly.md) message status word.</span></span><br/>                                                    |
| [<span data-ttu-id="a8864-186">**ReplyStatusSW1**</span><span class="sxs-lookup"><span data-stu-id="a8864-186">**ReplyStatusSW1**</span></span>](iscardcmd-get-replystatussw1.md)<br/>     | <span data-ttu-id="a8864-187">唯讀</span><span class="sxs-lookup"><span data-stu-id="a8864-187">Read-only</span></span><br/>  | <span data-ttu-id="a8864-188">回復 APDU 的 message SW1 status byte。</span><span class="sxs-lookup"><span data-stu-id="a8864-188">Reply APDU's message SW1 status byte.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="a8864-189">**ReplyStatusSW2**</span><span class="sxs-lookup"><span data-stu-id="a8864-189">**ReplyStatusSW2**</span></span>](iscardcmd-get-replystatussw2.md)<br/>     | <span data-ttu-id="a8864-190">唯讀</span><span class="sxs-lookup"><span data-stu-id="a8864-190">Read-only</span></span><br/>  | <span data-ttu-id="a8864-191">回復 APDU 的 message SW2 status byte。</span><span class="sxs-lookup"><span data-stu-id="a8864-191">Reply APDU's message SW2 status byte.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="a8864-192">**型別**</span><span class="sxs-lookup"><span data-stu-id="a8864-192">**Type**</span></span><br/>                                                   | <span data-ttu-id="a8864-193">唯讀</span><span class="sxs-lookup"><span data-stu-id="a8864-193">Read-only</span></span><br/>  | <span data-ttu-id="a8864-194">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="a8864-194">Reserved for future use.</span></span><br/>                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="a8864-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8864-195">Requirements</span></span>



| <span data-ttu-id="a8864-196">需求</span><span class="sxs-lookup"><span data-stu-id="a8864-196">Requirement</span></span> | <span data-ttu-id="a8864-197">值</span><span class="sxs-lookup"><span data-stu-id="a8864-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8864-198">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8864-198">Minimum supported client</span></span><br/> | <span data-ttu-id="a8864-199">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8864-199">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a8864-200">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8864-200">Minimum supported server</span></span><br/> | <span data-ttu-id="a8864-201">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8864-201">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a8864-202">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a8864-202">End of client support</span></span><br/>    | <span data-ttu-id="a8864-203">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8864-203">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a8864-204">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a8864-204">End of server support</span></span><br/>    | <span data-ttu-id="a8864-205">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8864-205">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a8864-206">標頭</span><span class="sxs-lookup"><span data-stu-id="a8864-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8864-207"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8864-207"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8864-208">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a8864-208">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8864-209"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a8864-209"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a8864-210">DLL</span><span class="sxs-lookup"><span data-stu-id="a8864-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8864-211"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8864-211"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8864-212">IID</span><span class="sxs-lookup"><span data-stu-id="a8864-212">IID</span></span><br/>                      | <span data-ttu-id="a8864-213">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a8864-213">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



 

 
