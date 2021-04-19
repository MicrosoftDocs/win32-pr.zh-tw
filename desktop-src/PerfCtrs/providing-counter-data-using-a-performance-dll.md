---
description: 需要提供計數器資料的服務、驅動程式或應用程式可以撰寫效能 DLL 來提供資料。
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: 使用效能 DLL 提供計數器資料
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979148"
---
# <a name="providing-counter-data-using-a-performance-dll"></a><span data-ttu-id="d1948-103">使用效能 DLL 提供計數器資料</span><span class="sxs-lookup"><span data-stu-id="d1948-103">Providing Counter Data Using a Performance DLL</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1948-104">由於有顯著的效能和可靠性限制，提供本主題所描述的效能計數器資料的方法，可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d1948-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="d1948-105">相反地，Microsoft 建議您使用使用 [2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md) 來建立新的效能計數器，以及遷移現有的效能計數器來使用該方法所述的方法。</span><span class="sxs-lookup"><span data-stu-id="d1948-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters, and that you migrate existing performance counters to use that method as well.</span></span>

<span data-ttu-id="d1948-106">需要提供計數器資料的服務、驅動程式或應用程式可以撰寫效能 DLL 來提供資料。</span><span class="sxs-lookup"><span data-stu-id="d1948-106">A service, driver, or application that wants to provide counter data can write a performance DLL to provide the data.</span></span> <span data-ttu-id="d1948-107">當取用者查詢效能資料時，系統會將提供者 DLL 載入取用者的進程，並呼叫提供者來收集資料。</span><span class="sxs-lookup"><span data-stu-id="d1948-107">When a consumer queries performance data, the system loads the provider DLL into the consumer's process and calls the provider to collect the data.</span></span> <span data-ttu-id="d1948-108">如需撰寫效能 DLL 的詳細資訊，請參閱 [建立效能延伸模組 dll](creating-a-performance-extension-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="d1948-108">For details on writing the performance DLL, see [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md).</span></span>

<span data-ttu-id="d1948-109">系統會使用登錄來判斷要呼叫的提供者。</span><span class="sxs-lookup"><span data-stu-id="d1948-109">The system uses the registry to determine which provider to call.</span></span> <span data-ttu-id="d1948-110">如需註冊提供者及其支援之計數器的詳細資訊，請參閱 [新增效能計數器](adding-performance-counters.md)。</span><span class="sxs-lookup"><span data-stu-id="d1948-110">For information on registering your provider and the counters that it supports, see [Adding Performance Counters](adding-performance-counters.md).</span></span>

> [!Note]
> <span data-ttu-id="d1948-111">Windows OneCore 不支援效能 Dll。</span><span class="sxs-lookup"><span data-stu-id="d1948-111">Performance DLLs are not supported on Windows OneCore.</span></span> <span data-ttu-id="d1948-112">如果要撰寫必須在 Windows OneCore 上執行的元件，請使用在 [使用2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md)中所述的方法。</span><span class="sxs-lookup"><span data-stu-id="d1948-112">If writing a component that must run on Windows OneCore, use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>
