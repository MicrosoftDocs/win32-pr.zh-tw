---
description: IByteBuffer 介面是提供來讀取、寫入和管理資料流程物件。 此物件基本上是 IStream 物件的包裝函式。
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: 'IByteBuffer 介面 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945038"
---
# <a name="ibytebuffer-interface"></a><span data-ttu-id="e9c7d-104">IByteBuffer 介面</span><span class="sxs-lookup"><span data-stu-id="e9c7d-104">IByteBuffer interface</span></span>

<span data-ttu-id="e9c7d-105">\[**IByteBuffer** 介面可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-105">\[The **IByteBuffer** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e9c7d-106">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e9c7d-107">[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)介面提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e9c7d-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="e9c7d-108">**IByteBuffer** 介面是提供來讀取、寫入和管理資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-108">The **IByteBuffer** interface is provided to read, write and manage stream objects.</span></span> <span data-ttu-id="e9c7d-109">此物件基本上是 **IStream** 物件的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-109">This object essentially is a wrapper for the **IStream** object.</span></span>

## <a name="members"></a><span data-ttu-id="e9c7d-110">成員</span><span class="sxs-lookup"><span data-stu-id="e9c7d-110">Members</span></span>

<span data-ttu-id="e9c7d-111">**IByteBuffer** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-111">The **IByteBuffer** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e9c7d-112">**IByteBuffer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e9c7d-112">**IByteBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="e9c7d-113">方法</span><span class="sxs-lookup"><span data-stu-id="e9c7d-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e9c7d-114">方法</span><span class="sxs-lookup"><span data-stu-id="e9c7d-114">Methods</span></span>

<span data-ttu-id="e9c7d-115">**IByteBuffer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-115">The **IByteBuffer** interface has these methods.</span></span>



| <span data-ttu-id="e9c7d-116">方法</span><span class="sxs-lookup"><span data-stu-id="e9c7d-116">Method</span></span>                                           | <span data-ttu-id="e9c7d-117">描述</span><span class="sxs-lookup"><span data-stu-id="e9c7d-117">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9c7d-118">**克隆**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-118">**Clone**</span></span>](ibytebuffer-clone.md)               | <span data-ttu-id="e9c7d-119">複製 **IByteBuffer** 物件。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-119">Clones an **IByteBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="e9c7d-120">**Commit**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-120">**Commit**</span></span>](ibytebuffer-commit.md)             | <span data-ttu-id="e9c7d-121">認可 [*交易*](/windows/desktop/SecGloss/t-gly)。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-121">Commits a [*transaction*](/windows/desktop/SecGloss/t-gly).</span></span><br/> |
| [<span data-ttu-id="e9c7d-122">**CopyTo**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-122">**CopyTo**</span></span>](ibytebuffer-copyto.md)             | <span data-ttu-id="e9c7d-123">將位元組複製到另一個物件。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-123">Copies bytes to another object.</span></span><br/>                                                                |
| [<span data-ttu-id="e9c7d-124">**初始化**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-124">**Initialize**</span></span>](ibytebuffer-initialize.md)     | <span data-ttu-id="e9c7d-125">初始化 **IByteBuffer** 物件。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-125">Initializes the **IByteBuffer** object.</span></span><br/>                                                        |
| [<span data-ttu-id="e9c7d-126">**LockRegion**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-126">**LockRegion**</span></span>](ibytebuffer-lockregion.md)     | <span data-ttu-id="e9c7d-127">限制存取範圍的位元組。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-127">Restricts access to a range of bytes.</span></span><br/>                                                          |
| [<span data-ttu-id="e9c7d-128">**讀**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-128">**Read**</span></span>](ibytebuffer-read.md)                 | <span data-ttu-id="e9c7d-129">將位元組讀入記憶體。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-129">Reads bytes into memory.</span></span><br/>                                                                       |
| [<span data-ttu-id="e9c7d-130">**恢復**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-130">**Revert**</span></span>](ibytebuffer-revert.md)             | <span data-ttu-id="e9c7d-131">捨棄上次 [**認可**](ibytebuffer-commit.md) 呼叫之後的變更。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-131">Discards changes since the last [**Commit**](ibytebuffer-commit.md) call.</span></span><br/>                     |
| [<span data-ttu-id="e9c7d-132">**Seek**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-132">**Seek**</span></span>](ibytebuffer-seek.md)                 | <span data-ttu-id="e9c7d-133">變更 seek 指標。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-133">Changes the seek pointer.</span></span><br/>                                                                      |
| [<span data-ttu-id="e9c7d-134">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-134">**SetSize**</span></span>](ibytebuffer-setsize.md)           | <span data-ttu-id="e9c7d-135">變更資料流物件的大小。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-135">Changes the size of the stream object.</span></span><br/>                                                         |
| [<span data-ttu-id="e9c7d-136">**統計**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-136">**Stat**</span></span>](ibytebuffer-stat.md)                 | <span data-ttu-id="e9c7d-137">捕獲資料流程的統計資訊。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-137">Retrieves statistical information about a stream.</span></span><br/>                                              |
| [<span data-ttu-id="e9c7d-138">**UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-138">**UnlockRegion**</span></span>](ibytebuffer-unlockregion.md) | <span data-ttu-id="e9c7d-139">移除 [**LockRegion**](ibytebuffer-lockregion.md)先前設定的存取限制。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-139">Removes access restriction previously set by [**LockRegion**](ibytebuffer-lockregion.md).</span></span><br/>     |
| [<span data-ttu-id="e9c7d-140">**寫**</span><span class="sxs-lookup"><span data-stu-id="e9c7d-140">**Write**</span></span>](ibytebuffer-write.md)               | <span data-ttu-id="e9c7d-141">將位元組寫入資料流程。</span><span class="sxs-lookup"><span data-stu-id="e9c7d-141">Writes bytes to the stream.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="e9c7d-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9c7d-142">Requirements</span></span>



| <span data-ttu-id="e9c7d-143">需求</span><span class="sxs-lookup"><span data-stu-id="e9c7d-143">Requirement</span></span> | <span data-ttu-id="e9c7d-144">值</span><span class="sxs-lookup"><span data-stu-id="e9c7d-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c7d-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9c7d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c7d-146">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9c7d-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e9c7d-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9c7d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c7d-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9c7d-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9c7d-149">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e9c7d-149">End of client support</span></span><br/>    | <span data-ttu-id="e9c7d-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e9c7d-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e9c7d-151">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e9c7d-151">End of server support</span></span><br/>    | <span data-ttu-id="e9c7d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9c7d-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e9c7d-153">標頭</span><span class="sxs-lookup"><span data-stu-id="e9c7d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9c7d-154"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9c7d-154"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9c7d-155">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e9c7d-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9c7d-156"><dt>Scardssp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e9c7d-156"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e9c7d-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e9c7d-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9c7d-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9c7d-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e9c7d-159">IID</span><span class="sxs-lookup"><span data-stu-id="e9c7d-159">IID</span></span><br/>                      | <span data-ttu-id="e9c7d-160">IID \_ IByteBuffer 定義為 E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="e9c7d-160">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

