---
description: SQL-DMO 最低需求
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: SQL-DMO 最低需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935903"
---
# <a name="dmo-minimum-requirements"></a><span data-ttu-id="7fc05-103">SQL-DMO 最低需求</span><span class="sxs-lookup"><span data-stu-id="7fc05-103">DMO Minimum Requirements</span></span>

<span data-ttu-id="7fc05-104">每個時都應該符合下列最低需求：</span><span class="sxs-lookup"><span data-stu-id="7fc05-104">Every DMO should meet the following minimum requirements:</span></span>

-   <span data-ttu-id="7fc05-105">它必須支援匯總。</span><span class="sxs-lookup"><span data-stu-id="7fc05-105">It must support aggregation.</span></span>
-   <span data-ttu-id="7fc05-106">它必須公開 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) 介面。</span><span class="sxs-lookup"><span data-stu-id="7fc05-106">It must expose the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span>
-   <span data-ttu-id="7fc05-107">執行緒模型必須是「兩者」。</span><span class="sxs-lookup"><span data-stu-id="7fc05-107">The threading model must be 'both'.</span></span> <span data-ttu-id="7fc05-108">DMOs 必須在自由執行緒環境中正確運作。</span><span class="sxs-lookup"><span data-stu-id="7fc05-108">DMOs must function correctly in a free-threaded environment.</span></span>

<span data-ttu-id="7fc05-109">音訊效果 DMOs 應該支援 [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) 介面，以便在 DirectMusic 和 DirectSound 中使用。</span><span class="sxs-lookup"><span data-stu-id="7fc05-109">Audio effect DMOs should support the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface, for use in DirectMusic and DirectSound.</span></span>

<span data-ttu-id="7fc05-110">下列是在其他地方記載的介面，但很適合用於許多 DMOs。</span><span class="sxs-lookup"><span data-stu-id="7fc05-110">The following interfaces are documented elsewhere, but are useful for many DMOs.</span></span> <span data-ttu-id="7fc05-111">不過，它們並不是必要的。</span><span class="sxs-lookup"><span data-stu-id="7fc05-111">They are not required, however.</span></span>

-   <span data-ttu-id="7fc05-112">**ISpecifyPropertyPages**， **IPropertyPage**：這些介面可讓您提供屬性頁，讓使用者設定屬性。</span><span class="sxs-lookup"><span data-stu-id="7fc05-112">**ISpecifyPropertyPages**, **IPropertyPage**: These interfaces enable a DMO to provide a property page, for the user to set properties.</span></span>
-   <span data-ttu-id="7fc05-113">**IPersistStream**：此介面可讓 sql-dmo 將其狀態儲存至持續性儲存體。</span><span class="sxs-lookup"><span data-stu-id="7fc05-113">**IPersistStream**: This interface enables the DMO to save its state to persistent storage.</span></span>
-   <span data-ttu-id="7fc05-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)：這些介面可讓用戶端設定編碼器的輸出格式和壓縮設定。</span><span class="sxs-lookup"><span data-stu-id="7fc05-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): These interfaces enable a client to configure an encoder's output format and compression settings.</span></span> <span data-ttu-id="7fc05-115"> (這兩個介面都是 DirectShow API 的一部分，但也建議 DMOs。 ) </span><span class="sxs-lookup"><span data-stu-id="7fc05-115">(These two interfaces are part of the DirectShow API, but are also recommended for DMOs.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fc05-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="7fc05-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fc05-117">撰寫 SQL-DMO</span><span class="sxs-lookup"><span data-stu-id="7fc05-117">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



