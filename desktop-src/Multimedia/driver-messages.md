---
title: 驅動程式訊息
description: 驅動程式訊息
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- 可安裝的驅動程式，訊息
- 可安裝的驅動程式、自訂訊息
- 驅動程式訊息
- 自訂驅動程式訊息
- 可安裝的驅動程式，DriverProc 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023340"
---
# <a name="driver-messages"></a><span data-ttu-id="6d6ef-108">驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="6d6ef-108">Driver Messages</span></span>

<span data-ttu-id="6d6ef-109">每個驅動程式訊息都是由訊息識別碼和 2 32 位參數所組成。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-109">Each driver message consists of a message identifier and two 32-bit parameters.</span></span> <span data-ttu-id="6d6ef-110">訊息識別碼是 [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) 函式所檢查的唯一值，可決定要執行的動作。訊息參數的意義取決於訊息。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-110">The message identifier is a unique value that the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function checks to determine which action to carry out. The meaning of the message parameters depends on the message.</span></span> <span data-ttu-id="6d6ef-111">這些參數可以代表值或位址。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-111">The parameters may represent values or addresses.</span></span> <span data-ttu-id="6d6ef-112">在許多情況下，不會使用參數，而且會設定為零。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-112">In many cases, the parameters are not used and are set to zero.</span></span>

<span data-ttu-id="6d6ef-113">驅動程式訊息可以是標準或自訂的。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-113">Driver messages can be standard or custom.</span></span> <span data-ttu-id="6d6ef-114">Windows 會將標準驅動程式訊息（例如 [**Winspool.drv \_ OPEN**](drv-open.md)、 [**Winspool.drv \_ CLOSE**](drv-close.md)和 [**winspool.drv \_ 設定**](drv-configure.md)）傳送至可安裝的驅動程式，以回應開啟、關閉或設定驅動程式的要求。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-114">Windows sends standard driver messages, such as [**DRV\_OPEN**](drv-open.md), [**DRV\_CLOSE**](drv-close.md), and [**DRV\_CONFIGURE**](drv-configure.md), to an installable driver in response to a request to open, close, or configure the driver.</span></span> <span data-ttu-id="6d6ef-115">標準訊息會指示可安裝的驅動程式載入或卸載其資源、啟用或停用其作業、開啟或關閉驅動程式實例，以及顯示設定對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-115">The standard messages direct the installable driver to load or unload its resources, enable or disable its operation, open or close a driver instance, and display a configuration dialog box.</span></span> <span data-ttu-id="6d6ef-116">某些標準訊息（例如 [**Winspool.drv \_ 電源**](drv-power.md) 和 [**winspool.drv \_ EXITSESSION**](drv-exitsession.md)）會將影響驅動程式或任何相關硬體操作的全系統事件通知驅動程式。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-116">Some standard messages, such as [**DRV\_POWER**](drv-power.md) and [**DRV\_EXITSESSION**](drv-exitsession.md), notify the driver of system-wide events that affect the operation of the driver or any related hardware.</span></span>

<span data-ttu-id="6d6ef-117">應用程式和 Dll 會傳送自訂驅動程式訊息，以導向可安裝的驅動程式，以執行驅動程式特定的動作。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-117">Applications and DLLs send custom driver messages to direct an installable driver to carry out driver-specific actions.</span></span> <span data-ttu-id="6d6ef-118">支援自訂訊息的可安裝驅動程式必須在 **DriverProc** 函式中包含適當的處理。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-118">Installable drivers that support custom messages must include appropriate processing in the **DriverProc** function.</span></span> <span data-ttu-id="6d6ef-119">為了避免自訂和標準驅動程式訊息之間的衝突，自訂訊息識別碼必須具有範圍從 WINSPOOL.DRV \_ 保留到 Winspool.drv 使用者的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-119">To prevent conflict between custom and standard driver messages, custom message identifiers must have values ranging from DRV\_RESERVED to DRV\_USER.</span></span> <span data-ttu-id="6d6ef-120">傳遞至 [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) 函數的自訂訊息會被忽略。</span><span class="sxs-lookup"><span data-stu-id="6d6ef-120">Custom messages passed to the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function are ignored.</span></span>

 

 