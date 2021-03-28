---
description: 下列功能可讓應用程式儲存、還原和重設裝置內容： SaveDC、RestoreDC 和 ResetDC。
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: 儲存、還原和重設裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973268"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a><span data-ttu-id="9fdcd-103">儲存、還原和重設裝置內容</span><span class="sxs-lookup"><span data-stu-id="9fdcd-103">Saving, Restoring, and Resetting a Device Context</span></span>

<span data-ttu-id="9fdcd-104">下列功能可讓應用程式儲存、還原和重設裝置內容： [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)、 [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)和 [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)。</span><span class="sxs-lookup"><span data-stu-id="9fdcd-104">The following functions enable an application to save, restore, and reset a device context: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc), and [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span></span> <span data-ttu-id="9fdcd-105">SaveDC 函式會在特殊的 GDI 堆疊上記錄目前的 DC 繪圖物件及其屬性和圖形模式。</span><span class="sxs-lookup"><span data-stu-id="9fdcd-105">The SaveDC function records on a special GDI stack the current DC's graphic objects and their attributes, and graphic modes.</span></span> <span data-ttu-id="9fdcd-106">繪圖應用程式可以在使用者開始繪圖之前呼叫這個函式，並儲存應用程式的原始狀態，為使用者提供乾淨的平板。</span><span class="sxs-lookup"><span data-stu-id="9fdcd-106">A drawing application can call this function before a user begins drawing and save the application's original state providing a clean slate for the user.</span></span> <span data-ttu-id="9fdcd-107">若要返回此原始狀態，應用程式會呼叫 RestoreDC 函數。</span><span class="sxs-lookup"><span data-stu-id="9fdcd-107">To return to this original state, the application calls the RestoreDC function.</span></span>

<span data-ttu-id="9fdcd-108">提供 [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)以重設印表機 DC 資料。</span><span class="sxs-lookup"><span data-stu-id="9fdcd-108">[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) is provided to reset printer DC data.</span></span> <span data-ttu-id="9fdcd-109">應用程式會呼叫此函式，以重設紙張方向、紙張大小、輸出縮放比例、要列印的份數、紙張來源 (或 bin) 、雙工模式等等。</span><span class="sxs-lookup"><span data-stu-id="9fdcd-109">An application calls this function to reset the paper orientation, paper size, output scaling factor, number of copies to be printed, paper source (or bin), duplex mode, and so on.</span></span> <span data-ttu-id="9fdcd-110">一般而言，應用程式會在使用者變更其中一個印表機選項，且系統已發出 [**WM \_ DEVMODECHANGE**](wm-devmodechange.md) 訊息之後，呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="9fdcd-110">Typically, an application calls this function after a user has changed one of the printer options and the system has issued a [**WM\_DEVMODECHANGE**](wm-devmodechange.md) message.</span></span>

 

 



