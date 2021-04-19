---
description: ISCardDatabase 介面提供執行智慧卡資源管理員的資料庫作業的方法。
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: 'ISCardDatabase 介面 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971002"
---
# <a name="iscarddatabase-interface"></a><span data-ttu-id="38098-103">ISCardDatabase 介面</span><span class="sxs-lookup"><span data-stu-id="38098-103">ISCardDatabase interface</span></span>

<span data-ttu-id="38098-104">\[**ISCardDatabase** 介面可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="38098-104">\[The **ISCardDatabase** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="38098-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="38098-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="38098-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="38098-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="38098-107">**ISCardDatabase** 介面提供執行 [*智慧卡*](../secgloss/s-gly.md)[*資源管理員的*](../secgloss/r-gly.md)資料庫作業的方法。</span><span class="sxs-lookup"><span data-stu-id="38098-107">The **ISCardDatabase** interface provides the methods for performing the [*smart card*](../secgloss/s-gly.md) [*resource manager's*](../secgloss/r-gly.md) database operations.</span></span> <span data-ttu-id="38098-108">這些作業包括列出已知的智慧卡、 [*讀取*](../secgloss/r-gly.md)器和讀取器群組，以及抓取智慧卡和其 [*主要服務提供者*](../secgloss/p-gly.md)所支援的介面。</span><span class="sxs-lookup"><span data-stu-id="38098-108">These operations include listing known smart cards, [*readers*](../secgloss/r-gly.md), and reader groups, plus retrieving the interfaces supported by a smart card and its [*primary service provider*](../secgloss/p-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="38098-109">主要服務提供者的識別碼是 COM GUID，可用來具現化和使用特定卡片的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="38098-109">The identifier of the primary service provider is a COM GUID that can be used to instantiate and use the COM objects for a specific card.</span></span>

 

<span data-ttu-id="38098-110">下列範例顯示 **ISCardDatabase** 介面的一般用法。</span><span class="sxs-lookup"><span data-stu-id="38098-110">The following example shows a typical use of the **ISCardDatabase** interface.</span></span> <span data-ttu-id="38098-111">在此情況下， **ISCardDatabase** 介面會用來列出所有已知的智慧卡。</span><span class="sxs-lookup"><span data-stu-id="38098-111">In this case, the **ISCardDatabase** interface is used to list all the known smart cards.</span></span>

<span data-ttu-id="38098-112">**將交易提交至特定卡片**</span><span class="sxs-lookup"><span data-stu-id="38098-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="38098-113">建立 **ISCardDatabase** 介面。</span><span class="sxs-lookup"><span data-stu-id="38098-113">Create an **ISCardDatabase** interface.</span></span>
2.  <span data-ttu-id="38098-114">呼叫 [**ListCards**](iscarddatabase-listcards.md) ，以根據 [*ATR 字串*](../secgloss/a-gly.md) 或其支援的介面來取得所有已知的智慧卡。</span><span class="sxs-lookup"><span data-stu-id="38098-114">Call [**ListCards**](iscarddatabase-listcards.md) to retrieve all the known smart cards based on an [*ATR string*](../secgloss/a-gly.md) or their supported interfaces.</span></span>
3.  <span data-ttu-id="38098-115">釋放 **ISCardDatabase** 介面。</span><span class="sxs-lookup"><span data-stu-id="38098-115">Release the **ISCardDatabase** interface.</span></span>

## <a name="members"></a><span data-ttu-id="38098-116">成員</span><span class="sxs-lookup"><span data-stu-id="38098-116">Members</span></span>

<span data-ttu-id="38098-117">**ISCardDatabase** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="38098-117">The **ISCardDatabase** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="38098-118">**ISCardDatabase** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="38098-118">**ISCardDatabase** also has these types of members:</span></span>

-   [<span data-ttu-id="38098-119">方法</span><span class="sxs-lookup"><span data-stu-id="38098-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="38098-120">方法</span><span class="sxs-lookup"><span data-stu-id="38098-120">Methods</span></span>

<span data-ttu-id="38098-121">**ISCardDatabase** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="38098-121">The **ISCardDatabase** interface has these methods.</span></span>



| <span data-ttu-id="38098-122">方法</span><span class="sxs-lookup"><span data-stu-id="38098-122">Method</span></span>                                                          | <span data-ttu-id="38098-123">描述</span><span class="sxs-lookup"><span data-stu-id="38098-123">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38098-124">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="38098-124">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)   | <span data-ttu-id="38098-125">抓取特定智慧卡之 [*主要服務提供者*](../secgloss/p-gly.md) 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="38098-125">Retrieves the identifier of the [*primary service provider*](../secgloss/p-gly.md) for a specific smart card.</span></span><br/> |
| [<span data-ttu-id="38098-126">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="38098-126">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md) | <span data-ttu-id="38098-127">抓取特定智慧卡支援的所有介面 (Guid) 的介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="38098-127">Retrieves the interface identifiers (GUIDs) of all the interfaces supported by a specific smart card.</span></span><br/>                                                                                 |
| [<span data-ttu-id="38098-128">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="38098-128">**ListCards**</span></span>](iscarddatabase-listcards.md)                   | <span data-ttu-id="38098-129">抓取符合一組特定介面識別碼 (Guid) 或 [*ATR 字串*](../secgloss/a-gly.md)的所有智慧卡名稱。</span><span class="sxs-lookup"><span data-stu-id="38098-129">Retrieves all the smart card names that match a specific set of interface identifiers (GUIDs) or an [*ATR string*](../secgloss/a-gly.md).</span></span><br/> |
| [<span data-ttu-id="38098-130">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="38098-130">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)     | <span data-ttu-id="38098-131">抓取資源管理員有知識的 [*讀者群組*](../secgloss/r-gly.md) 名稱。</span><span class="sxs-lookup"><span data-stu-id="38098-131">Retrieves the names of the [*reader groups*](../secgloss/r-gly.md) that the resource manager has knowledge of.</span></span><br/>                        |
| [<span data-ttu-id="38098-132">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="38098-132">**ListReaders**</span></span>](iscarddatabase-listreaders.md)               | <span data-ttu-id="38098-133">取得資源管理員有知識的 [*讀者*](../secgloss/r-gly.md) 名稱。</span><span class="sxs-lookup"><span data-stu-id="38098-133">Retrieve the names of the [*readers*](../secgloss/r-gly.md) of which the resource manager has knowledge.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="38098-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="38098-134">Requirements</span></span>



| <span data-ttu-id="38098-135">需求</span><span class="sxs-lookup"><span data-stu-id="38098-135">Requirement</span></span> | <span data-ttu-id="38098-136">值</span><span class="sxs-lookup"><span data-stu-id="38098-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38098-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38098-137">Minimum supported client</span></span><br/> | <span data-ttu-id="38098-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38098-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="38098-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38098-139">Minimum supported server</span></span><br/> | <span data-ttu-id="38098-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38098-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="38098-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="38098-141">End of client support</span></span><br/>    | <span data-ttu-id="38098-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="38098-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="38098-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="38098-143">End of server support</span></span><br/>    | <span data-ttu-id="38098-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38098-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="38098-145">標頭</span><span class="sxs-lookup"><span data-stu-id="38098-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="38098-146"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="38098-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="38098-147">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="38098-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="38098-148"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="38098-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="38098-149">DLL</span><span class="sxs-lookup"><span data-stu-id="38098-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38098-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38098-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="38098-151">IID</span><span class="sxs-lookup"><span data-stu-id="38098-151">IID</span></span><br/>                      | <span data-ttu-id="38098-152">IID \_ ISCardDatabase 定義為1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="38098-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



 

 
