---
description: 最後一個步驟是在假設的 >mysetup.bat 網頁上放置 Setup.exe 的參考， (MySetup.html) 以 URL 為基礎 Windows Installer 安裝範例中所述。
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: 建立 Setup.exe 的 HTML 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193113"
---
# <a name="establish-an-html-reference-to-setupexe"></a><span data-ttu-id="5c7a3-103">建立 Setup.exe 的 HTML 參考</span><span class="sxs-lookup"><span data-stu-id="5c7a3-103">Establish an HTML Reference to Setup.exe</span></span>

<span data-ttu-id="5c7a3-104">最後一個步驟是在假設的 >mysetup.bat 網頁上放置 Setup.exe 的參考， (MySetup.html) 以 [URL 為基礎 Windows Installer 安裝範例](a-url-based-windows-installer-installation-example.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="5c7a3-104">The final step is to place a reference to the Setup.exe on the hypothetical MySetup webpage (MySetup.html) described in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span> <span data-ttu-id="5c7a3-105">使用下列 HTML 腳本：</span><span class="sxs-lookup"><span data-stu-id="5c7a3-105">Use the following HTML script:</span></span>

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

<span data-ttu-id="5c7a3-106">按一下 [>mysetup.bat 安裝] 連結，可為使用者提供從該位置儲存或執行的選項。</span><span class="sxs-lookup"><span data-stu-id="5c7a3-106">Clicking on the "MySetup Installation" link presents users with the option to save or run from that location.</span></span> <span data-ttu-id="5c7a3-107">如果使用者從該位置選取 [執行]，Setup.exe 會在電腦上升級 Windows Installer 的版本（如有必要），以驗證安裝程式套件上的數位簽章，並在其電腦上安裝套件。</span><span class="sxs-lookup"><span data-stu-id="5c7a3-107">If the user selects run from that location, the Setup.exe upgrades the version of Windows Installer on the computer, if necessary, verifies the digital signature on the installer package, and installs the package on their computer.</span></span>

<span data-ttu-id="5c7a3-108">這會完成範例。</span><span class="sxs-lookup"><span data-stu-id="5c7a3-108">This completes the example.</span></span>

 

 



