---
description: CurrentAudioStream 屬性會設定或抓取已啟用之音訊串流的數目。
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: CurrentAudioStream 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973746"
---
# <a name="currentaudiostream-property"></a><span data-ttu-id="68e96-103">CurrentAudioStream 屬性</span><span class="sxs-lookup"><span data-stu-id="68e96-103">CurrentAudioStream Property</span></span>

> [!Note]  
> <span data-ttu-id="68e96-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="68e96-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="68e96-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="68e96-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="68e96-106">`CurrentAudioStream`屬性會設定或抓取已啟用的音訊資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="68e96-106">The `CurrentAudioStream` property sets or retrieves the number of the enabled audio stream.</span></span>

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a><span data-ttu-id="68e96-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="68e96-107">Return Value</span></span>

<span data-ttu-id="68e96-108">傳回從0到7的整數值，表示目前的音訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="68e96-108">Returns an integer value from 0 through 7 indicating the current audio stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="68e96-109">備註</span><span class="sxs-lookup"><span data-stu-id="68e96-109">Remarks</span></span>

<span data-ttu-id="68e96-110">此屬性是讀取/寫入，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="68e96-110">This property is read/write with no default value.</span></span> <span data-ttu-id="68e96-111">嘗試設定新的音訊串流之前，請先呼叫 [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) 來確認資料流程是否可用。</span><span class="sxs-lookup"><span data-stu-id="68e96-111">Before attempting to set a new audio stream, call [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) to verify that the stream is available.</span></span>

## <a name="see-also"></a><span data-ttu-id="68e96-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68e96-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e96-113">**AudioStreamsAvailable**</span><span class="sxs-lookup"><span data-stu-id="68e96-113">**AudioStreamsAvailable**</span></span>](audiostreamsavailable-property.md)
</dt> </dl>

 

 



