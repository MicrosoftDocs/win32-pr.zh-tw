---
description: 可讓您開啟及管理智慧卡的連接。
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: 'ISCard 介面 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512761"
---
# <a name="iscard-interface"></a><span data-ttu-id="b957e-103">ISCard 介面</span><span class="sxs-lookup"><span data-stu-id="b957e-103">ISCard interface</span></span>

<span data-ttu-id="b957e-104">\[**ISCard** 介面可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b957e-104">\[The **ISCard** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b957e-105">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="b957e-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b957e-106">**ISCard** 介面可讓您開啟及管理 [*智慧卡*](../secgloss/s-gly.md)的連接。</span><span class="sxs-lookup"><span data-stu-id="b957e-106">The **ISCard** interface lets you open and manage a connection to a [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="b957e-107">每張卡片的連接都需要單一的對應 **ISCard** 介面實例。</span><span class="sxs-lookup"><span data-stu-id="b957e-107">Each connection to a card requires a single, corresponding instance of the **ISCard** interface.</span></span>

<span data-ttu-id="b957e-108">每次建立 **ISCard** 的實例時，都必須可以使用智慧卡 [*資源管理員*](../secgloss/r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b957e-108">The smart card [*resource manager*](../secgloss/r-gly.md) must be available whenever an instance of **ISCard** is created.</span></span> <span data-ttu-id="b957e-109">如果此服務無法使用，則建立介面將會失敗。</span><span class="sxs-lookup"><span data-stu-id="b957e-109">If this service is unavailable, creation of the interface will fail.</span></span>

<span data-ttu-id="b957e-110">下列範例顯示 **ISCard** 介面的一般用法。</span><span class="sxs-lookup"><span data-stu-id="b957e-110">The following example shows a typical use of the **ISCard** interface.</span></span> <span data-ttu-id="b957e-111">**ISCard** 介面是用來連接智慧卡、提交 [*交易*](../secgloss/t-gly.md)，以及釋出智慧卡。</span><span class="sxs-lookup"><span data-stu-id="b957e-111">The **ISCard** interface is used to connect to the smart card, submit a [*transaction*](../secgloss/t-gly.md), and release the smart card.</span></span>

<span data-ttu-id="b957e-112">**將交易提交至特定卡片**</span><span class="sxs-lookup"><span data-stu-id="b957e-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="b957e-113">建立 **ISCard** 介面。</span><span class="sxs-lookup"><span data-stu-id="b957e-113">Create an **ISCard** interface.</span></span>
2.  <span data-ttu-id="b957e-114">藉由指定智慧卡 [*讀卡機*](../secgloss/r-gly.md) 或使用先前建立的有效控制碼，連接到智慧卡。</span><span class="sxs-lookup"><span data-stu-id="b957e-114">Attach to a smart card by specifying a smart card [*reader*](../secgloss/r-gly.md) or by using a previously established, valid handle.</span></span>
3.  <span data-ttu-id="b957e-115">使用 [**ISCardCmd**](iscardcmd.md)建立交易命令，並 [**ISCardISO7816**](iscardiso7816.md) 智慧卡介面。</span><span class="sxs-lookup"><span data-stu-id="b957e-115">Create transaction commands with [**ISCardCmd**](iscardcmd.md), and [**ISCardISO7816**](iscardiso7816.md) smart card interfaces.</span></span>
4.  <span data-ttu-id="b957e-116">使用 **ISCard** 提交交易命令以供智慧卡處理。</span><span class="sxs-lookup"><span data-stu-id="b957e-116">Use **ISCard** to submit the transaction commands for processing by the smart card.</span></span>
5.  <span data-ttu-id="b957e-117">使用 **ISCard** 釋放智慧卡。</span><span class="sxs-lookup"><span data-stu-id="b957e-117">Use **ISCard** to release the smart card.</span></span>
6.  <span data-ttu-id="b957e-118">釋放 **ISCard** 介面。</span><span class="sxs-lookup"><span data-stu-id="b957e-118">Release the **ISCard** interface.</span></span>

## <a name="members"></a><span data-ttu-id="b957e-119">成員</span><span class="sxs-lookup"><span data-stu-id="b957e-119">Members</span></span>

<span data-ttu-id="b957e-120">**ISCard** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="b957e-120">The **ISCard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b957e-121">**ISCard** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b957e-121">**ISCard** also has these types of members:</span></span>

-   [<span data-ttu-id="b957e-122">方法</span><span class="sxs-lookup"><span data-stu-id="b957e-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="b957e-123">屬性</span><span class="sxs-lookup"><span data-stu-id="b957e-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b957e-124">方法</span><span class="sxs-lookup"><span data-stu-id="b957e-124">Methods</span></span>

<span data-ttu-id="b957e-125">**ISCard** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b957e-125">The **ISCard** interface has these methods.</span></span>



| <span data-ttu-id="b957e-126">方法</span><span class="sxs-lookup"><span data-stu-id="b957e-126">Method</span></span>                                          | <span data-ttu-id="b957e-127">描述</span><span class="sxs-lookup"><span data-stu-id="b957e-127">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b957e-128">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="b957e-128">**AttachByHandle**</span></span>](iscard-attachbyhandle.md) | <span data-ttu-id="b957e-129">將物件附加至開啟和設定的智慧卡控點。</span><span class="sxs-lookup"><span data-stu-id="b957e-129">Attaches an object to an open and configured smart card handle.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="b957e-130">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="b957e-130">**AttachByReader**</span></span>](iscard-attachbyreader.md) | <span data-ttu-id="b957e-131">在指定的讀取器中開啟智慧卡。</span><span class="sxs-lookup"><span data-stu-id="b957e-131">Opens the smart card in the named reader.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="b957e-132">**中斷連結**</span><span class="sxs-lookup"><span data-stu-id="b957e-132">**Detach**</span></span>](iscard-detach.md)                 | <span data-ttu-id="b957e-133">關閉智慧卡的開啟連接。</span><span class="sxs-lookup"><span data-stu-id="b957e-133">Closes the open connection to the smart card.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="b957e-134">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="b957e-134">**LockSCard**</span></span>](iscard-lockscard.md)           | <span data-ttu-id="b957e-135">宣告智慧卡的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="b957e-135">Claims exclusive access to the smart card.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="b957e-136">**附加**</span><span class="sxs-lookup"><span data-stu-id="b957e-136">**ReAttach**</span></span>](iscard-reattach.md)             | <span data-ttu-id="b957e-137">重設並重新初始化智慧卡。</span><span class="sxs-lookup"><span data-stu-id="b957e-137">Resets and reinitializes the smart card.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="b957e-138">**交易**</span><span class="sxs-lookup"><span data-stu-id="b957e-138">**Transaction**</span></span>](iscard-transaction.md)       | <span data-ttu-id="b957e-139"> ([*應用程式協定資料單位*](../secgloss/a-gly.md)) 物件，執行智慧卡命令的寫入和讀取作業。</span><span class="sxs-lookup"><span data-stu-id="b957e-139">Executes a write and read operation on the smart card command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span><br/> |
| [<span data-ttu-id="b957e-140">**UnlockScard**</span><span class="sxs-lookup"><span data-stu-id="b957e-140">**UnlockScard**</span></span>](iscard-unlockscard.md)       | <span data-ttu-id="b957e-141">釋放智慧卡的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="b957e-141">Releases exclusive access to the smart card.</span></span><br/>                                                                                                                                                                         |



 

### <a name="properties"></a><span data-ttu-id="b957e-142">屬性</span><span class="sxs-lookup"><span data-stu-id="b957e-142">Properties</span></span>

<span data-ttu-id="b957e-143">**ISCard** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b957e-143">The **ISCard** interface has these properties.</span></span>



| <span data-ttu-id="b957e-144">屬性</span><span class="sxs-lookup"><span data-stu-id="b957e-144">Property</span></span>                                               | <span data-ttu-id="b957e-145">存取類型</span><span class="sxs-lookup"><span data-stu-id="b957e-145">Access type</span></span>          | <span data-ttu-id="b957e-146">Description</span><span class="sxs-lookup"><span data-stu-id="b957e-146">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b957e-147">**Atr**</span><span class="sxs-lookup"><span data-stu-id="b957e-147">**Atr**</span></span>](iscard-get-atr.md)<br/>               | <span data-ttu-id="b957e-148">唯讀</span><span class="sxs-lookup"><span data-stu-id="b957e-148">Read-only</span></span><br/> | <span data-ttu-id="b957e-149">抓取智慧卡的 [*ATR 字串*](../secgloss/a-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="b957e-149">Retrieves the [*ATR string*](../secgloss/a-gly.md) of the smart card.</span></span><br/>                                                                   |
| [<span data-ttu-id="b957e-150">**CardHandle**</span><span class="sxs-lookup"><span data-stu-id="b957e-150">**CardHandle**</span></span>](iscard-get-cardhandle.md)<br/> | <span data-ttu-id="b957e-151">唯讀</span><span class="sxs-lookup"><span data-stu-id="b957e-151">Read-only</span></span><br/> | <span data-ttu-id="b957e-152">抓取連接智慧卡的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b957e-152">Retrieves the handle for the connected smart card.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="b957e-153">**Context**</span><span class="sxs-lookup"><span data-stu-id="b957e-153">**Context**</span></span>](iscard-get-context.md)<br/>       | <span data-ttu-id="b957e-154">唯讀</span><span class="sxs-lookup"><span data-stu-id="b957e-154">Read-only</span></span><br/> | <span data-ttu-id="b957e-155">抓取目前的 [*resource manager 內容*](../secgloss/r-gly.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="b957e-155">Retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span><br/>                            |
| [<span data-ttu-id="b957e-156">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="b957e-156">**Protocol**</span></span>](iscard-get-protocol.md)<br/>     | <span data-ttu-id="b957e-157">唯讀</span><span class="sxs-lookup"><span data-stu-id="b957e-157">Read-only</span></span><br/> | <span data-ttu-id="b957e-158">抓取智慧卡上目前正在使用的通訊協定識別碼。</span><span class="sxs-lookup"><span data-stu-id="b957e-158">Retrieves the identifier of the protocol currently in use on the smart card.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="b957e-159">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b957e-159">**Status**</span></span>](iscard-get-status.md)<br/>         | <span data-ttu-id="b957e-160">唯讀</span><span class="sxs-lookup"><span data-stu-id="b957e-160">Read-only</span></span><br/> | <span data-ttu-id="b957e-161">抓取 [*智慧卡*](../secgloss/s-gly.md)所在的目前 [*狀態*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b957e-161">Retrieves the current [*state*](../secgloss/s-gly.md) the [*smart card*](../secgloss/s-gly.md) is in.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b957e-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="b957e-162">Requirements</span></span>



| <span data-ttu-id="b957e-163">需求</span><span class="sxs-lookup"><span data-stu-id="b957e-163">Requirement</span></span> | <span data-ttu-id="b957e-164">值</span><span class="sxs-lookup"><span data-stu-id="b957e-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b957e-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b957e-165">Minimum supported client</span></span><br/> | <span data-ttu-id="b957e-166">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b957e-166">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b957e-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b957e-167">Minimum supported server</span></span><br/> | <span data-ttu-id="b957e-168">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b957e-168">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b957e-169">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b957e-169">End of client support</span></span><br/>    | <span data-ttu-id="b957e-170">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b957e-170">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b957e-171">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="b957e-171">End of server support</span></span><br/>    | <span data-ttu-id="b957e-172">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b957e-172">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b957e-173">標頭</span><span class="sxs-lookup"><span data-stu-id="b957e-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="b957e-174"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="b957e-174"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="b957e-175">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b957e-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="b957e-176"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b957e-176"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b957e-177">DLL</span><span class="sxs-lookup"><span data-stu-id="b957e-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b957e-178"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b957e-178"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b957e-179">IID</span><span class="sxs-lookup"><span data-stu-id="b957e-179">IID</span></span><br/>                      | <span data-ttu-id="b957e-180">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b957e-180">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



 

 
