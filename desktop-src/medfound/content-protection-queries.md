---
description: 列出 IDirect3DAuthenticatedChannel9：： Query 方法的查詢。
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: 內容保護查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a72f7f054783a644cb352727f4bf65864bf5f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001655"
---
# <a name="content-protection-queries"></a><span data-ttu-id="3b4ec-103">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="3b4ec-103">Content Protection Queries</span></span>

<span data-ttu-id="3b4ec-104">列出 [**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) 方法的查詢。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-104">Lists the queries for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>



| <span data-ttu-id="3b4ec-105">狀態要求</span><span class="sxs-lookup"><span data-stu-id="3b4ec-105">Status request</span></span>                                                                                                                            | <span data-ttu-id="3b4ec-106">Description</span><span class="sxs-lookup"><span data-stu-id="3b4ec-106">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b4ec-107">**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-107">**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**</span></span>](d3dauthenticatedquery-accessibilityattributes.md)                                   | <span data-ttu-id="3b4ec-108">傳回用來將資料傳送至 GPU 的 i/o 匯流排類型。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-108">Returns the type of I/O bus used to send data to the GPU.</span></span>                                                                                                   |
| [<span data-ttu-id="3b4ec-109">**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-109">**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**</span></span>](d3dauthenticatedquery-channeltype.md)                                                           | <span data-ttu-id="3b4ec-110">傳回已驗證通道的類型。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-110">Returns the type of authenticated channel.</span></span>                                                                                                                  |
| [<span data-ttu-id="3b4ec-111">**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-111">**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**</span></span>](d3dauthenticatedquery-cryptosession.md)                                                       | <span data-ttu-id="3b4ec-112">傳回與指定的 DirectX Video 加速 2 (DXVA-2) 解碼器裝置相關聯的密碼編譯會話和 Direct3D 裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-112">Returns handles to the cryptographic session and Direct3D device that are associated with a specified DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span> |
| [<span data-ttu-id="3b4ec-113">**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-113">**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**</span></span>](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | <span data-ttu-id="3b4ec-114">傳回在 CPU 或匯流排可以存取內容之前套用的加密類型。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-114">Returns the encryption type that is applied before content becomes accessible to the CPU or bus.</span></span>                                                            |
| [<span data-ttu-id="3b4ec-115">**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-115">**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**</span></span>](d3dauthenticatedquery-devicehandle.md)                                                         | <span data-ttu-id="3b4ec-116">傳回與這個已驗證通道相關聯之裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-116">Returns a handle to the device that is associated with this authenticated channel.</span></span>                                                                          |
| [<span data-ttu-id="3b4ec-117">**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-117">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**</span></span>](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | <span data-ttu-id="3b4ec-118">傳回可供 CPU 或匯流排存取之前，用來加密內容的其中一種加密類型。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-118">Returns one of the encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>                                     |
| [<span data-ttu-id="3b4ec-119">**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-119">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span></span>](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | <span data-ttu-id="3b4ec-120">傳回可供 CPU 或匯流排存取之前，用來加密內容的加密類型數目。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-120">Returns the number of encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>                                  |
| [<span data-ttu-id="3b4ec-121">**D3DAUTHENTICATEDQUERY \_ OUTPUTID**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-121">**D3DAUTHENTICATEDQUERY\_OUTPUTID**</span></span>](d3dauthenticatedquery-outputid.md)                                                                 | <span data-ttu-id="3b4ec-122">傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的其中一個輸出識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-122">Returns one of the output identifiers that is associated with a specified cryptographic session and Direct3D device.</span></span>                                        |
| [<span data-ttu-id="3b4ec-123">**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-123">**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**</span></span>](d3dauthenticatedquery-outputidcount.md)                                                       | <span data-ttu-id="3b4ec-124">傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的輸出識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-124">Returns the number of output identifiers associated with a specified cryptographic session and Direct3D device.</span></span>                                             |
| [<span data-ttu-id="3b4ec-125">**D3DAUTHENTICATEDQUERY \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-125">**D3DAUTHENTICATEDQUERY\_PROTECTION**</span></span>](d3dauthenticatedquery-protection.md)                                                             | <span data-ttu-id="3b4ec-126">傳回裝置目前的保護層級。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-126">Returns the current protection level for the device.</span></span>                                                                                                        |
| [<span data-ttu-id="3b4ec-127">**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-127">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**</span></span>](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | <span data-ttu-id="3b4ec-128">傳回允許以限制存取開啟共用資源之進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-128">Returns information about a process that is allowed to open shared resources with restricted access.</span></span>                                                        |
| [<span data-ttu-id="3b4ec-129">**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-129">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**</span></span>](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | <span data-ttu-id="3b4ec-130">傳回允許以限制存取開啟共用資源的進程數目。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-130">Returns the number of processes that are allowed to open shared resources with restricted access.</span></span>                                                           |
| [<span data-ttu-id="3b4ec-131">**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span><span class="sxs-lookup"><span data-stu-id="3b4ec-131">**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span></span>](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | <span data-ttu-id="3b4ec-132">傳回任何進程可以開啟且沒有限制的受保護共用資源數目。</span><span class="sxs-lookup"><span data-stu-id="3b4ec-132">Returns the number of protected shared resources that can be opened by any process with no restrictions.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="3b4ec-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b4ec-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b4ec-134">Direct3D 影片 Api</span><span class="sxs-lookup"><span data-stu-id="3b4ec-134">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> <dt>

[<span data-ttu-id="3b4ec-135">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="3b4ec-135">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> </dl>

 

 



