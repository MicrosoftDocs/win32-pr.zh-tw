---
description: 若要讓應用程式使用任何 TAPIs 30 補充電話功能，它需要連線到 TAPI，才能接收訊息。
ms.assetid: c0211f64-4f73-4348-ae49-9a898d3aa093
title: 初始化和關閉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831b8cfda84ac564450caec554191198fd4c21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973897"
---
# <a name="initialization-and-shutdown"></a><span data-ttu-id="a83b4-103">初始化和關閉</span><span class="sxs-lookup"><span data-stu-id="a83b4-103">Initialization and Shutdown</span></span>

<span data-ttu-id="a83b4-104">若要讓應用程式使用任何 TAPI 的30個補充電話功能，它需要連線到 TAPI，才能接收訊息。</span><span class="sxs-lookup"><span data-stu-id="a83b4-104">For an application to use any of TAPI's 30 supplementary phone functions, it needs a connection to TAPI, through which it can receive messages.</span></span> <span data-ttu-id="a83b4-105">應用程式會使用 [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) 函數來建立此連接。</span><span class="sxs-lookup"><span data-stu-id="a83b4-105">The application establishes this connection using the [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) function.</span></span> <span data-ttu-id="a83b4-106">在此函式中，應用程式會指定通知機制，讓 TAPI 用來通知應用程式的電話狀態變更，以及電話功能的非同步完成。</span><span class="sxs-lookup"><span data-stu-id="a83b4-106">In this function, the application specifies the notification mechanism by which TAPI informs the application of changes in the state of the phone and of asynchronous completion of phone functions.</span></span>

<span data-ttu-id="a83b4-107">[**PhoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)函式會將兩項資訊傳回給應用程式：*應用程式控制碼*，以及電話裝置數目。</span><span class="sxs-lookup"><span data-stu-id="a83b4-107">The [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) function returns two pieces of information to the application: an *application handle*, and the number of phone devices.</span></span> <span data-ttu-id="a83b4-108">應用程式控制碼代表應用程式的 TAPI 使用情形。</span><span class="sxs-lookup"><span data-stu-id="a83b4-108">The application handle represents the application's usage of TAPI.</span></span> <span data-ttu-id="a83b4-109">使用電話控制碼的 TAPI 函式不需要應用程式控制碼，因為此控制碼衍生自指定的電話控點。</span><span class="sxs-lookup"><span data-stu-id="a83b4-109">The TAPI functions that use phone handles do not require the application handle, as this handle is derived from the specified phone handle.</span></span>

<span data-ttu-id="a83b4-110">[**PhoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)所傳回的第二個資訊是可供 TAPI 使用的電話裝置數目。</span><span class="sxs-lookup"><span data-stu-id="a83b4-110">The second piece of information returned by [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) is the number of phone devices available to TAPI.</span></span> <span data-ttu-id="a83b4-111">手機裝置會以裝置識別碼 (*裝置* 識別碼) 來識別。</span><span class="sxs-lookup"><span data-stu-id="a83b4-111">Phone devices are identified by their device identifier (*device ID*).</span></span> <span data-ttu-id="a83b4-112">有效的裝置識別碼範圍從零到電話裝置數目減一。</span><span class="sxs-lookup"><span data-stu-id="a83b4-112">Valid device identifiers range from zero to the number of phone devices minus one.</span></span> <span data-ttu-id="a83b4-113">例如，如果 **phoneInitializeEx** 報告系統中有兩個電話裝置，則有效的電話裝置識別碼為0和1。</span><span class="sxs-lookup"><span data-stu-id="a83b4-113">For example, if **phoneInitializeEx** reports that there are two phone devices in a system, then valid phone device identifiers are 0 and 1.</span></span> <span data-ttu-id="a83b4-114">使用 TAPI 的電話功能完成應用程式之後，它會叫用 [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)，並傳遞其應用程式控制碼以關閉其使用 tapi。</span><span class="sxs-lookup"><span data-stu-id="a83b4-114">After an application is finished using the phone functions of TAPI, it invokes [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown), passing its application handle to shut down its usage of TAPI.</span></span> <span data-ttu-id="a83b4-115">這可讓 TAPI 釋放指派給應用程式的任何資源。</span><span class="sxs-lookup"><span data-stu-id="a83b4-115">This allows TAPI to free any resources assigned to the application.</span></span>

<span data-ttu-id="a83b4-116">應用程式不應叫用 [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) ，而不需再開啟電話 (至少用於監視) 。</span><span class="sxs-lookup"><span data-stu-id="a83b4-116">Applications should not invoke [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) without subsequently opening a phone (at least for monitoring).</span></span> <span data-ttu-id="a83b4-117">如果應用程式未監視，且未使用任何裝置，則應該呼叫 [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) ，以便在不需要時釋放 TAPI 動態連結程式庫所配置的記憶體資源，而且可以在不需要時從記憶體卸載程式庫本身。</span><span class="sxs-lookup"><span data-stu-id="a83b4-117">If the application is not monitoring and not using any devices, it should call [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) so that memory resources allocated by the TAPI dynamic-link library can be released if unneeded, and the library itself can be unloaded from memory while not needed.</span></span>

<span data-ttu-id="a83b4-118">[**PhoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)和 [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)都是以同步方式運作。</span><span class="sxs-lookup"><span data-stu-id="a83b4-118">Both [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) and [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) operate synchronously.</span></span> <span data-ttu-id="a83b4-119">也就是說，這些函式會傳回成功或失敗指示，而且永遠不會傳回非同步要求識別碼。</span><span class="sxs-lookup"><span data-stu-id="a83b4-119">That is, these functions either return a success or failure indication, and never return an asynchronous request identifier.</span></span>

 

 



