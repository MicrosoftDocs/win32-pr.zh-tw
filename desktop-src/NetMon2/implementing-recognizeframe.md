---
description: 網路監視器會呼叫剖析器的 RecognizeFrame 函式，以判斷剖析器是否能辨識框架的取消認領資料。
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: 執行 RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970eee80a04168b3fa06b117c2c219c506da7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320555"
---
# <a name="implementing-recognizeframe"></a><span data-ttu-id="d6333-103">執行 RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="d6333-103">Implementing RecognizeFrame</span></span>

<span data-ttu-id="d6333-104">網路監視器會呼叫剖析器的 [**RecognizeFrame**](recognizeframe.md) 函式，以判斷剖析器是否能辨識框架的取消認領資料。</span><span class="sxs-lookup"><span data-stu-id="d6333-104">Network Monitors calls the [**RecognizeFrame**](recognizeframe.md) function of a parser to determine that the parser recognizes the unclaimed data of a frame.</span></span> <span data-ttu-id="d6333-105">取消認領資料可能位於框架的開頭，但是取消認領資料通常位於框架的中間。</span><span class="sxs-lookup"><span data-stu-id="d6333-105">The unclaimed data may be at the start of a frame, but typically, unclaimed data is located in the middle of a frame.</span></span> <span data-ttu-id="d6333-106">下圖顯示位於框架中間的取消認領資料。</span><span class="sxs-lookup"><span data-stu-id="d6333-106">The following illustration shows unclaimed data located in the middle of a frame.</span></span>

![取消認領位於框架中間的資料](images/recognizeframe1.png)

<span data-ttu-id="d6333-108">網路監視器在呼叫 [**RecognizeFrame**](recognizeframe.md) 函數時提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="d6333-108">Network Monitor provides the following information when it calls the [**RecognizeFrame**](recognizeframe.md) function:</span></span>

-   <span data-ttu-id="d6333-109">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d6333-109">A handle to the frame.</span></span>
-   <span data-ttu-id="d6333-110">框架開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="d6333-110">A pointer to the start of the frame.</span></span>
-   <span data-ttu-id="d6333-111">取消認領資料開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="d6333-111">A pointer to the start of the unclaimed data.</span></span>
-   <span data-ttu-id="d6333-112">框架中第一個通訊協定的 MAC 值。</span><span class="sxs-lookup"><span data-stu-id="d6333-112">The MAC value of the first protocol in the frame.</span></span>
-   <span data-ttu-id="d6333-113">取消認領資料中的位元組數目;也就是框架中剩餘的位元組。</span><span class="sxs-lookup"><span data-stu-id="d6333-113">The number of bytes in the unclaimed data; that is, the bytes remaining in the frame.</span></span>
-   <span data-ttu-id="d6333-114">先前通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d6333-114">A handle to the previous protocol.</span></span>
-   <span data-ttu-id="d6333-115">先前通訊協定的位移。</span><span class="sxs-lookup"><span data-stu-id="d6333-115">The offset of the previous protocol.</span></span>

<span data-ttu-id="d6333-116">當剖析器 DLL 判斷取消認領資料是從剖析器通訊協定開始時，剖析器 DLL 會決定下一個通訊協定的開始位置，以及接下來的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d6333-116">When the parser DLL determines that unclaimed data starts with the parser protocol, the parser DLL determines where the next protocol starts, and which protocol follows.</span></span> <span data-ttu-id="d6333-117">剖析器 DLL 會以下列條件方式運作：</span><span class="sxs-lookup"><span data-stu-id="d6333-117">The parser DLL functions in the following conditional ways:</span></span>

-   <span data-ttu-id="d6333-118">如果剖析器 DLL 辨識取消認領資料，剖析器 DLL 會設定 *pProtocolStatus* 參數，並將指標傳回至框架中的下一個通訊協定，或傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d6333-118">If the parser DLL recognizes unclaimed data, the parser DLL sets the *pProtocolStatus* parameter, and returns a pointer to either the next protocol in the frame, or **NULL**.</span></span> <span data-ttu-id="d6333-119">如果目前的通訊協定是框架中的最後一個通訊協定，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d6333-119">**NULL** is returned if the current protocol is the last protocol in the frame.</span></span>
-   <span data-ttu-id="d6333-120">如果剖析器 DLL 辨識出取消認領的資料，並從通訊協定) 所提供的資訊 (識別接下來的通訊協定，則剖析器 DLL 會將指標傳回至函式之 *phNextProtocol* 參數中下一個通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d6333-120">If the parser DLL recognizes unclaimed data and identifies the protocol that follows (from information provided in the protocol), then the parser DLL returns a pointer to the handle of the next protocol in the *phNextProtocol* parameter of the function.</span></span>
-   <span data-ttu-id="d6333-121">如果剖析器 DLL 無法辨識取消認領資料，剖析器 DLL 會傳回取消認領資料開頭的指標，網路監視器繼續嘗試剖析取消認領資料。</span><span class="sxs-lookup"><span data-stu-id="d6333-121">If the parser DLL does not recognize unclaimed data, the parser DLL returns the pointer to the start of unclaimed data, and Network Monitor continues trying to parse the unclaimed data.</span></span>

<span data-ttu-id="d6333-122">**若要執行 RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="d6333-122">**To implement RecognizeFrame**</span></span>

1.  <span data-ttu-id="d6333-123">測試以判斷您是否辨識了通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d6333-123">Test to determine that you recognize the protocol.</span></span>
2.  <span data-ttu-id="d6333-124">如果您辨識取消認領資料，並知道接下來的通訊協定，請將 *pProtocolStatus* 設定為 [通訊協定 \_ 狀態 \_ 下一個 \_ 通訊協定]，將 *phNextProtocol* 設定為指向下一個通訊協定控制碼的指標，然後將指標傳回至下一個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d6333-124">If you recognize unclaimed data and you know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_NEXT\_PROTOCOL, set *phNextProtocol* to a pointer that points to the handle for the next protocol, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="d6333-125">–或–</span><span class="sxs-lookup"><span data-stu-id="d6333-125">–or–</span></span>

    <span data-ttu-id="d6333-126">如果您辨識取消認領資料，但不知道接下來的通訊協定，請將 *pProtocolStatus* 設定為 [辨識的通訊協定 \_ 狀態 \_ ]，然後將指標傳回至下一個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d6333-126">If you recognize unclaimed data and you do not know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_RECOGNIZED, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="d6333-127">–或–</span><span class="sxs-lookup"><span data-stu-id="d6333-127">–or–</span></span>

    <span data-ttu-id="d6333-128">如果您辨識取消認領資料，而您的通訊協定是框架中的最後一個通訊協定，請將 *pProtocolStatus* 設定為已宣告的通訊協定 \_ 狀態，然後傳回 \_ **Null**。</span><span class="sxs-lookup"><span data-stu-id="d6333-128">If you recognize unclaimed data and your protocol is the last protocol in a frame, set *pProtocolStatus* to PROTOCOL\_STATUS\_CLAIMED, and then return **NULL**.</span></span>

    <span data-ttu-id="d6333-129">–或–</span><span class="sxs-lookup"><span data-stu-id="d6333-129">–or–</span></span>

    <span data-ttu-id="d6333-130">如果您無法辨識取消認領資料，請將 *pProtocolStatus* 設定為無法辨識的通訊協定 \_ 狀態 \_ \_ ，然後傳回在 *pProtocol* 中傳遞給您的指標。</span><span class="sxs-lookup"><span data-stu-id="d6333-130">If you do not recognize unclaimed data, set *pProtocolStatus* to PROTOCOL\_STATUS\_NOT\_RECOGNIZED, and then return the pointer that is passed to you in *pProtocol*.</span></span>

<span data-ttu-id="d6333-131">以下是 [**RecognizeFrame**](recognizeframe.md)的基本執行。</span><span class="sxs-lookup"><span data-stu-id="d6333-131">The following is a basic implementation of [**RecognizeFrame**](recognizeframe.md).</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



