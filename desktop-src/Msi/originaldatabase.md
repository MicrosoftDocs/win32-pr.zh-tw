---
description: Windows Installer 將 OriginalDatabase 屬性設定為用來啟動安裝的安裝資料庫路徑。
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: OriginalDatabase 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976065"
---
# <a name="originaldatabase-property"></a><span data-ttu-id="5cec4-103">OriginalDatabase 屬性</span><span class="sxs-lookup"><span data-stu-id="5cec4-103">OriginalDatabase property</span></span>

<span data-ttu-id="5cec4-104">Windows Installer 將 **OriginalDatabase** 屬性設定為用來啟動安裝的安裝資料庫路徑。</span><span class="sxs-lookup"><span data-stu-id="5cec4-104">The Windows Installer sets the **OriginalDatabase** property to the path of the installation database used to launch the installation.</span></span> <span data-ttu-id="5cec4-105">如果是從命令列啟動安裝，則此值取決於 [**REINSTALLMODE**](reinstallmode.md) 屬性中是否有 (-v 旗標) 的重新緩存套件選項。</span><span class="sxs-lookup"><span data-stu-id="5cec4-105">If the installation is launched from a command line, the value depends on whether the recache package option (the -v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>



| <span data-ttu-id="5cec4-106">安裝方式</span><span class="sxs-lookup"><span data-stu-id="5cec4-106">Installation Method</span></span>                                                                                                                                                                                  | <span data-ttu-id="5cec4-107">OriginalDatabase 值</span><span class="sxs-lookup"><span data-stu-id="5cec4-107">OriginalDatabase Value</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="5cec4-108">藉由叫用安裝套件的路徑來啟動的任何安裝 ( .msi 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="5cec4-108">Any installation launched by invoking the path of the installation package (.msi file).</span></span>                                                                                                              | <span data-ttu-id="5cec4-109">安裝套件的路徑 ( .msi 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="5cec4-109">Path to the installation package (.msi file).</span></span> |
| <span data-ttu-id="5cec4-110">從命令列啟動安裝。</span><span class="sxs-lookup"><span data-stu-id="5cec4-110">Installation launched from a command line.</span></span> <span data-ttu-id="5cec4-111">安裝不是從封裝路徑啟動。</span><span class="sxs-lookup"><span data-stu-id="5cec4-111">The installation is not launched from a package path.</span></span> <span data-ttu-id="5cec4-112">[**REINSTALLMODE**](reinstallmode.md)屬性中有 (-v 旗標) 的重新緩存選項。</span><span class="sxs-lookup"><span data-stu-id="5cec4-112">The recache option (-v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>     | <span data-ttu-id="5cec4-113">來源上資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="5cec4-113">Path to the database on the source.</span></span>           |
| <span data-ttu-id="5cec4-114">從命令列啟動安裝。</span><span class="sxs-lookup"><span data-stu-id="5cec4-114">Installation launched from a command line.</span></span> <span data-ttu-id="5cec4-115">安裝不是從封裝路徑啟動。</span><span class="sxs-lookup"><span data-stu-id="5cec4-115">The installation is not launched from a package path.</span></span> <span data-ttu-id="5cec4-116">[**REINSTALLMODE**](reinstallmode.md)屬性中沒有重新緩存選項 (-v 旗標) 。</span><span class="sxs-lookup"><span data-stu-id="5cec4-116">The recache option (-v flag) is not present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> | <span data-ttu-id="5cec4-117">快取資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="5cec4-117">Path to the cached database.</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="5cec4-118">備註</span><span class="sxs-lookup"><span data-stu-id="5cec4-118">Remarks</span></span>

<span data-ttu-id="5cec4-119">在第一次安裝時， [ResolveSource 動作](resolvesource-action.md) 之前排序的自訂動作可以使用 **OriginalDatabase** 屬性來判斷安裝來源的位置。</span><span class="sxs-lookup"><span data-stu-id="5cec4-119">During a first time installation, a custom action sequenced before the [ResolveSource action](resolvesource-action.md) can use the **OriginalDatabase** property to determine the location of the installation source.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cec4-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cec4-120">Requirements</span></span>



| <span data-ttu-id="5cec4-121">需求</span><span class="sxs-lookup"><span data-stu-id="5cec4-121">Requirement</span></span> | <span data-ttu-id="5cec4-122">值</span><span class="sxs-lookup"><span data-stu-id="5cec4-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cec4-123">版本</span><span class="sxs-lookup"><span data-stu-id="5cec4-123">Version</span></span><br/> | <span data-ttu-id="5cec4-124">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5cec4-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5cec4-125">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5cec4-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5cec4-126">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="5cec4-126">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5cec4-127">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="5cec4-127">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cec4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cec4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cec4-129">屬性</span><span class="sxs-lookup"><span data-stu-id="5cec4-129">Properties</span></span>](properties.md)
</dt> </dl>

 

 




