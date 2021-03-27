---
title: 圖層列舉
description: 本節包含圖層列舉的相關資訊。
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- 列舉，Direct3D 11 層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104971832"
---
# <a name="layer-enumerations"></a><span data-ttu-id="85b5f-104">圖層列舉</span><span class="sxs-lookup"><span data-stu-id="85b5f-104">Layer Enumerations</span></span>

<span data-ttu-id="85b5f-105">本節包含圖層列舉的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="85b5f-105">This section contains information about the layer enumerations.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="85b5f-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="85b5f-106">In this section</span></span>



| <span data-ttu-id="85b5f-107">主題</span><span class="sxs-lookup"><span data-stu-id="85b5f-107">Topic</span></span>                                                                                             | <span data-ttu-id="85b5f-108">描述</span><span class="sxs-lookup"><span data-stu-id="85b5f-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85b5f-109">**D3D11 \_ 訊息 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="85b5f-109">**D3D11\_MESSAGE\_CATEGORY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | <span data-ttu-id="85b5f-110">Debug 訊息的類別。</span><span class="sxs-lookup"><span data-stu-id="85b5f-110">Categories of debug messages.</span></span> <span data-ttu-id="85b5f-111">這將會在使用 [**ID3D11InfoQueue：： GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) 抓取訊息，以及使用 [**ID3D11InfoQueue：： AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage)來新增訊息時，識別訊息的類別。</span><span class="sxs-lookup"><span data-stu-id="85b5f-111">This will identify the category of a message when retrieving a message with [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) and when adding a message with [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <span data-ttu-id="85b5f-112">建立 [**資訊佇列篩選器**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)時，這些值可以用來允許或拒絕任何類別的訊息，以通過儲存體和抓取篩選。</span><span class="sxs-lookup"><span data-stu-id="85b5f-112">When creating an [**info queue filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.</span></span><br/> |
| [<span data-ttu-id="85b5f-113">**D3D11 \_ 訊息 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="85b5f-113">**D3D11\_MESSAGE\_ID**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | <span data-ttu-id="85b5f-114">設定資訊佇列篩選的偵錯工具 (參閱 [**D3D11 \_ 資訊 \_ 佇列 \_ 篩選**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)) ; 使用這些訊息來允許或拒絕訊息類別，以通過儲存體和抓取篩選。</span><span class="sxs-lookup"><span data-stu-id="85b5f-114">Debug messages for setting up an info-queue filter (see [**D3D11\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); use these messages to allow or deny message categories to pass through the storage and retrieval filters.</span></span> <span data-ttu-id="85b5f-115">這些識別碼是由 [**ID3D11InfoQueue：： GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) 或 [**ID3D11InfoQueue：： AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage)之類的方法所使用。</span><span class="sxs-lookup"><span data-stu-id="85b5f-115">These IDs are used by methods such as [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) or [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <br/>                                                             |
| [<span data-ttu-id="85b5f-116">**D3D11 \_ 訊息 \_ 嚴重性**</span><span class="sxs-lookup"><span data-stu-id="85b5f-116">**D3D11\_MESSAGE\_SEVERITY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | <span data-ttu-id="85b5f-117">資訊佇列的 Debug 訊息嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="85b5f-117">Debug message severity levels for an information queue.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="85b5f-118">**D3D11 \_ RLDO \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="85b5f-118">**D3D11\_RLDO\_FLAGS**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | <span data-ttu-id="85b5f-119">有關裝置物件存留期的報告資訊量選項。</span><span class="sxs-lookup"><span data-stu-id="85b5f-119">Options for the amount of information to report about a device object's lifetime.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="85b5f-120">**D3D11 \_ 著色器 \_ 追蹤 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="85b5f-120">**D3D11\_SHADER\_TRACKING\_OPTIONS**</span></span>](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | <span data-ttu-id="85b5f-121">指定如何執行著色器偵錯工具追蹤的選項。</span><span class="sxs-lookup"><span data-stu-id="85b5f-121">Options that specify how to perform shader debug tracking.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="85b5f-122">**D3D11 \_ 著色器 \_ 追蹤 \_ 資源 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="85b5f-122">**D3D11\_SHADER\_TRACKING\_RESOURCE\_TYPE**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | <span data-ttu-id="85b5f-123">指示要追蹤的資源類型。</span><span class="sxs-lookup"><span data-stu-id="85b5f-123">Indicates which resource types to track.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="85b5f-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="85b5f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85b5f-125">圖層參考</span><span class="sxs-lookup"><span data-stu-id="85b5f-125">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





