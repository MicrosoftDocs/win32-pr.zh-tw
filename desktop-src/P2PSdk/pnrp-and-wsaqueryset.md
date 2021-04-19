---
description: PNRP 會使用 WSAQUERYSET 結構搭配各種函式，以加速解析名稱和列舉名稱和雲端。
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: 'PNRP 和 WSAQUERYSET (P2P. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998306"
---
# <a name="pnrp-and-wsaqueryset"></a><span data-ttu-id="1614c-103">PNRP 和 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="1614c-103">PNRP and WSAQUERYSET</span></span>

<span data-ttu-id="1614c-104">PNRP 會使用 [**WSAQUERYSET**](winsock-nsp-reference-links.md) 結構搭配各種函式，以加速解析名稱和列舉名稱和雲端。</span><span class="sxs-lookup"><span data-stu-id="1614c-104">PNRP uses the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure in conjunction with various functions to facilitate resolving names and enumerating names and clouds.</span></span>

<span data-ttu-id="1614c-105">如需 [**WSAQUERYSET**](winsock-nsp-reference-links.md) 或 Windows 通訊端函式的完整定義，請參閱其在 Platform SDK 的 Windows 通訊端 2 API 檔中各自的定義。</span><span class="sxs-lookup"><span data-stu-id="1614c-105">For complete definitions of [**WSAQUERYSET**](winsock-nsp-reference-links.md) or Windows Sockets functions, see their respective definitions in the Windows Sockets 2 API documentation in the Platform SDK.</span></span>

## <a name="wsaqueryset-and-wsasetservice"></a><span data-ttu-id="1614c-106">WSAQUERYSET 和 WSASetService</span><span class="sxs-lookup"><span data-stu-id="1614c-106">WSAQUERYSET and WSASetService</span></span>

<span data-ttu-id="1614c-107">[**WSASetService**](winsock-nsp-reference-links.md)函數會使用 **WSAQUERYSET** 結構來註冊或移除對等名稱。</span><span class="sxs-lookup"><span data-stu-id="1614c-107">The [**WSASetService**](winsock-nsp-reference-links.md) function uses the **WSAQUERYSET** structure to register or remove peer names.</span></span> <span data-ttu-id="1614c-108">[PNRP 和 WSASetService](pnrp-and-wsasetservice.md)頁面概述如何搭配使用 **WSAQUERYSET** 結構與此函數。</span><span class="sxs-lookup"><span data-stu-id="1614c-108">The [PNRP and WSASetService](pnrp-and-wsasetservice.md) page outlines how to use the **WSAQUERYSET** structure with this function.</span></span>

## <a name="wsaqueryset-and-wsalookupservicebegin"></a><span data-ttu-id="1614c-109">WSAQUERYSET 和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="1614c-109">WSAQUERYSET and WSALookupServiceBegin</span></span>

<span data-ttu-id="1614c-110">[**WSAQUERYSET**](winsock-nsp-reference-links.md)結構廣泛用於 **WSALookupServiceBegin**、 **WSALookupServiceNext** 和 **WSALookupServiceEnd** 函數。</span><span class="sxs-lookup"><span data-stu-id="1614c-110">The [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure is used extensively with the **WSALookupServiceBegin**, **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span> <span data-ttu-id="1614c-111">下列參考頁面詳細說明這些函數如何使用 **WSAQUERYSET** 結構：</span><span class="sxs-lookup"><span data-stu-id="1614c-111">Details about how these functions use the **WSAQUERYSET** structure are detailed in the following reference pages:</span></span>

-   [<span data-ttu-id="1614c-112">PNRP 和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="1614c-112">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
-   [<span data-ttu-id="1614c-113">PNRP 和 WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="1614c-113">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
-   [<span data-ttu-id="1614c-114">PNRP 和 WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="1614c-114">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a><span data-ttu-id="1614c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1614c-115">Requirements</span></span>



| <span data-ttu-id="1614c-116">需求</span><span class="sxs-lookup"><span data-stu-id="1614c-116">Requirement</span></span> | <span data-ttu-id="1614c-117">值</span><span class="sxs-lookup"><span data-stu-id="1614c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1614c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1614c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1614c-119">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1614c-119">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1614c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1614c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1614c-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1614c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1614c-122">版本</span><span class="sxs-lookup"><span data-stu-id="1614c-122">Version</span></span><br/>                  | <span data-ttu-id="1614c-123">Windows XP （含 SP1）與 Windows XP 的 Advanced 網路套件</span><span class="sxs-lookup"><span data-stu-id="1614c-123">Windows XP with SP1 with the Advanced Networking Pack for Windows XP</span></span><br/>  |
| <span data-ttu-id="1614c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1614c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1614c-125"><dt>P2P。h</dt></span><span class="sxs-lookup"><span data-stu-id="1614c-125"><dt>P2P.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1614c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1614c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1614c-127">PNRP 和 BLOB</span><span class="sxs-lookup"><span data-stu-id="1614c-127">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="1614c-128">PNRP 和 WSASetService</span><span class="sxs-lookup"><span data-stu-id="1614c-128">PNRP and WSASetService</span></span>](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




