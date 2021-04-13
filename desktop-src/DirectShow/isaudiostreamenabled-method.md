---
description: IsAudioStreamEnabled 方法會抓取值，指出目前的標題中是否已啟用指定的音訊資料流程。
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: IsAudioStreamEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509760"
---
# <a name="isaudiostreamenabled-method"></a><span data-ttu-id="a6def-103">IsAudioStreamEnabled 方法</span><span class="sxs-lookup"><span data-stu-id="a6def-103">IsAudioStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="a6def-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="a6def-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a6def-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a6def-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a6def-106">`IsAudioStreamEnabled`方法會抓取值，指出目前的標題中是否已啟用指定的音訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="a6def-106">The `IsAudioStreamEnabled` method retrieves a value indicating whether the specified audio stream is enabled in the current title.</span></span>

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="a6def-107">參數</span><span class="sxs-lookup"><span data-stu-id="a6def-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6def-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="a6def-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="a6def-109">將音訊串流指定為0到7的整數值。</span><span class="sxs-lookup"><span data-stu-id="a6def-109">Specifies the audio stream as an Integer value from 0 through 7.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6def-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6def-110">Return Value</span></span>

<span data-ttu-id="a6def-111">傳回布林值，指出指定的音訊資料流程是否適用于目前的標題。</span><span class="sxs-lookup"><span data-stu-id="a6def-111">Returns a Boolean value indicating whether the specified audio stream is available for the current title.</span></span> <span data-ttu-id="a6def-112">True 表示它可供使用。</span><span class="sxs-lookup"><span data-stu-id="a6def-112">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6def-113">備註</span><span class="sxs-lookup"><span data-stu-id="a6def-113">Remarks</span></span>

<span data-ttu-id="a6def-114">雖然光碟最多可包含八個獨立的音訊串流，但每個標題都不一定會有每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="a6def-114">Although a disc can contain up to eight independent audio streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="a6def-115">例如，主要電影標題可能有三個英文、西班牙文和日文音訊串流，但 "景點" 標題可能只有一個英文的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="a6def-115">For example, a main movie title might have three audio streams for English, Spanish, and Japanese, but the "Coming Attractions" title might have only one audio stream in English.</span></span> <span data-ttu-id="a6def-116">在設定 [**CurrentAudioStream**](currentaudiostream-property.md) 屬性之前，請務必先確認是否有標題可用的資料流程。</span><span class="sxs-lookup"><span data-stu-id="a6def-116">Always verify that a stream is available for a title before setting the [**CurrentAudioStream**](currentaudiostream-property.md) property.</span></span>

 

 



