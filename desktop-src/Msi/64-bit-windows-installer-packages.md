---
description: 64位封裝包含部分或全部64位 Windows Installer 元件。
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: 64位 Windows Installer 套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849002"
---
# <a name="64-bit-windows-installer-packages"></a><span data-ttu-id="121b9-103">64位 Windows Installer 套件</span><span class="sxs-lookup"><span data-stu-id="121b9-103">64-bit Windows Installer Packages</span></span>

<span data-ttu-id="121b9-104">64位封裝包含部分或全部64位 [Windows Installer](windows-installer-components.md) 元件。</span><span class="sxs-lookup"><span data-stu-id="121b9-104">A 64-bit package consists partially or entirely of 64-bit [Windows Installer](windows-installer-components.md) components.</span></span> <span data-ttu-id="121b9-105">下列清單會識別每個64位 Windows Installer 套件的需求：</span><span class="sxs-lookup"><span data-stu-id="121b9-105">The following list identifies the requirements for every 64-bit Windows Installer package:</span></span>

-   <span data-ttu-id="121b9-106">只有當封裝在 Intel64 (Itanium) 處理器上執行時，才必須在 [ [**範本摘要**](template-summary.md) ] 屬性的 [平臺] 欄位中輸入 "Intel64" 值。</span><span class="sxs-lookup"><span data-stu-id="121b9-106">The value "Intel64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Intel64 (Itanium) processor.</span></span>
-   <span data-ttu-id="121b9-107">只有當封裝在 x64 處理器上執行時，才必須在 [ [**範本摘要**](template-summary.md) ] 屬性的 [平臺] 欄位中輸入值 "x64"。</span><span class="sxs-lookup"><span data-stu-id="121b9-107">The value "x64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an x64 processor.</span></span>
-   <span data-ttu-id="121b9-108">只有當封裝在 Arm64 處理器上執行時，才必須在 [**範本摘要**](template-summary.md) 屬性的 [platform] 欄位中輸入 "Arm64" 值。</span><span class="sxs-lookup"><span data-stu-id="121b9-108">The value "Arm64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Arm64 processor.</span></span>
-   <span data-ttu-id="121b9-109">[ [**頁面計數摘要**](page-count-summary.md) ] 屬性必須設定為整數200或更大，因為 Windows Installer 2.0 是能夠安裝64位元件的最小版本。</span><span class="sxs-lookup"><span data-stu-id="121b9-109">The [**Page Count Summary**](page-count-summary.md) property must be set to the integer 200 or greater, because Windows Installer 2.0 is the minimum version that is capable of installing 64-bit components.</span></span> <span data-ttu-id="121b9-110">Arm64 平臺的套件需要500或更高的值。</span><span class="sxs-lookup"><span data-stu-id="121b9-110">Packages for the Arm64 platform require a value of 500 or greater.</span></span>
-   <span data-ttu-id="121b9-111">封裝中的每個64位 Windows Installer 元件都必須在 [元件資料表](component-table.md)的 [屬性] 資料行中包含 **msidbComponentAttributes64bit** 位。</span><span class="sxs-lookup"><span data-stu-id="121b9-111">Each 64-bit Windows Installer component in the package must include the **msidbComponentAttributes64bit** bit in the Attributes column of the [Component Table](component-table.md).</span></span>

<span data-ttu-id="121b9-112">如需詳細資訊，請參閱 [64 位作業系統上的 Windows Installer](windows-installer-on-64-bit-operating-systems.md) 和 [32 位 Windows Installer 套件](32-bit-windows-installer-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="121b9-112">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md) and [32-bit Windows Installer Packages](32-bit-windows-installer-packages.md).</span></span>

 

 



