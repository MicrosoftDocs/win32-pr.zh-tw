---
description: 對等散發 API 會定義下列資料類型。
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: '對等散發 API 資料類型 (Peerdist. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001713"
---
# <a name="peer-distribution-api-data-types"></a><span data-ttu-id="e214d-103">對等散發 API 資料類型</span><span class="sxs-lookup"><span data-stu-id="e214d-103">Peer Distribution API Data Types</span></span>

<span data-ttu-id="e214d-104">對等散發 API 會定義下列資料類型。</span><span class="sxs-lookup"><span data-stu-id="e214d-104">The Peer Distribution API defines the following data types.</span></span>


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| <span data-ttu-id="e214d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e214d-105">Data type</span></span>                                                                                                                     | <span data-ttu-id="e214d-106">描述</span><span class="sxs-lookup"><span data-stu-id="e214d-106">Description</span></span>                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e214d-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**PEERDIST \_ 實例 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="e214d-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**PEERDIST\_INSTANCE\_HANDLE**</span></span>          | <span data-ttu-id="e214d-108">與對等散發實例相關聯的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e214d-108">A handle associated with the Peer Distribution instance.</span></span> <span data-ttu-id="e214d-109">這個控制碼是由 [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)所建立，並用於大部分的對等散發作業。</span><span class="sxs-lookup"><span data-stu-id="e214d-109">This handle is created by [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup), and used in most Peer Distribution operations.</span></span><br/>                                          |
| <span data-ttu-id="e214d-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**PEERDIST \_ 內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="e214d-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**PEERDIST\_CONTENT\_HANDLE**</span></span>             | <span data-ttu-id="e214d-111">與內容相關聯的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e214d-111">A handle associated with content.</span></span> <span data-ttu-id="e214d-112">這個控制碼是由 [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) 所建立，並且會在開啟、關閉、新增或發佈內容時參考。</span><span class="sxs-lookup"><span data-stu-id="e214d-112">This handle is created by [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) and is referenced when opening, closing, adding, or publishing content.</span></span><br/>                     |
| <span data-ttu-id="e214d-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**PEERDIST \_ CONTENTINFO \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="e214d-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**PEERDIST\_CONTENTINFO\_HANDLE**</span></span> | <span data-ttu-id="e214d-114">與內容資訊相關聯的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e214d-114">A handle associated with content information.</span></span> <span data-ttu-id="e214d-115">這個控制碼是由 [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)所建立，並且會在抓取編碼的內容資訊時使用。</span><span class="sxs-lookup"><span data-stu-id="e214d-115">This handle is created by [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation), and is used when retrieving encoded content information.</span></span><br/> |
| <span data-ttu-id="e214d-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**PEERDIST \_ 串流 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="e214d-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**PEERDIST\_STREAM\_HANDLE**</span></span>                | <span data-ttu-id="e214d-117">與資料流程相關聯的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e214d-117">A handle associated with a data stream.</span></span> <span data-ttu-id="e214d-118">這個控制碼是由 [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) 所建立，並且會在發行、關閉或新增至串流內容時參考。</span><span class="sxs-lookup"><span data-stu-id="e214d-118">This handle is created by [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) and is referenced when publishing, closing, or adding to streamed content.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="e214d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e214d-119">Requirements</span></span>



| <span data-ttu-id="e214d-120">需求</span><span class="sxs-lookup"><span data-stu-id="e214d-120">Requirement</span></span> | <span data-ttu-id="e214d-121">值</span><span class="sxs-lookup"><span data-stu-id="e214d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e214d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e214d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e214d-123">僅限 Windows 7 Professional \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e214d-123">Windows 7 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e214d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e214d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e214d-125">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e214d-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e214d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e214d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e214d-127"><dt>Peerdist. h</dt></span><span class="sxs-lookup"><span data-stu-id="e214d-127"><dt>Peerdist.h</dt></span></span> </dl> |



 

 




