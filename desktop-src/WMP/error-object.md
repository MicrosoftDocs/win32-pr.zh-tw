---
title: " (WMP SDK) 的 Error 物件"
description: Error 物件提供 ErrorItem 物件集合的存取權。
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Error 物件 Windows Media Player
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/09/2019
ms.locfileid: "106969891"
---
# <a name="error-object"></a><span data-ttu-id="dbd4d-104">Error 物件</span><span class="sxs-lookup"><span data-stu-id="dbd4d-104">Error Object</span></span>

<span data-ttu-id="dbd4d-105">**Error** 物件提供 [ErrorItem](erroritem-object.md)物件集合的存取權。</span><span class="sxs-lookup"><span data-stu-id="dbd4d-105">The **Error** object provides access to a collection of [ErrorItem](erroritem-object.md) objects.</span></span>

<span data-ttu-id="dbd4d-106">**Error** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="dbd4d-106">The **Error** object supports the following property.</span></span>



| <span data-ttu-id="dbd4d-107">屬性</span><span class="sxs-lookup"><span data-stu-id="dbd4d-107">Property</span></span>                           | <span data-ttu-id="dbd4d-108">描述</span><span class="sxs-lookup"><span data-stu-id="dbd4d-108">Description</span></span>                                        |
|------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="dbd4d-109">errorCount</span><span class="sxs-lookup"><span data-stu-id="dbd4d-109">errorCount</span></span>](error-errorcount.md) | <span data-ttu-id="dbd4d-110">捕獲錯誤佇列中的錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="dbd4d-110">Retrieves the number of errors in the error queue.</span></span> |



 

<span data-ttu-id="dbd4d-111">**Error** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="dbd4d-111">The **Error** object supports the following methods.</span></span>



| <span data-ttu-id="dbd4d-112">方法</span><span class="sxs-lookup"><span data-stu-id="dbd4d-112">Method</span></span>                                       | <span data-ttu-id="dbd4d-113">描述</span><span class="sxs-lookup"><span data-stu-id="dbd4d-113">Description</span></span>                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbd4d-114">clearErrorQueue</span><span class="sxs-lookup"><span data-stu-id="dbd4d-114">clearErrorQueue</span></span>](error-clearerrorqueue.md) | <span data-ttu-id="dbd4d-115">清除錯誤佇列中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="dbd4d-115">Clears the errors from the error queue.</span></span>                                                         |
| [<span data-ttu-id="dbd4d-116">item</span><span class="sxs-lookup"><span data-stu-id="dbd4d-116">item</span></span>](error-item.md)                       | <span data-ttu-id="dbd4d-117">從錯誤佇列中捕獲 [ErrorItem](erroritem-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="dbd4d-117">Retrieves an [ErrorItem](erroritem-object.md) object from the error queue.</span></span>                     |
| [<span data-ttu-id="dbd4d-118">webHelp</span><span class="sxs-lookup"><span data-stu-id="dbd4d-118">webHelp</span></span>](error-webhelp.md)                 | <span data-ttu-id="dbd4d-119">啟動 Windows Media Player 的 Web 說明頁，以顯示有關錯誤的進一步資訊。</span><span class="sxs-lookup"><span data-stu-id="dbd4d-119">Launches the Windows Media Player Web Help page to display further information about the error.</span></span> |



 

<span data-ttu-id="dbd4d-120">您可以透過下列屬性來存取 **Error** 物件。</span><span class="sxs-lookup"><span data-stu-id="dbd4d-120">The **Error** object is accessed through the following property.</span></span>



| <span data-ttu-id="dbd4d-121">Object</span><span class="sxs-lookup"><span data-stu-id="dbd4d-121">Object</span></span>                      | <span data-ttu-id="dbd4d-122">屬性</span><span class="sxs-lookup"><span data-stu-id="dbd4d-122">Property</span></span>                  |
|-----------------------------|---------------------------|
| [<span data-ttu-id="dbd4d-123">球員</span><span class="sxs-lookup"><span data-stu-id="dbd4d-123">Player</span></span>](player-object.md) | [<span data-ttu-id="dbd4d-124">error</span><span class="sxs-lookup"><span data-stu-id="dbd4d-124">error</span></span>](player-error.md) |



 

## <a name="see-also"></a><span data-ttu-id="dbd4d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbd4d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbd4d-126">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="dbd4d-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




