---
description: 一般而言，提供者會代表應用程式提供資料。
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: 與您的應用程式通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849297"
---
# <a name="communicating-with-your-application"></a><span data-ttu-id="f2e5d-103">與您的應用程式通訊</span><span class="sxs-lookup"><span data-stu-id="f2e5d-103">Communicating With Your Application</span></span>

<span data-ttu-id="f2e5d-104">一般而言，提供者會代表應用程式提供資料。</span><span class="sxs-lookup"><span data-stu-id="f2e5d-104">Typically, a provider provides data on behalf of an application.</span></span> <span data-ttu-id="f2e5d-105">例如，伺服器可能會建立效能 DLL 來提供其計數器資料。</span><span class="sxs-lookup"><span data-stu-id="f2e5d-105">For example, a server might create a performance DLL to provide its counter data.</span></span> <span data-ttu-id="f2e5d-106">應用程式與其提供者之間的通訊，會因使用者模式和核心模式應用程式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="f2e5d-106">Communication between an application and its provider differs for user-mode and kernel-mode applications.</span></span> <span data-ttu-id="f2e5d-107">提供者會在使用者模式中執行。</span><span class="sxs-lookup"><span data-stu-id="f2e5d-107">Providers execute in user mode.</span></span> <span data-ttu-id="f2e5d-108">因此，使用者模式應用程式（例如列印和顯示應用程式）可以使用任何技術進行處理序間通訊，例如具名管道、檔案對應或 RPC。</span><span class="sxs-lookup"><span data-stu-id="f2e5d-108">Because of this, user-mode applications, such as print and display applications, can use any technique for interprocess communication, such as named pipes, file mapping, or RPC.</span></span> <span data-ttu-id="f2e5d-109">不過，核心模式應用程式必須提供將效能資料傳回給提供者的 IOCTL 介面。</span><span class="sxs-lookup"><span data-stu-id="f2e5d-109">However, kernel-mode applications must provide an IOCTL interface that returns the performance data to the provider.</span></span>

> [!WARNING]
> <span data-ttu-id="f2e5d-110">請勿使用 COM 作為 IPC 機制。</span><span class="sxs-lookup"><span data-stu-id="f2e5d-110">Do not use COM as the IPC mechanism.</span></span> <span data-ttu-id="f2e5d-111">系統無法保證呼叫介面之執行緒的 COM 初始化狀態。</span><span class="sxs-lookup"><span data-stu-id="f2e5d-111">The system cannot guarantee the COM initialization state of the thread calling the interface.</span></span> <span data-ttu-id="f2e5d-112">因此，DLL 可能無法成功初始化 COM 並收集資料。</span><span class="sxs-lookup"><span data-stu-id="f2e5d-112">Therefore, the DLL may not be able to successfully initialize COM and collect the data.</span></span>

 

 

 



