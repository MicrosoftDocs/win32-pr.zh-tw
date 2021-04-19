---
description: 數位監視會監視數位的呼叫。
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: 數位監視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966693"
---
# <a name="digit-monitoring"></a><span data-ttu-id="d5668-103">數位監視</span><span class="sxs-lookup"><span data-stu-id="d5668-103">Digit Monitoring</span></span>

<span data-ttu-id="d5668-104">數位監視會監視數位的呼叫。</span><span class="sxs-lookup"><span data-stu-id="d5668-104">Digit monitoring monitors the call for digits.</span></span> <span data-ttu-id="d5668-105">TAPI 允許根據兩種方法 (數位模式) 來發出信號：</span><span class="sxs-lookup"><span data-stu-id="d5668-105">TAPI allows digits to be signaled according to two methods (digit modes):</span></span>

-   <span data-ttu-id="d5668-106">脈衝位數會以脈衝或旋轉順序發出信號。</span><span class="sxs-lookup"><span data-stu-id="d5668-106">Pulse Digits are signaled as pulse or rotary sequences.</span></span> <span data-ttu-id="d5668-107">在偵測的情況下，這些跳動資訊清單本身就只是可聽見的點擊順序。</span><span class="sxs-lookup"><span data-stu-id="d5668-107">For detection, these pulses manifest themselves as nothing more than sequences of audible clicks.</span></span> <span data-ttu-id="d5668-108">有效的脈衝數位為 ' 0 ' 到 ' 9 '。</span><span class="sxs-lookup"><span data-stu-id="d5668-108">Valid pulse digits are '0' through '9'.</span></span>
-   <span data-ttu-id="d5668-109">DTMF 數位會以 DTMF (雙色調的多重頻率) 色調來發出信號。</span><span class="sxs-lookup"><span data-stu-id="d5668-109">DTMF Digits are signaled as DTMF (Dual Tone Multiple Frequency) tones.</span></span> <span data-ttu-id="d5668-110">有效的 DTMF 數位為 ' 0 ' 到 ' 9 '、' A '。</span><span class="sxs-lookup"><span data-stu-id="d5668-110">Valid DTMF digits are '0' through '9', 'A'.</span></span> <span data-ttu-id="d5668-111">' B '、' C '、' d '、' \* ' 和 ' \# '。</span><span class="sxs-lookup"><span data-stu-id="d5668-111">'B', 'C', 'D', '\*', and '\#'.</span></span> <span data-ttu-id="d5668-112">可以監視 DTMF 數位的開頭和下邊緣。</span><span class="sxs-lookup"><span data-stu-id="d5668-112">Both the beginning and the down edge of DTMF digits can be monitored.</span></span>

<span data-ttu-id="d5668-113">應用程式可以使用 [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)來啟用或停用指定之呼叫的數位監視。</span><span class="sxs-lookup"><span data-stu-id="d5668-113">An application can enable or disable digit monitoring on a specified call with [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span></span> <span data-ttu-id="d5668-114">啟用數位監視時，偵測到的數位會導致應用程式收到 [**行 \_ MONITORDIGITS**](line-monitordigits.md) 訊息的通知。</span><span class="sxs-lookup"><span data-stu-id="d5668-114">When digit monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORDIGITS**](line-monitordigits.md) message.</span></span> <span data-ttu-id="d5668-115">此訊息提供偵測到數位的呼叫控制碼，以及數位值和數位模式。</span><span class="sxs-lookup"><span data-stu-id="d5668-115">This message provides the call handle on which the digit was detected as well as the digit value and the digit mode.</span></span> <span data-ttu-id="d5668-116">數位監視的範圍是由呼叫的存留期所限制。</span><span class="sxs-lookup"><span data-stu-id="d5668-116">The scope of digit monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="d5668-117">呼叫 *中斷* 連線或 *閒置* 時，呼叫上的數位監視就會結束。</span><span class="sxs-lookup"><span data-stu-id="d5668-117">Digit monitoring on a call ends as soon as the call *disconnects* or goes *idle*.</span></span>

 

 



