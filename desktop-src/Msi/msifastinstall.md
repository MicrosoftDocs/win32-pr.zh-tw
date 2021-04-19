---
description: MSIFASTINSTALL 屬性可以用來減少安裝大型 Windows Installer 套件所需的時間。
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: MSIFASTINSTALL 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987165"
---
# <a name="msifastinstall-property"></a><span data-ttu-id="fd83e-103">MSIFASTINSTALL 屬性</span><span class="sxs-lookup"><span data-stu-id="fd83e-103">MSIFASTINSTALL property</span></span>

<span data-ttu-id="fd83e-104">**MSIFASTINSTALL** 屬性可以用來減少安裝大型 Windows Installer 套件所需的時間。</span><span class="sxs-lookup"><span data-stu-id="fd83e-104">The **MSIFASTINSTALL** property can be used to reduce the time required to install a large Windows Installer package.</span></span> <span data-ttu-id="fd83e-105">您可以在命令列或 [屬性](property-table.md) 表中設定屬性，以設定使用者或開發人員所判斷的作業不是安裝的必要條件。</span><span class="sxs-lookup"><span data-stu-id="fd83e-105">The property can be set on the command line or in the [Property](property-table.md) table to configure operations that the user or developer determines are non-essential for the installation.</span></span>

<span data-ttu-id="fd83e-106">**MSIFASTINSTALL** 屬性的值可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="fd83e-106">The value of the **MSIFASTINSTALL** property can be a combination of the following values.</span></span>



| <span data-ttu-id="fd83e-107">值</span><span class="sxs-lookup"><span data-stu-id="fd83e-107">Value</span></span> | <span data-ttu-id="fd83e-108">意義</span><span class="sxs-lookup"><span data-stu-id="fd83e-108">Meaning</span></span>                                                                      |
|-------|------------------------------------------------------------------------------|
| <span data-ttu-id="fd83e-109">0</span><span class="sxs-lookup"><span data-stu-id="fd83e-109">0</span></span>     | <span data-ttu-id="fd83e-110">預設值</span><span class="sxs-lookup"><span data-stu-id="fd83e-110">Default value</span></span>                                                                |
| <span data-ttu-id="fd83e-111">1</span><span class="sxs-lookup"><span data-stu-id="fd83e-111">1</span></span>     | <span data-ttu-id="fd83e-112">此安裝不會儲存任何系統還原點。</span><span class="sxs-lookup"><span data-stu-id="fd83e-112">No system restore point is saved for this installation.</span></span>                      |
| <span data-ttu-id="fd83e-113">2</span><span class="sxs-lookup"><span data-stu-id="fd83e-113">2</span></span>     | <span data-ttu-id="fd83e-114">只執行檔案 [成本](file-costing.md) ，並略過檢查其他成本。</span><span class="sxs-lookup"><span data-stu-id="fd83e-114">Perform only [File Costing](file-costing.md) and skip checking other costs.</span></span> |
| <span data-ttu-id="fd83e-115">4</span><span class="sxs-lookup"><span data-stu-id="fd83e-115">4</span></span>     | <span data-ttu-id="fd83e-116">減少進度訊息的頻率。</span><span class="sxs-lookup"><span data-stu-id="fd83e-116">Reduce the frequency of progress messages.</span></span>                                   |



 

<span data-ttu-id="fd83e-117">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="fd83e-117">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="fd83e-118">從 Windows Installer 5.0 開始，可以使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="fd83e-118">This property is available beginning with Windows Installer 5.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd83e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd83e-119">Requirements</span></span>



| <span data-ttu-id="fd83e-120">需求</span><span class="sxs-lookup"><span data-stu-id="fd83e-120">Requirement</span></span> | <span data-ttu-id="fd83e-121">值</span><span class="sxs-lookup"><span data-stu-id="fd83e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd83e-122">版本</span><span class="sxs-lookup"><span data-stu-id="fd83e-122">Version</span></span><br/> | <span data-ttu-id="fd83e-123">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="fd83e-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fd83e-124">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="fd83e-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



 

 




