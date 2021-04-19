---
description: 地區設定 \_ ITIMEMARKPOSN
ms.assetid: 4aef2631-c05b-41e8-8f4d-f40da4143ab4
title: LOCALE_ITIMEMARKPOSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0182235754d8f5b6b95bad6c58b4fee87d394d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997287"
---
# <a name="locale_itimemarkposn"></a><span data-ttu-id="d6318-103">地區設定 \_ ITIMEMARKPOSN</span><span class="sxs-lookup"><span data-stu-id="d6318-103">LOCALE\_ITIMEMARKPOSN</span></span>

<span data-ttu-id="d6318-104">指定時間標記字串 (AM 或 PM 是否) 在時間字串之前或之後的規範。</span><span class="sxs-lookup"><span data-stu-id="d6318-104">Specifier indicating whether the time marker string (AM or PM) precedes or follows the time string.</span></span> <span data-ttu-id="d6318-105">ITimePrefix 登錄值的方式是與舊版 Windows 的相容性。</span><span class="sxs-lookup"><span data-stu-id="d6318-105">The registry value is iTimePrefix for compatibility with previous Asian versions of Windows.</span></span> <span data-ttu-id="d6318-106">規範必須有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d6318-106">The specifier must have one of the following values.</span></span> <span data-ttu-id="d6318-107">不允許使用者指定的值。</span><span class="sxs-lookup"><span data-stu-id="d6318-107">No user-specified values are allowed.</span></span> <span data-ttu-id="d6318-108">最好讓您的應用程式使用地區設定 [ \_ STIMEFORMAT](locale-stime-constants.md) 常數，而不是地區設定 \_ ITIMEMARKPOSN。</span><span class="sxs-lookup"><span data-stu-id="d6318-108">It is preferred for your application to use the [LOCALE\_STIMEFORMAT](locale-stime-constants.md) constant instead of LOCALE\_ITIMEMARKPOSN.</span></span>



| <span data-ttu-id="d6318-109">值</span><span class="sxs-lookup"><span data-stu-id="d6318-109">Value</span></span> | <span data-ttu-id="d6318-110">意義</span><span class="sxs-lookup"><span data-stu-id="d6318-110">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="d6318-111">0</span><span class="sxs-lookup"><span data-stu-id="d6318-111">0</span></span>     | <span data-ttu-id="d6318-112">使用做為尾碼。</span><span class="sxs-lookup"><span data-stu-id="d6318-112">Use as suffix.</span></span> |
| <span data-ttu-id="d6318-113">1</span><span class="sxs-lookup"><span data-stu-id="d6318-113">1</span></span>     | <span data-ttu-id="d6318-114">使用做為前置詞。</span><span class="sxs-lookup"><span data-stu-id="d6318-114">Use as prefix.</span></span> |



 

 

 



