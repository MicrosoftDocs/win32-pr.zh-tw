---
description: PATCHNEWSUMMARYCOMMENTS 屬性會在修補期間更新系統管理安裝的留言摘要屬性。
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: PATCHNEWSUMMARYCOMMENTS 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe2bff9613fa5d39ae300e15c3ee816c5c6fce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992831"
---
# <a name="patchnewsummarycomments-property"></a><span data-ttu-id="93bea-103">PATCHNEWSUMMARYCOMMENTS 屬性</span><span class="sxs-lookup"><span data-stu-id="93bea-103">PATCHNEWSUMMARYCOMMENTS property</span></span>

<span data-ttu-id="93bea-104">**PATCHNEWSUMMARYCOMMENTS** 屬性會在修補期間更新系統管理安裝的 [**留言摘要**](comments-summary.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="93bea-104">The **PATCHNEWSUMMARYCOMMENTS** property updates the [**Comments Summary**](comments-summary.md) property of an administrative installation during patching.</span></span> <span data-ttu-id="93bea-105">只有 .msp 檔中的轉換會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="93bea-105">This property is only set by a transform in a .msp file.</span></span> <span data-ttu-id="93bea-106">.Msp 檔必須包含將這個屬性加入至 [屬性工作表](property-table.md) 的轉換，並設定其值。</span><span class="sxs-lookup"><span data-stu-id="93bea-106">The .msp file must include a transform that adds this property to the [Property table](property-table.md) and sets its value.</span></span> <span data-ttu-id="93bea-107">然後，安裝程式會將 **PATCHNEWSUMMARYCOMMENTS** 的值寫入 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="93bea-107">The installer then writes the value of **PATCHNEWSUMMARYCOMMENTS** to the [**Revision Number Summary**](revision-number-summary.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="93bea-108">備註</span><span class="sxs-lookup"><span data-stu-id="93bea-108">Remarks</span></span>

<span data-ttu-id="93bea-109">[**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)、 **PATCHNEWSUMMARYCOMMENTS** 和 [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)屬性是用來在修補程式安裝至系統管理映射時，更新摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="93bea-109">The [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS**, and [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) properties are used to update the summary information when a patch is installed to an administrative image.</span></span>

## <a name="requirements"></a><span data-ttu-id="93bea-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="93bea-110">Requirements</span></span>



| <span data-ttu-id="93bea-111">需求</span><span class="sxs-lookup"><span data-stu-id="93bea-111">Requirement</span></span> | <span data-ttu-id="93bea-112">值</span><span class="sxs-lookup"><span data-stu-id="93bea-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93bea-113">版本</span><span class="sxs-lookup"><span data-stu-id="93bea-113">Version</span></span><br/> | <span data-ttu-id="93bea-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="93bea-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="93bea-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="93bea-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="93bea-116">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="93bea-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="93bea-117">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="93bea-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93bea-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93bea-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93bea-119">屬性</span><span class="sxs-lookup"><span data-stu-id="93bea-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




