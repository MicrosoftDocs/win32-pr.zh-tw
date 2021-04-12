---
description: 就像應用程式需要顯示裝置內容 (DC) ，才能開始在視窗的工作區中繪製，需要有印表機 DC 才能開始將輸出傳送至印表機。
ms.assetid: 5bdcec28-e28d-402d-8d80-e8aa5ecb4e74
title: '印表機裝置內容 (檔和列印) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b75fb79d6ab8bb4198bf52bff10eccf5ec3cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193186"
---
# <a name="printer-device-contexts-documents-and-printing"></a><span data-ttu-id="6041c-103">印表機裝置內容 (檔和列印) </span><span class="sxs-lookup"><span data-stu-id="6041c-103">Printer Device Contexts (Documents and Printing)</span></span>

<span data-ttu-id="6041c-104">就像應用程式需要顯示裝置內容 (DC) ，才能開始在視窗的工作區中繪製，需要有印表機 DC 才能開始將輸出傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="6041c-104">Just as an application requires a display device context (DC) before it can begin drawing in the client area of a window, it needs a printer DC before it can begin sending output to a printer.</span></span> <span data-ttu-id="6041c-105">印表機 DC 與顯示 DC 類似，因為它是內部資料結構，它會定義一組繪圖物件和其相關聯的屬性，並指定影響輸出的圖形模式。</span><span class="sxs-lookup"><span data-stu-id="6041c-105">A printer DC is similar to a display DC in that it is an internal data structure that defines a set of graphic objects and their associated attributes and specifies the graphic modes that affect output.</span></span> <span data-ttu-id="6041c-106">繪圖物件包括線條繪圖的畫筆、繪製和填滿的筆刷，以及文字輸出的字型。</span><span class="sxs-lookup"><span data-stu-id="6041c-106">The graphic objects include a pen for line drawing, a brush for painting and filling, and a font for text output.</span></span>

<span data-ttu-id="6041c-107">與顯示 DC 不同的是，印表機 DC 並非由 window 管理元件所擁有，而且無法藉由呼叫 [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) 函式取得。</span><span class="sxs-lookup"><span data-stu-id="6041c-107">Unlike a display DC, a printer DC is not owned by the window management component, and it cannot be obtained by calling the [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) function.</span></span> <span data-ttu-id="6041c-108">相反地，應用程式必須呼叫 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) 或 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函數。</span><span class="sxs-lookup"><span data-stu-id="6041c-108">Instead, an application must call the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) or [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function.</span></span>

<span data-ttu-id="6041c-109">如果您的應用程式呼叫 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) 函式，它必須提供驅動程式和埠名稱。</span><span class="sxs-lookup"><span data-stu-id="6041c-109">If your application calls the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function, it must supply a driver and port name.</span></span> <span data-ttu-id="6041c-110">若要取得這些名稱，請呼叫 [**GetPrinter**](getprinter.md) 或 [**>enumprinters**](enumprinters.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="6041c-110">To retrieve these names, call the [**GetPrinter**](getprinter.md) or [**EnumPrinters**](enumprinters.md) function.</span></span>

<span data-ttu-id="6041c-111">如果您的應用程式呼叫 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))函式，並 \_ 在 [**PrintDlgEx**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)結構的 **旗標** 成員中指定 PD RETURNDC 值，系統會針對使用者選取的印表機傳回裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="6041c-111">If your application calls the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function and specifies the PD\_RETURNDC value in the **Flags** member of the [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) structure, the system returns a handle to a device context for the printer selected by the user.</span></span> <span data-ttu-id="6041c-112">如需詳細資訊，請參閱[使用通用對話方塊](../dlgbox/using-common-dialog-boxes.md)中的[列印屬性工作表](../dlgbox/print-property-sheet.md)和「使用列印屬性工作表」。</span><span class="sxs-lookup"><span data-stu-id="6041c-112">For more information, see [Print Property Sheet](../dlgbox/print-property-sheet.md) and "Using the Print Property Sheet" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

 

 
