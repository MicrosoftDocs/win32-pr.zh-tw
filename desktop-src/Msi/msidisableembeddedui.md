---
description: 如果每一電腦的系統原則設定為1，則在電腦上會停用使用內嵌 UI 的功能。 預設值為0，可啟用內嵌的 UI 處理常式功能。
ms.assetid: f69d69a3-3c28-4841-a334-3acb61a06bc2
title: MsiDisableEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f5bfe6abfbb386253631c2858dab6ef36bcf39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945329"
---
# <a name="msidisableembeddedui"></a><span data-ttu-id="750c6-104">MsiDisableEmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="750c6-104">MsiDisableEmbeddedUI</span></span>

<span data-ttu-id="750c6-105">如果每一電腦的 [系統原則](system-policy.md) 設定為1，則在電腦上會停用使用內嵌 UI 的功能。</span><span class="sxs-lookup"><span data-stu-id="750c6-105">If this per-machine [system policy](system-policy.md) is set to 1, the capability to use embedded UI is disabled on the computer.</span></span> <span data-ttu-id="750c6-106">預設值為0，可啟用內嵌的 UI 處理常式功能。</span><span class="sxs-lookup"><span data-stu-id="750c6-106">The default value is 0, which enables the embedded UI handlers capability.</span></span>

<span data-ttu-id="750c6-107">若要停用單一封裝的內嵌 UI，您可以使用 [**MSIDISABLEEEUI**](msidisableeeui.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="750c6-107">To disable the embedded UI for a single package, you can use the [**MSIDISABLEEEUI**](msidisableeeui.md) property.</span></span>

<span data-ttu-id="750c6-108">**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="750c6-108">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="750c6-109">從 Windows Installer 4.5 開始，可以使用此函數。</span><span class="sxs-lookup"><span data-stu-id="750c6-109">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="750c6-110">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="750c6-110">Registry Key</span></span>

<span data-ttu-id="750c6-111">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="750c6-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="750c6-112">資料類型</span><span class="sxs-lookup"><span data-stu-id="750c6-112">Data Type</span></span>

<span data-ttu-id="750c6-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="750c6-113">**REG\_DWORD**</span></span>

 

 



