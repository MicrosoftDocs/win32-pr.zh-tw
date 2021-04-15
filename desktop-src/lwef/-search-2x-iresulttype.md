---
title: 'IResultType 介面 (WdsSharedIDL .h) '
description: 公開屬性類型資訊。
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- IResultType 介面舊版 Windows 環境功能
- IResultType 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464916"
---
# <a name="iresulttype-interface"></a><span data-ttu-id="fbec7-105">IResultType 介面</span><span class="sxs-lookup"><span data-stu-id="fbec7-105">IResultType interface</span></span>

> [!NOTE]
> <span data-ttu-id="fbec7-106">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="fbec7-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="fbec7-107">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="fbec7-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="fbec7-108">公開屬性類型資訊。</span><span class="sxs-lookup"><span data-stu-id="fbec7-108">Exposes property type information.</span></span>

## <a name="members"></a><span data-ttu-id="fbec7-109">成員</span><span class="sxs-lookup"><span data-stu-id="fbec7-109">Members</span></span>

<span data-ttu-id="fbec7-110">**IResultType** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="fbec7-110">The **IResultType** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fbec7-111">**IResultType** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fbec7-111">**IResultType** also has these types of members:</span></span>

-   [<span data-ttu-id="fbec7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fbec7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fbec7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="fbec7-113">Properties</span></span>

<span data-ttu-id="fbec7-114">**IResultType** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fbec7-114">The **IResultType** interface has these properties.</span></span>



| <span data-ttu-id="fbec7-115">屬性</span><span class="sxs-lookup"><span data-stu-id="fbec7-115">Property</span></span>                                                                 | <span data-ttu-id="fbec7-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="fbec7-116">Access type</span></span>           | <span data-ttu-id="fbec7-117">Description</span><span class="sxs-lookup"><span data-stu-id="fbec7-117">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="fbec7-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="fbec7-118">**DisplayName**</span></span>](-search-2x-iresulttype-displayname.md)<br/>     | <span data-ttu-id="fbec7-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="fbec7-119">Read-only</span></span><br/>  | <span data-ttu-id="fbec7-120">類型的當地語系化顯示名稱：</span><span class="sxs-lookup"><span data-stu-id="fbec7-120">Localized display name of the type:</span></span><br/>                                        |
| [<span data-ttu-id="fbec7-121">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="fbec7-121">**GetProperty**</span></span>](-search-2x-iresulttype-getproperty.md)<br/>     | <span data-ttu-id="fbec7-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fbec7-122">Read/write</span></span><br/> | <span data-ttu-id="fbec7-123">此屬性包含指定的屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="fbec7-123">This property contains specified property information.</span></span> <br/>                    |
| [<span data-ttu-id="fbec7-124">**PreceivedType**</span><span class="sxs-lookup"><span data-stu-id="fbec7-124">**PreceivedType**</span></span>](-search-2x-iresulttype-preceivedtype.md)<br/> | <span data-ttu-id="fbec7-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="fbec7-125">Read-only</span></span><br/>  | <span data-ttu-id="fbec7-126">這個屬性包含用來識別索引中之類型的字串。</span><span class="sxs-lookup"><span data-stu-id="fbec7-126">This property contains the string used to identify the type in the index.</span></span> <br/> |
| [<span data-ttu-id="fbec7-127">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="fbec7-127">**PropertyCount**</span></span>](-search-2x-iresulttype-propertycount.md)<br/> | <span data-ttu-id="fbec7-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="fbec7-128">Read-only</span></span><br/>  | <span data-ttu-id="fbec7-129">這個屬性包含型別所公開的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="fbec7-129">This property contains the number of properties exposed by the type.</span></span> <br/>      |
| [<span data-ttu-id="fbec7-130">**UID**</span><span class="sxs-lookup"><span data-stu-id="fbec7-130">**UID**</span></span>](-search-2x-iresulttype-uid.md)<br/>                     | <span data-ttu-id="fbec7-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="fbec7-131">Read-only</span></span><br/>  | <span data-ttu-id="fbec7-132">此屬性包含類型的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fbec7-132">This property contains the unique identifier for the type.</span></span> <br/>                |



 

## <a name="remarks"></a><span data-ttu-id="fbec7-133">備註</span><span class="sxs-lookup"><span data-stu-id="fbec7-133">Remarks</span></span>

<span data-ttu-id="fbec7-134">這些方法會公開傳回的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="fbec7-134">These methods expose the types of information returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbec7-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbec7-135">Requirements</span></span>



| <span data-ttu-id="fbec7-136">需求</span><span class="sxs-lookup"><span data-stu-id="fbec7-136">Requirement</span></span> | <span data-ttu-id="fbec7-137">值</span><span class="sxs-lookup"><span data-stu-id="fbec7-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbec7-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbec7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fbec7-139">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbec7-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fbec7-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbec7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fbec7-141">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbec7-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fbec7-142">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="fbec7-142">Redistributable</span></span><br/>          | <span data-ttu-id="fbec7-143">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="fbec7-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="fbec7-144">標頭</span><span class="sxs-lookup"><span data-stu-id="fbec7-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbec7-145"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbec7-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

