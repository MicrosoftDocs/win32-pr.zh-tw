---
title: TitleMenu 方法
description: TitleMenu 方法會停止播放標題，並顯示標題功能表。
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- titleMenu 方法 Windows Media Player
- titleMenu 方法 Windows Media Player、DVD 類別
- DVD 類別 Windows Media Player，titleMenu 方法
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317212"
---
# <a name="dvdtitlemenu-method"></a><span data-ttu-id="2f042-106">TitleMenu 方法</span><span class="sxs-lookup"><span data-stu-id="2f042-106">DVD.titleMenu method</span></span>

<span data-ttu-id="2f042-107">**TitleMenu** 方法會停止播放標題，並顯示標題功能表。</span><span class="sxs-lookup"><span data-stu-id="2f042-107">The **titleMenu** method stops title playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f042-108">語法</span><span class="sxs-lookup"><span data-stu-id="2f042-108">Syntax</span></span>


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a><span data-ttu-id="2f042-109">參數</span><span class="sxs-lookup"><span data-stu-id="2f042-109">Parameters</span></span>

<span data-ttu-id="2f042-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2f042-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f042-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f042-111">Return value</span></span>

<span data-ttu-id="2f042-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2f042-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f042-113">備註</span><span class="sxs-lookup"><span data-stu-id="2f042-113">Remarks</span></span>

<span data-ttu-id="2f042-114">每個 DVD 的撰寫方式不同。</span><span class="sxs-lookup"><span data-stu-id="2f042-114">Every DVD is authored differently.</span></span> <span data-ttu-id="2f042-115">DVD 必須包含功能表，這個方法才能運作。</span><span class="sxs-lookup"><span data-stu-id="2f042-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="2f042-116">撰寫一些 Dvd，讓 **topMenu** 和 **titleMenu** 方法開啟相同的功能表。</span><span class="sxs-lookup"><span data-stu-id="2f042-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="2f042-117">**TitleMenu** 方法通常會叫用標題功能表，但如果沒有可用的標題功能表，它可能會叫用上層功能表。</span><span class="sxs-lookup"><span data-stu-id="2f042-117">The **titleMenu** method usually invokes the title menu but it may invoke the top menu instead, if there is no title menu available.</span></span>

<span data-ttu-id="2f042-118">**Windows Media Player 10** 行動裝置版：這個方法一律會成功，但不會執行預定的作業。</span><span class="sxs-lookup"><span data-stu-id="2f042-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f042-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f042-119">Requirements</span></span>



| <span data-ttu-id="2f042-120">需求</span><span class="sxs-lookup"><span data-stu-id="2f042-120">Requirement</span></span> | <span data-ttu-id="2f042-121">值</span><span class="sxs-lookup"><span data-stu-id="2f042-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f042-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f042-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2f042-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f042-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f042-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f042-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2f042-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f042-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2f042-126">版本</span><span class="sxs-lookup"><span data-stu-id="2f042-126">Version</span></span><br/>                  | <span data-ttu-id="2f042-127">適用于 Windows XP 或更新版本的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="2f042-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="2f042-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2f042-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f042-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f042-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f042-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f042-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f042-131">**DVD 物件**</span><span class="sxs-lookup"><span data-stu-id="2f042-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="2f042-132">**TopMenu**</span><span class="sxs-lookup"><span data-stu-id="2f042-132">**DVD.topMenu**</span></span>](dvd-topmenu.md)
</dt> </dl>

 

 





