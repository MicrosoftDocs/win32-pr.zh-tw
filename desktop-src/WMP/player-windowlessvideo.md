---
title: WindowlessVideo
description: WindowlessVideo 屬性會指定或抓取值，指出 Windows Media Player 控制項是否以無視窗模式呈現影片。
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- WindowlessVideo Windows Media Player
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990049"
---
# <a name="playerwindowlessvideo"></a><span data-ttu-id="54066-104">WindowlessVideo</span><span class="sxs-lookup"><span data-stu-id="54066-104">Player.windowlessVideo</span></span>

<span data-ttu-id="54066-105">**WindowlessVideo** 屬性會指定或抓取值，指出 Windows Media Player 控制項是否以無視窗模式呈現影片。</span><span class="sxs-lookup"><span data-stu-id="54066-105">The **windowlessVideo** property specifies or retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="54066-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="54066-106">Syntax</span></span>

<span data-ttu-id="54066-107">*玩家*。**windowlessVideo**</span><span class="sxs-lookup"><span data-stu-id="54066-107">*player*.**windowlessVideo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="54066-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="54066-108">Possible Values</span></span>

<span data-ttu-id="54066-109">這個屬性是在設計階段指定的 **布林值** ，之後是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="54066-109">This property is a **Boolean** that is specified at design time and is read-only thereafter.</span></span>



| <span data-ttu-id="54066-110">值</span><span class="sxs-lookup"><span data-stu-id="54066-110">Value</span></span> | <span data-ttu-id="54066-111">描述</span><span class="sxs-lookup"><span data-stu-id="54066-111">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="54066-112">true</span><span class="sxs-lookup"><span data-stu-id="54066-112">true</span></span>  | <span data-ttu-id="54066-113">影片以無視窗模式呈現。</span><span class="sxs-lookup"><span data-stu-id="54066-113">The video is rendered in windowless mode.</span></span>        |
| <span data-ttu-id="54066-114">false</span><span class="sxs-lookup"><span data-stu-id="54066-114">false</span></span> | <span data-ttu-id="54066-115">預設值。</span><span class="sxs-lookup"><span data-stu-id="54066-115">Default.</span></span> <span data-ttu-id="54066-116">影片會以視窗模式呈現。</span><span class="sxs-lookup"><span data-stu-id="54066-116">The video is rendered in windowed mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="54066-117">備註</span><span class="sxs-lookup"><span data-stu-id="54066-117">Remarks</span></span>

<span data-ttu-id="54066-118">根據預設，內嵌的 Windows Media Player 控制項會在用戶端區域內的它自己的視窗中呈現影片。</span><span class="sxs-lookup"><span data-stu-id="54066-118">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="54066-119">當 **windowlessVideo** 設定為 true 時，播放程式控制項會直接在工作區中轉譯影片，因此您可以套用特殊效果或以文字將影片分層。</span><span class="sxs-lookup"><span data-stu-id="54066-119">When **windowlessVideo** is set to true, the Player control renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="54066-120">在 Windows Vista 中，以無視窗模式轉譯影片可能會降低效能。</span><span class="sxs-lookup"><span data-stu-id="54066-120">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="54066-121">Netscape Navigator 不支援 **windowlessVideo** 屬性。</span><span class="sxs-lookup"><span data-stu-id="54066-121">The **windowlessVideo** property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="54066-122">在 [導覽器] 中設定此屬性的值可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="54066-122">Setting a value for this property in Navigator may yield unexpected results.</span></span>

<span data-ttu-id="54066-123">**Windows Media Player 10** 行動裝置版：不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="54066-123">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="54066-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="54066-124">Requirements</span></span>



| <span data-ttu-id="54066-125">需求</span><span class="sxs-lookup"><span data-stu-id="54066-125">Requirement</span></span> | <span data-ttu-id="54066-126">值</span><span class="sxs-lookup"><span data-stu-id="54066-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54066-127">版本</span><span class="sxs-lookup"><span data-stu-id="54066-127">Version</span></span><br/> | <span data-ttu-id="54066-128">適用于 Windows XP 或更新版本的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="54066-128">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="54066-129">DLL</span><span class="sxs-lookup"><span data-stu-id="54066-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="54066-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54066-130"><dt>Wmp.dll</dt></span></span> </dl> |



 

 





