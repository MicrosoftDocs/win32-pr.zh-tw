---
description: 如果每一電腦的系統原則設定為1，則系統上沒有套件會取得元件資料表中 msidbComponentAttributesShared 屬性所啟用的共用元件功能。
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512020"
---
# <a name="disablesharedcomponent"></a><span data-ttu-id="1864a-103">DisableSharedComponent</span><span class="sxs-lookup"><span data-stu-id="1864a-103">DisableSharedComponent</span></span>

<span data-ttu-id="1864a-104">如果每一電腦的 [系統原則](system-policy.md)設定為1，則系統上沒有套件會取得 [元件資料表](component-table.md)中 **msidbComponentAttributesShared** 屬性所啟用的共用元件功能。</span><span class="sxs-lookup"><span data-stu-id="1864a-104">If this per-machine [system policy](system-policy.md) is set to 1, no package on the system gets the shared component functionality enabled by the **msidbComponentAttributesShared** attribute in the [Component table](component-table.md).</span></span> <span data-ttu-id="1864a-105">預設值為0，可針對所有封裝中標示為 **msidbComponentAttributesShared** 的元件啟用共用元件功能。</span><span class="sxs-lookup"><span data-stu-id="1864a-105">The default value is 0, which enables the shared component functionality for components marked with **msidbComponentAttributesShared** in all packages.</span></span>

<span data-ttu-id="1864a-106">**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="1864a-106">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="1864a-107">從 Windows Installer 4.5 開始，可以使用此函數。</span><span class="sxs-lookup"><span data-stu-id="1864a-107">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="1864a-108">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="1864a-108">Registry Key</span></span>

<span data-ttu-id="1864a-109">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="1864a-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="1864a-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="1864a-110">Data Type</span></span>

<span data-ttu-id="1864a-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1864a-111">**REG\_DWORD**</span></span>

 

 



