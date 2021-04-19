---
description: ATM 適用于 LAN 和 WAN 環境。
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Winsock ATM 附錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992423"
---
# <a name="winsock-atm-annex"></a><span data-ttu-id="37b27-103">Winsock ATM 附錄</span><span class="sxs-lookup"><span data-stu-id="37b27-103">Winsock ATM Annex</span></span>

<span data-ttu-id="37b27-104">ATM 適用于 LAN 和 WAN 環境。</span><span class="sxs-lookup"><span data-stu-id="37b27-104">ATM is applicable to both LAN and WAN environments.</span></span> <span data-ttu-id="37b27-105">ATM 網路同時傳輸了各式各樣的網路流量，包括語音、資料、影像和影片。</span><span class="sxs-lookup"><span data-stu-id="37b27-105">An ATM network simultaneously transports a wide variety of network traffic — voice, data, image, and video.</span></span> <span data-ttu-id="37b27-106">它會在每個虛擬通道上為使用者提供保證的服務品質 (VC) 基礎。</span><span class="sxs-lookup"><span data-stu-id="37b27-106">It provides users with a guaranteed quality of service on a per-virtual channel (VC) basis.</span></span>



| <span data-ttu-id="37b27-107">元素</span><span class="sxs-lookup"><span data-stu-id="37b27-107">Element</span></span>          | <span data-ttu-id="37b27-108">描述</span><span class="sxs-lookup"><span data-stu-id="37b27-108">Description</span></span>                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b27-109">通訊協定名稱 (s) </span><span class="sxs-lookup"><span data-stu-id="37b27-109">Protocol name(s)</span></span> | <span data-ttu-id="37b27-110">ATMPROTO \_ AAL5、ATMPROTO \_ AALUSER</span><span class="sxs-lookup"><span data-stu-id="37b27-110">ATMPROTO\_AAL5, ATMPROTO\_AALUSER</span></span>                                                                                                                           |
| <span data-ttu-id="37b27-111">Description</span><span class="sxs-lookup"><span data-stu-id="37b27-111">Description</span></span>      | <span data-ttu-id="37b27-112">ATM AAL5 會提供以連接為導向的傳輸服務、保留的訊息界限，以及保證的 QOS。</span><span class="sxs-lookup"><span data-stu-id="37b27-112">ATM AAL5 provides a transport service that is connection oriented, message-boundary preserved, and QOS guaranteed.</span></span> <span data-ttu-id="37b27-113">ATMPROTO \_ AALUSER 是使用者定義的 AAL。</span><span class="sxs-lookup"><span data-stu-id="37b27-113">ATMPROTO\_AALUSER is a user-defined AAL.</span></span> |
| <span data-ttu-id="37b27-114">位址系列</span><span class="sxs-lookup"><span data-stu-id="37b27-114">Address family</span></span>   | <span data-ttu-id="37b27-115">AF \_ ATM</span><span class="sxs-lookup"><span data-stu-id="37b27-115">AF\_ATM</span></span>                                                                                                                                                     |
| <span data-ttu-id="37b27-116">標頭檔</span><span class="sxs-lookup"><span data-stu-id="37b27-116">Header file</span></span>      | <span data-ttu-id="37b27-117">Ws2atm。h</span><span class="sxs-lookup"><span data-stu-id="37b27-117">Ws2atm.h</span></span>                                                                                                                                                    |



 

<span data-ttu-id="37b27-118">本節說明 (ATM) 專屬延伸模組所需的非同步傳輸模式，以支援在 ATM 論壇使用者網路介面中公開和指定的原生 ATM 服務 (單一) 規格版本 3.x (3.0 和 3.1) 。</span><span class="sxs-lookup"><span data-stu-id="37b27-118">This section describes the Asynchronous Transfer Mode (ATM)-specific extensions needed to support the native ATM services as exposed and specified in the ATM Forum User Network Interface (UNI) specification version 3.x (3.0 and 3.1).</span></span> <span data-ttu-id="37b27-119">本檔支援 AAL 類型 5 (訊息模式) 和使用者定義 AAL。</span><span class="sxs-lookup"><span data-stu-id="37b27-119">This document supports AAL type 5 (message mode) and user-defined AAL.</span></span> <span data-ttu-id="37b27-120">本檔的未來版本將支援其他類型的 AAL 以及單向4.0。</span><span class="sxs-lookup"><span data-stu-id="37b27-120">Future versions of this document will support other types of AAL as well as UNI 4.0.</span></span>

 

 



