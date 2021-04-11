---
title: 64位系統上的應用程式安裝
description: 64位的 Windows Installer 可以在64位的 Windows 上順暢地安裝32位的 MSI 應用程式。
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- 應用程式安裝 64-位 Windows 程式設計
- 安裝64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092864"
---
# <a name="application-installation-on-64-bit-systems"></a><span data-ttu-id="105d1-105">64位系統上的應用程式安裝</span><span class="sxs-lookup"><span data-stu-id="105d1-105">Application Installation on 64-bit Systems</span></span>

<span data-ttu-id="105d1-106">64位的 [Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) 可以在64位的 Windows 上順暢地安裝32位的 MSI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="105d1-106">The [64-bit Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span> <span data-ttu-id="105d1-107">針對使用16位存根來啟動32位安裝引擎的繼承應用程式，64位 Windows 會辨識特定的16位安裝程式，並替代已移植的32位版本。</span><span class="sxs-lookup"><span data-stu-id="105d1-107">For older applications that use a 16-bit stub to launch a 32-bit installation engine, 64-bit Windows recognizes specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span>

<span data-ttu-id="105d1-108">16位 DOS、Windows 或 OS/2 應用程式通常會使用16位的存根來檢查電腦類型，然後啟動32位安裝引擎以實際執行安裝。</span><span class="sxs-lookup"><span data-stu-id="105d1-108">16-bit DOS, Windows, or OS/2 applications often use a 16-bit stub to check the machine type, then launch a 32-bit installation engine to actually perform the installation.</span></span> <span data-ttu-id="105d1-109">為了讓您能夠安裝使用這項技術的應用程式，64位的 Windows 會將32位版本取代為下列16位安裝程式：</span><span class="sxs-lookup"><span data-stu-id="105d1-109">To enable installation of applications that use this technique, 64-bit Windows substitutes 32-bit versions for the following 16-bit installer programs:</span></span>

* <span data-ttu-id="105d1-110">適用于 Windows 1.2 的 Microsoft 安裝程式</span><span class="sxs-lookup"><span data-stu-id="105d1-110">Microsoft Setup for Windows 1.2</span></span>  
* <span data-ttu-id="105d1-111">適用于 Windows 2.6 的 Microsoft 安裝程式</span><span class="sxs-lookup"><span data-stu-id="105d1-111">Microsoft Setup for Windows 2.6</span></span>  
* <span data-ttu-id="105d1-112">適用于 Windows 3.0 的 Microsoft 安裝程式</span><span class="sxs-lookup"><span data-stu-id="105d1-112">Microsoft Setup for Windows 3.0</span></span>  
* <span data-ttu-id="105d1-113">適用于 Windows 3.01 的 Microsoft 安裝程式</span><span class="sxs-lookup"><span data-stu-id="105d1-113">Microsoft Setup for Windows 3.01</span></span>  
* <span data-ttu-id="105d1-114">InstallShield 5。x</span><span class="sxs-lookup"><span data-stu-id="105d1-114">InstallShield 5.x</span></span>  

<span data-ttu-id="105d1-115">替代清單儲存在登錄中的下列機碼底下： **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**。</span><span class="sxs-lookup"><span data-stu-id="105d1-115">The list of substitutions is stored in the registry under the following key: **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64**.</span></span>

> [!Note]  
> <span data-ttu-id="105d1-116">這項機制只是為了與使用本主題中所列之16位 Microsoft 安裝程式的32位應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="105d1-116">This mechanism is provided only for compatibility with 32-bit applications that use the 16-bit Microsoft installer programs listed in this topic.</span></span> <span data-ttu-id="105d1-117">不支援新增協力廠商安裝程式。</span><span class="sxs-lookup"><span data-stu-id="105d1-117">Addition of third-party installer programs is not supported.</span></span>

 

> [!Note]  
> <span data-ttu-id="105d1-118">ARM 上的 Windows 10 不包含這項機制。</span><span class="sxs-lookup"><span data-stu-id="105d1-118">This mechanism is not included on Windows 10 on ARM.</span></span>

 

 

 