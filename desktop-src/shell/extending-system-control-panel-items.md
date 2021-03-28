---
description: 在主控台中找到的某些系統專案是可擴充的。 若要安裝主控台擴充功能，請依照下列方式註冊您的 Shell 擴充功能，其中 name 是系統專案的預先定義名稱 (請參閱下表) 。
title: 擴充系統主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991158"
---
# <a name="extending-system-control-panel-items"></a><span data-ttu-id="9f085-104">擴充系統主控台專案</span><span class="sxs-lookup"><span data-stu-id="9f085-104">Extending System Control Panel Items</span></span>

<span data-ttu-id="9f085-105">在主控台中找到的某些系統專案是可擴充的。</span><span class="sxs-lookup"><span data-stu-id="9f085-105">Some of the system items found in the Control Panel are extensible.</span></span> <span data-ttu-id="9f085-106">若要安裝主控台擴充功能，請依照下列方式註冊您的 Shell 擴充功能，其中 *name* 是系統專案的預先定義名稱 (請參閱下表) 。</span><span class="sxs-lookup"><span data-stu-id="9f085-106">To install a Control Panel extension, register your Shell extension as follows, where *name* is the predefined name of the system item (see table below).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

<span data-ttu-id="9f085-107">這與您針對預先定義的 Shell 物件註冊擴充功能的方式類似。</span><span class="sxs-lookup"><span data-stu-id="9f085-107">This is similar to the way you would register an extension for a predefined Shell object.</span></span> <span data-ttu-id="9f085-108">因為主控台專案所支援的唯一 Shell 擴充功能是屬性工作表，所以註冊必須在 **shellex** PropertySheetHandlers 子機碼下 \\  。</span><span class="sxs-lookup"><span data-stu-id="9f085-108">Because the only Shell extensions supported by Control Panel items are property sheets, the registration must be under the **shellex**\\**PropertySheetHandlers** subkey.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f085-109">主控台專案</span><span class="sxs-lookup"><span data-stu-id="9f085-109">Control Panel item</span></span></th>
<th><span data-ttu-id="9f085-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="9f085-110"><em>name</em></span></span></th>
<th><span data-ttu-id="9f085-111">備註</span><span class="sxs-lookup"><span data-stu-id="9f085-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9f085-112">顯示</span><span class="sxs-lookup"><span data-stu-id="9f085-112">Display</span></span></td>
<td><span data-ttu-id="9f085-113">桌子</span><span class="sxs-lookup"><span data-stu-id="9f085-113">Desk</span></span></td>
<td><span data-ttu-id="9f085-114">也支援取代 <strong>桌面</strong> 網頁。</span><span class="sxs-lookup"><span data-stu-id="9f085-114">Also supports replacement of the <strong>Desktop</strong> page.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f085-115">Windows Vista 已不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="9f085-115">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f085-116">顯示設定 Advanced</span><span class="sxs-lookup"><span data-stu-id="9f085-116">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="9f085-117">裝置</span><span class="sxs-lookup"><span data-stu-id="9f085-117">Device</span></span></td>
<td><span data-ttu-id="9f085-118">Nonhardware 特定的 advanced 屬性。</span><span class="sxs-lookup"><span data-stu-id="9f085-118">Nonhardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f085-119">Windows Vista 已不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="9f085-119">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f085-120">顯示設定 Advanced</span><span class="sxs-lookup"><span data-stu-id="9f085-120">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="9f085-121">顯示</span><span class="sxs-lookup"><span data-stu-id="9f085-121">Display</span></span></td>
<td><span data-ttu-id="9f085-122">硬體特定的 advanced 屬性。</span><span class="sxs-lookup"><span data-stu-id="9f085-122">Hardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f085-123">Windows Vista 已不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="9f085-123">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f085-124">網際網路選項</span><span class="sxs-lookup"><span data-stu-id="9f085-124">Internet Options</span></span></td>
<td><span data-ttu-id="9f085-125">網際網路</span><span class="sxs-lookup"><span data-stu-id="9f085-125">Internet</span></span></td>
<td><span data-ttu-id="9f085-126">延伸模組頁面的最大數目為18。</span><span class="sxs-lookup"><span data-stu-id="9f085-126">The maximum number of extension pages is 18.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f085-127">鍵盤</span><span class="sxs-lookup"><span data-stu-id="9f085-127">Keyboard</span></span></td>
<td><span data-ttu-id="9f085-128">鍵盤</span><span class="sxs-lookup"><span data-stu-id="9f085-128">Keyboard</span></span></td>
<td><span data-ttu-id="9f085-129">延伸頁面的最大數目為30。</span><span class="sxs-lookup"><span data-stu-id="9f085-129">The maximum number of extension pages is 30.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f085-130">滑鼠</span><span class="sxs-lookup"><span data-stu-id="9f085-130">Mouse</span></span></td>
<td><span data-ttu-id="9f085-131">滑鼠</span><span class="sxs-lookup"><span data-stu-id="9f085-131">Mouse</span></span></td>
<td><span data-ttu-id="9f085-132">也支援取代標準頁面。</span><span class="sxs-lookup"><span data-stu-id="9f085-132">Also supports replacement of standard pages.</span></span> <span data-ttu-id="9f085-133">延伸模組頁面的數目上限為8。</span><span class="sxs-lookup"><span data-stu-id="9f085-133">The maximum number of extension pages is 8.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f085-134">電源選項</span><span class="sxs-lookup"><span data-stu-id="9f085-134">Power Options</span></span></td>
<td><span data-ttu-id="9f085-135">電源</span><span class="sxs-lookup"><span data-stu-id="9f085-135">Power</span></span></td>
<td><span data-ttu-id="9f085-136">頁面數目上限（包括標準頁面）為18。</span><span class="sxs-lookup"><span data-stu-id="9f085-136">The maximum number of pages, including standard pages, is 18.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f085-137">系統</span><span class="sxs-lookup"><span data-stu-id="9f085-137">System</span></span></td>
<td><span data-ttu-id="9f085-138">系統</span><span class="sxs-lookup"><span data-stu-id="9f085-138">System</span></span></td>
<td><span data-ttu-id="9f085-139">延伸模組頁面的數目上限為8。</span><span class="sxs-lookup"><span data-stu-id="9f085-139">The maximum number of extension pages is 8.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f085-140">Windows Vista 已不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="9f085-140">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9f085-141">Windows XP 主控台中的 [ **新增或移除程式** ] 專案不是屬性工作表，因此無法透過此處討論的方法來擴充。</span><span class="sxs-lookup"><span data-stu-id="9f085-141">The **Add or Remove Programs** item in the Windows XP Control Panel is not a property sheet and therefore cannot be extended by the methods discussed here.</span></span> <span data-ttu-id="9f085-142">相反地，它的內容是從應用程式發行者取得的。</span><span class="sxs-lookup"><span data-stu-id="9f085-142">Instead, its content is obtained from application publishers.</span></span> <span data-ttu-id="9f085-143">如需有關新增內容至 **新增或移除程式** 的詳細資訊，請參閱 [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher)、 [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)和 [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp)。</span><span class="sxs-lookup"><span data-stu-id="9f085-143">For more information on adding content to **Add or Remove Programs**, see [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps), and [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f085-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f085-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f085-145">主控台專案</span><span class="sxs-lookup"><span data-stu-id="9f085-145">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="9f085-146">使用者體驗指南</span><span class="sxs-lookup"><span data-stu-id="9f085-146">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="9f085-147">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="9f085-147">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="9f085-148">使用 CPLApplet</span><span class="sxs-lookup"><span data-stu-id="9f085-148">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="9f085-149">主控台訊息處理</span><span class="sxs-lookup"><span data-stu-id="9f085-149">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="9f085-150">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="9f085-150">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="9f085-151">指派主控台分類</span><span class="sxs-lookup"><span data-stu-id="9f085-151">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="9f085-152">建立主控台專案的可搜尋工作連結</span><span class="sxs-lookup"><span data-stu-id="9f085-152">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="9f085-153">在 Windows Vista 下存取安全模式下的主控台</span><span class="sxs-lookup"><span data-stu-id="9f085-153">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




