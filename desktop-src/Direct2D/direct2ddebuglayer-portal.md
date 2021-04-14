---
title: Direct2D Debug 圖層
description: Direct2D 的執行時間延伸模組，可提供描述性的錯誤訊息、物件流失偵測、效能注意事項，以及協助您建立 Direct2D 應用程式的其他提示。
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371927"
---
# <a name="direct2d-debug-layer"></a><span data-ttu-id="59f1c-103">Direct2D Debug 圖層</span><span class="sxs-lookup"><span data-stu-id="59f1c-103">Direct2D Debug Layer</span></span>

## <a name="purpose"></a><span data-ttu-id="59f1c-104">目的</span><span class="sxs-lookup"><span data-stu-id="59f1c-104">Purpose</span></span>

<span data-ttu-id="59f1c-105">Direct2D debug 層會在其本身 DLL 中的 Direct2D （名為 d2d1debug.dll）分開執行，提供設計階段的偵測訊息，讓您可以將執行時間應用程式失敗降至最低。</span><span class="sxs-lookup"><span data-stu-id="59f1c-105">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="59f1c-106">偵測到的訊息通常是因為違反 API 合約的結果（例如無效參數） (可能是 Direct3D 相關) 、不正確資源、執行緒違規和其他效能問題，例如在剪輯足夠時使用圖層。</span><span class="sxs-lookup"><span data-stu-id="59f1c-106">The debug messages often result from violations of API contracts such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and other performance issues such as using a layer when a clip would suffice.</span></span>

<span data-ttu-id="59f1c-107">為了協助您決定 debug 層所追蹤的資訊數量，debug 層提供三個 debug 層級：資訊、警告和錯誤。</span><span class="sxs-lookup"><span data-stu-id="59f1c-107">To help you decide how much information is traced by the debug layer, the debug layer offers three debug levels: information, warning, and error.</span></span> <span data-ttu-id="59f1c-108">這三個層級的解讀方式如下：</span><span class="sxs-lookup"><span data-stu-id="59f1c-108">These three levels are interpreted as follows:</span></span>

-   <span data-ttu-id="59f1c-109">**錯誤：** Direct2D 會將嚴重的錯誤訊息傳送至 debug 層。</span><span class="sxs-lookup"><span data-stu-id="59f1c-109">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="59f1c-110">例如，中斷線程條件約束將會產生嚴重的錯誤。</span><span class="sxs-lookup"><span data-stu-id="59f1c-110">For example, breaking a threading constraint will generate a severe error.</span></span>

    <span data-ttu-id="59f1c-111">此外，層級錯誤訊息會觸發中斷點，以協助您進行調試。</span><span class="sxs-lookup"><span data-stu-id="59f1c-111">Further, a message of level error triggers the breakpoint to help you debug.</span></span>

-   <span data-ttu-id="59f1c-112">**警告：** Direct2D 會將錯誤訊息和警告傳送至 debug 圖層，以便您可以處理這些訊息。</span><span class="sxs-lookup"><span data-stu-id="59f1c-112">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="59f1c-113">**資訊：** Direct2D 會將錯誤訊息、警告和其他診斷資訊傳送至 debug 圖層。</span><span class="sxs-lookup"><span data-stu-id="59f1c-113">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="59f1c-114">例如，效能改進訊息將會在這個 debug 層級傳送。</span><span class="sxs-lookup"><span data-stu-id="59f1c-114">For example, performance improvement messages will be sent at this debug level.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="59f1c-115">本節內容</span><span class="sxs-lookup"><span data-stu-id="59f1c-115">In this section</span></span>



| <span data-ttu-id="59f1c-116">主題</span><span class="sxs-lookup"><span data-stu-id="59f1c-116">Topic</span></span>                                                                                     | <span data-ttu-id="59f1c-117">描述</span><span class="sxs-lookup"><span data-stu-id="59f1c-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="59f1c-118">安裝 Direct2D Debug Layer</span><span class="sxs-lookup"><span data-stu-id="59f1c-118">Installing the Direct2D Debug Layer</span></span>](installing-the-direct2d-debug-layer.md)<br/> | <span data-ttu-id="59f1c-119">說明如何安裝 Direct2D debug 圖層。</span><span class="sxs-lookup"><span data-stu-id="59f1c-119">Describes how to install the Direct2D debug layer.</span></span><br/>      |
| [<span data-ttu-id="59f1c-120">Direct2D Debug 圖層總覽</span><span class="sxs-lookup"><span data-stu-id="59f1c-120">Direct2D Debug Layer Overview</span></span>](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [<span data-ttu-id="59f1c-121">Debug 訊息</span><span class="sxs-lookup"><span data-stu-id="59f1c-121">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)<br/>                         | <span data-ttu-id="59f1c-122">列出來自 Direct2D Debug 層的 debug 訊息。</span><span class="sxs-lookup"><span data-stu-id="59f1c-122">Lists the debug messages from the Direct2D Debug Layer.</span></span><br/> |



 

 

 





