---
title: Data-Pull 模型和 Data-Push 模型
description: Data-Pull 模型和 Data-Push 模型
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383014"
---
# <a name="data-pull-model-and-data-push-model"></a><span data-ttu-id="a719f-103">Data-Pull 模型和 Data-Push 模型</span><span class="sxs-lookup"><span data-stu-id="a719f-103">Data-Pull Model and Data-Push Model</span></span>

<span data-ttu-id="a719f-104">非同步標記的用戶端可以在資料提取和資料推送模型之間進行選擇，以驅動非同步 [**IMoniker：： BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 作業並接收非同步通知。</span><span class="sxs-lookup"><span data-stu-id="a719f-104">A client of an asynchronous moniker can choose between a data-pull and data-push model for driving an asynchronous [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) operation and receiving asynchronous notifications.</span></span> <span data-ttu-id="a719f-105">在資料提取模型中，用戶端會驅動系結作業，而且只有在讀取時，才會將資料提供給用戶端。</span><span class="sxs-lookup"><span data-stu-id="a719f-105">In the data-pull model, the client drives the bind operation and the moniker provides data to the client only as it is read.</span></span> <span data-ttu-id="a719f-106">換句話說，在第一次呼叫 [**IBindStatusCallback：： OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))之後，除非用戶端已取用所有已經可用的資料，否則該名字不會將任何資料提供給用戶端。</span><span class="sxs-lookup"><span data-stu-id="a719f-106">In other words, after the first call to [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), the moniker does not provide any data to the client unless the client has consumed all of the data that is already available.</span></span>

<span data-ttu-id="a719f-107">因為資料只會在要求時下載，所以選擇資料提取模型的用戶端必須務必及時讀取此資料。</span><span class="sxs-lookup"><span data-stu-id="a719f-107">Because data is downloaded only as it is requested, clients that choose the data-pull model must make sure to read this data in a timely manner.</span></span> <span data-ttu-id="a719f-108">在使用 [URL](url-monikers.md)標記的網際網路下載案例中，如果用戶端在要求更多資料之前等候太久，系結作業可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="a719f-108">In the case of Internet downloads with [URL monikers](url-monikers.md), the bind operation may fail if a client waits too long before requesting more data.</span></span>

<span data-ttu-id="a719f-109">在資料推送模型中，此標記會驅動非同步系結作業，並在每次有新資料可用時持續通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="a719f-109">In the data-push model, the moniker drives the asynchronous bind operation and continuously notifies the client whenever new data is available.</span></span> <span data-ttu-id="a719f-110">用戶端可選擇是否要在系結作業期間的任何時間點讀取資料，但不論是哪一種，都要將系結作業驅動到完成。</span><span class="sxs-lookup"><span data-stu-id="a719f-110">The client may choose whether to read the data at any point during the bind operation, but the moniker will drive the bind operation to completion regardless.</span></span>

<span data-ttu-id="a719f-111">此外，使用非同步標記時，您必須記得遵循 COM 規則來進行記憶體配置，具體如下：</span><span class="sxs-lookup"><span data-stu-id="a719f-111">Also, you need to remember to follow the COM rules for memory allocation when using asynchronous monikers, specifically the following:</span></span>

-   <span data-ttu-id="a719f-112">每當 COM 介面或函式呼叫傳回緩衝區 (字串或其他) 至其用戶端時，用戶端會藉由呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來負責釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="a719f-112">Whenever a COM interface or function call returns a buffer (string or other) to its client, the client is responsible for freeing the memory by calling [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>
-   <span data-ttu-id="a719f-113">每當 COM 介面或函式需要其用戶端的緩衝區時，用戶端就必須使用 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 配置該緩衝區，而且被呼叫端必須釋放它。</span><span class="sxs-lookup"><span data-stu-id="a719f-113">Whenever a COM interface or function requires a buffer from its client, the client must allocate that buffer using [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) and the callee must free it.</span></span>

<span data-ttu-id="a719f-114">配置傳遞給非同步標記的字串或緩衝區時，請務必遵循這些規則，並記得釋放非同步名字所傳回的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a719f-114">Be sure to follow these rules when allocating strings or buffers that are passed to asynchronous monikers, and remember to free memory returned by asynchronous monikers.</span></span> <span data-ttu-id="a719f-115">如需完整的詳細資料，請參閱 [管理記憶體配置](the-com-library.md) 和相關主題。</span><span class="sxs-lookup"><span data-stu-id="a719f-115">See [Managing Memory Allocation](the-com-library.md) and related topics for complete details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a719f-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="a719f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a719f-117">非同步名字</span><span class="sxs-lookup"><span data-stu-id="a719f-117">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 