---
description: Version9X 屬性可提供適用于9x 版本之 Windows 作業系統的版本號碼。這個屬性的值是整數： MajorVersion \* 100 + MinorVersion。
ms.assetid: 0a22de88-4958-46be-82c3-6465aec86d33
title: Version9X 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1df599629fdf978837a8f53df7d1faa4f476db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991546"
---
# <a name="version9x-property"></a><span data-ttu-id="c9f63-103">Version9X 屬性</span><span class="sxs-lookup"><span data-stu-id="c9f63-103">Version9X property</span></span>

<span data-ttu-id="c9f63-104">**Version9X** 屬性可提供適用于9x 版本之 Windows 作業系統的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c9f63-104">The **Version9X** property gives the version number for 9x versions of Windows operating systems.</span></span>

<span data-ttu-id="c9f63-105">這個屬性的值是整數： MajorVersion \* 100 + MinorVersion。</span><span class="sxs-lookup"><span data-stu-id="c9f63-105">The value of this property is an integer: MajorVersion \* 100 + MinorVersion.</span></span> <span data-ttu-id="c9f63-106">如果作業系統不是9x 版本，屬性會保持未定義。</span><span class="sxs-lookup"><span data-stu-id="c9f63-106">The property remains undefined if the operating system is not a 9x version.</span></span> <span data-ttu-id="c9f63-107">如需詳細資訊，請參閱 [作業系統屬性值](operating-system-property-values.md)。</span><span class="sxs-lookup"><span data-stu-id="c9f63-107">For more information, see [Operating System Property Values](operating-system-property-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9f63-108">備註</span><span class="sxs-lookup"><span data-stu-id="c9f63-108">Remarks</span></span>

<span data-ttu-id="c9f63-109">條件運算式可以使用屬性名稱測試版本，也可以使用比較運算子來驗證版本。</span><span class="sxs-lookup"><span data-stu-id="c9f63-109">Condition expressions can test for the version by using the property name or may verify the version by using a comparison operator.</span></span>

<span data-ttu-id="c9f63-110">所有屬性名稱都會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c9f63-110">All property names are case-sensitive.</span></span> <span data-ttu-id="c9f63-111">請注意，名稱 **Version9X** 中的 X 為大寫。</span><span class="sxs-lookup"><span data-stu-id="c9f63-111">Note that the X in the name **Version9X** is uppercase.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9f63-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9f63-112">Requirements</span></span>



| <span data-ttu-id="c9f63-113">需求</span><span class="sxs-lookup"><span data-stu-id="c9f63-113">Requirement</span></span> | <span data-ttu-id="c9f63-114">值</span><span class="sxs-lookup"><span data-stu-id="c9f63-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f63-115">版本</span><span class="sxs-lookup"><span data-stu-id="c9f63-115">Version</span></span><br/> | <span data-ttu-id="c9f63-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c9f63-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c9f63-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c9f63-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c9f63-118">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="c9f63-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c9f63-119">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="c9f63-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9f63-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9f63-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f63-121">屬性</span><span class="sxs-lookup"><span data-stu-id="c9f63-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




