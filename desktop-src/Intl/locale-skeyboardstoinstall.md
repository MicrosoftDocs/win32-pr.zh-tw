---
description: 地區設定 \_ SKEYBOARDSTOINSTALL
ms.assetid: 67bb616f-319b-42ab-969e-009258ec458d
title: LOCALE_SKEYBOARDSTOINSTALL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f7983b05b0dc043a2fcef58eeb4003ec1182f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997960"
---
# <a name="locale_skeyboardstoinstall"></a><span data-ttu-id="7f088-103">地區設定 \_ SKEYBOARDSTOINSTALL</span><span class="sxs-lookup"><span data-stu-id="7f088-103">LOCALE\_SKEYBOARDSTOINSTALL</span></span>

<span data-ttu-id="7f088-104">**Windows Vista 和更新版本：** 以分號分隔的鍵盤清單，可能會針對地區設定進行安裝，並由 Windows 在內部使用。</span><span class="sxs-lookup"><span data-stu-id="7f088-104">**Windows Vista and later:** A semicolon-delimited list of keyboards to potentially install for the locale and to be used internally by Windows.</span></span> <span data-ttu-id="7f088-105">此字串允許的字元數沒有限制。</span><span class="sxs-lookup"><span data-stu-id="7f088-105">There is no limit on the number of characters allowed for this string.</span></span> <span data-ttu-id="7f088-106">若要取得使用中輸入地區設定識別碼的名稱 (先前稱為鍵盤配置) ，您的應用程式可以呼叫 [**GetKeyboardLayoutName**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea) 函數。</span><span class="sxs-lookup"><span data-stu-id="7f088-106">To retrieve the name of the active input locale identifier (formerly called the keyboard layout), your application can call the [**GetKeyboardLayoutName**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea) function.</span></span>

 

 
