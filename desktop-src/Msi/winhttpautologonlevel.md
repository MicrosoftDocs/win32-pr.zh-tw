---
description: 自動登入 (自動登入) 原則會決定 WinHTTP 可接受的時間，以在伺服器的要求中包含預設認證。
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: WinHttpAutoLogonLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849936"
---
# <a name="winhttpautologonlevel"></a><span data-ttu-id="4a502-103">WinHttpAutoLogonLevel</span><span class="sxs-lookup"><span data-stu-id="4a502-103">WinHttpAutoLogonLevel</span></span>

<span data-ttu-id="4a502-104">自動登入 (自動登入) 原則會決定 *WinHTTP* 可接受的時間，以在伺服器的要求中包含預設認證。</span><span class="sxs-lookup"><span data-stu-id="4a502-104">The automatic logon (auto-logon) policy determines when it is acceptable for *WinHTTP* to include the default credentials in a request to the server.</span></span>

<span data-ttu-id="4a502-105">您可以將此值設定為 **L** ，讓 **winHTTP 自動登入 \_ \_ 安全性 \_ 等級 \_ 下限**，設定為 **M** 表示 **WinHTTP 自動登入安全性等級 \_ \_ \_ \_ 中等**，並設定為 **H** （winHTTP 自動登入安全性 **\_ \_ \_ 等級 \_ 高**）。</span><span class="sxs-lookup"><span data-stu-id="4a502-105">You can set this value to **L** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW**, set to **M** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**, and set to **H** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH**.</span></span> <span data-ttu-id="4a502-106">預設層級為 **WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 中**。</span><span class="sxs-lookup"><span data-stu-id="4a502-106">The default level is **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**.</span></span> <span data-ttu-id="4a502-107">如需自動登入原則的詳細資訊，請參閱 [WinHTTP 中的驗證](../winhttp/authentication-in-winhttp.md)一節。</span><span class="sxs-lookup"><span data-stu-id="4a502-107">For more information about automatic logon policy, see the section for [Authentication in WinHTTP](../winhttp/authentication-in-winhttp.md).</span></span>

<span data-ttu-id="4a502-108">**Windows 8 和 Windows Server 2012：** 此原則需要在 Windows 8 或 Windows Server 2012 上執行 Windows Installer，且在所有舊版 Windows 上都無法使用。</span><span class="sxs-lookup"><span data-stu-id="4a502-108">**Windows 8 and Windows Server 2012:** This policy requires Windows Installer running on the Windows 8 or Windows Server 2012 and is unavailable on all earlier versions of Windows.</span></span>

## <a name="registry-key"></a><span data-ttu-id="4a502-109">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="4a502-109">Registry Key</span></span>

<span data-ttu-id="4a502-110">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="4a502-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="4a502-111">資料類型</span><span class="sxs-lookup"><span data-stu-id="4a502-111">Data Type</span></span>

<span data-ttu-id="4a502-112">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="4a502-112">**REG\_SZ**</span></span>

 

 
