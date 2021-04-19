---
description: 如果每一電腦的系統原則設定為 &\# 0034; 1&\# 0034;，則安裝程式在網頁中的腳本使用安裝程式的自動化介面時，不會提示使用者。
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981153"
---
# <a name="safeforscripting"></a><span data-ttu-id="4f42a-103">SafeForScripting</span><span class="sxs-lookup"><span data-stu-id="4f42a-103">SafeForScripting</span></span>

<span data-ttu-id="4f42a-104">如果每一電腦的 [系統原則](system-policy.md) 設定為 "1"，則安裝程式在網頁中的腳本使用安裝程式的 [自動化介面](automation-interface.md)時，不會提示使用者。</span><span class="sxs-lookup"><span data-stu-id="4f42a-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer does not prompt users when scripts within a Web page use the installer's [automation interface](automation-interface.md).</span></span>

<span data-ttu-id="4f42a-105">在設定此原則之前，您應該考慮上述使用者提示是否為使用者提供適當的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="4f42a-105">Before setting this policy, you should consider whether foregoing the user prompt provides an appropriate level of security for your users.</span></span> <span data-ttu-id="4f42a-106">如果未設定此原則，當網際網路瀏覽器裝載的腳本嘗試安裝應用程式時，系統會警告使用者，並要求他們接受或拒絕安裝。</span><span class="sxs-lookup"><span data-stu-id="4f42a-106">If this policy is not set, when a script hosted by an Internet browser tries to install an application, the system warns the user and asks them to accept or refuse the installation.</span></span> <span data-ttu-id="4f42a-107">設定 SafeForScripting 會抑制此警告，而且可能會允許在系統上安裝應用程式，而不需要使用者的知識。</span><span class="sxs-lookup"><span data-stu-id="4f42a-107">Setting SafeForScripting suppresses this warning and may allow the installation of applications on the system without the user's knowledge.</span></span> <span data-ttu-id="4f42a-108">此原則可能適用于使用 web 型工具來散發程式的企業。</span><span class="sxs-lookup"><span data-stu-id="4f42a-108">This policy may be useful for an enterprise that uses web-based tools to distribute programs.</span></span>

<span data-ttu-id="4f42a-109">如需詳細資訊，請參閱 [撰寫安全安裝](guidelines-for-authoring-secure-installations.md) 和 [數位簽章](digital-signatures-and-windows-installer.md) 的指導方針，以及 [從網際網路下載安裝](downloading-an-installation-from-the-internet.md)的 Windows Installer 和下載。</span><span class="sxs-lookup"><span data-stu-id="4f42a-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="4f42a-110">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="4f42a-110">Registry Key</span></span>

<span data-ttu-id="4f42a-111">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="4f42a-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="4f42a-112">資料類型</span><span class="sxs-lookup"><span data-stu-id="4f42a-112">Data Type</span></span>

<span data-ttu-id="4f42a-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4f42a-113">**REG\_DWORD**</span></span>

 

 



