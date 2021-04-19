---
description: AdminProperties 應該撰寫在屬性工作表中。
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: AdminProperties 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000485"
---
# <a name="adminproperties-property"></a><span data-ttu-id="98f43-103">AdminProperties 屬性</span><span class="sxs-lookup"><span data-stu-id="98f43-103">AdminProperties property</span></span>

<span data-ttu-id="98f43-104">**AdminProperties** 應該撰寫在 [屬性工作表](property-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="98f43-104">The **AdminProperties** should be authored into the [Property Table](property-table.md).</span></span> <span data-ttu-id="98f43-105">**AdminProperties** 的值是以分號分隔的屬性名稱清單。</span><span class="sxs-lookup"><span data-stu-id="98f43-105">The value of **AdminProperties** is a list of property names separated by semicolons.</span></span> <span data-ttu-id="98f43-106">安裝程式會在 [系統管理安裝](administrative-installation.md)時儲存這些列出屬性的值。</span><span class="sxs-lookup"><span data-stu-id="98f43-106">The installer saves the values of these listed properties at the time of an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="98f43-107">當使用者從系統管理映射安裝時，安裝會使用屬性的儲存值，而不是 .msi 檔案中的值。</span><span class="sxs-lookup"><span data-stu-id="98f43-107">When users install from the administrative image, the installation uses the saved values of the properties, rather than the values in the .msi file.</span></span>

## <a name="remarks"></a><span data-ttu-id="98f43-108">備註</span><span class="sxs-lookup"><span data-stu-id="98f43-108">Remarks</span></span>

<span data-ttu-id="98f43-109">清單中的屬性名稱可以是大寫和小寫字母 (私用屬性) ，或) 全部大寫 (公用屬性。</span><span class="sxs-lookup"><span data-stu-id="98f43-109">The property names in the list can be uppercase and lowercase letters (private properties), or all uppercase (public properties).</span></span>

<span data-ttu-id="98f43-110">這個屬性絕不能以分號結尾。</span><span class="sxs-lookup"><span data-stu-id="98f43-110">This property must never end with a semicolon.</span></span>

## <a name="requirements"></a><span data-ttu-id="98f43-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="98f43-111">Requirements</span></span>



| <span data-ttu-id="98f43-112">需求</span><span class="sxs-lookup"><span data-stu-id="98f43-112">Requirement</span></span> | <span data-ttu-id="98f43-113">值</span><span class="sxs-lookup"><span data-stu-id="98f43-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f43-114">版本</span><span class="sxs-lookup"><span data-stu-id="98f43-114">Version</span></span><br/> | <span data-ttu-id="98f43-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="98f43-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="98f43-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="98f43-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="98f43-117">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="98f43-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="98f43-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="98f43-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98f43-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98f43-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f43-120">屬性</span><span class="sxs-lookup"><span data-stu-id="98f43-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




