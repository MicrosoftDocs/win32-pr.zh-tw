---
description: ISCardLocate 介面提供用來依名稱尋找智慧卡的服務。
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: 'ISCardLocate 介面 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979216"
---
# <a name="iscardlocate-interface"></a><span data-ttu-id="e7908-103">ISCardLocate 介面</span><span class="sxs-lookup"><span data-stu-id="e7908-103">ISCardLocate interface</span></span>

<span data-ttu-id="e7908-104">\[**ISCardLocate** 介面可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e7908-104">\[The **ISCardLocate** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e7908-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="e7908-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e7908-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e7908-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e7908-107">**ISCardLocate** 介面提供用來依名稱尋找 [*智慧卡*](../secgloss/s-gly.md)的服務。</span><span class="sxs-lookup"><span data-stu-id="e7908-107">The **ISCardLocate** interface provides services for locating a [*smart card*](../secgloss/s-gly.md) by its name.</span></span>

<span data-ttu-id="e7908-108">此介面可以顯示智慧卡 [*使用者介面*](../secgloss/u-gly.md) （如有需要）。</span><span class="sxs-lookup"><span data-stu-id="e7908-108">This interface can display the smart card [*user interface*](../secgloss/u-gly.md) if it is required.</span></span>

<span data-ttu-id="e7908-109">下列案例顯示 **ISCardLocate** 介面的一般用法。</span><span class="sxs-lookup"><span data-stu-id="e7908-109">The following scenario shows a typical use of the **ISCardLocate** interface.</span></span> <span data-ttu-id="e7908-110">**ISCardLocate** 介面可用來建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="e7908-110">The **ISCardLocate** interface is used to build an [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

<span data-ttu-id="e7908-111">**使用名稱找出特定的卡片**</span><span class="sxs-lookup"><span data-stu-id="e7908-111">**To locate a specific card using its name**</span></span>

1.  <span data-ttu-id="e7908-112">建立 **ISCardLocate** 介面。</span><span class="sxs-lookup"><span data-stu-id="e7908-112">Create an **ISCardLocate** interface.</span></span>
2.  <span data-ttu-id="e7908-113">呼叫 [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) 以搜尋智慧卡名稱。</span><span class="sxs-lookup"><span data-stu-id="e7908-113">Call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to search for a smart card name.</span></span>
3.  <span data-ttu-id="e7908-114">呼叫 [**FindCard**](iscardlocate-findcard.md) 以搜尋智慧卡。</span><span class="sxs-lookup"><span data-stu-id="e7908-114">Call [**FindCard**](iscardlocate-findcard.md) to search for the smart card.</span></span>
4.  <span data-ttu-id="e7908-115">解譯解譯。</span><span class="sxs-lookup"><span data-stu-id="e7908-115">Interpret the results.</span></span>
5.  <span data-ttu-id="e7908-116">釋放 **ISCardLocate** 介面。</span><span class="sxs-lookup"><span data-stu-id="e7908-116">Release the **ISCardLocate** interface.</span></span>

## <a name="members"></a><span data-ttu-id="e7908-117">成員</span><span class="sxs-lookup"><span data-stu-id="e7908-117">Members</span></span>

<span data-ttu-id="e7908-118">**ISCardLocate** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="e7908-118">The **ISCardLocate** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e7908-119">**ISCardLocate** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e7908-119">**ISCardLocate** also has these types of members:</span></span>

-   [<span data-ttu-id="e7908-120">方法</span><span class="sxs-lookup"><span data-stu-id="e7908-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e7908-121">方法</span><span class="sxs-lookup"><span data-stu-id="e7908-121">Methods</span></span>

<span data-ttu-id="e7908-122">**ISCardLocate** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e7908-122">The **ISCardLocate** interface has these methods.</span></span>



| <span data-ttu-id="e7908-123">方法</span><span class="sxs-lookup"><span data-stu-id="e7908-123">Method</span></span>                                                                  | <span data-ttu-id="e7908-124">描述</span><span class="sxs-lookup"><span data-stu-id="e7908-124">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="e7908-125">**ConfigureCardGuidSearch**</span><span class="sxs-lookup"><span data-stu-id="e7908-125">**ConfigureCardGuidSearch**</span></span>                                             | <span data-ttu-id="e7908-126">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e7908-126">Reserved for future use.</span></span><br/>                                        |
| [<span data-ttu-id="e7908-127">**ConfigureCardNameSearch**</span><span class="sxs-lookup"><span data-stu-id="e7908-127">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md) | <span data-ttu-id="e7908-128">指定要在搜尋中使用的卡片名稱。</span><span class="sxs-lookup"><span data-stu-id="e7908-128">Specifies the card name to be used in the search.</span></span><br/>               |
| [<span data-ttu-id="e7908-129">**FindCard**</span><span class="sxs-lookup"><span data-stu-id="e7908-129">**FindCard**</span></span>](iscardlocate-findcard.md)                               | <span data-ttu-id="e7908-130">搜尋智慧卡，並對其開啟有效的連接。</span><span class="sxs-lookup"><span data-stu-id="e7908-130">Searches for the smart card and opens a valid connection to it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e7908-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7908-131">Requirements</span></span>



| <span data-ttu-id="e7908-132">需求</span><span class="sxs-lookup"><span data-stu-id="e7908-132">Requirement</span></span> | <span data-ttu-id="e7908-133">值</span><span class="sxs-lookup"><span data-stu-id="e7908-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7908-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7908-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e7908-135">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7908-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e7908-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7908-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e7908-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7908-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7908-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e7908-138">End of client support</span></span><br/>    | <span data-ttu-id="e7908-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e7908-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e7908-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e7908-140">End of server support</span></span><br/>    | <span data-ttu-id="e7908-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7908-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e7908-142">標頭</span><span class="sxs-lookup"><span data-stu-id="e7908-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7908-143"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7908-143"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7908-144">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e7908-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7908-145"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e7908-145"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e7908-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e7908-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7908-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7908-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7908-148">IID</span><span class="sxs-lookup"><span data-stu-id="e7908-148">IID</span></span><br/>                      | <span data-ttu-id="e7908-149">IID \_ ISCardLocate 定義為1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e7908-149">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



 

 
