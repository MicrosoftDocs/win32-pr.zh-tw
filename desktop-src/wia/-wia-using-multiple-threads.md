---
description: 當您在單一進程內使用多個執行緒中的 Windows 映像取得 (WIA) 介面時，應用程式必須提供該介面的封送處理。
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: 在 WIA 應用程式中使用多個執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113273"
---
# <a name="using-multiple-threads-in-a-wia-application"></a><span data-ttu-id="b0c38-103">在 WIA 應用程式中使用多個執行緒</span><span class="sxs-lookup"><span data-stu-id="b0c38-103">Using Multiple Threads in a WIA Application</span></span>

<span data-ttu-id="b0c38-104">當您在單一進程內使用多個執行緒中的 Windows 映像取得 (WIA) 介面時，應用程式必須提供該介面的封送處理。</span><span class="sxs-lookup"><span data-stu-id="b0c38-104">When using a Windows Image Acquisition (WIA) interface in more than one thread within a single process, an application must provide marshalling for that interface.</span></span> <span data-ttu-id="b0c38-105">如果有一個執行緒建立介面指標，您就不能在不同的執行緒中使用該指標，而不需要封送處理。</span><span class="sxs-lookup"><span data-stu-id="b0c38-105">If one thread creates an interface pointer, you cannot use that pointer in a different thread without marshalling.</span></span>

<span data-ttu-id="b0c38-106">例如，如果應用程式中有一個執行緒取得 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 或 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標，則個別的執行緒無法使用該介面指標，而不需要封送處理。</span><span class="sxs-lookup"><span data-stu-id="b0c38-106">For example, if one thread in an application obtains a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface, a separate thread cannot use that interface pointer without marshalling.</span></span>

<span data-ttu-id="b0c38-107">用來完成此封送處理的常見技術是使用全域介面資料表。</span><span class="sxs-lookup"><span data-stu-id="b0c38-107">A common technique used to accomplish this marshalling is to use the global interface table.</span></span> <span data-ttu-id="b0c38-108">全域介面資料表是在單一進程內的所有線程上維護的資料表。</span><span class="sxs-lookup"><span data-stu-id="b0c38-108">The global interface table is a table maintained across all threads within a single process.</span></span> <span data-ttu-id="b0c38-109">在進程內執行的所有線程都可以取出註冊至全域介面資料表的介面。</span><span class="sxs-lookup"><span data-stu-id="b0c38-109">All threads running within the process can retrieve interfaces that are registered to the global interface table.</span></span> <span data-ttu-id="b0c38-110">這項技術可避免需要建立資料流程，以便線上程之間傳遞介面。</span><span class="sxs-lookup"><span data-stu-id="b0c38-110">This technique avoids the need to create streams for passing interfaces between threads.</span></span>

<span data-ttu-id="b0c38-111">如需有關如何使用全域介面表的詳細資訊，請參閱 [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable)。</span><span class="sxs-lookup"><span data-stu-id="b0c38-111">For information on how to use the global interface table, see [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="b0c38-112">即使您不想在 WIA 應用程式中使用多個執行緒，您也必須假設所有資料傳輸或裝置事件回呼函式都在不同的執行緒中執行。</span><span class="sxs-lookup"><span data-stu-id="b0c38-112">Even if you do not intend to use multiple threads in a WIA application, you must assume that all data transfer or device event callback functions run in separate threads.</span></span>

 

 
