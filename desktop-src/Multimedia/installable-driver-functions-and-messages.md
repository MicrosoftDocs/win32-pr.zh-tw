---
title: 可安裝的驅動程式功能和訊息
description: 可安裝的驅動程式功能和訊息
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- 可安裝的驅動程式，函式
- 可安裝的驅動程式，訊息
- 可安裝的驅動程式，OpenDriver 函式
- OpenDriver 函式
- 可安裝的驅動程式、自訂訊息
- 驅動程式訊息
- 自訂驅動程式訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66e6ebaac73bf8eb779119750cb390481152c3f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933199"
---
# <a name="installable-driver-functions-and-messages"></a><span data-ttu-id="d7e61-110">可安裝的驅動程式功能和訊息</span><span class="sxs-lookup"><span data-stu-id="d7e61-110">Installable Driver Functions and Messages</span></span>

<span data-ttu-id="d7e61-111">您可以使用 [**OpenDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) 函數，從應用程式開啟可安裝的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d7e61-111">You can open an installable driver from an application by using the [**OpenDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) function.</span></span> <span data-ttu-id="d7e61-112">此函式會建立驅動程式的實例，如果沒有其他實例存在，則將驅動程式載入記憶體，並傳回新實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7e61-112">This function creates an instance of the driver, loading the driver into memory if no other instance exists, and returns the handle of the new instance.</span></span> <span data-ttu-id="d7e61-113">開啟可安裝的驅動程式時，您必須提供驅動程式的完整路徑，或登錄機碼的名稱和與驅動程式相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="d7e61-113">When opening an installable driver, you must supply either the full path of the driver or the names of the registry key and value associated with the driver.</span></span>

<span data-ttu-id="d7e61-114">開啟驅動程式之後，您可以使用 [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) 函式將驅動程式訊息傳送至驅動程式，指示它執行工作。</span><span class="sxs-lookup"><span data-stu-id="d7e61-114">Once a driver is open, you can direct it to carry out tasks by using the [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) function to send driver messages to the driver.</span></span> <span data-ttu-id="d7e61-115">例如，您可以藉由傳送 [**Winspool.drv \_ 設定**](drv-configure.md) 訊息，指示驅動程式顯示其設定對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d7e61-115">For example, you can direct the driver to display its configuration dialog box by sending the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="d7e61-116">傳送此訊息之前，您必須藉由傳送 [**Winspool.drv \_ QUERYCONFIGURE**](drv-queryconfigure.md) 訊息並檢查非零的傳回值，判斷驅動程式是否有設定對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d7e61-116">Before sending this message, you must determine whether the driver has a configuration dialog box by sending the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message and checking for a nonzero return value.</span></span> <span data-ttu-id="d7e61-117">許多驅動程式都會提供一組自訂訊息，您可以傳送這些訊息來指示驅動程式的作業。</span><span class="sxs-lookup"><span data-stu-id="d7e61-117">Many drivers provide a set of custom messages that you can send to direct the operations of the driver.</span></span>

<span data-ttu-id="d7e61-118">如果您需要可安裝驅動程式的特殊存取權（例如存取其資源），您可以使用 [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) 函式來取出驅動程式的模組控制碼。</span><span class="sxs-lookup"><span data-stu-id="d7e61-118">If you need special access to an installable driver, such as access to its resources, you can retrieve the module handle of the driver by using the [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) function.</span></span>

<span data-ttu-id="d7e61-119">當您不再需要可安裝的驅動程式時，您可以使用 [**CloseDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) 函式將其關閉。</span><span class="sxs-lookup"><span data-stu-id="d7e61-119">When you no longer need the installable driver, you can close it by using the [**CloseDriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) function.</span></span>

<span data-ttu-id="d7e61-120">您可以使用可安裝的驅動程式功能和訊息來開啟和管理任何可安裝的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d7e61-120">You can use the installable driver functions and messages to open and manage any installable driver.</span></span> <span data-ttu-id="d7e61-121">不過，開啟和管理多媒體裝置的建議動作是先使用標準服務 (例如，波形輸出裝置) 的 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)、 [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)和 [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d7e61-121">However, the recommended course of action for opening and managing multimedia devices is to first use standard services (such as [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage), and [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) for waveform output devices), if they exist.</span></span> <span data-ttu-id="d7e61-122">如果多媒體驅動程式沒有標準服務存在，請使用可安裝的驅動程式功能和訊息來開啟和管理驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d7e61-122">If standard services do not exist for a multimedia driver, then open and manage the driver using the installable driver functions and messages.</span></span>

> [!Note]  
> <span data-ttu-id="d7e61-123">[**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)和 [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)函數是用來將訊息傳送至驅動程式，以及取得模組實例控制碼的慣用函數。</span><span class="sxs-lookup"><span data-stu-id="d7e61-123">The [**SendDriverMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) and [**GetDriverModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) functions are the preferred functions to use to send messages to a driver and to obtain a handle to a module instance.</span></span> <span data-ttu-id="d7e61-124">不過，已包含舊版的 [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) 函式，以維持與舊版 Windows 作業系統的相容性。</span><span class="sxs-lookup"><span data-stu-id="d7e61-124">The older [**DrvGetModuleHandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) function, however, has been included to maintain compatibility with previous versions of the Windows operating system.</span></span>

 

 

 