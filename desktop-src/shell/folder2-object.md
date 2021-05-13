---
description: 擴充資料夾物件以支援離線資料夾。
title: 'Folder2 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: c2c630ef36f6e4b2b58f3902c3d5728a31ad1f0d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842059"
---
# <a name="folder2-object"></a><span data-ttu-id="a0af9-103">Folder2 物件</span><span class="sxs-lookup"><span data-stu-id="a0af9-103">Folder2 object</span></span>

<span data-ttu-id="a0af9-104">擴充 [**資料夾**](folder.md) 物件以支援離線資料夾。</span><span class="sxs-lookup"><span data-stu-id="a0af9-104">Extends the [**Folder**](folder.md) object to support offline folders.</span></span>

## <a name="members"></a><span data-ttu-id="a0af9-105">成員</span><span class="sxs-lookup"><span data-stu-id="a0af9-105">Members</span></span>

<span data-ttu-id="a0af9-106">**Folder2** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a0af9-106">The **Folder2** object has these types of members:</span></span>

-   [<span data-ttu-id="a0af9-107">方法</span><span class="sxs-lookup"><span data-stu-id="a0af9-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0af9-108">屬性</span><span class="sxs-lookup"><span data-stu-id="a0af9-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0af9-109">方法</span><span class="sxs-lookup"><span data-stu-id="a0af9-109">Methods</span></span>

<span data-ttu-id="a0af9-110">**Folder2** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a0af9-110">The **Folder2** object has these methods.</span></span>



| <span data-ttu-id="a0af9-111">方法</span><span class="sxs-lookup"><span data-stu-id="a0af9-111">Method</span></span>                                                                 | <span data-ttu-id="a0af9-112">描述</span><span class="sxs-lookup"><span data-stu-id="a0af9-112">Description</span></span>                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0af9-113">**DismissedWebViewBarricade**</span><span class="sxs-lookup"><span data-stu-id="a0af9-113">**DismissedWebViewBarricade**</span></span>](folder2-dismissedwebviewbarricade.md) | <span data-ttu-id="a0af9-114">呼叫以回應使用者所關閉的 web view barricade。</span><span class="sxs-lookup"><span data-stu-id="a0af9-114">Called in response to the web view barricade being dismissed by the user.</span></span><br/> |
| [<span data-ttu-id="a0af9-115">**同步**</span><span class="sxs-lookup"><span data-stu-id="a0af9-115">**Synchronize**</span></span>](folder2-synchronize.md)                             | <span data-ttu-id="a0af9-116">同步處理資料夾中的所有離線檔案。</span><span class="sxs-lookup"><span data-stu-id="a0af9-116">Synchronizes all offline files in the folder.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="a0af9-117">屬性</span><span class="sxs-lookup"><span data-stu-id="a0af9-117">Properties</span></span>

<span data-ttu-id="a0af9-118">**Folder2** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a0af9-118">The **Folder2** object has these properties.</span></span>



| <span data-ttu-id="a0af9-119">屬性</span><span class="sxs-lookup"><span data-stu-id="a0af9-119">Property</span></span>                                                                            | <span data-ttu-id="a0af9-120">存取類型</span><span class="sxs-lookup"><span data-stu-id="a0af9-120">Access type</span></span>          | <span data-ttu-id="a0af9-121">描述</span><span class="sxs-lookup"><span data-stu-id="a0af9-121">Description</span></span>                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="a0af9-122">**HaveToShowWebViewBarricade**</span><span class="sxs-lookup"><span data-stu-id="a0af9-122">**HaveToShowWebViewBarricade**</span></span>](folder2-havetoshowwebviewbarricade.md)<br/> | <span data-ttu-id="a0af9-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="a0af9-123">Read-only</span></span><br/> | <span data-ttu-id="a0af9-124">目前不支援。</span><span class="sxs-lookup"><span data-stu-id="a0af9-124">Not currently supported.</span></span><br/>                                       |
| [<span data-ttu-id="a0af9-125">**OfflineStatus**</span><span class="sxs-lookup"><span data-stu-id="a0af9-125">**OfflineStatus**</span></span>](folder2-offlinestatus.md)<br/>                           | <span data-ttu-id="a0af9-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="a0af9-126">Read-only</span></span><br/> | <span data-ttu-id="a0af9-127">包含資料夾的離線狀態。</span><span class="sxs-lookup"><span data-stu-id="a0af9-127">Contains the offline status of the folder.</span></span><br/>                     |
| [<span data-ttu-id="a0af9-128">**自我**</span><span class="sxs-lookup"><span data-stu-id="a0af9-128">**Self**</span></span>](folder2-self.md)<br/>                                             | <span data-ttu-id="a0af9-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="a0af9-129">Read-only</span></span><br/> | <span data-ttu-id="a0af9-130">包含資料夾的 [**FolderItem**](folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a0af9-130">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a0af9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0af9-131">Requirements</span></span>



| <span data-ttu-id="a0af9-132">需求</span><span class="sxs-lookup"><span data-stu-id="a0af9-132">Requirement</span></span> | <span data-ttu-id="a0af9-133">值</span><span class="sxs-lookup"><span data-stu-id="a0af9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0af9-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0af9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a0af9-135">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0af9-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0af9-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0af9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a0af9-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0af9-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a0af9-138">標頭</span><span class="sxs-lookup"><span data-stu-id="a0af9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0af9-139"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a0af9-140">Idl</span><span class="sxs-lookup"><span data-stu-id="a0af9-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0af9-141"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a0af9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a0af9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0af9-143"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0af9-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0af9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0af9-145">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="a0af9-145">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




