---
description: 時間提供者會實作為 DLL。 每個 DLL 都可以支援多個時間提供者。 每個提供者都必須負責自己的設定和同步處理。
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: 建立時間提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001769"
---
# <a name="creating-a-time-provider"></a><span data-ttu-id="4b7b0-105">建立時間提供者</span><span class="sxs-lookup"><span data-stu-id="4b7b0-105">Creating a Time Provider</span></span>

<span data-ttu-id="4b7b0-106">時間提供者會實作為 DLL。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-106">A time provider is implemented as a DLL.</span></span> <span data-ttu-id="4b7b0-107">每個 DLL 都可以支援多個時間提供者。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-107">Each DLL can support multiple time providers.</span></span> <span data-ttu-id="4b7b0-108">每個提供者都必須負責自己的設定和同步處理。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-108">Each provider is responsible for its own configuration and synchronization.</span></span>

<span data-ttu-id="4b7b0-109">時間提供者必須執行下列回呼函數：</span><span class="sxs-lookup"><span data-stu-id="4b7b0-109">Time providers must implement the following callback functions:</span></span>

-   [<span data-ttu-id="4b7b0-110">**TimeProvClose**</span><span class="sxs-lookup"><span data-stu-id="4b7b0-110">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [<span data-ttu-id="4b7b0-111">**TimeProvCommand**</span><span class="sxs-lookup"><span data-stu-id="4b7b0-111">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [<span data-ttu-id="4b7b0-112">**TimeProvOpen**</span><span class="sxs-lookup"><span data-stu-id="4b7b0-112">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

<span data-ttu-id="4b7b0-113">載入提供者 DLL 之後，時間提供者管理員會呼叫 [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)，並將提供者的名稱和指標傳遞至下列函式：</span><span class="sxs-lookup"><span data-stu-id="4b7b0-113">After it has loaded the provider DLL, the time provider manager calls [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), passing the name of the provider and pointers to the following functions:</span></span>

-   [<span data-ttu-id="4b7b0-114">**AlertSamplesAvailFunc**</span><span class="sxs-lookup"><span data-stu-id="4b7b0-114">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [<span data-ttu-id="4b7b0-115">**GetTimeSysInfoFunc**</span><span class="sxs-lookup"><span data-stu-id="4b7b0-115">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [<span data-ttu-id="4b7b0-116">**LogTimeProvEventFunc**</span><span class="sxs-lookup"><span data-stu-id="4b7b0-116">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

<span data-ttu-id="4b7b0-117">這些函數可供時間提供者使用。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-117">These functions are for use by the time provider.</span></span> <span data-ttu-id="4b7b0-118">時間提供者會使用 [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) ，來傳回時間提供者管理員在傳送命令給時間提供者時所使用的提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-118">The time provider uses [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) to return a provider handle that the time provider manager uses when sending commands to the time provider.</span></span> <span data-ttu-id="4b7b0-119">控制碼值是由時間提供者所定義，而且主要是用來區分在相同 DLL 中執行的不同提供者。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-119">The handle value is defined by the time provider and is used primarily to distinguish between different providers implemented in the same DLL.</span></span> <span data-ttu-id="4b7b0-120">時間提供者可以使用 [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)記錄重要的事件。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-120">The time provider can log significant events using [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).</span></span>

<span data-ttu-id="4b7b0-121">時間提供者管理員會使用 [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) 將命令傳送給時間提供者。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-121">The time provider manager uses [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) to send commands to the time provider.</span></span> <span data-ttu-id="4b7b0-122">當時間提供者需要通知時間提供者管理員有可用的時間範例時，它會呼叫 [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-122">When the time provider needs to notify the time provider manager that it has time samples available, it calls [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc).</span></span> <span data-ttu-id="4b7b0-123">時間提供者管理員接著會使用 TPC \_ GetSamples 命令來呼叫 TimeProvCommand，以取出時間範例。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-123">The time provider manager then calls **TimeProvCommand** with the TPC\_GetSamples command to retrieve the time samples.</span></span> <span data-ttu-id="4b7b0-124">時間提供者管理員最多可能需要16秒鐘的時間來要求範例。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-124">It can take up to 16 seconds for the time provider manager to request the sample.</span></span> <span data-ttu-id="4b7b0-125">因此，應用程式不應該等待要求。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-125">Therefore, the application should not wait for the request.</span></span>

<span data-ttu-id="4b7b0-126">為確保精確度，時間提供者應該使用 [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)來取出所有時間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-126">To ensure accuracy, the time provider should retrieve all time-related information using [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).</span></span>

<span data-ttu-id="4b7b0-127">當您關閉時間提供者時，時間提供者管理員會呼叫 [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)。</span><span class="sxs-lookup"><span data-stu-id="4b7b0-127">When it is time to shut down the time provider, the time provider manager calls [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).</span></span>

 

 



