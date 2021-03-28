---
description: 父裝置內容可讓應用程式將設定視窗裁剪區域所需的時間減至最少。
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: 父代顯示裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972593"
---
# <a name="parent-display-device-contexts"></a><span data-ttu-id="2c4b1-103">父代顯示裝置內容</span><span class="sxs-lookup"><span data-stu-id="2c4b1-103">Parent Display Device Contexts</span></span>

<span data-ttu-id="2c4b1-104">*父裝置內容* 可讓應用程式將設定視窗裁剪區域所需的時間減至最少。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-104">A *parent device context* enables an application to minimize the time necessary to set up the clipping region for a window.</span></span> <span data-ttu-id="2c4b1-105">應用程式通常會使用上層裝置內容來加速控制視窗的繪製，而不需要私人或類別的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-105">An application typically uses parent device contexts to speed up drawing for control windows without requiring a private or class device context.</span></span> <span data-ttu-id="2c4b1-106">例如，系統會使用推播按鈕和編輯控制項的父裝置內容。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-106">For example, the system uses parent device contexts for push button and edit controls.</span></span> <span data-ttu-id="2c4b1-107">父裝置內容僅適用于子視窗，絕不會使用最上層或快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-107">Parent device contexts are intended for use with child windows only, never with top-level or pop-up windows.</span></span>

<span data-ttu-id="2c4b1-108">應用程式可以指定 CS \_ PARENTDC 樣式，將子視窗的裁剪區域設定為父視窗的裁剪區域，讓子視窗可以在父系中繪製。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-108">An application can specify the CS\_PARENTDC style to set the clipping region of the child window to that of the parent window so that the child can draw in the parent.</span></span> <span data-ttu-id="2c4b1-109">指定 CS \_ PARENTDC 可增強應用程式的效能，因為系統不需要持續重新計算每個子視窗的可見區域。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-109">Specifying CS\_PARENTDC enhances an application's performance because the system doesn't need to keep recalculating the visible region for each child window.</span></span>

<span data-ttu-id="2c4b1-110">父視窗所設定的屬性值不會保留給子視窗;例如，父視窗無法設定其子視窗的筆刷。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-110">Attribute values set by the parent window are not preserved for the child window; for example, the parent window cannot set the brush for its child windows.</span></span> <span data-ttu-id="2c4b1-111">唯一保留的屬性是裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-111">The only property preserved is the clipping region.</span></span> <span data-ttu-id="2c4b1-112">視窗必須將本身的輸出裁剪至視窗的限制。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-112">The window must clip its own output to the limits of the window.</span></span> <span data-ttu-id="2c4b1-113">因為父裝置內容的裁剪區域與父視窗相同，所以子視窗可能會在整個父視窗上繪製，但不能以這種方式使用父裝置內容。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-113">Because the clipping region for the parent device context is identical to the parent window, the child window can potentially draw over the entire parent window, but the parent device context must not be used in this way.</span></span>

<span data-ttu-id="2c4b1-114">如果父視窗 \_ 使用私用或類別裝置內容，系統會忽略 CS PARENTDC 樣式，如果父視窗裁剪其子視窗，或子視窗裁剪其子視窗或同級視窗。</span><span class="sxs-lookup"><span data-stu-id="2c4b1-114">The system ignores the CS\_PARENTDC style if the parent window uses a private or class device context, if the parent window clips its child windows, or if the child window clips its child windows or sibling windows.</span></span>

 

 



