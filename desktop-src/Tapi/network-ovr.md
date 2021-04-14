---
description: 網路會被視為傳輸機制，可將資料從某個點傳達給另一個點。
ms.assetid: 88374ac9-81c3-48c3-bf1a-5cfd734c257c
title: 網路
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d25f0c643ed1b54edb0ec45d47abfdc2f29fd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469244"
---
# <a name="network"></a><span data-ttu-id="f93c6-103">網路</span><span class="sxs-lookup"><span data-stu-id="f93c6-103">Network</span></span>

<span data-ttu-id="f93c6-104">網路會被視為傳輸機制，可將資料從某個點傳達給另一個點。</span><span class="sxs-lookup"><span data-stu-id="f93c6-104">A network is viewed as the transport mechanism that conveys data from one point to another.</span></span> <span data-ttu-id="f93c6-105">TAPI 服務提供者會處理執行作業所需的特定通訊協定，例如在指定的網路上建立通訊會話。</span><span class="sxs-lookup"><span data-stu-id="f93c6-105">TAPI service providers handle the specific protocols required to perform operations such as establishing a communications session on a given network.</span></span> <span data-ttu-id="f93c6-106">一般使用者或伺服器應用程式通常只需要非常一般的網路資訊，例如網址類別型。</span><span class="sxs-lookup"><span data-stu-id="f93c6-106">An end-user or server application normally requires only very general network information, such as address type.</span></span>

<span data-ttu-id="f93c6-107">一些常見的網路類型：</span><span class="sxs-lookup"><span data-stu-id="f93c6-107">Some common types of networks:</span></span>

-   <span data-ttu-id="f93c6-108">**(單純舊的電話語音) 的 POTS：** 語音和資料會在 *本機迴圈* 中以類比格式傳輸，並以數位方式傳送到其他位置。</span><span class="sxs-lookup"><span data-stu-id="f93c6-108">**POTS (Plain Old Telephone Service):** Voice and data are transmitted in analog format while in the *local loop* and are digitally transmitted elsewhere.</span></span> <span data-ttu-id="f93c6-109">一般來說，每個呼叫都會有一個媒體類型，每行一個通道。</span><span class="sxs-lookup"><span data-stu-id="f93c6-109">Typically, one media type per call, one channel per line.</span></span>
-   <span data-ttu-id="f93c6-110">**ISDN (整合式服務數位網路) ：** 經過數位傳送。</span><span class="sxs-lookup"><span data-stu-id="f93c6-110">**ISDN (Integrated Services Digital Network):** Transmitted digitally.</span></span> <span data-ttu-id="f93c6-111">在基本速率介面上，最高可達 128 Kbps 的速度 (BRI-ISDN) 行，而主要速率介面 (PRI-ISDN) 行。</span><span class="sxs-lookup"><span data-stu-id="f93c6-111">Speeds of up to 128 Kbps on Basic Rate Interface (BRI-ISDN) lines and much higher on Primary Rate Interface (PRI-ISDN) lines.</span></span> <span data-ttu-id="f93c6-112">至少有三個通道以及最多32個通道，以同時獨立運作的語音和資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="f93c6-112">At least three channels and as many as 32 channels, for simultaneous, independently operated transmission of voice and data.</span></span> <span data-ttu-id="f93c6-113">國際標準。</span><span class="sxs-lookup"><span data-stu-id="f93c6-113">International standard.</span></span>
-   <span data-ttu-id="f93c6-114">**T1/E1：** 經過數位傳送。</span><span class="sxs-lookup"><span data-stu-id="f93c6-114">**T1/E1:** Transmitted digitally.</span></span> <span data-ttu-id="f93c6-115">T1 是容量為 1.544 Mbps 的傳輸連結，通常用於跨遠端距離連接網路。</span><span class="sxs-lookup"><span data-stu-id="f93c6-115">T1 is a transmission link with a capacity of 1.544 Mbps, typically used for connecting networks across remote distances.</span></span> <span data-ttu-id="f93c6-116">在歐洲聯集 T1 中稱為 E1。</span><span class="sxs-lookup"><span data-stu-id="f93c6-116">In the European Union T1 is called E1.</span></span>
-   <span data-ttu-id="f93c6-117">**切換56：** 透過撥接電話線路以 56 Kbps 發出信號，但需要特殊設備。</span><span class="sxs-lookup"><span data-stu-id="f93c6-117">**Switched 56:** Signaling at 56 Kbps over dial-up telephone lines, but requires special equipment.</span></span> <span data-ttu-id="f93c6-118">受限於呼叫其他特殊配備的設備。</span><span class="sxs-lookup"><span data-stu-id="f93c6-118">Limited to calls to other specially equipped facilities.</span></span>
-   <span data-ttu-id="f93c6-119">**CENTREX：** 透過一般電話線路和使用電話公司設備的集中式網路服務。</span><span class="sxs-lookup"><span data-stu-id="f93c6-119">**CENTREX:** Centralized network services through regular telephone lines and using telephone company equipment.</span></span> <span data-ttu-id="f93c6-120">不需要特殊設備。</span><span class="sxs-lookup"><span data-stu-id="f93c6-120">No special equipment required.</span></span>
-   <span data-ttu-id="f93c6-121">**數位 pbx (私用分支交換) 和關鍵系統：** 使用專屬介面在私人電話系統上傳輸語音和資料。</span><span class="sxs-lookup"><span data-stu-id="f93c6-121">**Digital PBXs (private branch exchanges) and key systems:** Voice and data transmitted on private telephone systems using proprietary interfaces.</span></span>
-   <span data-ttu-id="f93c6-122">**IP 網路：** 使用網際網路通訊協定在網路上傳輸的語音和資料 (IP) ，例如網際網路本身或公司內部網路。</span><span class="sxs-lookup"><span data-stu-id="f93c6-122">**IP Networks:** Voice and data transmitted on networks using the Internet Protocol (IP), such as the Internet itself or a corporate intranet.</span></span>

<span data-ttu-id="f93c6-123">請注意這並不是完整的清單。</span><span class="sxs-lookup"><span data-stu-id="f93c6-123">Please note that this list is not exhaustive.</span></span> <span data-ttu-id="f93c6-124">如果有適當的服務提供者，就可以支援任何網路傳輸機制。</span><span class="sxs-lookup"><span data-stu-id="f93c6-124">Any network transport mechanism can be supported, given appropriate service providers.</span></span>

 

 



