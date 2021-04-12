---
title: 通知類型
description: 通知類型
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372463"
---
# <a name="types-of-notifications"></a><span data-ttu-id="fc512-103">通知類型</span><span class="sxs-lookup"><span data-stu-id="fc512-103">Types of Notifications</span></span>

<span data-ttu-id="fc512-104">通知分為三個群組：複合檔案、資料和查看。</span><span class="sxs-lookup"><span data-stu-id="fc512-104">Notifications fall into three groups: compound document, data, and view.</span></span> <span data-ttu-id="fc512-105">物件會傳送複合檔案通知，以回應重新命名、儲存、關閉，或在連結的情況下，將其連結來源重新命名。</span><span class="sxs-lookup"><span data-stu-id="fc512-105">An object sends compound document notifications in response to being renamed, saved, closed or, in the case of a link, having its link source renamed.</span></span> <span data-ttu-id="fc512-106">如您所預期，物件會傳送資料通知以回應其資料的變更，並傳送視圖通知以回應其簡報中的變更。</span><span class="sxs-lookup"><span data-stu-id="fc512-106">As you would expect, objects send data notifications in response to changes in their data and send view notifications in response to changes in their presentation.</span></span> <span data-ttu-id="fc512-107">容器應用程式必須個別註冊這些通知類型，但全部都可由單一諮詢接收來處理。</span><span class="sxs-lookup"><span data-stu-id="fc512-107">Container applications must register separately for each of these notification types, but all can be handled by a single advisory sink.</span></span>

<span data-ttu-id="fc512-108">複合檔案通知的所有容器、物件處理常式和連結化物件註冊。</span><span class="sxs-lookup"><span data-stu-id="fc512-108">All containers, the object handler, and the linked object register for compound document notifications.</span></span> <span data-ttu-id="fc512-109">一般容器也會註冊查看通知。</span><span class="sxs-lookup"><span data-stu-id="fc512-109">The typical container also registers for view notifications.</span></span> <span data-ttu-id="fc512-110">資料通知通常會同時傳送至連結化物件和物件處理常式。</span><span class="sxs-lookup"><span data-stu-id="fc512-110">Data notifications are usually sent to both the linked object and object handler.</span></span> <span data-ttu-id="fc512-111">特定用途的容器（例如呈現資料本身的容器），可能會因為接收資料通知而不是 view 通知而受益。</span><span class="sxs-lookup"><span data-stu-id="fc512-111">A special purpose container, such as one that renders the data itself, might benefit from receiving data notifications instead of view notifications.</span></span> <span data-ttu-id="fc512-112">例如，具有資料表連結的內嵌圖表容器可以註冊資料通知。</span><span class="sxs-lookup"><span data-stu-id="fc512-112">For example, an embedded chart container with a link to a table can register for data notifications.</span></span> <span data-ttu-id="fc512-113">因為資料表的變更會影響圖表，所以資料通知的接收會指示容器取得新的表格式資料。</span><span class="sxs-lookup"><span data-stu-id="fc512-113">Because a change to the table affects the chart, the receipt of a data notification would direct the container to get the new tabular data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc512-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc512-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc512-115">通知</span><span class="sxs-lookup"><span data-stu-id="fc512-115">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 




