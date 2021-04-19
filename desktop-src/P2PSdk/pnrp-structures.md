---
description: PNRP 命名空間提供者 API 會使用下列結構：
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: PNRP 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974452"
---
# <a name="pnrp-structures"></a><span data-ttu-id="f7982-103">PNRP 結構</span><span class="sxs-lookup"><span data-stu-id="f7982-103">PNRP Structures</span></span>

<span data-ttu-id="f7982-104">PNRP 命名空間提供者 API 會使用下列結構：</span><span class="sxs-lookup"><span data-stu-id="f7982-104">The PNRP Namespace Provider API uses the following structures:</span></span>



| <span data-ttu-id="f7982-105">結構</span><span class="sxs-lookup"><span data-stu-id="f7982-105">Structure</span></span>                                                             | <span data-ttu-id="f7982-106">Description</span><span class="sxs-lookup"><span data-stu-id="f7982-106">Description</span></span>                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7982-107">**對等 \_ PNRP \_ 端點 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f7982-107">**PEER\_PNRP\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | <span data-ttu-id="f7982-108">包含與對等端點相關聯的 IP 位址和資料。</span><span class="sxs-lookup"><span data-stu-id="f7982-108">Contains the IP addresses and data associated with a peer endpoint.</span></span>                                                                                                 |
| [<span data-ttu-id="f7982-109">**對等 \_ PNRP \_ 雲端 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f7982-109">**PEER\_PNRP\_CLOUD\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | <span data-ttu-id="f7982-110">包含 (PNRP) 雲端之對等名稱解析通訊協定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f7982-110">Contains information about a Peer Name Resolution Protocol (PNRP) cloud.</span></span>                                                                                            |
| [<span data-ttu-id="f7982-111">**對等 \_ PNRP \_ 註冊 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f7982-111">**PEER\_PNRP\_REGISTRATION\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | <span data-ttu-id="f7982-112">包含向 PNRP 雲端註冊時，對等身分識別所提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="f7982-112">Contains the information provided by a peer identity when it registers with a PNRP cloud.</span></span>                                                                           |
| [<span data-ttu-id="f7982-113">PNRP 和 BLOB</span><span class="sxs-lookup"><span data-stu-id="f7982-113">PNRP and BLOB</span></span>](pnrp-and-blob.md)                                    | <span data-ttu-id="f7982-114">呼叫多個函數時，將資料傳遞至 [**WSAQUERYSET**](winsock-nsp-reference-links.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="f7982-114">Passes data to the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure during calls to several functions.</span></span>                                                  |
| [<span data-ttu-id="f7982-115">PNRP 和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="f7982-115">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)                      | <span data-ttu-id="f7982-116">有助於解析名稱和雲端的名稱和列舉。</span><span class="sxs-lookup"><span data-stu-id="f7982-116">Facilitates the resolving of names and the enumeration of names and clouds.</span></span>                                                                                         |
| [<span data-ttu-id="f7982-117">**PNRP \_ 雲端 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="f7982-117">**PNRP\_CLOUD\_ID**</span></span>](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | <span data-ttu-id="f7982-118">包含定義網路雲端的值。</span><span class="sxs-lookup"><span data-stu-id="f7982-118">Contains the values that define a network cloud.</span></span>                                                                                                                    |
| [<span data-ttu-id="f7982-119">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="f7982-119">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | <span data-ttu-id="f7982-120">由 [**WSAQUERYSET**](winsock-nsp-reference-links.md)結構的 **lpBlob** 成員指向。</span><span class="sxs-lookup"><span data-stu-id="f7982-120">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure.</span></span>                                                            |
| [<span data-ttu-id="f7982-121">**PNRPINFO \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f7982-121">**PNRPINFO\_V1**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | <span data-ttu-id="f7982-122">由 [**WSAQUERYSET**](winsock-nsp-reference-links.md)結構的 **lpBlob** 成員指向</span><span class="sxs-lookup"><span data-stu-id="f7982-122">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure</span></span>                                                             |
| <span data-ttu-id="f7982-123">[**PNRPINFO \_ V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7982-123">[**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span></span>                                   | <span data-ttu-id="f7982-124">由 [**WSAQUERYSET**](winsock-nsp-reference-links.md)結構的 **lpBlob** 成員指向，並提供應用程式特定的不透明資料的支援。</span><span class="sxs-lookup"><span data-stu-id="f7982-124">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure, and provides support for application-specific opaque data.</span></span> |



 

 

 
