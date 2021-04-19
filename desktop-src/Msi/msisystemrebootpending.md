---
description: 如果有暫止的作業要重新命名檔案，安裝程式會將 MsiSystemRebootPending 屬性的值設定為1。
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: MsiSystemRebootPending 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999631"
---
# <a name="msisystemrebootpending-property"></a><span data-ttu-id="0d932-103">MsiSystemRebootPending 屬性</span><span class="sxs-lookup"><span data-stu-id="0d932-103">MsiSystemRebootPending property</span></span>

<span data-ttu-id="0d932-104">如果有暫止的作業要重新命名檔案，安裝程式會將 **MsiSystemRebootPending** 屬性的值設定為1。</span><span class="sxs-lookup"><span data-stu-id="0d932-104">The installer sets the value of the **MsiSystemRebootPending** property to 1 if there is an operation pending to rename a file.</span></span>

<span data-ttu-id="0d932-105">封裝作者可以在這個屬性的 [LaunchCondition 資料表](launchcondition-table.md) 中建立條件，以防止在有作業暫止重新命名檔案的情況下安裝套件。</span><span class="sxs-lookup"><span data-stu-id="0d932-105">Package authors can base a condition in the [LaunchCondition table](launchcondition-table.md) on this property to prevent the installation of their package in cases where there is an operation pending to rename a file.</span></span> <span data-ttu-id="0d932-106">這可能是為了避免重新命名檔案所造成的作業系統重新開機。</span><span class="sxs-lookup"><span data-stu-id="0d932-106">This may be done to prevent a restart of the operating system caused by the renaming of the file.</span></span> <span data-ttu-id="0d932-107">安裝程式在所有需要重新開機系統的情況下，都不會設定 **MsiSystemRebootPending** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0d932-107">The installer does not set the **MsiSystemRebootPending** property in all cases that require a restart of the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d932-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d932-108">Requirements</span></span>



| <span data-ttu-id="0d932-109">需求</span><span class="sxs-lookup"><span data-stu-id="0d932-109">Requirement</span></span> | <span data-ttu-id="0d932-110">值</span><span class="sxs-lookup"><span data-stu-id="0d932-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d932-111">版本</span><span class="sxs-lookup"><span data-stu-id="0d932-111">Version</span></span><br/> | <span data-ttu-id="0d932-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="0d932-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0d932-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="0d932-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0d932-114">Windows Server 2003 或 Windows XP 上的 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="0d932-114">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0d932-115">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d932-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d932-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d932-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d932-117">屬性</span><span class="sxs-lookup"><span data-stu-id="0d932-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="0d932-118">系統重新開機</span><span class="sxs-lookup"><span data-stu-id="0d932-118">System Reboots</span></span>](system-reboots.md)
</dt> <dt>

[<span data-ttu-id="0d932-119">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="0d932-119">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




