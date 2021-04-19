---
description: MsiNetAssemblySupport 屬性指出電腦是否支援通用語言執行時間元件。
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: MsiNetAssemblySupport 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999182"
---
# <a name="msinetassemblysupport-property"></a><span data-ttu-id="1f2a6-103">MsiNetAssemblySupport 屬性</span><span class="sxs-lookup"><span data-stu-id="1f2a6-103">MsiNetAssemblySupport property</span></span>

<span data-ttu-id="1f2a6-104">**MsiNetAssemblySupport** 屬性指出電腦是否支援通用語言執行時間元件。</span><span class="sxs-lookup"><span data-stu-id="1f2a6-104">The **MsiNetAssemblySupport** property indicates whether the computer supports common language run-time assemblies.</span></span> <span data-ttu-id="1f2a6-105">在支援通用語言執行時間元件的系統上，安裝程式會將 **MsiNetAssemblySupport** 的值設定為 Fusion.dll 的檔案版本。</span><span class="sxs-lookup"><span data-stu-id="1f2a6-105">On systems that support common language run-time assemblies, the installer sets the value of **MsiNetAssemblySupport** to the file version of Fusion.dll.</span></span> <span data-ttu-id="1f2a6-106">如果作業系統不支援通用語言執行時間元件，安裝程式就不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1f2a6-106">The installer does not set this property if the operating system does not support common language run-time assemblies.</span></span> <span data-ttu-id="1f2a6-107">當使用者電腦上並存安裝多個版本的 Fusion.dll 時，這個屬性會設定為最新版本的 Fusion.dll 檔案。</span><span class="sxs-lookup"><span data-stu-id="1f2a6-107">When multiple versions of Fusion.dll are installed side-by-side on the user's computer, this property is set to the latest version of the Fusion.dll file.</span></span> <span data-ttu-id="1f2a6-108">例如，如果 .NET Framework version v1.0.3705 (Fusion.dll version 1.0.3705.15) 和 .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) 會並存安裝， **MsiNetAssemblySupport** 屬性會設定為1.1.4322.314。</span><span class="sxs-lookup"><span data-stu-id="1f2a6-108">For example, if .NET Framework version 1.0.3705 (Fusion.dll version 1.0.3705.15)and .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) are installed side-by-side, the **MsiNetAssemblySupport** property is set to 1.1.4322.314.</span></span> <span data-ttu-id="1f2a6-109">如需詳細資訊，請參閱 [元件](assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="1f2a6-109">For more information, see [Assemblies](assemblies.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2a6-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f2a6-110">Requirements</span></span>



| <span data-ttu-id="1f2a6-111">需求</span><span class="sxs-lookup"><span data-stu-id="1f2a6-111">Requirement</span></span> | <span data-ttu-id="1f2a6-112">值</span><span class="sxs-lookup"><span data-stu-id="1f2a6-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2a6-113">版本</span><span class="sxs-lookup"><span data-stu-id="1f2a6-113">Version</span></span><br/> | <span data-ttu-id="1f2a6-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="1f2a6-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1f2a6-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="1f2a6-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1f2a6-116">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="1f2a6-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1f2a6-117">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="1f2a6-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f2a6-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f2a6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f2a6-119">屬性</span><span class="sxs-lookup"><span data-stu-id="1f2a6-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




