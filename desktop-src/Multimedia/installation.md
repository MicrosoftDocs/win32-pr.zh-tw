---
title: '安裝 (Windows 多媒體) '
description: 安裝
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- 可安裝的驅動程式，安裝
- 可安裝的驅動程式，DRV_INSTALL 訊息
- 可安裝的驅動程式，DRV_REMOVE 訊息
- DRV_INSTALL 訊息
- DRV_REMOVE 訊息
- DRVCONFIGINFO 訊息
- 安裝驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ebebd090c7499698c59c325d1ac0d487902454
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383633"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="2c602-110">安裝 (Windows 多媒體) </span><span class="sxs-lookup"><span data-stu-id="2c602-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="2c602-111">可安裝的驅動程式可以在處理 [**Winspool.drv \_ 安裝**](drv-install.md) 和 [**winspool.drv \_ 移除**](drv-remove.md) 訊息時，執行驅動程式特定的安裝工作。</span><span class="sxs-lookup"><span data-stu-id="2c602-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="2c602-112">安裝或移除驅動程式時，安裝應用程式（例如主控台應用程式）會將訊息傳送至驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2c602-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="2c602-113">處理 WINSPOOL.DRV \_ 安裝訊息時，驅動程式通常會確認所需的硬體存在，然後顯示 [設定] 對話方塊，讓使用者選擇驅動程式和相關聯硬體的初始設定。</span><span class="sxs-lookup"><span data-stu-id="2c602-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="2c602-114">訊息包含 [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) 結構的位址，其中包含與驅動程式相關聯的登錄機碼和值的名稱。驅動程式會檢查登錄值以取得預設的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="2c602-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="2c602-115">最後，驅動程式也會建立成功操作所需的任何其他登錄機碼和值。</span><span class="sxs-lookup"><span data-stu-id="2c602-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="2c602-116">處理 WINSPOOL.DRV \_ 移除訊息時，驅動程式會移除任何可能已建立的登錄機碼和值。</span><span class="sxs-lookup"><span data-stu-id="2c602-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
