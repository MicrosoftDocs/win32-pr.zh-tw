---
title: 'Configuration (Windows 多媒體) '
description: 組態
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- 可安裝的驅動程式，設定
- 可安裝的驅動程式，DRV_CONFIGURE 訊息
- DRV_CONFIGURE 訊息
- DRV_QUERYCONFIGURE 訊息
- DRVCONFIGINFO 訊息
- 設定可安裝的驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a248f992a857b88b723bd54c771f1af5709d97
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024450"
---
# <a name="configuration-windows-multimedia"></a><span data-ttu-id="bd247-109">Configuration (Windows 多媒體) </span><span class="sxs-lookup"><span data-stu-id="bd247-109">Configuration (Windows Multimedia)</span></span>

<span data-ttu-id="bd247-110">可安裝的驅動程式可讓使用者在處理 [**Winspool.drv \_ 設定**](drv-configure.md) 訊息時顯示設定對話方塊，以選擇驅動程式和相關聯硬體的設定。</span><span class="sxs-lookup"><span data-stu-id="bd247-110">An installable driver can let users choose configuration settings for the driver and associated hardware by displaying a configuration dialog box when processing the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="bd247-111">驅動程式負責建立及管理對話方塊、處理對話方塊中的任何使用者輸入，以及變更使用者要求的驅動程式或硬體設定。</span><span class="sxs-lookup"><span data-stu-id="bd247-111">The driver is responsible for creating and managing the dialog box, processing any user input from the dialog box, and changing the configuration of the driver or hardware as requested by the user.</span></span> <span data-ttu-id="bd247-112">驅動程式必須提供個別的對話方塊程式來處理對話方塊的視窗訊息，以及一個對話方塊範本來定義對話方塊的外觀和內容。</span><span class="sxs-lookup"><span data-stu-id="bd247-112">The driver must provide a separate dialog box procedure to process window messages for the dialog box and a dialog box template to define the appearance and content of the dialog box.</span></span>

<span data-ttu-id="bd247-113">接收 WINSPOOL.DRV \_ 設定訊息之前，驅動程式會收到 [**winspool.drv \_ QUERYCONFIGURE**](drv-queryconfigure.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="bd247-113">Before receiving the DRV\_CONFIGURE message, a driver receives the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message.</span></span> <span data-ttu-id="bd247-114">驅動程式必須傳回非零值給查詢，以確保收到後續 WINSPOOL.DRV \_ 設定訊息。</span><span class="sxs-lookup"><span data-stu-id="bd247-114">The driver must return a nonzero value to the query to ensure receipt of the subsequent DRV\_CONFIGURE message.</span></span>

<span data-ttu-id="bd247-115">初始化設定對話方塊時，驅動程式通常會從登錄中抓取設定資訊。</span><span class="sxs-lookup"><span data-stu-id="bd247-115">When initializing the configuration dialog box, the driver typically retrieves configuration information from the registry.</span></span> <span data-ttu-id="bd247-116">為了協助找出這項資訊，WINSPOOL.DRV \_ 設定訊息通常會包含 [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) 結構的位址，其中包含與驅動程式相關聯的登錄機碼和值的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd247-116">To help locate this information, the DRV\_CONFIGURE message usually includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver.</span></span> <span data-ttu-id="bd247-117">如果使用者要求變更設定，驅動程式應該會更新登錄中的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="bd247-117">If the user requests changes to the configuration, the driver should update the configuration information in the registry.</span></span>

 

 
