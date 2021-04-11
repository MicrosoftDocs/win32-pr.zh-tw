---
description: MIME 資料表會建立 MIME 內容類型與副檔名或 CLSID 之間的關聯，以產生廣告 (多用途網際網路郵件延伸) 內容的通告所需的擴充功能或 COM 伺服器資訊。
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: MIME 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194090"
---
# <a name="mime-table"></a><span data-ttu-id="b2ccc-103">MIME 資料表</span><span class="sxs-lookup"><span data-stu-id="b2ccc-103">MIME Table</span></span>

<span data-ttu-id="b2ccc-104">MIME 資料表會建立 MIME 內容類型與副檔名或 CLSID 之間的關聯，以產生廣告 (多用途網際網路郵件延伸) 內容的通告所需的擴充功能或 COM 伺服器資訊。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-104">The MIME table associates a MIME content type with a file name extension or a CLSID to generate the extension or COM server information required for advertisement of the MIME (Multipurpose Internet Mail Extensions) content.</span></span>

<span data-ttu-id="b2ccc-105">MIME 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-105">The MIME table has the following columns.</span></span>



| <span data-ttu-id="b2ccc-106">Column</span><span class="sxs-lookup"><span data-stu-id="b2ccc-106">Column</span></span>      | <span data-ttu-id="b2ccc-107">類型</span><span class="sxs-lookup"><span data-stu-id="b2ccc-107">Type</span></span>             | <span data-ttu-id="b2ccc-108">答案</span><span class="sxs-lookup"><span data-stu-id="b2ccc-108">Key</span></span> | <span data-ttu-id="b2ccc-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="b2ccc-109">Nullable</span></span> |
|-------------|------------------|-----|----------|
| <span data-ttu-id="b2ccc-110">ContentType</span><span class="sxs-lookup"><span data-stu-id="b2ccc-110">ContentType</span></span> | [<span data-ttu-id="b2ccc-111">Text</span><span class="sxs-lookup"><span data-stu-id="b2ccc-111">Text</span></span>](text.md) | <span data-ttu-id="b2ccc-112">Y</span><span class="sxs-lookup"><span data-stu-id="b2ccc-112">Y</span></span>   | <span data-ttu-id="b2ccc-113">N</span><span class="sxs-lookup"><span data-stu-id="b2ccc-113">N</span></span>        |
| <span data-ttu-id="b2ccc-114">分機\_</span><span class="sxs-lookup"><span data-stu-id="b2ccc-114">Extension\_</span></span> | [<span data-ttu-id="b2ccc-115">Text</span><span class="sxs-lookup"><span data-stu-id="b2ccc-115">Text</span></span>](text.md) | <span data-ttu-id="b2ccc-116">N</span><span class="sxs-lookup"><span data-stu-id="b2ccc-116">N</span></span>   | <span data-ttu-id="b2ccc-117">N</span><span class="sxs-lookup"><span data-stu-id="b2ccc-117">N</span></span>        |
| <span data-ttu-id="b2ccc-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="b2ccc-118">CLSID</span></span>       | [<span data-ttu-id="b2ccc-119">GUID</span><span class="sxs-lookup"><span data-stu-id="b2ccc-119">GUID</span></span>](guid.md) | <span data-ttu-id="b2ccc-120">N</span><span class="sxs-lookup"><span data-stu-id="b2ccc-120">N</span></span>   | <span data-ttu-id="b2ccc-121">Y</span><span class="sxs-lookup"><span data-stu-id="b2ccc-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b2ccc-122">資料行</span><span class="sxs-lookup"><span data-stu-id="b2ccc-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b2ccc-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span><span class="sxs-lookup"><span data-stu-id="b2ccc-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span></span>
</dt> <dd>

<span data-ttu-id="b2ccc-124">此資料行是 MIME 內容的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-124">This column is an identifier for the MIME content.</span></span> <span data-ttu-id="b2ccc-125">它通常是以型別/格式來撰寫。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-125">It is commonly written in the form of type/format.</span></span>

</dd> <dt>

<span data-ttu-id="b2ccc-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>擴展\_</span><span class="sxs-lookup"><span data-stu-id="b2ccc-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="b2ccc-127">此資料行包含要與 MIME 內容相關聯的伺服器延伸模組（不含點）。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-127">This column contains the server extension that is to be associated with the MIME content, without the dot.</span></span> <span data-ttu-id="b2ccc-128">此資料行是 [延伸模組資料表](extension-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-128">This column is a foreign key into the [Extension table](extension-table.md).</span></span> <span data-ttu-id="b2ccc-129">延伸模組資料表包含用來作為公告一部分的副檔名伺服器資訊。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-129">The Extension table contains file name extension server information which is used as a part of advertisement.</span></span>

</dd> <dt>

<span data-ttu-id="b2ccc-130"><span id="CLSID"></span><span id="clsid"></span>Clsid</span><span class="sxs-lookup"><span data-stu-id="b2ccc-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="b2ccc-131">此資料行包含要與 MIME 內容相關聯的 COM 伺服器 CLSID。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-131">This column contains the COM server CLSID that is to be associated with the MIME content.</span></span> <span data-ttu-id="b2ccc-132">此資料行中的 CLSID 可以是 [類別資料表](class-table.md) 中的外鍵，也可以是已存在於使用者電腦上的 clsid。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-132">The CLSID in this column can be a foreign key into the [Class table](class-table.md) or it can be a CLSID that already exists on the user's machine.</span></span> <span data-ttu-id="b2ccc-133">類別資料表包含 COM 伺服器的相關資訊，此資訊可作為公告的一部分。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-133">The Class table contains COM server-related information which is used as a part of advertisement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2ccc-134">備註</span><span class="sxs-lookup"><span data-stu-id="b2ccc-134">Remarks</span></span>

<span data-ttu-id="b2ccc-135">當執行 [RegisterMIMEInfo 動作](registermimeinfo-action.md) 或 [UnregisterMIMEInfo 動作](unregistermimeinfo-action.md) 時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-135">This table is referred to when the [RegisterMIMEInfo action](registermimeinfo-action.md) or the [UnregisterMIMEInfo action](unregistermimeinfo-action.md) is executed.</span></span> <span data-ttu-id="b2ccc-136">在 [公告] 模式中，[RegisterMIMEInfo] 動作會從已啟用對應功能的 MIME 資料表中，註冊伺服器的所有 MIME 資訊。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-136">In advertise mode, the RegisterMIMEInfo action registers all MIME information for servers from the MIME table for which the corresponding feature is enabled.</span></span> <span data-ttu-id="b2ccc-137">否則，此動作會從 MIME 資料表中，為目前選取要安裝對應功能的伺服器註冊 MIME 資訊。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-137">Otherwise the action registers MIME information for servers from the MIME table for which the corresponding feature is currently selected to be installed.</span></span> <span data-ttu-id="b2ccc-138">[UnregisterMIMEInfo 動作](unregistermimeinfo-action.md)會從系統中取消註冊 MIME 相關的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-138">The [UnregisterMIMEInfo action](unregistermimeinfo-action.md) unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="b2ccc-139">動作會從 MIME 資料表中取消註冊伺服器的 MIME 資訊，而這項功能目前已選取要卸載的對應功能。</span><span class="sxs-lookup"><span data-stu-id="b2ccc-139">The action unregisters MIME information for servers from the MIME table for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="validation"></a><span data-ttu-id="b2ccc-140">驗證</span><span class="sxs-lookup"><span data-stu-id="b2ccc-140">Validation</span></span>

<dl>

[<span data-ttu-id="b2ccc-141">ICE03</span><span class="sxs-lookup"><span data-stu-id="b2ccc-141">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b2ccc-142">ICE06</span><span class="sxs-lookup"><span data-stu-id="b2ccc-142">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b2ccc-143">ICE15</span><span class="sxs-lookup"><span data-stu-id="b2ccc-143">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="b2ccc-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="b2ccc-144">ICE32</span></span>](ice32.md)  
</dl>

 

 



