---
description: 下列程式碼片段說明如何要求及設定會議的多播位址。
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: 取得多播位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112613"
---
# <a name="acquiring-a-multicast-address"></a><span data-ttu-id="41ce1-103">取得多播位址</span><span class="sxs-lookup"><span data-stu-id="41ce1-103">Acquiring a Multicast Address</span></span>

<span data-ttu-id="41ce1-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="41ce1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="41ce1-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="41ce1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="41ce1-106">下列程式碼片段說明如何要求及設定會議的多播位址。</span><span class="sxs-lookup"><span data-stu-id="41ce1-106">The following code fragment illustrates how to request and set a multicast address for a conference.</span></span>

<span data-ttu-id="41ce1-107">為了簡單起見，此片段顯示將一個多播位址指派給一個媒體專案。</span><span class="sxs-lookup"><span data-stu-id="41ce1-107">For the sake of simplicity, this fragment shows the assignment of one multicast address to one media item.</span></span> <span data-ttu-id="41ce1-108">在實際情況下，會針對參與會議的每個媒體專案，執行選取範圍、多播位址要求和指派。</span><span class="sxs-lookup"><span data-stu-id="41ce1-108">In actuality, the selection of a scope, the multicast address request, and the assignment will be performed for every media item involved in the conference.</span></span>

<span data-ttu-id="41ce1-109">此片段假設已經執行 [連接到 ILS 伺服器](connecting-to-an-ils-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="41ce1-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span> <span data-ttu-id="41ce1-110">此處所示的作業會在 [建立會議公告](creating-a-conference-announcement.md)的「必要時修改設定」一節中執行。</span><span class="sxs-lookup"><span data-stu-id="41ce1-110">The operations shown here would be performed in the "Modify the settings if necessary" section of [Creating a Conference Announcement](creating-a-conference-announcement.md).</span></span>


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a><span data-ttu-id="41ce1-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="41ce1-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41ce1-112">多播 COM 介面</span><span class="sxs-lookup"><span data-stu-id="41ce1-112">Multicast COM Interfaces</span></span>](multicast-com-interfaces.md)
</dt> <dt>

[<span data-ttu-id="41ce1-113">**IMcastAddressAllocation**</span><span class="sxs-lookup"><span data-stu-id="41ce1-113">**IMcastAddressAllocation**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[<span data-ttu-id="41ce1-114">**IMcastScope**</span><span class="sxs-lookup"><span data-stu-id="41ce1-114">**IMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[<span data-ttu-id="41ce1-115">**IMcastLeaseInfo**</span><span class="sxs-lookup"><span data-stu-id="41ce1-115">**IMcastLeaseInfo**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[<span data-ttu-id="41ce1-116">**IEnumMcastScope**</span><span class="sxs-lookup"><span data-stu-id="41ce1-116">**IEnumMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[<span data-ttu-id="41ce1-117">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="41ce1-117">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="41ce1-118">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="41ce1-118">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="41ce1-119">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="41ce1-119">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="41ce1-120">**IEnumBstr**</span><span class="sxs-lookup"><span data-stu-id="41ce1-120">**IEnumBstr**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[<span data-ttu-id="41ce1-121">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="41ce1-121">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="41ce1-122">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="41ce1-122">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 



