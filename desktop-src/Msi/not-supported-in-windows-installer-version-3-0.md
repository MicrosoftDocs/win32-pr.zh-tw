---
description: 在此頁面上列出的 Windows Installer 函式、資料表和屬性，Windows Installer&160、 \# 3.0 和較早的版本不支援此功能。
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Windows Installer 3.0 中不支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980788"
---
# <a name="not-supported-in-windows-installer-30"></a><span data-ttu-id="e37bb-103">Windows Installer 3.0 中不支援</span><span class="sxs-lookup"><span data-stu-id="e37bb-103">Not Supported in Windows Installer 3.0</span></span>

<span data-ttu-id="e37bb-104">Windows Installer 3.0 及更早版本不支援此頁面上所列的 Windows Installer 函數、資料表和屬性。</span><span class="sxs-lookup"><span data-stu-id="e37bb-104">The Windows Installer functions, tables, and properties listed on this page are not supported by Windows Installer 3.0 and earlier versions.</span></span> <span data-ttu-id="e37bb-105">這份清單缺少某項功能，並不保證支援此功能。</span><span class="sxs-lookup"><span data-stu-id="e37bb-105">The absence of a feature from this list does not guarantee that the feature is supported.</span></span> <span data-ttu-id="e37bb-106">請參閱主要檔，以判斷特定功能所需的 Windows Installer 版本。</span><span class="sxs-lookup"><span data-stu-id="e37bb-106">See the main documentation to determine which Windows Installer version is required for a particular feature.</span></span> <span data-ttu-id="e37bb-107">如需其他 Windows Installer 版本的詳細資訊，請參閱 [Windows Installer 中的新功能](what-s-new-in-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="e37bb-107">For information about other Windows Installer versions see [What's New in Windows Installer](what-s-new-in-windows-installer.md).</span></span>

<span data-ttu-id="e37bb-108">Windows Installer 3.0 適用于 Windows Server 2003、Windows XP 或 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="e37bb-108">Windows Installer 3.0 is available for Windows Server 2003, Windows XP, or Windows 2000.</span></span> <span data-ttu-id="e37bb-109">如需所有 Windows Installer 版本和可轉散發套件的清單，請參閱 [Windows Installer 的發行版本](released-versions-of-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="e37bb-109">For a list of all Windows Installer versions and redistributables, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

<span data-ttu-id="e37bb-110">Windows Installer 3.0 及更舊版本中不支援下列功能。</span><span class="sxs-lookup"><span data-stu-id="e37bb-110">The following features are not supported in Windows Installer 3.0 and earlier versions.</span></span>

[<span data-ttu-id="e37bb-111">安裝程式函數</span><span class="sxs-lookup"><span data-stu-id="e37bb-111">Installer Functions</span></span>](installer-functions.md)

-   [<span data-ttu-id="e37bb-112">**MsiSetExternalUIRecord**</span><span class="sxs-lookup"><span data-stu-id="e37bb-112">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="e37bb-113">**MsiNotifySidChange**</span><span class="sxs-lookup"><span data-stu-id="e37bb-113">**MsiNotifySidChange**</span></span>](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

<span data-ttu-id="e37bb-114">回呼函數原型</span><span class="sxs-lookup"><span data-stu-id="e37bb-114">Callback Function Prototype</span></span>

-   [<span data-ttu-id="e37bb-115">**INSTALLUI \_ 處理常式 \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="e37bb-115">**INSTALLUI\_HANDLER\_RECORD**</span></span>](/windows/win32/api/msi/nc-msi-installui_handler_record)

[<span data-ttu-id="e37bb-116">資料庫資料表</span><span class="sxs-lookup"><span data-stu-id="e37bb-116">Database Tables</span></span>](database-tables.md)

-   <span data-ttu-id="e37bb-117">[MsiPatchMetadata 資料表](msipatchmetadata-table.md)的 Value 資料行接受 **OptimizedInstallMode** 和 **MinorUpdateTargetRTM**。</span><span class="sxs-lookup"><span data-stu-id="e37bb-117">The Value column of the [MsiPatchMetadata Table](msipatchmetadata-table.md) accepts **OptimizedInstallMode** and **MinorUpdateTargetRTM**.</span></span>

[<span data-ttu-id="e37bb-118">屬性</span><span class="sxs-lookup"><span data-stu-id="e37bb-118">Properties</span></span>](properties.md)

-   [<span data-ttu-id="e37bb-119">**Msix64 屬性**</span><span class="sxs-lookup"><span data-stu-id="e37bb-119">**Msix64 Property**</span></span>](msix64.md)

[<span data-ttu-id="e37bb-120">64位作業系統上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e37bb-120">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)

-   <span data-ttu-id="e37bb-121">[**範本摘要屬性**](template-summary.md)接受 x64 值。</span><span class="sxs-lookup"><span data-stu-id="e37bb-121">The [**Template Summary Property**](template-summary.md) accepts the value x64.</span></span>

[<span data-ttu-id="e37bb-122">內部一致性評估工具-Ices-003</span><span class="sxs-lookup"><span data-stu-id="e37bb-122">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

-   [<span data-ttu-id="e37bb-123">ICE99</span><span class="sxs-lookup"><span data-stu-id="e37bb-123">ICE99</span></span>](ice99.md)

 

 
