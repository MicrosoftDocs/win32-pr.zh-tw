---
description: Microsoft 對等散發服務支援下列結構。
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: 對等散發 API 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977326"
---
# <a name="peer-distribution-api-structures"></a><span data-ttu-id="f15aa-103">對等散發 API 結構</span><span class="sxs-lookup"><span data-stu-id="f15aa-103">Peer Distribution API Structures</span></span>

<span data-ttu-id="f15aa-104">Microsoft 對等散發服務支援下列結構。</span><span class="sxs-lookup"><span data-stu-id="f15aa-104">The Microsoft Peer Distribution service supports the following structures.</span></span>



| <span data-ttu-id="f15aa-105">結構</span><span class="sxs-lookup"><span data-stu-id="f15aa-105">Structure</span></span>                                                              | <span data-ttu-id="f15aa-106">Description</span><span class="sxs-lookup"><span data-stu-id="f15aa-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f15aa-107">**PEERDIST \_ 用戶端 \_ 基本 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f15aa-107">**PEERDIST\_CLIENT\_BASIC\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | <span data-ttu-id="f15aa-108">指出是否有許多用戶端同時下載相同的內容。</span><span class="sxs-lookup"><span data-stu-id="f15aa-108">Indicates whether or not there are many clients simultaneously downloading the same content.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="f15aa-109">**PEERDIST \_ 內容 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="f15aa-109">**PEERDIST\_CONTENT\_TAG**</span></span>](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | <span data-ttu-id="f15aa-110">包含用戶端提供的標記，這是 [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)的輸入值。</span><span class="sxs-lookup"><span data-stu-id="f15aa-110">Contains a client supplied tag which is an input value for [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span></span> <span data-ttu-id="f15aa-111">此標記與內容區段相關聯，並用於內容管理 Api，例如 [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)。</span><span class="sxs-lookup"><span data-stu-id="f15aa-111">The tag is associated with the content segment and is used in content management APIs, like [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span></span> |
| [<span data-ttu-id="f15aa-112">**PEERDIST \_ 發行集 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="f15aa-112">**PEERDIST\_PUBLICATION\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | <span data-ttu-id="f15aa-113">包含發行集選項，包括 API 版本資訊和可能的選項旗標。</span><span class="sxs-lookup"><span data-stu-id="f15aa-113">Contains publication options, including the API version information and possible option flags.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="f15aa-114">**對等抓取 \_ \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="f15aa-114">**PEER\_RETRIEVAL\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | <span data-ttu-id="f15aa-115">包含要取出的內容資訊版本。</span><span class="sxs-lookup"><span data-stu-id="f15aa-115">Contains version of the content information to retrieve.</span></span>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="f15aa-116">**PEERDIST \_ 狀態 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f15aa-116">**PEERDIST\_STATUS\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | <span data-ttu-id="f15aa-117">包含本機電腦上 BranchCache 服務目前狀態和功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f15aa-117">Contains information about the current status and capabilities of the BranchCache service on the local computer.</span></span>                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="f15aa-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="f15aa-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f15aa-119">對等散發 API 參考</span><span class="sxs-lookup"><span data-stu-id="f15aa-119">Peer Distribution API Reference</span></span>](peer-distribution-api-reference.md)
</dt> </dl>

 

 



