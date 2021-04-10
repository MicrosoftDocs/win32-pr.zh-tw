---
description: 使用主控描繪功能表來支援 Tablet PC 的語音功能。
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: 使用 Owner-Drawn 功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690312"
---
# <a name="using-owner-drawn-menus"></a><span data-ttu-id="d8fde-103">使用 Owner-Drawn 功能表</span><span class="sxs-lookup"><span data-stu-id="d8fde-103">Using Owner-Drawn Menus</span></span>

<span data-ttu-id="d8fde-104">使用主控描繪功能表時，您必須讓功能表名稱可支援語音功能。</span><span class="sxs-lookup"><span data-stu-id="d8fde-104">When using owner-drawn menus, you must make the menu names available to support speech functionality.</span></span> <span data-ttu-id="d8fde-105">作法有二：</span><span class="sxs-lookup"><span data-stu-id="d8fde-105">There are two ways to do this:</span></span>

-   <span data-ttu-id="d8fde-106">使用 MSAAMENUINFO 結構來公開功能表項目名稱。</span><span class="sxs-lookup"><span data-stu-id="d8fde-106">Expose the menu item name by using the MSAAMENUINFO structure.</span></span>
-   <span data-ttu-id="d8fde-107">提供選項，以在協助工具協助工具啟用時，使用標準文字功能表來取代圖形功能表。</span><span class="sxs-lookup"><span data-stu-id="d8fde-107">Provide an option to replace graphic menus with standard text menus when an accessibility aid is active.</span></span> <span data-ttu-id="d8fde-108">如果 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式傳回 **TRUE** ，並將其 *uiAction* 參數設定為 SPI \_ GETSCREENREADER，請使用標準功能表。應用程式應該監看是否有 WM \_ SETTINGSCHANGE 訊息，並藉由查詢此選項的狀態並適當地調整其顯示來回應。</span><span class="sxs-lookup"><span data-stu-id="d8fde-108">If the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function returns **TRUE** with its *uiAction* parameter set to SPI\_GETSCREENREADER, use standard menus.The application should watch for the WM\_SETTINGSCHANGE message and respond by querying the state of this option and adjusting its display appropriately.</span></span> <span data-ttu-id="d8fde-109">例如，Microsoft Visual Studio 提供選項來使用標準功能表，而不是預設顯示的自訂功能表。</span><span class="sxs-lookup"><span data-stu-id="d8fde-109">For example, Microsoft Visual Studio provides an option to use standard menus instead of the custom menus that are displayed by default.</span></span>

 

 
