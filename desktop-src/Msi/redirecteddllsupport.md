---
description: 如果執行安裝的系統平臺支援隔離的元件，安裝程式會設定 RedirectedDLLSupport 屬性。
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: RedirectedDLLSupport 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993506"
---
# <a name="redirecteddllsupport-property"></a><span data-ttu-id="c019b-103">RedirectedDLLSupport 屬性</span><span class="sxs-lookup"><span data-stu-id="c019b-103">RedirectedDLLSupport property</span></span>

<span data-ttu-id="c019b-104">如果執行安裝的系統平臺支援 [隔離的元件](isolated-components.md)，安裝程式會設定 **RedirectedDLLSupport** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c019b-104">The installer sets the **RedirectedDLLSupport** property if the system platform performing the installation supports [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="c019b-105">如果執行安裝的系統支援根據的 [隔離元件](isolated-components.md)，則安裝程式會將 **RedirectedDLLSupport** 屬性設定為1的值。本機檔案。</span><span class="sxs-lookup"><span data-stu-id="c019b-105">The installer sets the **RedirectedDLLSupport** property to a value of 1 if the system performing the installation supports [Isolated Components](isolated-components.md) based on .LOCAL files.</span></span> <span data-ttu-id="c019b-106">如果執行安裝的系統支援使用兩者進行隔離，則安裝程式會將 **RedirectedDLLSupport** 屬性設定為2的值。本機檔案或 Win32 並存元件。</span><span class="sxs-lookup"><span data-stu-id="c019b-106">The installer sets the **RedirectedDLLSupport** property to a value of 2 if the system that performs the installation supports isolation using either .LOCAL files or Win32 side-by-side assemblies.</span></span>

<span data-ttu-id="c019b-107">**RedirectedDLLSupport** 屬性可以用來在 [InstallUISequence 資料表](installuisequence-table.md)或 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中條件 [IsolateComponents 動作](isolatecomponents-action.md)。</span><span class="sxs-lookup"><span data-stu-id="c019b-107">The **RedirectedDLLSupport** property can be used to condition the [IsolateComponents action](isolatecomponents-action.md) in the [InstallUISequence table](installuisequence-table.md) or [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c019b-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="c019b-108">Requirements</span></span>



| <span data-ttu-id="c019b-109">需求</span><span class="sxs-lookup"><span data-stu-id="c019b-109">Requirement</span></span> | <span data-ttu-id="c019b-110">值</span><span class="sxs-lookup"><span data-stu-id="c019b-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c019b-111">版本</span><span class="sxs-lookup"><span data-stu-id="c019b-111">Version</span></span><br/> | <span data-ttu-id="c019b-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c019b-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c019b-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c019b-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c019b-114">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="c019b-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c019b-115">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="c019b-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c019b-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c019b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c019b-117">屬性</span><span class="sxs-lookup"><span data-stu-id="c019b-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




