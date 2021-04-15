---
description: 關於拓撲
ms.assetid: 4f69b099-0ca7-4ea6-8412-0f1ea02e1600
title: 關於拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35008d839e8054554370039dd13297ae7a1f0b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555604"
---
# <a name="about-topologies"></a><span data-ttu-id="2484b-103">關於拓撲</span><span class="sxs-lookup"><span data-stu-id="2484b-103">About Topologies</span></span>

<span data-ttu-id="2484b-104">拓撲是物件，代表管線中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="2484b-104">A topology is an object that represents how data flows in the pipeline.</span></span> <span data-ttu-id="2484b-105">應用程式會建立拓撲，以描述每個串流從媒體來源到媒體接收器所採用的路徑。</span><span class="sxs-lookup"><span data-stu-id="2484b-105">An application creates a topology to describe the path that each stream takes from the media source to a media sink.</span></span> <span data-ttu-id="2484b-106">應用程式會將拓撲傳遞給媒體會話，而媒體會話會使用拓撲來控制資料流程。</span><span class="sxs-lookup"><span data-stu-id="2484b-106">The application passes the topology to the Media Session, and the Media Session uses the topology to control the data flow.</span></span>

<span data-ttu-id="2484b-107">管線中的資料處理元件 (媒體來源、轉換和媒體接收器) 會在拓撲中表示為 *節點*。</span><span class="sxs-lookup"><span data-stu-id="2484b-107">The data-processing components in the pipeline (media sources, transforms, and media sinks) are represented in the topology as *nodes*.</span></span> <span data-ttu-id="2484b-108">從某個元件到另一個元件的資料流程會以節點之間的連接來表示。</span><span class="sxs-lookup"><span data-stu-id="2484b-108">The flow of data from one component to another is represented by a connection between the nodes.</span></span> <span data-ttu-id="2484b-109">以下是定義的節點類型：</span><span class="sxs-lookup"><span data-stu-id="2484b-109">The following node types are defined:</span></span>

-   <span data-ttu-id="2484b-110">來源節點：代表媒體來源上的媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="2484b-110">Source node: Represents a media stream on a media source.</span></span>
-   <span data-ttu-id="2484b-111">轉換節點：代表媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="2484b-111">Transform node: Represents a Media Foundation transform (MFT).</span></span>
-   <span data-ttu-id="2484b-112">輸出節點：表示媒體接收上的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="2484b-112">Output node: Represents a stream sink on a media sink.</span></span>
-   <span data-ttu-id="2484b-113">T a node：代表資料流程中的分支。</span><span class="sxs-lookup"><span data-stu-id="2484b-113">Tee node: Represents a fork in the stream.</span></span> <span data-ttu-id="2484b-114">T 節點是節點代表管線物件的規則例外。</span><span class="sxs-lookup"><span data-stu-id="2484b-114">Tee nodes are an exception to the rule that a node represents a pipeline object.</span></span> <span data-ttu-id="2484b-115">與其他節點型別不同的是，t 節點會直接導向資料的流程。</span><span class="sxs-lookup"><span data-stu-id="2484b-115">Unlike other node types, the tee node simply directs the flow of data.</span></span>

<span data-ttu-id="2484b-116">正常運作的拓撲必須包含至少一個連接至輸出節點的來源節點，可能是透過一或多個轉換節點。</span><span class="sxs-lookup"><span data-stu-id="2484b-116">A functioning topology must contain at least one source node connected to an output node, possibly through one or more transform nodes.</span></span> <span data-ttu-id="2484b-117">例如，下圖顯示具有一個資料流程的簡單拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-117">For example, the following diagram shows a simple topology with one stream.</span></span>

![顯示具有一個資料流程之拓撲的圖表。](images/topology01.png)

<span data-ttu-id="2484b-119">針對檔案播放，轉換節點可能代表一個解碼器，輸出節點則代表音訊或影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="2484b-119">For file playback, the transform node might represent a decoder and the output node would represent the audio or video renderer.</span></span> <span data-ttu-id="2484b-120">針對檔案編碼，[轉換] 節點會代表一個編碼器，而輸出節點則代表一個封存接收器，例如「ASF 檔案接收」。</span><span class="sxs-lookup"><span data-stu-id="2484b-120">For file encoding, the transform node would represent an encoder and the output node would represent an archive sink, such as the ASF file sink.</span></span>

<span data-ttu-id="2484b-121">如果有兩個節點連接，則產生資料的節點稱為 *上游* 節點，而接收資料的節點稱為 *下游* 節點。</span><span class="sxs-lookup"><span data-stu-id="2484b-121">If two nodes are connected, the node that produces data is called the *upstream* node, and the node that receives data is called the *downstream* node.</span></span> <span data-ttu-id="2484b-122">例如，在上圖中，來源節點是 [轉換] 節點的上游。</span><span class="sxs-lookup"><span data-stu-id="2484b-122">For example, in the previous diagram, the source node is upstream from the transform node.</span></span>

<span data-ttu-id="2484b-123">在一對連接的節點中，上游節點上的連接點稱為 *輸出*。</span><span class="sxs-lookup"><span data-stu-id="2484b-123">In a pair of connected nodes, the connection point on the upstream node is called an *output*.</span></span> <span data-ttu-id="2484b-124">下游節點上的連接點稱為 *輸入*。</span><span class="sxs-lookup"><span data-stu-id="2484b-124">The connection point on the downstream node is called an *input*.</span></span> <span data-ttu-id="2484b-125">下圖顯示一對節點及其連接點，以及兩者之間的資料流程動。</span><span class="sxs-lookup"><span data-stu-id="2484b-125">The following diagram shows a pair of nodes with their connection points, and the flow of data between them.</span></span> <span data-ttu-id="2484b-126">連接點不會以拓撲中的個別物件表示。</span><span class="sxs-lookup"><span data-stu-id="2484b-126">The connection points are not represented as separate objects in the topology.</span></span> <span data-ttu-id="2484b-127">它們是由節點物件上的索引值所指定。</span><span class="sxs-lookup"><span data-stu-id="2484b-127">They are specified by index value on the node object.</span></span>

![顯示兩個已連線節點的圖表。](images/topology04.png)

<span data-ttu-id="2484b-129">來源節點不能有任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2484b-129">A source node cannot have any inputs.</span></span> <span data-ttu-id="2484b-130">因此，不能有來自來源節點的任何節點上游。</span><span class="sxs-lookup"><span data-stu-id="2484b-130">Therefore, there cannot be any nodes upstream from a source node.</span></span> <span data-ttu-id="2484b-131">同樣地，輸出節點不能有輸出，也不能有輸出節點下游的任何節點。</span><span class="sxs-lookup"><span data-stu-id="2484b-131">Similarly, an output node cannot have outputs, and there cannot be any nodes downstream from an output node.</span></span> <span data-ttu-id="2484b-132">從來源節點到輸出節點的節點鏈稱為拓撲的 *分支* 。</span><span class="sxs-lookup"><span data-stu-id="2484b-132">A chain of nodes from a source node to an output node is called a *branch* of the topology.</span></span> <span data-ttu-id="2484b-133">本主題中的第一個圖表顯示具有單一分支的拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-133">The first diagram in this topic shows a topology with a single branch.</span></span> <span data-ttu-id="2484b-134">一般來說，每個串流都有一個分支。</span><span class="sxs-lookup"><span data-stu-id="2484b-134">Generally there is one branch per stream.</span></span> <span data-ttu-id="2484b-135">例如，若要播放包含一個音訊串流和一個影片串流的檔案，則需要具有兩個分支的拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-135">To play a file with one audio stream and one video stream, for example, requires a topology with two branches.</span></span>

## <a name="partial-topologies"></a><span data-ttu-id="2484b-136">部分拓撲</span><span class="sxs-lookup"><span data-stu-id="2484b-136">Partial Topologies</span></span>

<span data-ttu-id="2484b-137">完整或 *完整* 拓撲包含所需的每個管線物件的節點。</span><span class="sxs-lookup"><span data-stu-id="2484b-137">A complete or *full* topology contains a node for every pipeline object that is needed.</span></span> <span data-ttu-id="2484b-138">不過，應用程式不一定需要建立完整的拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-138">However, the application does not always need to create a full topology.</span></span> <span data-ttu-id="2484b-139">相反地，它會建立省略一或多個轉換節點的 *部分* 拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-139">Instead, it creates a *partial* topology that omits one or more transform nodes.</span></span>

<span data-ttu-id="2484b-140">媒體會話會使用稱為 *拓撲載入* 器的物件來完成拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-140">The Media Session completes the topology by using an object called the *topology loader*.</span></span> <span data-ttu-id="2484b-141">拓撲載入器會插入所需的轉換，將部分拓撲轉換成完整的拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-141">The topology loader converts partial topologies into full topologies by inserting the needed transforms.</span></span> <span data-ttu-id="2484b-142">轉換的處理常式稱為 *解析* 拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-142">The process of conversion is called *resolving* the topology.</span></span>

<span data-ttu-id="2484b-143">例如，若要播放編碼的音訊串流，拓撲在來源和輸出節點之間必須有一個解碼器。</span><span class="sxs-lookup"><span data-stu-id="2484b-143">For example, to play an encoded audio stream, the topology must have a decoder between the source and output nodes.</span></span> <span data-ttu-id="2484b-144">應用程式會建立部分拓撲，將來源節點直接連接至輸出節點，而不使用解碼器。</span><span class="sxs-lookup"><span data-stu-id="2484b-144">The application creates a partial topology that connects the source node directly to the output node, without the decoder.</span></span> <span data-ttu-id="2484b-145">拓撲載入器會檢查串流格式、尋找正確的解碼器，並將轉換節點插入拓撲中。</span><span class="sxs-lookup"><span data-stu-id="2484b-145">The topology loader examines the stream formats, finds the right decoder, and inserts a transform node into the topology.</span></span>

<span data-ttu-id="2484b-146">下圖顯示應用程式所建立的部分拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-146">The following diagram shows the partial topology created by the application.</span></span>

![顯示部分具有來源節點和輸出節點的圖表。](images/topology02.png)

<span data-ttu-id="2484b-148">下圖顯示拓撲載入器解析之後的完整拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-148">The next diagram shows the full topology after the topology loader resolves it.</span></span> <span data-ttu-id="2484b-149">在此範例中，拓撲載入器已插入了該解碼器的轉換節點。</span><span class="sxs-lookup"><span data-stu-id="2484b-149">In this example, the topology loader has inserted a transform node for the decoder.</span></span>

![顯示完整拓撲的圖表。](images/topology03.png)

<span data-ttu-id="2484b-151">在目前版本的媒體基礎中，拓撲載入器支援播放的拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-151">In the current version of Media Foundation, the topology loader supports topologies for playback.</span></span> <span data-ttu-id="2484b-152">針對檔案編碼和其他案例，應用程式必須建立完整的拓撲。</span><span class="sxs-lookup"><span data-stu-id="2484b-152">For file encoding and other scenarios, the application must construct a full topology.</span></span>

<span data-ttu-id="2484b-153">應用程式也可以建立拓撲載入器並直接使用。</span><span class="sxs-lookup"><span data-stu-id="2484b-153">Applications can also create the topology loader and use it directly.</span></span> <span data-ttu-id="2484b-154">例如，您可以使用拓撲載入器來解析部分拓撲，然後修改完整拓撲，再將它提供給媒體會話。</span><span class="sxs-lookup"><span data-stu-id="2484b-154">For example, you can use the topology loader to resolve a partial topology and then modify the full topology before giving it to the Media Session.</span></span> <span data-ttu-id="2484b-155">若要建立拓撲載入器，請呼叫 [**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)。</span><span class="sxs-lookup"><span data-stu-id="2484b-155">To create the topology loader, call [**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2484b-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="2484b-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2484b-157">拓撲</span><span class="sxs-lookup"><span data-stu-id="2484b-157">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



