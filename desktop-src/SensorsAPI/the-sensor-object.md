---
description: 感應器物件代表特定的感應器。
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: 感應器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997165"
---
# <a name="the-sensor-object"></a><span data-ttu-id="9729d-103">感應器物件</span><span class="sxs-lookup"><span data-stu-id="9729d-103">The Sensor Object</span></span>

<span data-ttu-id="9729d-104">感應器物件代表特定的感應器。</span><span class="sxs-lookup"><span data-stu-id="9729d-104">The sensor object represents a particular sensor.</span></span>

<span data-ttu-id="9729d-105">感應器 API 會將每個感應器表示為感應器物件。</span><span class="sxs-lookup"><span data-stu-id="9729d-105">The Sensor API represents each sensor as a sensor object.</span></span> <span data-ttu-id="9729d-106">您可以透過其 [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) 介面使用特定的感應器物件。</span><span class="sxs-lookup"><span data-stu-id="9729d-106">You can work with a particular sensor object through its [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface.</span></span> <span data-ttu-id="9729d-107">這個介面可讓您：</span><span class="sxs-lookup"><span data-stu-id="9729d-107">This interface enables you to:</span></span>

-   <span data-ttu-id="9729d-108">取得感應器的相關中繼資料，例如其識別碼、類型或易記名稱。</span><span class="sxs-lookup"><span data-stu-id="9729d-108">Retrieve metadata about the sensor, such as its ID, type, or friendly name.</span></span>
-   <span data-ttu-id="9729d-109">取得感應器可提供之特定資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9729d-109">Retrieve information about the specific data the sensor can provide.</span></span>
-   <span data-ttu-id="9729d-110">以同步方式取得資料。</span><span class="sxs-lookup"><span data-stu-id="9729d-110">Retrieve the data, synchronously.</span></span>
-   <span data-ttu-id="9729d-111">取得狀態資訊，例如感應器是否就緒。</span><span class="sxs-lookup"><span data-stu-id="9729d-111">Retrieve state information, such as whether the sensor is ready.</span></span>
-   <span data-ttu-id="9729d-112">指定程式將接收的事件。</span><span class="sxs-lookup"><span data-stu-id="9729d-112">Specify which events your program will receive.</span></span>
-   <span data-ttu-id="9729d-113">指定可供感應器 API 用來為您的程式提供事件通知的回呼介面。</span><span class="sxs-lookup"><span data-stu-id="9729d-113">Specify the callback interface that the Sensor API can use to provide your program with event notifications.</span></span>

 

 



