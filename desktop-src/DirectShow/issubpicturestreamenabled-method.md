---
description: IsSubpictureStreamEnabled 方法會抓取值，指出目前的標題中是否已啟用指定的子圖片資料流程。
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: IsSubpictureStreamEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846640"
---
# <a name="issubpicturestreamenabled-method"></a><span data-ttu-id="2c3b7-103">IsSubpictureStreamEnabled 方法</span><span class="sxs-lookup"><span data-stu-id="2c3b7-103">IsSubpictureStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="2c3b7-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="2c3b7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2c3b7-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="2c3b7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2c3b7-106">`IsSubpictureStreamEnabled`方法會抓取值，指出目前的標題中是否已啟用指定的子圖片資料流程。</span><span class="sxs-lookup"><span data-stu-id="2c3b7-106">The `IsSubpictureStreamEnabled` method retrieves a value indicating whether the specified subpicture stream is enabled in the current title.</span></span>

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="2c3b7-107">參數</span><span class="sxs-lookup"><span data-stu-id="2c3b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c3b7-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="2c3b7-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="2c3b7-109">將子圖片資料流程指定為整數。</span><span class="sxs-lookup"><span data-stu-id="2c3b7-109">Specifies the subpicture stream as an Integer.</span></span>



| <span data-ttu-id="2c3b7-110">值</span><span class="sxs-lookup"><span data-stu-id="2c3b7-110">Value</span></span>   | <span data-ttu-id="2c3b7-111">描述</span><span class="sxs-lookup"><span data-stu-id="2c3b7-111">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="2c3b7-112">0到31</span><span class="sxs-lookup"><span data-stu-id="2c3b7-112">0 to 31</span></span> | <span data-ttu-id="2c3b7-113">子圖片資料流程</span><span class="sxs-lookup"><span data-stu-id="2c3b7-113">subpicture stream</span></span>        |
| <span data-ttu-id="2c3b7-114">63</span><span class="sxs-lookup"><span data-stu-id="2c3b7-114">63</span></span>      | <span data-ttu-id="2c3b7-115">靜音低位元速率串流</span><span class="sxs-lookup"><span data-stu-id="2c3b7-115">muted low-bitrate stream</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c3b7-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c3b7-116">Return Value</span></span>

<span data-ttu-id="2c3b7-117">傳回布林值，指出指定的音訊資料流程是否可在目前的標題中使用。</span><span class="sxs-lookup"><span data-stu-id="2c3b7-117">Returns a Boolean value indicating whether the specified audio stream is available in the current title.</span></span> <span data-ttu-id="2c3b7-118">True 表示它可供使用。</span><span class="sxs-lookup"><span data-stu-id="2c3b7-118">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c3b7-119">備註</span><span class="sxs-lookup"><span data-stu-id="2c3b7-119">Remarks</span></span>

<span data-ttu-id="2c3b7-120">雖然光碟最多可包含32子圖片串流，但每個標題都不一定會有每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="2c3b7-120">Although a disc can contain up to 32 subpicture streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="2c3b7-121">在設定 [**CurrentSubpictureStream**](currentsubpicturestream-property.md) 屬性之前，請務必先確認是否有標題可用的資料流程。</span><span class="sxs-lookup"><span data-stu-id="2c3b7-121">Always verify that a stream is available for a title before setting the [**CurrentSubpictureStream**](currentsubpicturestream-property.md) property.</span></span>

 

 



