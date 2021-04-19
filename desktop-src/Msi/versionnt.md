---
description: 如果作業系統不是 Windows NT、Windows 2000、Windows XP、Windows Vista、Windows Server 2008 或 Windows 7，安裝程式會將 VersionNT 屬性設定為作業系統的版本號碼。
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: VersionNT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995328"
---
# <a name="versionnt-property"></a><span data-ttu-id="ae4ac-103">VersionNT 屬性</span><span class="sxs-lookup"><span data-stu-id="ae4ac-103">VersionNT property</span></span>

<span data-ttu-id="ae4ac-104">如果作業系統不是 Windows NT、Windows 2000、Windows XP、Windows Vista、Windows Server 2008 或 Windows 7，安裝程式會將 **VersionNT** 屬性設定為作業系統的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="ae4ac-104">The installer sets the **VersionNT** property to the version number for the operating system, undefined if the operating system is not Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008, or Windows 7.</span></span> <span data-ttu-id="ae4ac-105">此值為整數： MajorVersion \* 100 + MinorVersion。</span><span class="sxs-lookup"><span data-stu-id="ae4ac-105">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="ae4ac-106">相依于作業系統的條件陳述式可以使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="ae4ac-106">Conditional statements that depend upon the operating system can use this property.</span></span>

<span data-ttu-id="ae4ac-107">另請參閱 [作業系統屬性值](operating-system-property-values.md)。</span><span class="sxs-lookup"><span data-stu-id="ae4ac-107">See also [Operating System Property Values](operating-system-property-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ae4ac-108">備註</span><span class="sxs-lookup"><span data-stu-id="ae4ac-108">Remarks</span></span>

<span data-ttu-id="ae4ac-109">條件運算式可以使用屬性名稱來測試 Windows NT、Windows 2000 或 Windows XP，或可使用比較運算子來驗證版本。</span><span class="sxs-lookup"><span data-stu-id="ae4ac-109">Condition expressions can test for Windows NT, Windows 2000, or Windows XP by using the property name, or may verify the version by using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae4ac-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae4ac-110">Requirements</span></span>



| <span data-ttu-id="ae4ac-111">需求</span><span class="sxs-lookup"><span data-stu-id="ae4ac-111">Requirement</span></span> | <span data-ttu-id="ae4ac-112">值</span><span class="sxs-lookup"><span data-stu-id="ae4ac-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae4ac-113">版本</span><span class="sxs-lookup"><span data-stu-id="ae4ac-113">Version</span></span><br/> | <span data-ttu-id="ae4ac-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ae4ac-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ae4ac-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ae4ac-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ae4ac-116">Windows Installer 在 Windows Server 2003 或 Windows XP 上，請參閱 Windows Installer Run-Time Windows Installer 版本所需的最低 Windows service pack 相關資訊的 [需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="ae4ac-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae4ac-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae4ac-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae4ac-118">屬性</span><span class="sxs-lookup"><span data-stu-id="ae4ac-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




