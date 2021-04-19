---
description: 儲存和還原 DvdState 物件
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: 儲存和還原 DvdState 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106995180"
---
# <a name="saving-and-restoring-dvdstate-objects"></a><span data-ttu-id="f1876-103">儲存和還原 DvdState 物件</span><span class="sxs-lookup"><span data-stu-id="f1876-103">Saving and Restoring DvdState Objects</span></span>

<span data-ttu-id="f1876-104">[**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) 物件可讓應用程式儲存使用者會話的快照集，包括光碟上的目前位置、正在觀賞之人員的家長監護、選取的音訊和子圖片串流等資訊。</span><span class="sxs-lookup"><span data-stu-id="f1876-104">[**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) objects enable applications to save a snapshot of the user session, including information such as the current location on the disc, the parental level of the person who is viewing, the selected audio and subpicture streams, and so on.</span></span> <span data-ttu-id="f1876-105">這表示使用者可以將它們放在 DVD-Video 光碟上，並于稍後觀看。</span><span class="sxs-lookup"><span data-stu-id="f1876-105">This means that users can save their place on a DVD-Video disc and watch it at a later time.</span></span>

<span data-ttu-id="f1876-106">應用程式無法建立 DvdState 物件。</span><span class="sxs-lookup"><span data-stu-id="f1876-106">Applications cannot create DvdState objects.</span></span> <span data-ttu-id="f1876-107">當應用程式呼叫 [**IDvdInfo2：： >getstate**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate)時，DVD 導覽器會在內部建立這些物件。</span><span class="sxs-lookup"><span data-stu-id="f1876-107">These objects are created internally by the DVD Navigator when an application calls [**IDvdInfo2::GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span></span> <span data-ttu-id="f1876-108">DvdState 物件會公開 [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) 介面，以允許應用程式查詢特定資訊。</span><span class="sxs-lookup"><span data-stu-id="f1876-108">DvdState objects expose the [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) interface to allow applications to query for certain information.</span></span>

<span data-ttu-id="f1876-109">在 DVD 範例應用程式中， **CDvdCore：： RestoreBookmark** 和 **CDvdCore：： SaveBookmark** 函式會示範如何儲存和取出 DvdState 物件。</span><span class="sxs-lookup"><span data-stu-id="f1876-109">In the DVD sample application, the **CDvdCore::RestoreBookmark** and **CDvdCore::SaveBookmark** functions show how to save and retrieve DvdState objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1876-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1876-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1876-111">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="f1876-111">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



