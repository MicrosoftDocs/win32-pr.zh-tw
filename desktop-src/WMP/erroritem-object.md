---
title: ErrorItem 物件
description: ErrorItem 物件提供存取錯誤資訊的方法。
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- ErrorItem 物件 Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c273d00477363c66c49dfa1f77a66dab42c711cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966833"
---
# <a name="erroritem-object"></a><span data-ttu-id="86fb3-104">ErrorItem 物件</span><span class="sxs-lookup"><span data-stu-id="86fb3-104">ErrorItem Object</span></span>

<span data-ttu-id="86fb3-105">**ErrorItem** 物件提供存取錯誤資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="86fb3-105">The **ErrorItem** object provides a way to access error information.</span></span>

<span data-ttu-id="86fb3-106">**ErrorItem** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="86fb3-106">The **ErrorItem** object supports the following properties.</span></span>



| <span data-ttu-id="86fb3-107">屬性</span><span class="sxs-lookup"><span data-stu-id="86fb3-107">Property</span></span>                                           | <span data-ttu-id="86fb3-108">描述</span><span class="sxs-lookup"><span data-stu-id="86fb3-108">Description</span></span>                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86fb3-109">條件</span><span class="sxs-lookup"><span data-stu-id="86fb3-109">condition</span></span>](erroritem-condition.md)               | <span data-ttu-id="86fb3-110">抓取指出錯誤條件的值。</span><span class="sxs-lookup"><span data-stu-id="86fb3-110">Retrieves a value indicating the condition for the error.</span></span>                                       |
| [<span data-ttu-id="86fb3-111">customUrl</span><span class="sxs-lookup"><span data-stu-id="86fb3-111">customUrl</span></span>](erroritem-customurl.md)               | <span data-ttu-id="86fb3-112">抓取網站的 URL，該網站會顯示有關編解碼器下載失敗的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="86fb3-112">Retrieves the URL of a website that displays specific information about codec download failure.</span></span> |
| [<span data-ttu-id="86fb3-113">errorCode</span><span class="sxs-lookup"><span data-stu-id="86fb3-113">errorCode</span></span>](erroritem-errorcode.md)               | <span data-ttu-id="86fb3-114">抓取目前的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="86fb3-114">Retrieves the current error code.</span></span>                                                               |
| [<span data-ttu-id="86fb3-115">errorCoNtext</span><span class="sxs-lookup"><span data-stu-id="86fb3-115">errorContext</span></span>](erroritem-errorcontext.md)         | <span data-ttu-id="86fb3-116">捕獲指出錯誤內容的值。</span><span class="sxs-lookup"><span data-stu-id="86fb3-116">Retrieves a value indicating the context of the error.</span></span>                                          |
| [<span data-ttu-id="86fb3-117">errorDescription</span><span class="sxs-lookup"><span data-stu-id="86fb3-117">errorDescription</span></span>](erroritem-errordescription.md) | <span data-ttu-id="86fb3-118">捕獲錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="86fb3-118">Retrieves a description of the error.</span></span>                                                           |
| <span data-ttu-id="86fb3-119">**補救**</span><span class="sxs-lookup"><span data-stu-id="86fb3-119">**remedy**</span></span>                                         | <span data-ttu-id="86fb3-120">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="86fb3-120">Reserved for future use.</span></span>                                                                        |



 

<span data-ttu-id="86fb3-121">**ErrorItem** 物件是透過下列方法來存取。</span><span class="sxs-lookup"><span data-stu-id="86fb3-121">The **ErrorItem** object is accessed through the following methods.</span></span>



| <span data-ttu-id="86fb3-122">Object</span><span class="sxs-lookup"><span data-stu-id="86fb3-122">Object</span></span>                    | <span data-ttu-id="86fb3-123">方法</span><span class="sxs-lookup"><span data-stu-id="86fb3-123">Method</span></span>                   |
|---------------------------|--------------------------|
| [<span data-ttu-id="86fb3-124">錯誤</span><span class="sxs-lookup"><span data-stu-id="86fb3-124">Error</span></span>](error-object.md) | [<span data-ttu-id="86fb3-125">item</span><span class="sxs-lookup"><span data-stu-id="86fb3-125">item</span></span>](error-item.md)   |
| [<span data-ttu-id="86fb3-126">媒體</span><span class="sxs-lookup"><span data-stu-id="86fb3-126">Media</span></span>](media-object.md) | [<span data-ttu-id="86fb3-127">error</span><span class="sxs-lookup"><span data-stu-id="86fb3-127">error</span></span>](media-error.md) |



 

<span data-ttu-id="86fb3-128">例如，*播放* 程式的用途。*錯誤*。參考語法區段中會使用 (*索引*) 的 *專案*。</span><span class="sxs-lookup"><span data-stu-id="86fb3-128">For purposes of illustration, *player*.*error*.*item*(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="86fb3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86fb3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86fb3-130">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="86fb3-130">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




