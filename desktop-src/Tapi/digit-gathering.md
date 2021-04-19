---
description: 除了啟用數位監視，以及一次有一個數位的通知，應用程式也可以要求在緩衝區中收集多個數位。
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: 數位收集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5eab4185882b86a5a8e5dcb1444f39c9db2b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987457"
---
# <a name="digit-gathering"></a><span data-ttu-id="cb8f6-103">數位收集</span><span class="sxs-lookup"><span data-stu-id="cb8f6-103">Digit Gathering</span></span>

<span data-ttu-id="cb8f6-104">除了啟用數位監視，以及一次有一個數位的通知，應用程式也可以要求在緩衝區中收集多個數位。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-104">Besides enabling digit monitoring and being notified of digits one at a time, an application can also request that multiple digits be collected in a buffer.</span></span> <span data-ttu-id="cb8f6-105">只有當緩衝區已滿或符合某些其他終止條件時，應用程式才會收到通知。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-105">Only when the buffer is full or when some other termination condition is met is the application notified.</span></span> <span data-ttu-id="cb8f6-106">數位收集適用于信用卡號碼集合之類的功能。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-106">Digit gathering is useful for functions such as credit card number collection.</span></span> <span data-ttu-id="cb8f6-107">它會在應用程式呼叫 [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)時執行，並指定緩衝區以數位填滿。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-107">It is performed when an application calls [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), specifying a buffer to fill with digits.</span></span> <span data-ttu-id="cb8f6-108">當下列其中一個條件成立時，就會終止數位收集：</span><span class="sxs-lookup"><span data-stu-id="cb8f6-108">Digit gathering terminates when one of the following conditions is true:</span></span>

-   <span data-ttu-id="cb8f6-109">已收集要求的數位數目。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-109">The requested number of digits has been collected.</span></span>
-   <span data-ttu-id="cb8f6-110">偵測到多個終止數位的其中一個。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-110">One of multiple termination digits is detected.</span></span> <span data-ttu-id="cb8f6-111">終止數位會指定為 [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)，而且終止數位也會放在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-111">The termination digits are specified to [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), and the termination digit is placed in the buffer as well.</span></span>
-   <span data-ttu-id="cb8f6-112">兩個超時的其中一個過期。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-112">One of two timeouts expires.</span></span> <span data-ttu-id="cb8f6-113">Timeout 是第一個位數的 timeout，指定必須收集第一個數位之前的最大持續時間，以及指定連續位數之間的最大持續時間長度（以位數為限）的時間長度。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-113">The timeouts are a first digit timeout, specifying the maximum duration before the first digit must be collected, and an inter-digit timeout, specifying the maximum duration between successive digits.</span></span>
-   <span data-ttu-id="cb8f6-114">[**LineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)會以另一組參數再次取消數位收集，以啟動新的收集要求或使用 **Null** 位數的緩衝區參數來取消。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-114">Digit gathering is canceled explicitly by [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) again with either another set of parameters to start a new gathering request or by using a **NULL** digit buffer parameter to cancel.</span></span>

<span data-ttu-id="cb8f6-115">當數位收集因任何原因而終止時，會將 [**行 \_ GATHERDIGITS**](line-gatherdigits.md) 訊息傳送至要求數位收集的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-115">When digit gathering terminates for any reason, a [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is sent to the application that requested the digit gathering.</span></span> <span data-ttu-id="cb8f6-116">在呼叫擁有者的所有應用程式中，只有單一數位收集要求可以在任何指定時間的時間內完成。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-116">Only a single digit gathering request can be outstanding on a call at any given time across all applications that are owners of the call.</span></span>

<span data-ttu-id="cb8f6-117">您可以同時在相同的呼叫上啟用數位收集和數位監視。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-117">Digit gathering and digit monitoring can be enabled on the same call at the same time.</span></span> <span data-ttu-id="cb8f6-118">在這種情況下，應用程式將會收到每個偵測到之數位的 [**行 \_ MONITORDIGITS**](line-monitordigits.md) 訊息，以及 \_ 傳送回緩衝區時的個別行 GATHERDIGITS 訊息。</span><span class="sxs-lookup"><span data-stu-id="cb8f6-118">In that case, the application will receive a [**LINE\_MONITORDIGITS**](line-monitordigits.md) message for each detected digit and a separate LINE\_GATHERDIGITS message when the buffer is sent back.</span></span>

 

 



