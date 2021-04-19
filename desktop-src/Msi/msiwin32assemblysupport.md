---
description: MsiWin32AssemblySupport 屬性指出電腦是否支援 Win32 元件。
ms.assetid: 037202b6-41e4-4631-abbe-11291a5e5000
title: MsiWin32AssemblySupport 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ab0c0e11d9e8a4b98503268c3a2c7ef67341c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980147"
---
# <a name="msiwin32assemblysupport-property"></a><span data-ttu-id="5cd73-103">MsiWin32AssemblySupport 屬性</span><span class="sxs-lookup"><span data-stu-id="5cd73-103">MsiWin32AssemblySupport property</span></span>

<span data-ttu-id="5cd73-104">**MsiWin32AssemblySupport** 屬性指出電腦是否支援 Win32 元件。</span><span class="sxs-lookup"><span data-stu-id="5cd73-104">The **MsiWin32AssemblySupport** property indicates whether the computer supports Win32 assemblies.</span></span> <span data-ttu-id="5cd73-105">在支援 Win32 元件的系統上，安裝程式會將 **MsiWin32AssemblySupport** 的值設定為 sxs.dll 的檔案版本。</span><span class="sxs-lookup"><span data-stu-id="5cd73-105">On systems that support Win32 assemblies, the installer sets the value of **MsiWin32AssemblySupport** to the file version of sxs.dll.</span></span> <span data-ttu-id="5cd73-106">如果作業系統不支援 Win32 元件，安裝程式就不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5cd73-106">The installer does not set this property if the operating system does not support Win32 assemblies.</span></span> <span data-ttu-id="5cd73-107">如需詳細資訊，請參閱 [元件](assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="5cd73-107">For more information, see [Assemblies](assemblies.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cd73-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cd73-108">Requirements</span></span>



| <span data-ttu-id="5cd73-109">需求</span><span class="sxs-lookup"><span data-stu-id="5cd73-109">Requirement</span></span> | <span data-ttu-id="5cd73-110">值</span><span class="sxs-lookup"><span data-stu-id="5cd73-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cd73-111">版本</span><span class="sxs-lookup"><span data-stu-id="5cd73-111">Version</span></span><br/> | <span data-ttu-id="5cd73-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5cd73-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5cd73-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5cd73-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5cd73-114">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="5cd73-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5cd73-115">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="5cd73-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cd73-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cd73-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cd73-117">屬性</span><span class="sxs-lookup"><span data-stu-id="5cd73-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




