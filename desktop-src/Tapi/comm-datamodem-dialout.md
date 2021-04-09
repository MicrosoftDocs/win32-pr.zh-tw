---
description: 通訊/datamodem/撥出
ms.assetid: b1cc19d2-4a9f-4d3f-a868-d5928654ad75
title: 通訊/datamodem/撥出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553e998acdfe77509d62050b825dae6ea88d3b3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944731"
---
# <a name="commdatamodemdialout"></a><span data-ttu-id="342bc-103">通訊/datamodem/撥出</span><span class="sxs-lookup"><span data-stu-id="342bc-103">comm/datamodem/dialout</span></span>

<span data-ttu-id="342bc-104">**通訊/datamodem/撥** 出裝置類別包含僅用於撥出電話的 datamodem 裝置。</span><span class="sxs-lookup"><span data-stu-id="342bc-104">The **comm/datamodem/dialout** device class consists of datamodem devices only used for outgoing calls.</span></span> <span data-ttu-id="342bc-105">此類別會取代 Windows 2000 和更新版本作業系統上的 [**comm/datamodem**](comm-datamodem.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="342bc-105">This class replaces the [**comm/datamodem**](comm-datamodem.md) class on Windows 2000 and later operating systems.</span></span>

<span data-ttu-id="342bc-106">在 Windows 2000 之前，Unimodem TSP 只支援 [**comm/datamodem**](comm-datamodem.md) 裝置類別。</span><span class="sxs-lookup"><span data-stu-id="342bc-106">Before Windows 2000, the Unimodem TSP only supported the [**comm/datamodem**](comm-datamodem.md) device class.</span></span> <span data-ttu-id="342bc-107">當應用程式撥出來電時發生非預期的行為。當應用程式撥出來電時，可能會變更由服務等候來電的設定。</span><span class="sxs-lookup"><span data-stu-id="342bc-107">Unexpected behavior may occur when an application dialing an outbound call changes the configuration set by a service waiting for an incoming call.</span></span> <span data-ttu-id="342bc-108">使用 Windows 2000 和更新版本作業系統的應用程式應在對 [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)或 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)的呼叫中，指定 [**通訊/datamodem/撥**](comm-datamodem-dialin.md)入或 **comm/datamodem/撥** 出。</span><span class="sxs-lookup"><span data-stu-id="342bc-108">Applications using Windows 2000 and later operating systems should specify either [**comm/datamodem/dialin**](comm-datamodem-dialin.md) or **comm/datamodem/dialout** in calls to [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) or [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig).</span></span> <span data-ttu-id="342bc-109">這可讓 Unimodem 維持與撥出設定無關的撥入設定。</span><span class="sxs-lookup"><span data-stu-id="342bc-109">This enables Unimodem to maintain a dial-in configuration independent of the dial-out configuration.</span></span>

<span data-ttu-id="342bc-110">當 Unimodem 在 Windows 2000 和更新版本上使用 **comm/datamodem/撥** 出時，其他 tsp 也可以在任何平臺上使用。</span><span class="sxs-lookup"><span data-stu-id="342bc-110">While **comm/datamodem/dialout** is used by Unimodem on Windows 2000 and later, it may also be used by other TSPs on any platform.</span></span> <span data-ttu-id="342bc-111">必須在所有平臺上執行的應用程式應該先在需要裝置類別的 API 呼叫中使用 **通訊/datamodem/撥** 出，而且如果 Api 傳回 **LINEERR \_ INVALCALLSTATE**，則只使用 [**通訊/datamodem**](comm-datamodem.md) 。</span><span class="sxs-lookup"><span data-stu-id="342bc-111">Applications that must run on all platforms should first use **comm/datamodem/dialout** in calls to API that require a device class and only use [**comm/datamodem**](comm-datamodem.md) if the API returns **LINEERR\_INVALCALLSTATE**.</span></span>

<span data-ttu-id="342bc-112">Unimodem 服務提供者會將 [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)和 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)呼叫中的 [**comm/datamodem**](comm-datamodem.md)裝置類別轉譯為 [**comm/datamodem/撥**](comm-datamodem-dialin.md)入或 **comm/datamodem/撥** 出，如下所示：</span><span class="sxs-lookup"><span data-stu-id="342bc-112">The Unimodem Service Provider translates the [**comm/datamodem**](comm-datamodem.md) device class in calls to [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) and [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) to either [**comm/datamodem/dialin**](comm-datamodem-dialin.md) or **comm/datamodem/dialout** as follows:</span></span>

-   <span data-ttu-id="342bc-113">Windows 2000 和更新版本：</span><span class="sxs-lookup"><span data-stu-id="342bc-113">Windows 2000 and later:</span></span>
    -   <span data-ttu-id="342bc-114">如果在呼叫 [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)的 *lpszDeviceClass* 參數中指定了 **Null** ，則會假設有 [**通訊/datamodem/撥**](comm-datamodem-dialin.md)入。</span><span class="sxs-lookup"><span data-stu-id="342bc-114">If **NULL** is specified in the *lpszDeviceClass* parameter in the call to [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem assumes [**comm/datamodem/dialin**](comm-datamodem-dialin.md).</span></span> <span data-ttu-id="342bc-115">如果在 **lineConfigDialog** 的呼叫中指定了 [**comm/datamodem**](comm-datamodem.md)或 [**tapi/line**](tapi-line.md) ，則 Unimodem 會將其轉譯為 **comm/datamodem/撥** 出。</span><span class="sxs-lookup"><span data-stu-id="342bc-115">If [**comm/datamodem**](comm-datamodem.md) or [**tapi/line**](tapi-line.md) is specified in the call to **lineConfigDialog**, Unimodem translates this to **comm/datamodem/dialout**.</span></span>
    -   <span data-ttu-id="342bc-116">在對 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) 或 [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)的呼叫中，會將 [**comm/datamodem**](comm-datamodem.md) 處理為 **comm/datamodem/撥** 出。</span><span class="sxs-lookup"><span data-stu-id="342bc-116">In the call to [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) or [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig), [**comm/datamodem**](comm-datamodem.md) is handled as **comm/datamodem/dialout**.</span></span> <span data-ttu-id="342bc-117">**Null** 表示不正確裝置類別。</span><span class="sxs-lookup"><span data-stu-id="342bc-117">**NULL** indicates an invalid device class.</span></span>
-   <span data-ttu-id="342bc-118">Windows 2000 之前：</span><span class="sxs-lookup"><span data-stu-id="342bc-118">Before Windows 2000:</span></span>
    -   <span data-ttu-id="342bc-119">如果在 [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)中指定了 **Null** 或 [**tapi/行**](tapi-line.md)，則會假設是 [**comm/datamodem**](comm-datamodem.md)。</span><span class="sxs-lookup"><span data-stu-id="342bc-119">If either **NULL** or [**tapi/line**](tapi-line.md) is specified in [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem assumes [**comm/datamodem**](comm-datamodem.md).</span></span>

<span data-ttu-id="342bc-120">**Comm/datamodem/撥** 出類別會使用 [**comm/datamodem**](comm-datamodem.md)裝置類別中所述的結構和設定。</span><span class="sxs-lookup"><span data-stu-id="342bc-120">The **comm/datamodem/dialout** class uses the structures and configurations described in the [**comm/datamodem**](comm-datamodem.md) device class.</span></span>

 

 



