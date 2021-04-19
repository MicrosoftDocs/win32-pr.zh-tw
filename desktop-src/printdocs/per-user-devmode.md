---
description: 使用者可以指定印表機的預設檔設定。 這稱為每一使用者的 DEVMODE，因為它只會影響特定使用者的預設值，而每個印表機的資訊會定義在不同的 DEVMODE 結構中。
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee5a79d314e0f9ab89210ba4d2644d2b8ec99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969347"
---
# <a name="per-user-devmode"></a><span data-ttu-id="222f2-104">Per-User DEVMODE</span><span class="sxs-lookup"><span data-stu-id="222f2-104">Per-User DEVMODE</span></span>

<span data-ttu-id="222f2-105">使用者可以指定印表機的預設檔設定。</span><span class="sxs-lookup"><span data-stu-id="222f2-105">A user can specify the default document settings for a printer.</span></span> <span data-ttu-id="222f2-106">這稱為每一 *使用者的 DEVMODE* ，因為它只會影響特定使用者的預設值，而每個印表機的資訊會定義在不同的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構中。</span><span class="sxs-lookup"><span data-stu-id="222f2-106">This is called the *per-user DEVMODE* because it only affects the defaults for a particular user, and the information for each printer is defined in a separate [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

<span data-ttu-id="222f2-107">若要設定每位使用者的 DEVMODE，請使用 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)或 [**印表機 \_ 資訊 \_ 9**](printer-info-9.md)結構來呼叫 [**SetPrinter**](setprinter.md) 。</span><span class="sxs-lookup"><span data-stu-id="222f2-107">To set the per-user DEVMODE, call [**SetPrinter**](setprinter.md) with either the [**PRINTER\_INFO\_2**](printer-info-2.md) or the [**PRINTER\_INFO\_9**](printer-info-9.md) structure.</span></span> <span data-ttu-id="222f2-108">若要將每位使用者的 DEVMODE 重設為全域預設的 [**devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)，請使用 [**印表機 \_ 資訊 \_ 8**](printer-info-8.md)結構來呼叫 **SetPrinter** 。</span><span class="sxs-lookup"><span data-stu-id="222f2-108">To reset the per-user DEVMODE to the global default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), call **SetPrinter** with the [**PRINTER\_INFO\_8**](printer-info-8.md) structure.</span></span>

 

 



