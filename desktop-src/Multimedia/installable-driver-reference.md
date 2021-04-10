---
title: 可安裝的驅動程式參考
description: 可安裝的驅動程式參考
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows 多媒體、可安裝的驅動程式參考
- 多媒體、可安裝的驅動程式參考
- 可安裝的驅動程式，參考
- 可安裝的驅動程式參考，關於
- 可安裝驅動程式的參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842144"
---
# <a name="installable-driver-reference"></a><span data-ttu-id="32f16-108">可安裝的驅動程式參考</span><span class="sxs-lookup"><span data-stu-id="32f16-108">Installable Driver Reference</span></span>

<span data-ttu-id="32f16-109">與可安裝的驅動程式相關聯的函式和訊息會依下列方式分組。</span><span class="sxs-lookup"><span data-stu-id="32f16-109">The functions and messages associated with installable drivers are grouped as follows.</span></span>

## <a name="loading-and-unloading-drivers"></a><span data-ttu-id="32f16-110">載入和卸載驅動程式</span><span class="sxs-lookup"><span data-stu-id="32f16-110">Loading and Unloading Drivers</span></span>

-   [<span data-ttu-id="32f16-111">GetDriverModuleHandle</span><span class="sxs-lookup"><span data-stu-id="32f16-111">GetDriverModuleHandle</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [<span data-ttu-id="32f16-112">OpenDriver</span><span class="sxs-lookup"><span data-stu-id="32f16-112">OpenDriver</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [<span data-ttu-id="32f16-113">SendDriverMessage</span><span class="sxs-lookup"><span data-stu-id="32f16-113">SendDriverMessage</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a><span data-ttu-id="32f16-114">CloseDriver</span><span class="sxs-lookup"><span data-stu-id="32f16-114">CloseDriver</span></span>

-   [<span data-ttu-id="32f16-115">**WINSPOOL.DRV \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="32f16-115">**DRV\_CLOSE**</span></span>](drv-close.md)
-   [<span data-ttu-id="32f16-116">**WINSPOOL.DRV \_ DISABLE**</span><span class="sxs-lookup"><span data-stu-id="32f16-116">**DRV\_DISABLE**</span></span>](drv-disable.md)
-   [<span data-ttu-id="32f16-117">**WINSPOOL.DRV \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="32f16-117">**DRV\_ENABLE**</span></span>](drv-enable.md)
-   [<span data-ttu-id="32f16-118">**\_免費 WINSPOOL.DRV**</span><span class="sxs-lookup"><span data-stu-id="32f16-118">**DRV\_FREE**</span></span>](drv-free.md)
-   [<span data-ttu-id="32f16-119">**WINSPOOL.DRV \_ 載入**</span><span class="sxs-lookup"><span data-stu-id="32f16-119">**DRV\_LOAD**</span></span>](drv-load.md)
-   [<span data-ttu-id="32f16-120">**WINSPOOL.DRV \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="32f16-120">**DRV\_OPEN**</span></span>](drv-open.md)

## <a name="configuring-a-driver"></a><span data-ttu-id="32f16-121">設定驅動程式</span><span class="sxs-lookup"><span data-stu-id="32f16-121">Configuring a Driver</span></span>

-   [<span data-ttu-id="32f16-122">**WINSPOOL.DRV \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="32f16-122">**DRV\_CONFIGURE**</span></span>](drv-configure.md)
-   [<span data-ttu-id="32f16-123">**WINSPOOL.DRV \_ QUERYCONFIGURE**</span><span class="sxs-lookup"><span data-stu-id="32f16-123">**DRV\_QUERYCONFIGURE**</span></span>](drv-queryconfigure.md)
-   [<span data-ttu-id="32f16-124">**DRVCONFIGINFO**</span><span class="sxs-lookup"><span data-stu-id="32f16-124">**DRVCONFIGINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a><span data-ttu-id="32f16-125">安裝驅動程式</span><span class="sxs-lookup"><span data-stu-id="32f16-125">Installing a Driver</span></span>

-   [<span data-ttu-id="32f16-126">**WINSPOOL.DRV \_ 安裝**</span><span class="sxs-lookup"><span data-stu-id="32f16-126">**DRV\_INSTALL**</span></span>](drv-install.md)
-   [<span data-ttu-id="32f16-127">**WINSPOOL.DRV \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="32f16-127">**DRV\_REMOVE**</span></span>](drv-remove.md)

## <a name="driver-functions"></a><span data-ttu-id="32f16-128">驅動程式函數</span><span class="sxs-lookup"><span data-stu-id="32f16-128">Driver Functions</span></span>

-   [<span data-ttu-id="32f16-129">DefDriverProc</span><span class="sxs-lookup"><span data-stu-id="32f16-129">DefDriverProc</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [<span data-ttu-id="32f16-130">DriverCallback</span><span class="sxs-lookup"><span data-stu-id="32f16-130">DriverCallback</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [<span data-ttu-id="32f16-131">DriverProc</span><span class="sxs-lookup"><span data-stu-id="32f16-131">DriverProc</span></span>](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a><span data-ttu-id="32f16-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="32f16-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32f16-133">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="32f16-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> </dl>

 

 