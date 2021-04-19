---
title: 'IResultVerb 介面 (WdsSharedIDL .h) '
description: 公開動詞屬性。
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- IResultVerb 介面舊版 Windows 環境功能
- IResultVerb 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967551"
---
# <a name="iresultverb-interface"></a><span data-ttu-id="87f6c-105">IResultVerb 介面</span><span class="sxs-lookup"><span data-stu-id="87f6c-105">IResultVerb interface</span></span>

> [!NOTE]
> <span data-ttu-id="87f6c-106">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="87f6c-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="87f6c-107">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="87f6c-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="87f6c-108">公開動詞屬性。</span><span class="sxs-lookup"><span data-stu-id="87f6c-108">Exposes verb properties.</span></span>

## <a name="members"></a><span data-ttu-id="87f6c-109">成員</span><span class="sxs-lookup"><span data-stu-id="87f6c-109">Members</span></span>

<span data-ttu-id="87f6c-110">**IResultVerb** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="87f6c-110">The **IResultVerb** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="87f6c-111">**IResultVerb** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="87f6c-111">**IResultVerb** also has these types of members:</span></span>

-   [<span data-ttu-id="87f6c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="87f6c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87f6c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="87f6c-113">Properties</span></span>

<span data-ttu-id="87f6c-114">**IResultVerb** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="87f6c-114">The **IResultVerb** interface has these properties.</span></span>



| <span data-ttu-id="87f6c-115">屬性</span><span class="sxs-lookup"><span data-stu-id="87f6c-115">Property</span></span>                                                             | <span data-ttu-id="87f6c-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="87f6c-116">Access type</span></span>           | <span data-ttu-id="87f6c-117">Description</span><span class="sxs-lookup"><span data-stu-id="87f6c-117">Description</span></span>                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87f6c-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="87f6c-118">**DisplayName**</span></span>](-search-2x-iresultverb-displayname.md)<br/> | <span data-ttu-id="87f6c-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="87f6c-119">Read-only</span></span><br/>  | <span data-ttu-id="87f6c-120">這個屬性會傳回動詞之當地語系化顯示名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="87f6c-120">This property returns a pointer to the localized display name for the verb.</span></span> <br/>                           |
| [<span data-ttu-id="87f6c-121">**Doit r**</span><span class="sxs-lookup"><span data-stu-id="87f6c-121">**DoIt**</span></span>](-search-2x-iresultverb-doit.md)<br/>               | <span data-ttu-id="87f6c-122">唯寫</span><span class="sxs-lookup"><span data-stu-id="87f6c-122">Write-only</span></span><br/> | <span data-ttu-id="87f6c-123">執行動詞。</span><span class="sxs-lookup"><span data-stu-id="87f6c-123">Executes the verb.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="87f6c-124">**啟用**</span><span class="sxs-lookup"><span data-stu-id="87f6c-124">**Enabled**</span></span>](-search-2x-iresultverb-enabled.md)<br/>         | <span data-ttu-id="87f6c-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="87f6c-125">Read-only</span></span><br/>  | <span data-ttu-id="87f6c-126">如果已啟用動詞，這個屬性會傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="87f6c-126">This property returns TRUE if the verb is enabled.</span></span> <br/>                                                    |
| [<span data-ttu-id="87f6c-127">**HelpText**</span><span class="sxs-lookup"><span data-stu-id="87f6c-127">**HelpText**</span></span>](-search-2x-iresultverb-helptext.md)<br/>       | <span data-ttu-id="87f6c-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="87f6c-128">Read-only</span></span><br/>  | <span data-ttu-id="87f6c-129">這個屬性會傳回動詞的當地語系化說明字串指標。</span><span class="sxs-lookup"><span data-stu-id="87f6c-129">This property returns a pointer to the localized help string for the verb.</span></span> <br/>                            |
| [<span data-ttu-id="87f6c-130">**圖示**</span><span class="sxs-lookup"><span data-stu-id="87f6c-130">**Icon**</span></span>](-search-2x-iresultverb-icon.md)<br/>               | <span data-ttu-id="87f6c-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="87f6c-131">Read-only</span></span><br/>  | <span data-ttu-id="87f6c-132">這個屬性會傳回與動詞相關聯之選擇性圖示的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="87f6c-132">This property returns a pointer to handle of the optional icon associated with the verb.</span></span> <br/>              |
| [<span data-ttu-id="87f6c-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="87f6c-133">**Name**</span></span>](-search-2x-iresultverb-name.md)<br/>               | <span data-ttu-id="87f6c-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="87f6c-134">Read-only</span></span><br/>  | <span data-ttu-id="87f6c-135">這個屬性會傳回動詞的 cononical 名稱指標，例如 print、open 等等。</span><span class="sxs-lookup"><span data-stu-id="87f6c-135">This property returns a pointer to the cononical name for the verb such as print, open, and so forth.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="87f6c-136">備註</span><span class="sxs-lookup"><span data-stu-id="87f6c-136">Remarks</span></span>

<span data-ttu-id="87f6c-137">這些方法會公開適用于動詞的屬性和動作。</span><span class="sxs-lookup"><span data-stu-id="87f6c-137">These methods expose properties and actions applicable to verbs.</span></span>

## <a name="requirements"></a><span data-ttu-id="87f6c-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="87f6c-138">Requirements</span></span>



| <span data-ttu-id="87f6c-139">需求</span><span class="sxs-lookup"><span data-stu-id="87f6c-139">Requirement</span></span> | <span data-ttu-id="87f6c-140">值</span><span class="sxs-lookup"><span data-stu-id="87f6c-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f6c-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87f6c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="87f6c-142">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87f6c-142">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="87f6c-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87f6c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="87f6c-144">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87f6c-144">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="87f6c-145">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="87f6c-145">Redistributable</span></span><br/>          | <span data-ttu-id="87f6c-146">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="87f6c-146">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="87f6c-147">標頭</span><span class="sxs-lookup"><span data-stu-id="87f6c-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="87f6c-148"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="87f6c-148"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

