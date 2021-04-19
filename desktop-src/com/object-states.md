---
title: 物件狀態
description: 物件狀態
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969439"
---
# <a name="object-states"></a><span data-ttu-id="111a1-103">物件狀態</span><span class="sxs-lookup"><span data-stu-id="111a1-103">Object States</span></span>

<span data-ttu-id="111a1-104">綜合物件存在於下列三種狀態之一：被動、已載入或正在執行。</span><span class="sxs-lookup"><span data-stu-id="111a1-104">A compound object exists in one of three states: passive, loaded, or running.</span></span> <span data-ttu-id="111a1-105">複合檔案物件的狀態會描述其容器中的物件與負責其建立的應用程式之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="111a1-105">A compound-document object's state describes the relationship between the object in its container and the application responsible for its creation.</span></span> <span data-ttu-id="111a1-106">下表摘要說明這些狀態。</span><span class="sxs-lookup"><span data-stu-id="111a1-106">The following table summarizes these states.</span></span>



| <span data-ttu-id="111a1-107">物件狀態</span><span class="sxs-lookup"><span data-stu-id="111a1-107">Object state</span></span>       | <span data-ttu-id="111a1-108">Description</span><span class="sxs-lookup"><span data-stu-id="111a1-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="111a1-109">被動</span><span class="sxs-lookup"><span data-stu-id="111a1-109">Passive</span></span><br/> | <span data-ttu-id="111a1-110">複合檔案物件只存在於磁片上或資料庫中的儲存體。</span><span class="sxs-lookup"><span data-stu-id="111a1-110">The compound-document object exists only in storage, either on disk or in a database.</span></span> <span data-ttu-id="111a1-111">在此狀態下，物件無法用於進行查看或編輯。</span><span class="sxs-lookup"><span data-stu-id="111a1-111">In this state, the object is unavailable for viewing or editing.</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="111a1-112">已載入</span><span class="sxs-lookup"><span data-stu-id="111a1-112">Loaded</span></span><br/>  | <span data-ttu-id="111a1-113">物件處理常式所建立的物件資料結構位於容器的記憶體中。</span><span class="sxs-lookup"><span data-stu-id="111a1-113">The object's data structures created by the object handler are in the container's memory.</span></span> <span data-ttu-id="111a1-114">容器已與物件處理常式建立通訊，而且有快取的呈現資料可用於轉譯物件。</span><span class="sxs-lookup"><span data-stu-id="111a1-114">The container has established communication with the object handler and there is cached presentation data available for rendering the object.</span></span> <span data-ttu-id="111a1-115">呼叫是由物件處理常式處理。</span><span class="sxs-lookup"><span data-stu-id="111a1-115">Calls are processed by the object handler.</span></span> <span data-ttu-id="111a1-116">由於此狀態的負擔很低，因此當使用者只是要查看或列印物件時，就會使用此狀態。</span><span class="sxs-lookup"><span data-stu-id="111a1-116">This state, because of its low overhead, is used when a user is simply viewing or printing an object.</span></span><br/> |
| <span data-ttu-id="111a1-117">執行中</span><span class="sxs-lookup"><span data-stu-id="111a1-117">Running</span></span><br/> | <span data-ttu-id="111a1-118">已建立控制遠端處理的物件，而且正在執行 OLE 伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="111a1-118">The objects that control remoting have been created and the OLE server application is running.</span></span> <span data-ttu-id="111a1-119">物件的介面可供存取，而容器可以接收變更的通知。</span><span class="sxs-lookup"><span data-stu-id="111a1-119">The object's interfaces are accessible, and the container can receive notification of changes.</span></span> <span data-ttu-id="111a1-120">在此狀態下，終端使用者可以編輯或以其他方式操作物件。</span><span class="sxs-lookup"><span data-stu-id="111a1-120">In this state, an end user can edit or otherwise manipulate the object.</span></span><br/>                                                                                                                    |



 

<span data-ttu-id="111a1-121">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="111a1-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="111a1-122">進入載入的狀態</span><span class="sxs-lookup"><span data-stu-id="111a1-122">Entering the Loaded State</span></span>](entering-the-loaded-state.md)
-   [<span data-ttu-id="111a1-123">正在進入執行狀態</span><span class="sxs-lookup"><span data-stu-id="111a1-123">Entering the Running State</span></span>](entering-the-running-state.md)
-   [<span data-ttu-id="111a1-124">進入被動狀態</span><span class="sxs-lookup"><span data-stu-id="111a1-124">Entering the Passive State</span></span>](entering-the-passive-state.md)

## <a name="related-topics"></a><span data-ttu-id="111a1-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="111a1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="111a1-126">複合檔案</span><span class="sxs-lookup"><span data-stu-id="111a1-126">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 





