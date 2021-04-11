---
description: TAPI 會將電話按鈕和燈模型為按鈕的燈配對。
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: 電話按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692232"
---
# <a name="phone-buttons"></a><span data-ttu-id="7f2dd-103">電話按鈕</span><span class="sxs-lookup"><span data-stu-id="7f2dd-103">Phone Buttons</span></span>

<span data-ttu-id="7f2dd-104">TAPI 將電話的按鈕和燈模型為按鈕的燈配對。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-104">TAPI models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="7f2dd-105">它旁邊沒有燈的按鈕或沒有按鈕的燈泡，會使用「虛擬」指標來指定遺漏的燈泡或按鈕。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-105">A button with no lamp next to it or a lamp with no button is specified using a "dummy" indicator for the missing lamp or button.</span></span> <span data-ttu-id="7f2dd-106">具有多個燈的按鈕會使用多個按鈕的燈配對來建立模型。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="7f2dd-107">您可以設定和取出與電話按鈕相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="7f2dd-108">按下按鈕時，會將 [**電話 \_ 按鈕**](phone-button.md) 訊息傳送至應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-108">When a button is pressed, a [**PHONE\_BUTTON**](phone-button.md) message is sent to the application function.</span></span> <span data-ttu-id="7f2dd-109">此訊息的參數是手機裝置的控制碼，以及按下按鈕的按鈕燈泡識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-109">The parameters of this message are a handle to the phone device and the button-lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="7f2dd-110">鍵盤按鈕 ' 0 ' 到 ' 9 '、' \* ' 和 ' \# ' 都會被指派固定的按鈕-燈泡識別碼0到11。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-110">The keypad buttons '0' through '9', '\*', and '\#' are assigned the fixed button-lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="7f2dd-111">與按鈕相關聯的函式為 [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo)，可設定與手機裝置上的按鈕相關聯的資訊，以及 [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)，這會傳回與手機裝置上按鈕相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-111">The functions associated with buttons are [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), which sets the information associated with a button on a phone device, and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), which returns information associated with a button on a phone device.</span></span> <span data-ttu-id="7f2dd-112">\_當按下電話上的按鈕時，會將電話按鈕訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-112">The PHONE\_BUTTON message is sent to an application when a button on the phone is pressed.</span></span>

<span data-ttu-id="7f2dd-113">與按鈕相關聯的資訊在 TAPI 方面並沒有任何語義意義。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-113">The information associated with a button does not carry any semantic meaning as far as TAPI is concerned.</span></span> <span data-ttu-id="7f2dd-114">它適用于瞭解特定電話裝置的這項資訊意義，或向使用者顯示（例如線上說明）的裝置專屬應用程式。</span><span class="sxs-lookup"><span data-stu-id="7f2dd-114">It is useful for device-specific applications that understand the meaning of this information for a given phone device, or for display to the user, such as online help.</span></span>

 

 



