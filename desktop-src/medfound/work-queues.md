---
description: 在 Microsoft 媒體基礎中，工作佇列是在另一個執行緒上執行非同步作業的有效方式。
ms.assetid: f886d096-b1f5-42e4-8888-501b58bffd50
title: 工作佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b1e5e8a0a3776f718f645550813bf008b38aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193008"
---
# <a name="work-queues"></a><span data-ttu-id="5256f-103">工作佇列</span><span class="sxs-lookup"><span data-stu-id="5256f-103">Work Queues</span></span>

<span data-ttu-id="5256f-104">在 Microsoft 媒體基礎中，工作佇列是在另一個執行緒上執行非同步作業的有效方式。</span><span class="sxs-lookup"><span data-stu-id="5256f-104">In Microsoft Media Foundation, a work queue is an efficient way to perform asynchronous operations on another thread.</span></span>

<span data-ttu-id="5256f-105">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="5256f-105">This section contains the following topics.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5256f-106">主題</span><span class="sxs-lookup"><span data-stu-id="5256f-106">Topic</span></span></th>
<th><span data-ttu-id="5256f-107">描述</span><span class="sxs-lookup"><span data-stu-id="5256f-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5256f-108"><a href="using-work-queues.md">使用工作佇列</a></span><span class="sxs-lookup"><span data-stu-id="5256f-108"><a href="using-work-queues.md">Using Work Queues</a></span></span></td>
<td><span data-ttu-id="5256f-109">描述應用程式或元件如何使用工作佇列來執行非同步作業。</span><span class="sxs-lookup"><span data-stu-id="5256f-109">Describes how an application or component can use work queues to perform asynchronous operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5256f-110"><a href="writing-an-asynchronous-method.md">撰寫非同步方法</a></span><span class="sxs-lookup"><span data-stu-id="5256f-110"><a href="writing-an-asynchronous-method.md">Writing an Asynchronous Method</a></span></span></td>
<td><span data-ttu-id="5256f-111">描述如何撰寫會遵循 <a href="asynchronous-callback-methods.md">非同步回呼方法</a>中所述之 Begin/End 模式的非同步方法。</span><span class="sxs-lookup"><span data-stu-id="5256f-111">Describes how to write an asynchronous method that follows the Begin/End pattern described in <a href="asynchronous-callback-methods.md">Asynchronous Callback Methods</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5256f-112"><a href="custom-asynchronous-result-objects.md">自訂非同步結果物件</a></span><span class="sxs-lookup"><span data-stu-id="5256f-112"><a href="custom-asynchronous-result-objects.md">Custom Asynchronous Result Objects</a></span></span></td>
<td><span data-ttu-id="5256f-113">描述如何建立 <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> 介面的自訂執行。</span><span class="sxs-lookup"><span data-stu-id="5256f-113">Describes how to create a custom implementation of the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5256f-114">大部分的應用程式都應該使用 <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>所提供的庫存實作為。</span><span class="sxs-lookup"><span data-stu-id="5256f-114">Most applications should use the stock implementation provided by <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span></span> <span data-ttu-id="5256f-115">本主題適用于具有 advanced 需求的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5256f-115">This topic is for applications with advanced requirements.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5256f-116"><a href="media-foundation-work-queue-and-threading-improvements.md">工作佇列和執行緒改進</a></span><span class="sxs-lookup"><span data-stu-id="5256f-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Work Queue and Threading Improvements</a></span></span></td>
<td><span data-ttu-id="5256f-117">描述媒體基礎平臺中工作佇列和執行緒 Windows 8 的增強功能。</span><span class="sxs-lookup"><span data-stu-id="5256f-117">Describes improvements in Windows 8 for work queues and threading in the Media Foundation platform.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5256f-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="5256f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5256f-119">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="5256f-119">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 




