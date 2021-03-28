---
description: 印表機 DC 可以在使用點矩陣印表機、噴墨印表機、雷射印表機或繪圖器列印時使用。
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: " (Windows GDI) 的印表機裝置內容"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972565"
---
# <a name="printer-device-contexts-windows-gdi"></a><span data-ttu-id="f82f3-103"> (Windows GDI) 的印表機裝置內容</span><span class="sxs-lookup"><span data-stu-id="f82f3-103">Printer Device Contexts (Windows GDI)</span></span>

<span data-ttu-id="f82f3-104">印表機 DC 可以在使用點矩陣印表機、噴墨印表機、雷射印表機或繪圖器列印時使用。</span><span class="sxs-lookup"><span data-stu-id="f82f3-104">The printer DC can be used when printing on a dot-matrix printer, ink-jet printer, laser printer, or plotter.</span></span> <span data-ttu-id="f82f3-105">應用程式會藉由呼叫 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 函式，並提供適當的引數 (印表機驅動程式的名稱、印表機的名稱、實體輸出媒體的檔案或裝置名稱，以及其他初始化資料) 來建立印表機 DC。</span><span class="sxs-lookup"><span data-stu-id="f82f3-105">An application creates a printer DC by calling the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function and supplying the appropriate arguments (the name of the printer driver, the name of the printer, the file or device name for the physical output medium, and other initialization data).</span></span> <span data-ttu-id="f82f3-106">當應用程式完成列印時，它會藉由呼叫 [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) 函式來刪除印表機 DC。</span><span class="sxs-lookup"><span data-stu-id="f82f3-106">When an application has finished printing, it deletes the printer DC by calling the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span> <span data-ttu-id="f82f3-107">應用程式必須刪除 (而不是) 印表機 DC 中的版本;當應用程式嘗試使用它來釋放印表機 DC 時， [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式會失敗。</span><span class="sxs-lookup"><span data-stu-id="f82f3-107">An application must delete (rather than release) a printer DC; the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function fails when an application attempts to use it to release a printer DC.</span></span>

<span data-ttu-id="f82f3-108">如需詳細資訊，請參閱 [印表機輸出](../printdocs/printer-output.md)。</span><span class="sxs-lookup"><span data-stu-id="f82f3-108">For more information, see [Printer Output](../printdocs/printer-output.md).</span></span>

 

 
