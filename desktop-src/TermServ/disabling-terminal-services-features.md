---
title: 停用遠端桌面服務功能
description: 為了加強安全性，您可以選擇停用遠端桌面服務功能。
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/01/2020
ms.locfileid: "103933795"
---
# <a name="disabling-remote-desktop-services-features"></a><span data-ttu-id="0a9a1-103">停用遠端桌面服務功能</span><span class="sxs-lookup"><span data-stu-id="0a9a1-103">Disabling Remote Desktop Services features</span></span>

<span data-ttu-id="0a9a1-104">為了加強安全性，您可以選擇停用遠端桌面服務功能，例如使用遠端桌面 ActiveX 控制項連接至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器之用戶端的「剪貼簿重新導向」和「印表機重新導向」。</span><span class="sxs-lookup"><span data-stu-id="0a9a1-104">For enhanced security, you might choose to disable Remote Desktop Services features such as clipboard redirection and printer redirection for clients that connect to Remote Desktop Session Host (RD Session Host) servers using the Remote Desktop ActiveX Control.</span></span>

<span data-ttu-id="0a9a1-105">**停用遠端桌面服務功能**</span><span class="sxs-lookup"><span data-stu-id="0a9a1-105">**To disable Remote Desktop Services features**</span></span>

1.  <span data-ttu-id="0a9a1-106">編輯用戶端電腦的登錄，並新增下列機碼：</span><span class="sxs-lookup"><span data-stu-id="0a9a1-106">Edit the registry of the client computer and add the following keys:</span></span>

    -   <span data-ttu-id="0a9a1-107">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 終端機伺服器 \\ DisableClipboardRedirection**</span><span class="sxs-lookup"><span data-stu-id="0a9a1-107">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableClipboardRedirection**</span></span>
    -   <span data-ttu-id="0a9a1-108">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 終端機伺服器 \\ DisableDriveRedirection**</span><span class="sxs-lookup"><span data-stu-id="0a9a1-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableDriveRedirection**</span></span>
    -   <span data-ttu-id="0a9a1-109">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 終端機伺服器 \\ DisablePrinterRedirection**</span><span class="sxs-lookup"><span data-stu-id="0a9a1-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisablePrinterRedirection**</span></span>

2.  <span data-ttu-id="0a9a1-110">將兩個索引鍵的值設定為 **REG \_ DWORD** 1。</span><span class="sxs-lookup"><span data-stu-id="0a9a1-110">Set the value of both keys to **REG\_DWORD** 1.</span></span>

 

 




