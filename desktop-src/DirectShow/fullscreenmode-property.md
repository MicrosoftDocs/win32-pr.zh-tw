---
description: FullScreenMode 屬性會設定或抓取值，指出顯示器是否處於全螢幕模式。
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: FullScreenMode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108537"
---
# <a name="fullscreenmode-property"></a><span data-ttu-id="7c88a-103">FullScreenMode 屬性</span><span class="sxs-lookup"><span data-stu-id="7c88a-103">FullScreenMode Property</span></span>

> [!Note]  
> <span data-ttu-id="7c88a-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="7c88a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7c88a-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="7c88a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7c88a-106">`FullScreenMode`屬性會設定或抓取值，指出顯示器是否處於全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="7c88a-106">The `FullScreenMode` property sets or retrieves a value indicating whether the display is in full-screen mode.</span></span>

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a><span data-ttu-id="7c88a-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c88a-107">Return Value</span></span>

<span data-ttu-id="7c88a-108">傳回布林值，指出是否要啟用或停用全螢幕播放。</span><span class="sxs-lookup"><span data-stu-id="7c88a-108">Returns a Boolean value indicating whether to enable or disable full-screen playback.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c88a-109">備註</span><span class="sxs-lookup"><span data-stu-id="7c88a-109">Remarks</span></span>

<span data-ttu-id="7c88a-110">這個屬性是讀取/寫入，預設值是 false。</span><span class="sxs-lookup"><span data-stu-id="7c88a-110">This property is read/write with a default value of false.</span></span>



| <span data-ttu-id="7c88a-111">值</span><span class="sxs-lookup"><span data-stu-id="7c88a-111">Value</span></span> | <span data-ttu-id="7c88a-112">描述</span><span class="sxs-lookup"><span data-stu-id="7c88a-112">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="7c88a-113">true</span><span class="sxs-lookup"><span data-stu-id="7c88a-113">true</span></span>  | <span data-ttu-id="7c88a-114">啟用全螢幕播放。</span><span class="sxs-lookup"><span data-stu-id="7c88a-114">Enable full-screen playback.</span></span> <span data-ttu-id="7c88a-115">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="7c88a-115">This is the default value</span></span> |
| <span data-ttu-id="7c88a-116">false</span><span class="sxs-lookup"><span data-stu-id="7c88a-116">false</span></span> | <span data-ttu-id="7c88a-117">停用全螢幕播放。</span><span class="sxs-lookup"><span data-stu-id="7c88a-117">Disable full-screen playback.</span></span>                          |



 

<span data-ttu-id="7c88a-118">只有當 MSWebDVD 控制項以視窗模式執行時，才可使用全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="7c88a-118">Full screen mode is only available when the MSWebDVD control is running in windowed mode.</span></span>

 

 



