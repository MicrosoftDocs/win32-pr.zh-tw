---
description: DMOEnum 範例
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: DMOEnum 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187550"
---
# <a name="dmoenum-sample"></a><span data-ttu-id="8b614-103">DMOEnum 範例</span><span class="sxs-lookup"><span data-stu-id="8b614-103">DMOEnum Sample</span></span>

## <a name="description"></a><span data-ttu-id="8b614-104">Description</span><span class="sxs-lookup"><span data-stu-id="8b614-104">Description</span></span>

<span data-ttu-id="8b614-105">這個範例應用程式會列舉所有的 [DirectX 媒體物件](directx-media-objects.md) (DMOs) 在使用者的系統中註冊，並顯示其相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8b614-105">This sample application enumerates all of the [DirectX Media Objects](directx-media-objects.md) (DMOs) registered in the user's system, and displays information about them.</span></span>

<span data-ttu-id="8b614-106">此範例會使用 [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) 函數和 [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) 介面來列舉 DMOs。</span><span class="sxs-lookup"><span data-stu-id="8b614-106">The sample uses the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function and the [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) interface to enumerate the DMOs.</span></span> <span data-ttu-id="8b614-107">它會使用 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) 介面和其他的 sql-dmo 介面，來取得每個的資訊。</span><span class="sxs-lookup"><span data-stu-id="8b614-107">It uses the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface and other DMO interfaces to retrieve information about each DMO.</span></span>

## <a name="usage"></a><span data-ttu-id="8b614-108">使用方式</span><span class="sxs-lookup"><span data-stu-id="8b614-108">Usage</span></span>

<span data-ttu-id="8b614-109">當應用程式啟動時，它會列舉所有已安裝的 DMOs。</span><span class="sxs-lookup"><span data-stu-id="8b614-109">When the application launches, it enumerates all of the installed DMOs.</span></span> <span data-ttu-id="8b614-110">如果您選取特定的 SQL-DMO 類別，應用程式只會顯示該類別中的 DMOs。</span><span class="sxs-lookup"><span data-stu-id="8b614-110">If you select a specific DMO category, the application displays only the DMOs in that category.</span></span> <span data-ttu-id="8b614-111">若要查看一組的相關資訊，請從清單中選取 []。</span><span class="sxs-lookup"><span data-stu-id="8b614-111">To view information about a DMO, select the DMO from the list.</span></span> <span data-ttu-id="8b614-112">應用程式會顯示資料流程的數目、慣用的媒體類型、該的 DLL 伺服器，以及該的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="8b614-112">The application displays the number of streams, the preferred media types, the DLL server for that DMO, and other information about the DMO.</span></span> <span data-ttu-id="8b614-113">若要包含或排除索引 DMOs，請切換 [ **包含金鑰 DMOs？** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="8b614-113">To include or exclude keyed DMOs, toggle the **Include Keyed DMOs?** checkbox.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="8b614-114">下載範例</span><span class="sxs-lookup"><span data-stu-id="8b614-114">Downloading the Sample</span></span>

<span data-ttu-id="8b614-115">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="8b614-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="8b614-116">此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 其他 \\ DMOEnum。</span><span class="sxs-lookup"><span data-stu-id="8b614-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Misc\\DMOEnum.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b614-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b614-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b614-118">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="8b614-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



