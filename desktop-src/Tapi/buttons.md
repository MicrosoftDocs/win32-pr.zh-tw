---
description: Microsoft 電話語音會將電話按鈕和燈模型為按鈕的燈配對。
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: " (電話語音 API) 的按鈕"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993058"
---
# <a name="buttons-telephony-api"></a><span data-ttu-id="b04a3-103"> (電話語音 API) 的按鈕</span><span class="sxs-lookup"><span data-stu-id="b04a3-103">Buttons (Telephony API)</span></span>

<span data-ttu-id="b04a3-104">Microsoft 電話語音會將電話的按鈕和燈模型為按鈕的燈配對。</span><span class="sxs-lookup"><span data-stu-id="b04a3-104">Microsoft Telephony models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="b04a3-105">旁邊沒有燈泡的按鈕，或使用遺失燈或按鈕的虛擬指標來指定沒有按鈕的燈。</span><span class="sxs-lookup"><span data-stu-id="b04a3-105">A button with no lamp next to it, or a lamp with no button is specified using a dummy indicator for the missing lamp or button.</span></span> <span data-ttu-id="b04a3-106">具有多個燈的按鈕會使用多個按鈕的燈配對來建立模型。</span><span class="sxs-lookup"><span data-stu-id="b04a3-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="b04a3-107">您可以設定和取出與電話按鈕相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="b04a3-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="b04a3-108">按下按鈕時，服務提供者會將 [**電話 \_ 按鈕**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) 訊息傳送至 TAPI 回呼函式。</span><span class="sxs-lookup"><span data-stu-id="b04a3-108">When a button is pressed, the service provider sends a [**PHONE\_BUTTON**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) message to the TAPI callback function.</span></span> <span data-ttu-id="b04a3-109">此訊息的參數是手機裝置的控制碼，以及按下按鈕的按鈕/燈泡識別碼。</span><span class="sxs-lookup"><span data-stu-id="b04a3-109">Parameters of this message are a handle to the phone device and the button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="b04a3-110">鍵盤按鍵 ' 0 ' 到 ' 9 '、' \* ' 和 ' \# ' 是指派固定的按鈕/燈泡識別碼0到11。</span><span class="sxs-lookup"><span data-stu-id="b04a3-110">The keypad button '0' through '9', '\*', and '\#' are assigned fixed button/lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="b04a3-111">函式 [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) 會設定與手機裝置上的按鈕相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="b04a3-111">The function [**TSPI\_phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="b04a3-112">[**TSPI \_ phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) 會傳回與手機裝置上按鈕相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="b04a3-112">[**TSPI\_phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) returns information associated with a button on a phone device.</span></span> <span data-ttu-id="b04a3-113">\_當按下電話上的按鈕時，服務提供者會將電話按鈕訊息傳送至 TAPI 回呼函式。</span><span class="sxs-lookup"><span data-stu-id="b04a3-113">The service provider sends a PHONE\_BUTTON message to the TAPI callback function when a button on the phone is pressed.</span></span>

<span data-ttu-id="b04a3-114">與按鈕相關聯的資訊在 TSPI 時並不會包含任何語義意義。</span><span class="sxs-lookup"><span data-stu-id="b04a3-114">The information associated with a button does not carry any semantic meaning as far as TSPI is concerned.</span></span> <span data-ttu-id="b04a3-115">它適用于針對指定的電話裝置解讀這項資訊的裝置特定應用程式，或向使用者顯示（例如在應用程式的說明系統中）。</span><span class="sxs-lookup"><span data-stu-id="b04a3-115">It is useful for device-specific applications that interpret this information for a given phone device, or for display to the user, such as in an application's help system.</span></span>

 

 
