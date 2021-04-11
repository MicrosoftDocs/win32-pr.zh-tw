---
description: 提供支援其他智慧卡 COM 介面的使用者所需的方法。
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: 'ISCardTypeConv 介面 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849251"
---
# <a name="iscardtypeconv-interface"></a><span data-ttu-id="a50af-103">ISCardTypeConv 介面</span><span class="sxs-lookup"><span data-stu-id="a50af-103">ISCardTypeConv interface</span></span>

<span data-ttu-id="a50af-104">\[**ISCardTypeConv** 介面可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a50af-104">\[The **ISCardTypeConv** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a50af-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="a50af-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a50af-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="a50af-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a50af-107">**ISCardTypeConv** 介面提供支援其他 [*智慧卡*](../secgloss/s-gly.md)COM 介面的使用者所需的方法。</span><span class="sxs-lookup"><span data-stu-id="a50af-107">The **ISCardTypeConv** interface provides the methods needed to support the users of the other [*smart card*](../secgloss/s-gly.md) COM interfaces.</span></span> <span data-ttu-id="a50af-108">這個介面僅提供回溯相容性，不應再使用。</span><span class="sxs-lookup"><span data-stu-id="a50af-108">This interface is provided for backward compatibility only and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="a50af-109">成員</span><span class="sxs-lookup"><span data-stu-id="a50af-109">Members</span></span>

<span data-ttu-id="a50af-110">**ISCardTypeConv** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="a50af-110">The **ISCardTypeConv** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a50af-111">**ISCardTypeConv** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a50af-111">**ISCardTypeConv** also has these types of members:</span></span>

-   [<span data-ttu-id="a50af-112">方法</span><span class="sxs-lookup"><span data-stu-id="a50af-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a50af-113">方法</span><span class="sxs-lookup"><span data-stu-id="a50af-113">Methods</span></span>

<span data-ttu-id="a50af-114">**ISCardTypeConv** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a50af-114">The **ISCardTypeConv** interface has these methods.</span></span>



| <span data-ttu-id="a50af-115">方法</span><span class="sxs-lookup"><span data-stu-id="a50af-115">Method</span></span>                                                                              | <span data-ttu-id="a50af-116">描述</span><span class="sxs-lookup"><span data-stu-id="a50af-116">Description</span></span>                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a50af-117">**ConvertByteArrayToByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="a50af-117">**ConvertByteArrayToByteBuffer**</span></span>](iscardtypeconv-convertbytearraytobytebuffer.md) | <span data-ttu-id="a50af-118">將典型的 C/c + + 位元組陣列轉換成 (**IStream** 物件) 的通用位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a50af-118">Converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span><br/>                                   |
| [<span data-ttu-id="a50af-119">**ConvertByteBufferToByteArray**</span><span class="sxs-lookup"><span data-stu-id="a50af-119">**ConvertByteBufferToByteArray**</span></span>](iscardtypeconv-convertbytebuffertobytearray.md) | <span data-ttu-id="a50af-120">將對應至通用位元組緩衝區的位元組陣列 (**IStream** 物件) 轉換為一般 C/c + + 位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="a50af-120">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span><br/>          |
| [<span data-ttu-id="a50af-121">**ConvertByteBufferToSafeArray**</span><span class="sxs-lookup"><span data-stu-id="a50af-121">**ConvertByteBufferToSafeArray**</span></span>](iscardtypeconv-convertbytebuffertosafearray.md) | <span data-ttu-id="a50af-122">將對應至位元組 (**IStream** 物件) 的位元組陣列轉換成不帶正負號 char (byte) 的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="a50af-122">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span><br/> |
| [<span data-ttu-id="a50af-123">**ConvertSafeArrayToByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="a50af-123">**ConvertSafeArrayToByteBuffer**</span></span>](iscardtypeconv-convertsafearraytobytebuffer.md) | <span data-ttu-id="a50af-124">將定義為 SAFEARRAY 的位元組陣列轉換成 (**IStream** 物件) 的通用位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a50af-124">Converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span><br/>                          |
| [<span data-ttu-id="a50af-125">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="a50af-125">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)                           | <span data-ttu-id="a50af-126">建立位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="a50af-126">Creates an array of bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="a50af-127">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="a50af-127">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)                         | <span data-ttu-id="a50af-128">建立對應至 **IStream** ([**IByteBuffer**](ibytebuffer.md)) 物件的通用位元組緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a50af-128">Creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span><br/>                  |
| [<span data-ttu-id="a50af-129">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="a50af-129">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)                           | <span data-ttu-id="a50af-130">建立不帶正負號字元的自動化 SAFEARRAY， (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="a50af-130">Creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span><br/>                                                              |
| [<span data-ttu-id="a50af-131">**FreeIStreamMemoryPtr**</span><span class="sxs-lookup"><span data-stu-id="a50af-131">**FreeIStreamMemoryPtr**</span></span>](iscardtypeconv-freeistreammemoryptr.md)                 | <span data-ttu-id="a50af-132">釋放由 **IStream** COM 介面管理之 HGLOBAL 記憶體區塊的記憶體指標。</span><span class="sxs-lookup"><span data-stu-id="a50af-132">Frees a memory pointer to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span><br/>                                  |
| [<span data-ttu-id="a50af-133">**GetAtIStreamMemory**</span><span class="sxs-lookup"><span data-stu-id="a50af-133">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)                     | <span data-ttu-id="a50af-134">取得由 **IStream** COM 介面管理的 HGLOBAL 記憶體區塊的位元組指標。</span><span class="sxs-lookup"><span data-stu-id="a50af-134">Acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span><br/>                        |
| [<span data-ttu-id="a50af-135">**SizeOfIStream**</span><span class="sxs-lookup"><span data-stu-id="a50af-135">**SizeOfIStream**</span></span>](iscardtypeconv-sizeofistream.md)                               | <span data-ttu-id="a50af-136">決定 **IStream** COM 介面)  (位元組數的大小。</span><span class="sxs-lookup"><span data-stu-id="a50af-136">Determines the size (number of bytes) of an **IStream** COM interface.</span></span><br/>                                                       |



 

## <a name="requirements"></a><span data-ttu-id="a50af-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="a50af-137">Requirements</span></span>



| <span data-ttu-id="a50af-138">需求</span><span class="sxs-lookup"><span data-stu-id="a50af-138">Requirement</span></span> | <span data-ttu-id="a50af-139">值</span><span class="sxs-lookup"><span data-stu-id="a50af-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a50af-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a50af-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a50af-141">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a50af-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a50af-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a50af-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a50af-143">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a50af-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a50af-144">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a50af-144">End of client support</span></span><br/>    | <span data-ttu-id="a50af-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a50af-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a50af-146">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a50af-146">End of server support</span></span><br/>    | <span data-ttu-id="a50af-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a50af-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a50af-148">標頭</span><span class="sxs-lookup"><span data-stu-id="a50af-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="a50af-149"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="a50af-149"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a50af-150">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a50af-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="a50af-151"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a50af-151"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a50af-152">DLL</span><span class="sxs-lookup"><span data-stu-id="a50af-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a50af-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a50af-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a50af-154">IID</span><span class="sxs-lookup"><span data-stu-id="a50af-154">IID</span></span><br/>                      | <span data-ttu-id="a50af-155">IID \_ ISCardTypeConv 定義為53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a50af-155">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



 

 
