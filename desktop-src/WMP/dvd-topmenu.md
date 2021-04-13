---
title: TopMenu 方法
description: TopMenu 方法會停止播放標題，並顯示目前標題的上方 (或根) 功能表。
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- topMenu 方法 Windows Media Player
- topMenu 方法 Windows Media Player、DVD 類別
- DVD 類別 Windows Media Player，topMenu 方法
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465749"
---
# <a name="dvdtopmenu-method"></a><span data-ttu-id="82f93-106">TopMenu 方法</span><span class="sxs-lookup"><span data-stu-id="82f93-106">DVD.topMenu method</span></span>

<span data-ttu-id="82f93-107">**TopMenu** 方法會停止播放標題，並顯示目前標題的上方 (或根) 功能表。</span><span class="sxs-lookup"><span data-stu-id="82f93-107">The **topMenu** method stops title playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f93-108">語法</span><span class="sxs-lookup"><span data-stu-id="82f93-108">Syntax</span></span>


```JScript
DVD.topMenu()
```



## <a name="parameters"></a><span data-ttu-id="82f93-109">參數</span><span class="sxs-lookup"><span data-stu-id="82f93-109">Parameters</span></span>

<span data-ttu-id="82f93-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="82f93-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="82f93-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="82f93-111">Return value</span></span>

<span data-ttu-id="82f93-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="82f93-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82f93-113">備註</span><span class="sxs-lookup"><span data-stu-id="82f93-113">Remarks</span></span>

<span data-ttu-id="82f93-114">每個 DVD 的撰寫方式不同。</span><span class="sxs-lookup"><span data-stu-id="82f93-114">Every DVD is authored differently.</span></span> <span data-ttu-id="82f93-115">DVD 必須包含功能表，這個方法才能運作。</span><span class="sxs-lookup"><span data-stu-id="82f93-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="82f93-116">撰寫一些 Dvd，讓 **topMenu** 和 **titleMenu** 方法開啟相同的功能表。</span><span class="sxs-lookup"><span data-stu-id="82f93-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="82f93-117">**TopMenu** 方法通常會叫用 top (或 root) 功能表，但如果沒有可用的根功能表，它可能會改為叫用標題功能表。</span><span class="sxs-lookup"><span data-stu-id="82f93-117">The **topMenu** method usually invokes the top (or root) menu but it may invoke the title menu instead, if there is no root menu available.</span></span>

<span data-ttu-id="82f93-118">**Windows Media Player 10** 行動裝置版：這個方法一律會成功，但不會執行預定的作業。</span><span class="sxs-lookup"><span data-stu-id="82f93-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="82f93-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="82f93-119">Requirements</span></span>



| <span data-ttu-id="82f93-120">需求</span><span class="sxs-lookup"><span data-stu-id="82f93-120">Requirement</span></span> | <span data-ttu-id="82f93-121">值</span><span class="sxs-lookup"><span data-stu-id="82f93-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82f93-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82f93-122">Minimum supported client</span></span><br/> | <span data-ttu-id="82f93-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82f93-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82f93-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82f93-124">Minimum supported server</span></span><br/> | <span data-ttu-id="82f93-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82f93-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="82f93-126">版本</span><span class="sxs-lookup"><span data-stu-id="82f93-126">Version</span></span><br/>                  | <span data-ttu-id="82f93-127">適用于 Windows XP 或更新版本的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="82f93-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="82f93-128">DLL</span><span class="sxs-lookup"><span data-stu-id="82f93-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82f93-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82f93-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82f93-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82f93-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f93-131">**DVD 物件**</span><span class="sxs-lookup"><span data-stu-id="82f93-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="82f93-132">**TitleMenu**</span><span class="sxs-lookup"><span data-stu-id="82f93-132">**DVD.titleMenu**</span></span>](dvd-titlemenu.md)
</dt> </dl>

 

 





