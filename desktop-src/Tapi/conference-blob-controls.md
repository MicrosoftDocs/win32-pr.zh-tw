---
description: 下圖說明與 TAPI 3 會議 blob 控制項相關的主要物件。 顯示的介面會以超連結的形式出現在相關的參考頁面中。
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: 會議 Blob 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512144"
---
# <a name="conference-blob-controls"></a><span data-ttu-id="f0d54-104">會議 Blob 控制項</span><span class="sxs-lookup"><span data-stu-id="f0d54-104">Conference Blob Controls</span></span>

<span data-ttu-id="f0d54-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="f0d54-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f0d54-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f0d54-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f0d54-107">下圖說明與 TAPI 3 會議 blob 控制項相關的主要物件。</span><span class="sxs-lookup"><span data-stu-id="f0d54-107">The following diagram illustrates the main objects involved in TAPI 3 conference blob controls.</span></span> <span data-ttu-id="f0d54-108">顯示的介面會以超連結的形式出現在相關的參考頁面中。</span><span class="sxs-lookup"><span data-stu-id="f0d54-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![會議 blob 控制項和介面](images/rendblob.png)

<span data-ttu-id="f0d54-110">會議 blob 包含會議物件的提供者特定資訊。</span><span class="sxs-lookup"><span data-stu-id="f0d54-110">The conference blob contains provider-specific information on a conference object.</span></span> <span data-ttu-id="f0d54-111">[**ITConferenceBlob**](itconferenceblob.md)介面 blob 的指標是藉由在 [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)上執行 QueryInterface 來取得的。</span><span class="sxs-lookup"><span data-stu-id="f0d54-111">A pointer to the [**ITConferenceBlob**](itconferenceblob.md) interface blob is obtained by doing a QueryInterface on [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span></span> <span data-ttu-id="f0d54-112">**ITConferenceBlob** 介面提供一般會議 blob 基本操作的方法。</span><span class="sxs-lookup"><span data-stu-id="f0d54-112">The **ITConferenceBlob** interface provides methods for basic manipulation of a generic conference blob.</span></span> <span data-ttu-id="f0d54-113">使用非 SDP 會議 blob 的應用程式必須針對詳細操作來執行自己的方法。</span><span class="sxs-lookup"><span data-stu-id="f0d54-113">An application using non-SDP conference blobs must implement its own methods for detail manipulation.</span></span>

<span data-ttu-id="f0d54-114">會合提供用來操作 SDP 會議 blob 的 [**ITSdp**](itsdp.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="f0d54-114">Rendezvous provides the [**ITSdp**](itsdp.md) interface for manipulating SDP conference blobs.</span></span> <span data-ttu-id="f0d54-115">SDP 是一種通訊協定，用來描述多媒體會話及其相關的排程資訊。</span><span class="sxs-lookup"><span data-stu-id="f0d54-115">The SDP is a protocol for describing multimedia sessions and their related scheduling information.</span></span> <span data-ttu-id="f0d54-116">如需 SDP 通訊協定的詳細資訊，請找出網際網路工程任務推動小組 (IETF) RFC 2327，其標題為「SDP： Session Description Protocol」。</span><span class="sxs-lookup"><span data-stu-id="f0d54-116">For additional information on the SDP protocol, locate Internet Engineering Task Force (IETF) RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="f0d54-117">如果指定的會議 blob 有 **ITSDP** 介面，您可以在 [**ITConferenceBlob**](itconferenceblob.md)上執行 **QueryInterface** 來取得它的指標。</span><span class="sxs-lookup"><span data-stu-id="f0d54-117">If the **ITSDP** interface exists for a given conference blob, you can obtain a pointer to it by doing a **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

<span data-ttu-id="f0d54-118">針對 SDP 會議 blob， [**ITTimeCollection**](ittimecollection.md)、 [**ITTime**](ittime.md)、 [**ITMediaCollection**](itmediacollection.md)和 [**ITMedia**](itmedia.md) 介面可讓您更詳細地控制 sdp 會議時間和媒體特性。</span><span class="sxs-lookup"><span data-stu-id="f0d54-118">For SDP conference blobs, the [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md), and [**ITMedia**](itmedia.md) interfaces allow detailed control of SDP conference time and media characteristics.</span></span>

 

 



