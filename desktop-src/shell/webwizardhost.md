---
description: 公開方法，這些方法可讓您在 wizard 擴充功能中裝載的 HTML 網頁與 wizard 進行通訊。
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: 'WebWizardHost 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 1fbaf53db11fda577e9e9c5384af5f7c62fe1944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944174"
---
# <a name="webwizardhost-object"></a><span data-ttu-id="db4df-103">WebWizardHost 物件</span><span class="sxs-lookup"><span data-stu-id="db4df-103">WebWizardHost object</span></span>

<span data-ttu-id="db4df-104">公開方法，這些方法可讓您在 wizard 擴充功能中裝載的 HTML 網頁與 wizard 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="db4df-104">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span>

## <a name="members"></a><span data-ttu-id="db4df-105">成員</span><span class="sxs-lookup"><span data-stu-id="db4df-105">Members</span></span>

<span data-ttu-id="db4df-106">**WebWizardHost** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="db4df-106">The **WebWizardHost** object has these types of members:</span></span>

-   [<span data-ttu-id="db4df-107">方法</span><span class="sxs-lookup"><span data-stu-id="db4df-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="db4df-108">屬性</span><span class="sxs-lookup"><span data-stu-id="db4df-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="db4df-109">方法</span><span class="sxs-lookup"><span data-stu-id="db4df-109">Methods</span></span>

<span data-ttu-id="db4df-110">**WebWizardHost** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="db4df-110">The **WebWizardHost** object has these methods.</span></span>



| <span data-ttu-id="db4df-111">方法</span><span class="sxs-lookup"><span data-stu-id="db4df-111">Method</span></span>                                                      | <span data-ttu-id="db4df-112">描述</span><span class="sxs-lookup"><span data-stu-id="db4df-112">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db4df-113">**取消**</span><span class="sxs-lookup"><span data-stu-id="db4df-113">**Cancel**</span></span>](iwebwizardhost-cancel.md)                     | <span data-ttu-id="db4df-114">模擬 [ **取消** ] 按鈕的按一下。</span><span class="sxs-lookup"><span data-stu-id="db4df-114">Simulates a **Cancel** button click.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="db4df-115">**FinalBack**</span><span class="sxs-lookup"><span data-stu-id="db4df-115">**FinalBack**</span></span>](iwebwizardhost-finalback.md)               | <span data-ttu-id="db4df-116">在主控伺服器端 HTML 頁面的頁面上，直接流覽至用戶端頁面。</span><span class="sxs-lookup"><span data-stu-id="db4df-116">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span><br/>                                                                    |
| [<span data-ttu-id="db4df-117">**FinalNext**</span><span class="sxs-lookup"><span data-stu-id="db4df-117">**FinalNext**</span></span>](iwebwizardhost-finalnext.md)               | <span data-ttu-id="db4df-118">流覽至裝載伺服器端 HTML 頁面的頁面下的用戶端 wizard 頁面，或者，如果沒有進一步的用戶端頁面，則完成 wizard。</span><span class="sxs-lookup"><span data-stu-id="db4df-118">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span><br/> |
| [<span data-ttu-id="db4df-119">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="db4df-119">**SetHeaderText**</span></span>](iwebwizardhost-setheadertext.md)       | <span data-ttu-id="db4df-120">設定出現在 wizard 標頭中的標題和副標題。</span><span class="sxs-lookup"><span data-stu-id="db4df-120">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="db4df-121">一般而言，用戶端會將標頭顯示在 HTML 和標題列下方。</span><span class="sxs-lookup"><span data-stu-id="db4df-121">In general, the client will display the header above the HTML and below the title bar.</span></span><br/>                    |
| [<span data-ttu-id="db4df-122">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="db4df-122">**SetWizardButtons**</span></span>](iwebwizardhost-setwizardbuttons.md) | <span data-ttu-id="db4df-123">更新用戶端的 wizard 框架中的 [ **上一頁**]、 **[下一頁**] 和 **[完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="db4df-123">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="db4df-124">屬性</span><span class="sxs-lookup"><span data-stu-id="db4df-124">Properties</span></span>

<span data-ttu-id="db4df-125">**WebWizardHost** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="db4df-125">The **WebWizardHost** object has these properties.</span></span>



| <span data-ttu-id="db4df-126">屬性</span><span class="sxs-lookup"><span data-stu-id="db4df-126">Property</span></span>                                               | <span data-ttu-id="db4df-127">存取類型</span><span class="sxs-lookup"><span data-stu-id="db4df-127">Access type</span></span>           | <span data-ttu-id="db4df-128">Description</span><span class="sxs-lookup"><span data-stu-id="db4df-128">Description</span></span>                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="db4df-129">**標題**</span><span class="sxs-lookup"><span data-stu-id="db4df-129">**Caption**</span></span>](iwebwizardhost-caption.md)<br/>   | <span data-ttu-id="db4df-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="db4df-130">Read/write</span></span><br/> | <span data-ttu-id="db4df-131">未實作。</span><span class="sxs-lookup"><span data-stu-id="db4df-131">Not implemented.</span></span><br/>                              |
| [<span data-ttu-id="db4df-132">**屬性**</span><span class="sxs-lookup"><span data-stu-id="db4df-132">**Property**</span></span>](iwebwizardhost-property.md)<br/> | <span data-ttu-id="db4df-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="db4df-133">Read/write</span></span><br/> | <span data-ttu-id="db4df-134">設定或抓取屬性的目前值。</span><span class="sxs-lookup"><span data-stu-id="db4df-134">Sets or retrieves a property's current value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="db4df-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="db4df-135">Requirements</span></span>



| <span data-ttu-id="db4df-136">需求</span><span class="sxs-lookup"><span data-stu-id="db4df-136">Requirement</span></span> | <span data-ttu-id="db4df-137">值</span><span class="sxs-lookup"><span data-stu-id="db4df-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db4df-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db4df-138">Minimum supported client</span></span><br/> | <span data-ttu-id="db4df-139">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db4df-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="db4df-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db4df-140">Minimum supported server</span></span><br/> | <span data-ttu-id="db4df-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db4df-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="db4df-142">標頭</span><span class="sxs-lookup"><span data-stu-id="db4df-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="db4df-143"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="db4df-143"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="db4df-144">Idl</span><span class="sxs-lookup"><span data-stu-id="db4df-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db4df-145"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="db4df-145"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="db4df-146">IID</span><span class="sxs-lookup"><span data-stu-id="db4df-146">IID</span></span><br/>                      | <span data-ttu-id="db4df-147">CLSID \_ WebWizardHost</span><span class="sxs-lookup"><span data-stu-id="db4df-147">CLSID\_WebWizardHost</span></span><br/>                                                        |



 

 




