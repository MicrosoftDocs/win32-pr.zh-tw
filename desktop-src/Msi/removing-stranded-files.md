---
description: Windows Installer 卸載無法移除應用程式的所有檔案的可能原因清單。
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: 移除擱置的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978001"
---
# <a name="removing-stranded-files"></a><span data-ttu-id="bd054-103">移除擱置的檔案</span><span class="sxs-lookup"><span data-stu-id="bd054-103">Removing Stranded Files</span></span>

<span data-ttu-id="bd054-104">如果在執行卸載後，應該從使用者的電腦移除的檔案仍保持安裝，則安裝程式可能會因為下列一或多個原因而無法移除包含檔案的元件：</span><span class="sxs-lookup"><span data-stu-id="bd054-104">If a file that should have been removed from the user's computer remains installed after running an uninstall, the installer may not be removing the component containing the file for one or more of the following reasons:</span></span>

-   <span data-ttu-id="bd054-105">在 [元件資料表](component-table.md)的 [屬性] 資料行中，已設定元件的 msidbComponentAttributesPermanent 位。</span><span class="sxs-lookup"><span data-stu-id="bd054-105">The msidbComponentAttributesPermanent bit was set for the component in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="bd054-106">未在元件資料表的 [元件] 資料行中輸入元件的值。</span><span class="sxs-lookup"><span data-stu-id="bd054-106">No value was entered for the component in the ComponentId column of the Component table.</span></span>
-   <span data-ttu-id="bd054-107">另一個仍安裝的應用程式或功能會使用此元件。</span><span class="sxs-lookup"><span data-stu-id="bd054-107">The component is used by another application or feature that is still installed.</span></span>
-   <span data-ttu-id="bd054-108">[條件](condition-table.md)資料表中指定的條件會在安裝期間啟用功能，並在卸載期間停用此功能。</span><span class="sxs-lookup"><span data-stu-id="bd054-108">There is a condition specified in the [Condition](condition-table.md) table that enables a feature during installation and disables the feature during uninstallation.</span></span>
-   <span data-ttu-id="bd054-109">元件的金鑰檔在 **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **shareddll** 底下有先前的參考計數。</span><span class="sxs-lookup"><span data-stu-id="bd054-109">The key file for the component has a previous reference count under **HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**SharedDLLs**.</span></span>
-   <span data-ttu-id="bd054-110">元件會安裝在系統資料夾中，而且元件中的任何檔案在 **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **shareddll** 底下都有先前的參考計數。</span><span class="sxs-lookup"><span data-stu-id="bd054-110">The component is installed in the System folder and any file in the component has a previous reference count under **HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**SharedDLLs**.</span></span>
-   <span data-ttu-id="bd054-111">Windows Installer 不會移除 [Windows 資源保護](../wfp/windows-resource-protection-portal.md) (WRP) 所保護的任何檔案或登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="bd054-111">The Windows Installer does not remove any files or registry keys that are protected by [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) (WRP).</span></span> <span data-ttu-id="bd054-112">如需詳細資訊，請參閱 [使用 Windows Installer 和 Windows 資源保護](windows-resource-protection-on-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="bd054-112">For more information, see [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).</span></span> <span data-ttu-id="bd054-113">在 Windows Server 2003、Windows XP 及 Windows 2000 上，安裝程式不會移除受 Windows 檔案保護 (WFP) 保護的任何檔案。</span><span class="sxs-lookup"><span data-stu-id="bd054-113">On Windows Server 2003, Windows XP, and Windows 2000, the installer does not remove any files that are protected by Windows File Protection (WFP).</span></span> <span data-ttu-id="bd054-114">如果元件的金鑰路徑檔案或登錄機碼受到 WFP 或 WRP 的保護，安裝程式就不會移除該元件。</span><span class="sxs-lookup"><span data-stu-id="bd054-114">If a component's key path file or registry key is protected by WFP or WRP, the installer does not remove the component.</span></span>
    > [!Note]  
    > <span data-ttu-id="bd054-115">因為 Windows Installer 不會安裝、更新或移除任何受 WRP 保護的資源，所以您不應該在安裝套件中包含受保護的資源。</span><span class="sxs-lookup"><span data-stu-id="bd054-115">Because Windows Installer does not install, update, or remove any resource that is protected by WRP, you should not include protected resources in an installation package.</span></span> <span data-ttu-id="bd054-116">相反地，請只使用[Windows 資源保護](../wfp/windows-resource-protection-portal.md)一節中所述的[支援資源取代機制](../wfp/supported-file-replacement-mechanisms.md)。</span><span class="sxs-lookup"><span data-stu-id="bd054-116">Instead, use only the [supported resource replacement mechanisms](../wfp/supported-file-replacement-mechanisms.md) described in the [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) section.</span></span>

     

 

 
