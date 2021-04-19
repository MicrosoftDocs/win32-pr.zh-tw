---
title: 設定. invokeURLs
description: InvokeURLs 屬性會指定或抓取值，指出 URL 事件是否應該啟動網頁瀏覽器。
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- 設定. invokeURLs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977689"
---
# <a name="settingsinvokeurls"></a><span data-ttu-id="11f93-104">設定. invokeURLs</span><span class="sxs-lookup"><span data-stu-id="11f93-104">Settings.invokeURLs</span></span>

<span data-ttu-id="11f93-105">**InvokeURLs** 屬性會指定或抓取值，指出 URL 事件是否應該啟動網頁瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="11f93-105">The **invokeURLs** property specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f93-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="11f93-106">Syntax</span></span>

<span data-ttu-id="11f93-107">invokeURLs</span><span class="sxs-lookup"><span data-stu-id="11f93-107">player.settings.invokeURLs</span></span>

## <a name="possible-values"></a><span data-ttu-id="11f93-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="11f93-108">Possible Values</span></span>

<span data-ttu-id="11f93-109">這個屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="11f93-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="11f93-110">值</span><span class="sxs-lookup"><span data-stu-id="11f93-110">Value</span></span> | <span data-ttu-id="11f93-111">描述</span><span class="sxs-lookup"><span data-stu-id="11f93-111">Description</span></span>                                  |
|-------|----------------------------------------------|
| <span data-ttu-id="11f93-112">true</span><span class="sxs-lookup"><span data-stu-id="11f93-112">true</span></span>  | <span data-ttu-id="11f93-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="11f93-113">Default.</span></span> <span data-ttu-id="11f93-114">URL 事件應該會啟動瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="11f93-114">URL events should launch a browser.</span></span> |
| <span data-ttu-id="11f93-115">false</span><span class="sxs-lookup"><span data-stu-id="11f93-115">false</span></span> | <span data-ttu-id="11f93-116">URL 事件不應該啟動瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="11f93-116">URL events should not launch a browser.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="11f93-117">備註</span><span class="sxs-lookup"><span data-stu-id="11f93-117">Remarks</span></span>

<span data-ttu-id="11f93-118">媒體檔案可以包含 Url。</span><span class="sxs-lookup"><span data-stu-id="11f93-118">Media files can contain URLs.</span></span> <span data-ttu-id="11f93-119">將 URL 傳送至 Windows Media Player 控制項時，會先將它傳遞給 **ScriptCommand** 事件處理常式，而不論 **invokeURLs** 中的值為何。</span><span class="sxs-lookup"><span data-stu-id="11f93-119">When a URL is sent to the Windows Media Player control, it is passed first to the **ScriptCommand** event handler regardless of the value in **invokeURLs**.</span></span> <span data-ttu-id="11f93-120">**ScriptCommand** 結束後，Windows Media Player 會檢查 **invokeURLs** ，以判斷是否要使用 URL 啟動預設的網際網路瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="11f93-120">After **ScriptCommand** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Internet browser with the URL.</span></span> <span data-ttu-id="11f93-121">您可以選擇性地顯示 Url，方法是在 **ScriptCommand** 中進行檢查，並視需要設定 **invokeURLs** 。</span><span class="sxs-lookup"><span data-stu-id="11f93-121">You can selectively display URLs by checking them in **ScriptCommand** and setting **invokeURLs** as desired.</span></span>

<span data-ttu-id="11f93-122">**Windows Media Player 10** 行動裝置版：此屬性只接受或傳回 false。</span><span class="sxs-lookup"><span data-stu-id="11f93-122">**Windows Media Player 10 Mobile**: This property only accepts or returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f93-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="11f93-123">Requirements</span></span>



| <span data-ttu-id="11f93-124">需求</span><span class="sxs-lookup"><span data-stu-id="11f93-124">Requirement</span></span> | <span data-ttu-id="11f93-125">值</span><span class="sxs-lookup"><span data-stu-id="11f93-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11f93-126">版本</span><span class="sxs-lookup"><span data-stu-id="11f93-126">Version</span></span><br/> | <span data-ttu-id="11f93-127">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="11f93-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="11f93-128">DLL</span><span class="sxs-lookup"><span data-stu-id="11f93-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="11f93-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11f93-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11f93-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11f93-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f93-131">**ScriptCommand 事件**</span><span class="sxs-lookup"><span data-stu-id="11f93-131">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="11f93-132">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="11f93-132">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





