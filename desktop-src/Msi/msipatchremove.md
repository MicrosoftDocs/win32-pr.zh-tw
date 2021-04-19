---
description: MSIPATCHREMOVE 屬性會指定要在安裝期間移除的修補程式清單。
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: MSIPATCHREMOVE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976010"
---
# <a name="msipatchremove-property"></a><span data-ttu-id="5aca3-103">MSIPATCHREMOVE 屬性</span><span class="sxs-lookup"><span data-stu-id="5aca3-103">MSIPATCHREMOVE property</span></span>

<span data-ttu-id="5aca3-104">**MSIPATCHREMOVE** 屬性會指定要在安裝期間移除的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5aca3-104">The **MSIPATCHREMOVE** property specifies the list of patches to remove during an installation.</span></span> <span data-ttu-id="5aca3-105">清單中的個別修補程式會以分號分隔，並且可由 patch 程式碼 GUID 或修補程式的完整路徑來表示。</span><span class="sxs-lookup"><span data-stu-id="5aca3-105">Individual patches in the list are separated by semicolons and can be represented by patch code GUID or the full path to the patch.</span></span> <span data-ttu-id="5aca3-106">[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)函式和 [安裝程式](installer-object.md)物件的 [**RemovePatches**](installer-removepatches.md)方法會設定 **MSIPATCHREMOVE** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5aca3-106">The [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function and the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object set the **MSIPATCHREMOVE** property.</span></span>

<span data-ttu-id="5aca3-107">您可以在命令列上設定 **MSIPATCHREMOVE** 屬性，如下所示來移除修補程式。</span><span class="sxs-lookup"><span data-stu-id="5aca3-107">The **MSIPATCHREMOVE** property can be set on the command line as follows to remove a patch.</span></span>

<span data-ttu-id="5aca3-108">**msiexec/i A： \\Example.msi MSIPATCHREMOVE = c： \\ 修補程式 \\ qfe1 .msp; {0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0};{A86B443B-E3BF-4009-ADED-F716FC735858}/qb**</span><span class="sxs-lookup"><span data-stu-id="5aca3-108">**msiexec /i A:\\Example.msi MSIPATCHREMOVE=c:\\patches\\qfe1.msp;{0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0};{A86B443B-E3BF-4009-ADED-F716FC735858}/qb**</span></span>

## <a name="requirements"></a><span data-ttu-id="5aca3-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="5aca3-109">Requirements</span></span>



| <span data-ttu-id="5aca3-110">需求</span><span class="sxs-lookup"><span data-stu-id="5aca3-110">Requirement</span></span> | <span data-ttu-id="5aca3-111">值</span><span class="sxs-lookup"><span data-stu-id="5aca3-111">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aca3-112">版本</span><span class="sxs-lookup"><span data-stu-id="5aca3-112">Version</span></span><br/> | <span data-ttu-id="5aca3-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5aca3-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5aca3-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5aca3-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5aca3-115">Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5aca3-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5aca3-116">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="5aca3-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5aca3-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5aca3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aca3-118">屬性</span><span class="sxs-lookup"><span data-stu-id="5aca3-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="5aca3-119">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="5aca3-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




