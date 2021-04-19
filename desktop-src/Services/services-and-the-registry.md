---
description: 服務不應該存取 HKEY \_ CURRENT \_ USER 或 HKEY \_ 類別 \_ ROOT，尤其是在模擬使用者時。 請改用 RegOpenCurrentUser 或 RegOpenUserClassesRoot 函數。
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: 服務和登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994507"
---
# <a name="services-and-the-registry"></a><span data-ttu-id="85214-104">服務和登錄</span><span class="sxs-lookup"><span data-stu-id="85214-104">Services and the Registry</span></span>

<span data-ttu-id="85214-105">服務不應該存取 **HKEY \_ CURRENT \_ user** 或 **HKEY \_ 類別 \_ ROOT**，尤其是在模擬使用者時。</span><span class="sxs-lookup"><span data-stu-id="85214-105">A service should not access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT**, especially when impersonating a user.</span></span> <span data-ttu-id="85214-106">請改用 [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) 或 [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) 函數。</span><span class="sxs-lookup"><span data-stu-id="85214-106">Instead, use the [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) or [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) function.</span></span>

<span data-ttu-id="85214-107">如果您嘗試從服務存取 **HKEY \_ CURRENT \_ USER** 或 **HKEY \_ 類別 \_ ROOT** ，它可能會失敗，或似乎運作正常，但有可能導致載入或卸載使用者設定檔時發生問題的根本洩漏。</span><span class="sxs-lookup"><span data-stu-id="85214-107">If you attempt to access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT** from a service it may fail, or it may appear to work but there is an underlying leak that can lead to problems loading or unloading the user profile.</span></span>

 

 
