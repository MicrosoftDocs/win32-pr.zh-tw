---
description: CurrentSubpictureStream 屬性會設定或抓取目前的子圖片資料流程。
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: CurrentSubpictureStream 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510303"
---
# <a name="currentsubpicturestream-property"></a><span data-ttu-id="ce6d7-103">CurrentSubpictureStream 屬性</span><span class="sxs-lookup"><span data-stu-id="ce6d7-103">CurrentSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="ce6d7-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="ce6d7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ce6d7-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ce6d7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ce6d7-106">`CurrentSubpictureStream`屬性會設定或抓取目前的子圖片資料流程。</span><span class="sxs-lookup"><span data-stu-id="ce6d7-106">The `CurrentSubpictureStream` property sets or retrieves the current subpicture stream.</span></span>

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="ce6d7-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce6d7-107">Return Value</span></span>

<span data-ttu-id="ce6d7-108">傳回代表資料流程的整數值。</span><span class="sxs-lookup"><span data-stu-id="ce6d7-108">Returns an integer value representing the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce6d7-109">備註</span><span class="sxs-lookup"><span data-stu-id="ce6d7-109">Remarks</span></span>

<span data-ttu-id="ce6d7-110">這個屬性的可能值為：</span><span class="sxs-lookup"><span data-stu-id="ce6d7-110">The possible values of this property are:</span></span>



| <span data-ttu-id="ce6d7-111">值</span><span class="sxs-lookup"><span data-stu-id="ce6d7-111">Value</span></span>   | <span data-ttu-id="ce6d7-112">描述</span><span class="sxs-lookup"><span data-stu-id="ce6d7-112">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="ce6d7-113">0到31</span><span class="sxs-lookup"><span data-stu-id="ce6d7-113">0 to 31</span></span> | <span data-ttu-id="ce6d7-114">子圖片資料流程</span><span class="sxs-lookup"><span data-stu-id="ce6d7-114">The subpicture stream</span></span>    |
| <span data-ttu-id="ce6d7-115">63</span><span class="sxs-lookup"><span data-stu-id="ce6d7-115">63</span></span>      | <span data-ttu-id="ce6d7-116">靜音低位元速率串流</span><span class="sxs-lookup"><span data-stu-id="ce6d7-116">Muted low-bitrate stream</span></span> |



 

<span data-ttu-id="ce6d7-117">此屬性是讀取/寫入，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="ce6d7-117">This property is read/write with no default value.</span></span> <span data-ttu-id="ce6d7-118">在設定新的子圖片資料流程之前，請先呼叫 [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) 確認資料流程是否可用。</span><span class="sxs-lookup"><span data-stu-id="ce6d7-118">Before setting a new subpicture stream, call [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) to verify that the stream is available.</span></span>

<span data-ttu-id="ce6d7-119">設定這個屬性會使 [**SubpictureOn**](subpictureon-property.md) 屬性切換為 **True**。</span><span class="sxs-lookup"><span data-stu-id="ce6d7-119">Setting this property causes the [**SubpictureOn**](subpictureon-property.md) property to toggle to **True**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce6d7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce6d7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6d7-121">**SubpictureOn**</span><span class="sxs-lookup"><span data-stu-id="ce6d7-121">**SubpictureOn**</span></span>](subpictureon-property.md)
</dt> <dt>

[<span data-ttu-id="ce6d7-122">**SubpictureStreamsAvailable**</span><span class="sxs-lookup"><span data-stu-id="ce6d7-122">**SubpictureStreamsAvailable**</span></span>](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



