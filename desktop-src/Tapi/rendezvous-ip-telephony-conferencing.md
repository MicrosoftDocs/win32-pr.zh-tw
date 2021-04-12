---
description: TAPI 3 會合控制項可讓程式設計人員建立可建立及探索多媒體多播 IP 會議的應用程式。
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: 彙集 IP 電話語音會議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192733"
---
# <a name="rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="4cab6-103">彙集 IP 電話語音會議</span><span class="sxs-lookup"><span data-stu-id="4cab6-103">Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="4cab6-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="4cab6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4cab6-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="4cab6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4cab6-106">TAPI 3 會合控制項可讓程式設計人員建立可建立及探索多媒體多播 IP 會議的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4cab6-106">The TAPI 3 Rendezvous controls enable a programmer to create applications that can create and discover multimedia multicast IP conferences.</span></span>

<span data-ttu-id="4cab6-107">彙集的主要元件：</span><span class="sxs-lookup"><span data-stu-id="4cab6-107">The key components of Rendezvous:</span></span>

<span data-ttu-id="4cab6-108">[目錄控制項](directory-controls.md) 是 ILS 或 NTDS 伺服器上的會議清單摘要。</span><span class="sxs-lookup"><span data-stu-id="4cab6-108">[Directory Controls](directory-controls.md) are an abstraction of conference listings on an ILS or NTDS server.</span></span>

<span data-ttu-id="4cab6-109">[會議 Blob 控制項](conference-blob-controls.md) 代表會議特定的資訊，例如開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="4cab6-109">[Conference Blob Controls](conference-blob-controls.md) represent conference-specific information such as start and stop time.</span></span> <span data-ttu-id="4cab6-110">提供適用于 SDP 通訊協定 blob 的特殊介面。</span><span class="sxs-lookup"><span data-stu-id="4cab6-110">Special interfaces are provided for SDP protocol blobs.</span></span> <span data-ttu-id="4cab6-111">如需詳細資訊，請參閱 RFC 2327，其標題為「SDP： Session Description Protocol」。</span><span class="sxs-lookup"><span data-stu-id="4cab6-111">For detailed information, see RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="4cab6-112">您可以使用網際網路搜尋引擎來找出此 RFC 的目前複本。</span><span class="sxs-lookup"><span data-stu-id="4cab6-112">A current copy of this RFC can be located using an Internet search engine.</span></span>

<span data-ttu-id="4cab6-113">[多播 COM 介面](multicast-com-interfaces.md) 是 MADCAP 函式的 COM 包裝函式，先前稱為 MDHCP。</span><span class="sxs-lookup"><span data-stu-id="4cab6-113">[Multicast COM Interfaces](multicast-com-interfaces.md) are COM wrappers for the MADCAP functions, formerly know as MDHCP.</span></span> <span data-ttu-id="4cab6-114">這些介面可讓應用程式從多播位址佈建服務器取得多播位址。</span><span class="sxs-lookup"><span data-stu-id="4cab6-114">These interfaces allow an application to get multicast addresses from a multicast address allocation server.</span></span>

<span data-ttu-id="4cab6-115">下列內容提供 IP 電話語音和會議的會合控制項一般總覽和一些使用範例。</span><span class="sxs-lookup"><span data-stu-id="4cab6-115">The following material provides a general overview and some usage examples of the Rendezvous controls for IP telephony and conferencing.</span></span>

 

 



