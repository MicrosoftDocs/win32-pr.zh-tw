---
description: TAPI 3 牽涉到許多與其五個主要 TAPI 物件無關的物件 (TAPI、Address、Call、CallHub 和 Terminal) 。
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Stand-Alone 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849233"
---
# <a name="stand-alone-objects"></a><span data-ttu-id="a5ad5-103">Stand-Alone 物件</span><span class="sxs-lookup"><span data-stu-id="a5ad5-103">Stand-Alone Objects</span></span>

<span data-ttu-id="a5ad5-104">TAPI 3 牽涉到許多與其五個主要 TAPI 物件無關的物件 (TAPI、Address、Call、CallHub 和 Terminal) 。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-104">TAPI 3 involves a number of objects that are independent of its five main TAPI objects (TAPI, Address, Call, CallHub, and Terminal).</span></span> <span data-ttu-id="a5ad5-105">[事件介面](./event-interfaces.md) 和 [列舉值介面](enumerator-interfaces.md) 是獨立的物件，而且會分開摘要。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-105">[Event Interfaces](./event-interfaces.md) and [Enumerator Interfaces](enumerator-interfaces.md) are stand-alone objects, and are summarized separately.</span></span> <span data-ttu-id="a5ad5-106">以下摘要說明非事件和非列舉值的獨立介面。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-106">The following summarizes non-event and non-enumerator stand-alone interfaces.</span></span>



| <span data-ttu-id="a5ad5-107">介面</span><span class="sxs-lookup"><span data-stu-id="a5ad5-107">Interface</span></span>                                             | <span data-ttu-id="a5ad5-108">描述</span><span class="sxs-lookup"><span data-stu-id="a5ad5-108">Description</span></span>                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5ad5-109">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-109">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | <span data-ttu-id="a5ad5-110">提供可讓自動化用戶端應用程式（例如 Visual Basic）取出集合資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-110">Provides methods to allow Automation client applications such as Visual Basic to retrieve collection information.</span></span>                                                                                             |
| [<span data-ttu-id="a5ad5-111">**ITCollection2**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-111">**ITCollection2**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | <span data-ttu-id="a5ad5-112">藉由提供修改集合的其他方法來擴充 [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) 。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-112">Extends [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) by providing additional methods for modifying collections.</span></span>                                                                                                       |
| [<span data-ttu-id="a5ad5-113">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-113">**IDispatch**</span></span>](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | <span data-ttu-id="a5ad5-114">用來執行自動化的標準 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-114">Standard COM interface for implementing Automation.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="a5ad5-115">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-115">**IUnknown**</span></span>](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | <span data-ttu-id="a5ad5-116">用來取得物件介面指標的標準 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-116">Standard COM interface for getting pointers to object interfaces.</span></span>                                                                                                                                             |
| [<span data-ttu-id="a5ad5-117">**ITDispatchMapper**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-117">**ITDispatchMapper**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | <span data-ttu-id="a5ad5-118">允許應用程式在給定目前 [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) 指標的情況下，取得物件上另一個介面的分派指標。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-118">Allows an application to retrieve the dispatch pointer of another interface on an object, given a current [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) pointer.</span></span> <span data-ttu-id="a5ad5-119">適用于一些指令碼語言。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-119">Useful for some scripting languages.</span></span> |
| [<span data-ttu-id="a5ad5-120">**ITRequest**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-120">**ITRequest**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | <span data-ttu-id="a5ad5-121">提供可讓 TAPI 3 應用程式使用 [輔助電話語音](assisted-telephony-overview.md)的方法。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-121">Provides methods that allow a TAPI 3 application to use [Assisted Telephony](assisted-telephony-overview.md).</span></span>                                                                                                |



 



| <span data-ttu-id="a5ad5-122">介面</span><span class="sxs-lookup"><span data-stu-id="a5ad5-122">Interface</span></span>                                  | <span data-ttu-id="a5ad5-123">描述</span><span class="sxs-lookup"><span data-stu-id="a5ad5-123">Description</span></span>                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5ad5-124">**ITMediaControl**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-124">**ITMediaControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | <span data-ttu-id="a5ad5-125">啟動、停止和暫停目前的動作，例如播放。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-125">Starts, stops, and pauses current actions, such as a playback.</span></span>                                                                                                             |
| [<span data-ttu-id="a5ad5-126">**ITMediaPlayback**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-126">**ITMediaPlayback**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | <span data-ttu-id="a5ad5-127">提供可讓應用程式執行這類作業的播放特定方法，例如，設定要播放及變更播放速度的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-127">Provides playback-specific methods that allow an application to perform such operations as setting the list of files to play and changing the playback speed.</span></span>              |
| [<span data-ttu-id="a5ad5-128">**ITMediaRecord**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-128">**ITMediaRecord**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | <span data-ttu-id="a5ad5-129">提供記錄特有的方法，可讓應用程式執行這類作業，例如設定記錄檔的名稱，以及變更錄製的持續時間。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-129">Provides recording-specific methods that allow an application to perform such operations as setting the names of files to record and changing the duration of a recording.</span></span> |



 



| <span data-ttu-id="a5ad5-130">介面</span><span class="sxs-lookup"><span data-stu-id="a5ad5-130">Interface</span></span>                                                  | <span data-ttu-id="a5ad5-131">描述</span><span class="sxs-lookup"><span data-stu-id="a5ad5-131">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5ad5-132">**ITScriptableAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-132">**ITScriptableAudioFormat**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | <span data-ttu-id="a5ad5-133">從取出音訊格式，或設定播放軌的音訊格式。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-133">Retrieves the audio format from, or sets the audio format for, a track.</span></span>                                                                                             |
| [<span data-ttu-id="a5ad5-134">**ITStaticAudioTerminal**</span><span class="sxs-lookup"><span data-stu-id="a5ad5-134">**ITStaticAudioTerminal**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | <span data-ttu-id="a5ad5-135">提供支援電話裝置所需之靜態音訊終端機物件的方法。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-135">Provides methods on static audio terminal objects that are needed to support phone devices.</span></span> <span data-ttu-id="a5ad5-136">TAPI 3.1 Msp 必須在所有靜態音訊終端機上公開這個介面。</span><span class="sxs-lookup"><span data-stu-id="a5ad5-136">TAPI 3.1 MSPs must expose this interface on all static audio terminals.</span></span> |



 

 

 
