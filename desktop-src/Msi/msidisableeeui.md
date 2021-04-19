---
description: 若要停用 MsiEmbeddedUI 資料表中定義之安裝的內嵌使用者介面，請在命令列上將 MSIDISABLEEEUI 屬性設定為1。
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: MSIDISABLEEEUI 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998414"
---
# <a name="msidisableeeui-property"></a><span data-ttu-id="ccd4c-103">MSIDISABLEEEUI 屬性</span><span class="sxs-lookup"><span data-stu-id="ccd4c-103">MSIDISABLEEEUI property</span></span>

<span data-ttu-id="ccd4c-104">若要停用 [MsiEmbeddedUI 資料表](msiembeddedui-table.md)中定義之安裝的內嵌使用者介面，請在命令列上將 MSIDISABLEEEUI 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="ccd4c-104">To disable the embedded user interface for the installation defined in the [MsiEmbeddedUI table](msiembeddedui-table.md), set the MSIDISABLEEEUI property to 1 on the command line.</span></span>

<span data-ttu-id="ccd4c-105">**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="ccd4c-105">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="ccd4c-106">早于 Windows Installer 4.5 的版本會忽略 MSIDISABLEEEUI 屬性。</span><span class="sxs-lookup"><span data-stu-id="ccd4c-106">Versions earlier than Windows Installer 4.5 ignore the MSIDISABLEEEUI Property.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccd4c-107">備註</span><span class="sxs-lookup"><span data-stu-id="ccd4c-107">Remarks</span></span>

<span data-ttu-id="ccd4c-108">在多套件安裝中，子封裝通常應該使用父封裝的使用者介面，而不會初始化它自己的內嵌 UI。</span><span class="sxs-lookup"><span data-stu-id="ccd4c-108">In a multiple-package installation, a child package should typically use the user interface of the parent package and not initialize its own embedded UI.</span></span> <span data-ttu-id="ccd4c-109">如果未在父封裝內設定 MSIDISABLEEEUI 屬性，則子封裝預設會使用父封裝的內嵌 UI，並忽略子封裝內的 MSIDISABLEEEUI 屬性。</span><span class="sxs-lookup"><span data-stu-id="ccd4c-109">If the MSIDISABLEEEUI property is not set inside the parent package, the child package uses the embedded UI of the parent package by default and ignores the MSIDISABLEEEUI property within the child package.</span></span>

<span data-ttu-id="ccd4c-110">MSIDISABLEEEUI 屬性會停用單一封裝的內嵌使用者介面。</span><span class="sxs-lookup"><span data-stu-id="ccd4c-110">The MSIDISABLEEEUI property disables the embedded user interface for a single package.</span></span> <span data-ttu-id="ccd4c-111">您可以使用 [MsiDisableEmbeddedUI](msidisableembeddedui.md) 原則來停用電腦上所有封裝的內嵌使用者介面。</span><span class="sxs-lookup"><span data-stu-id="ccd4c-111">You can use the [MsiDisableEmbeddedUI](msidisableembeddedui.md) policy to disable embedded user interfaces for all packages on the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd4c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccd4c-112">Requirements</span></span>



| <span data-ttu-id="ccd4c-113">需求</span><span class="sxs-lookup"><span data-stu-id="ccd4c-113">Requirement</span></span> | <span data-ttu-id="ccd4c-114">值</span><span class="sxs-lookup"><span data-stu-id="ccd4c-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd4c-115">版本</span><span class="sxs-lookup"><span data-stu-id="ccd4c-115">Version</span></span><br/> | <span data-ttu-id="ccd4c-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ccd4c-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ccd4c-117">Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP 上的 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ccd4c-117">Windows Installer 4.5 on Windows Server 2008, Windows Vista, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="ccd4c-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="ccd4c-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ccd4c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccd4c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd4c-120">屬性</span><span class="sxs-lookup"><span data-stu-id="ccd4c-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




