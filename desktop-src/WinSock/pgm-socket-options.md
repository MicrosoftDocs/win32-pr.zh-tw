---
description: PGM 使用通訊端選項來設定狀態、提供多播參數，並以其他方式執行其多播功能。
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: PGM 通訊端選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848004"
---
# <a name="pgm-socket-options"></a><span data-ttu-id="43612-103">PGM 通訊端選項</span><span class="sxs-lookup"><span data-stu-id="43612-103">PGM Socket Options</span></span>

<span data-ttu-id="43612-104">PGM 使用通訊端選項來設定狀態、提供多播參數，並以其他方式執行其多播功能。</span><span class="sxs-lookup"><span data-stu-id="43612-104">PGM uses socket options to set state, provide multicast parameters, and otherwise implement its multicast capabilities.</span></span> <span data-ttu-id="43612-105">此頁面指定應如何設定 PGM 通訊端選項、列舉適用于 PGM 的通訊端選項，以及在適當的情況下，提供各種選項的使用範例和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="43612-105">This page specifies how PGM socket options should be set, enumerates the socket options available for PGM, and where appropriate, provides usage examples and additional information for various options.</span></span> <span data-ttu-id="43612-106">如需每個 PCM 通訊端選項的基本定義，請參閱 [通訊端選項](socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="43612-106">For basic definitions of each PCM socket option, see [Socket Options](socket-options.md).</span></span>

<span data-ttu-id="43612-107">**WINDOWS XP：** 不支援可靠的多播程式設計 (的 PGM) 。</span><span class="sxs-lookup"><span data-stu-id="43612-107">**Windows XP:** Reliable Multicast Programming (PGM) is not supported.</span></span>

<span data-ttu-id="43612-108">下列通訊端選項適用于 PGM 寄件者：</span><span class="sxs-lookup"><span data-stu-id="43612-108">The following socket options are available for PGM senders:</span></span>

<dl> <span data-ttu-id="43612-109">RM \_ LATEJOIN</span><span class="sxs-lookup"><span data-stu-id="43612-109">RM\_LATEJOIN</span></span>  
<span data-ttu-id="43612-110">RM \_ 速率 \_ 視窗 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="43612-110">RM\_RATE\_WINDOW\_SIZE</span></span>  
<span data-ttu-id="43612-111">RM \_ 傳送 \_ 視窗 \_ 進階 \_ 率</span><span class="sxs-lookup"><span data-stu-id="43612-111">RM\_SEND\_WINDOW\_ADV\_RATE</span></span>  
<span data-ttu-id="43612-112">RM 傳送者 \_ \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="43612-112">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="43612-113">RM 傳送者 \_ \_ 視窗 \_ 前進 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="43612-113">RM\_SENDER\_WINDOW\_ADVANCE\_METHOD</span></span>  
<span data-ttu-id="43612-114">RM \_ SET \_ MCAST \_ TTL</span><span class="sxs-lookup"><span data-stu-id="43612-114">RM\_SET\_MCAST\_TTL</span></span>  
<span data-ttu-id="43612-115">RM \_ 設定 \_ 訊息 \_ 界限</span><span class="sxs-lookup"><span data-stu-id="43612-115">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="43612-116">RM \_ 設定 \_ 傳送 \_ IF</span><span class="sxs-lookup"><span data-stu-id="43612-116">RM\_SET\_SEND\_IF</span></span>  
<span data-ttu-id="43612-117">RM \_ 使用 \_ FEC</span><span class="sxs-lookup"><span data-stu-id="43612-117">RM\_USE\_FEC</span></span>  
</dl>

<span data-ttu-id="43612-118">[RM \_ \_ 傳送者] 視窗 [ \_ 前進方法] 選項會指定在 \_ 前進尾端 edge 傳送視窗時所使用的方法。</span><span class="sxs-lookup"><span data-stu-id="43612-118">The RM\_SENDER\_WINDOW\_ADVANCE\_METHOD option specifies the method used when advancing the trailing edge send window.</span></span> <span data-ttu-id="43612-119">Optval 參數只能透過 \_ \_ \_ (預設) 的時間，以電子視窗前進 \_ 。</span><span class="sxs-lookup"><span data-stu-id="43612-119">The optval parameter can only be E\_WINDOW\_ADVANCE\_BY\_TIME (the default).</span></span> <span data-ttu-id="43612-120">請注意， \_ \_ 不支援使用 E 視窗 \_ 作為資料快取 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="43612-120">Note that E\_WINDOW\_USE\_AS\_DATA\_CACHE is not supported.</span></span>

<span data-ttu-id="43612-121">以下是適用于 PGM 接收器的通訊端選項：</span><span class="sxs-lookup"><span data-stu-id="43612-121">The following socket options are available for PGM receivers:</span></span>

<dl> <span data-ttu-id="43612-122">RM \_ 新增 \_ 接收（ \_ 如果</span><span class="sxs-lookup"><span data-stu-id="43612-122">RM\_ADD\_RECEIVE\_IF</span></span>  
<span data-ttu-id="43612-123">RM \_ DEL \_ 接收 \_</span><span class="sxs-lookup"><span data-stu-id="43612-123">RM\_DEL\_RECEIVE\_IF</span></span>  
<span data-ttu-id="43612-124">RM \_ 高速 \_ \_ 內部網路 \_ 選擇</span><span class="sxs-lookup"><span data-stu-id="43612-124">RM\_HIGH\_SPEED\_INTRANET\_OPT</span></span>  
<span data-ttu-id="43612-125">RM \_ 接收器 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="43612-125">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

## <a name="setting-pgm-socket-options"></a><span data-ttu-id="43612-126">設定 PGM 通訊端選項</span><span class="sxs-lookup"><span data-stu-id="43612-126">Setting PGM Socket Options</span></span>

<span data-ttu-id="43612-127">下列程式碼片段說明設定 PGM 通訊端選項的程式設計指導方針：</span><span class="sxs-lookup"><span data-stu-id="43612-127">The following code snippet illustrates a programming guideline for setting PGM socket options:</span></span>


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



<span data-ttu-id="43612-128">在上述程式碼片段中， *OptionData* 的類型和內容取決於所設定的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="43612-128">In the snippet above, the type and contents of *OptionData* are dependent on the socket option being set.</span></span> <span data-ttu-id="43612-129">針對所有的 PGM 通訊端選項，通訊端層級為 IPPROTO \_ RM。</span><span class="sxs-lookup"><span data-stu-id="43612-129">For all PGM socket options, the socket level is IPPROTO\_RM.</span></span> <span data-ttu-id="43612-130">您必須在呼叫 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) 函式之後立即設定 PGM 通訊端選項，但有下列例外狀況：</span><span class="sxs-lookup"><span data-stu-id="43612-130">PGM socket options must be set immediately following the call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, with the following exceptions:</span></span>

<dl> <span data-ttu-id="43612-131">RM \_ 設定 \_ 訊息 \_ 界限</span><span class="sxs-lookup"><span data-stu-id="43612-131">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="43612-132">RM 傳送者 \_ \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="43612-132">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="43612-133">RM \_ 接收器 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="43612-133">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

 

 



