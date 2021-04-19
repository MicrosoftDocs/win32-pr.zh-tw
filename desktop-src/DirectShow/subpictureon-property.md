---
description: SubpictureOn 屬性會 (on 或 off) 來設定或抓取目前的子圖片狀態。
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: SubpictureOn 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984714"
---
# <a name="subpictureon-property"></a><span data-ttu-id="fd4dd-103">SubpictureOn 屬性</span><span class="sxs-lookup"><span data-stu-id="fd4dd-103">SubpictureOn Property</span></span>

> [!Note]  
> <span data-ttu-id="fd4dd-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="fd4dd-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fd4dd-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="fd4dd-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fd4dd-106">`SubpictureOn`屬性會設定或抓取 (on 或 off) 的目前子圖片狀態。</span><span class="sxs-lookup"><span data-stu-id="fd4dd-106">The `SubpictureOn` property sets or retrieves the current subpicture state (on or off).</span></span>

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a><span data-ttu-id="fd4dd-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd4dd-107">Return Value</span></span>

<span data-ttu-id="fd4dd-108">傳回布林值，指出是否顯示子圖片。</span><span class="sxs-lookup"><span data-stu-id="fd4dd-108">Returns a Boolean value indicating whether the subpicture is displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd4dd-109">備註</span><span class="sxs-lookup"><span data-stu-id="fd4dd-109">Remarks</span></span>

<span data-ttu-id="fd4dd-110">這個屬性不會影響隱藏式輔助字幕的顯示。</span><span class="sxs-lookup"><span data-stu-id="fd4dd-110">This property does not affect display of Closed Captions.</span></span> <span data-ttu-id="fd4dd-111">隱藏式輔助字幕內嵌于影片資料流程中。</span><span class="sxs-lookup"><span data-stu-id="fd4dd-111">Closed Captions are embedded within the video stream.</span></span> <span data-ttu-id="fd4dd-112">DVD subpictures 會在不同的串流上傳輸。</span><span class="sxs-lookup"><span data-stu-id="fd4dd-112">DVD subpictures are transported on a separate stream.</span></span>

<span data-ttu-id="fd4dd-113">當使用 [**CurrentSubpictureStream**](currentsubpicturestream-property.md)變更子圖片資料流程時，屬性會 `SubpictureOn` 切換為 **True**。</span><span class="sxs-lookup"><span data-stu-id="fd4dd-113">When the subpicture stream is changed using [**CurrentSubpictureStream**](currentsubpicturestream-property.md), the `SubpictureOn` property toggles to **True**.</span></span>

<span data-ttu-id="fd4dd-114">這個屬性是讀取/寫入，預設值是 false。</span><span class="sxs-lookup"><span data-stu-id="fd4dd-114">This property is read/write with a default value of false.</span></span>

 

 



