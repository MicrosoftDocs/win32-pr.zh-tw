---
description: 安裝程式會將 ProgramFiles64Folder 屬性設定為預先定義之64位 Program Files 資料夾的完整路徑。 現有的 ProgramFilesFolder 屬性會設定為對應的32位資料夾。
ms.assetid: 9301628a-3d56-4d0a-aab5-88663742daa1
title: ProgramFiles64Folder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb8b85e0a433a3a4b51cfe23ef2de1f75dba09c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993522"
---
# <a name="programfiles64folder-property"></a><span data-ttu-id="f6757-104">ProgramFiles64Folder 屬性</span><span class="sxs-lookup"><span data-stu-id="f6757-104">ProgramFiles64Folder property</span></span>

<span data-ttu-id="f6757-105">安裝程式會將 **ProgramFiles64Folder** 屬性設定為預先定義之64位 Program Files 資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f6757-105">The installer sets the **ProgramFiles64Folder** property to the full path of the predefined 64-bit Program Files folder.</span></span> <span data-ttu-id="f6757-106">現有的 [**ProgramFilesFolder**](programfilesfolder.md) 屬性會設定為對應的32位資料夾。</span><span class="sxs-lookup"><span data-stu-id="f6757-106">The existing [**ProgramFilesFolder**](programfilesfolder.md) property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6757-107">備註</span><span class="sxs-lookup"><span data-stu-id="f6757-107">Remarks</span></span>

<span data-ttu-id="f6757-108">安裝程式會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f6757-108">The installer sets this property.</span></span> <span data-ttu-id="f6757-109">例如，在64位的 Windows 上，此值可能是 C： \\ Program Files。</span><span class="sxs-lookup"><span data-stu-id="f6757-109">For example, on 64-bit Windows, the value may be C:\\Program Files.</span></span> <span data-ttu-id="f6757-110">這個屬性不會用於32位的 Windows 上。</span><span class="sxs-lookup"><span data-stu-id="f6757-110">This property is not used on 32-bit Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6757-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6757-111">Requirements</span></span>



| <span data-ttu-id="f6757-112">需求</span><span class="sxs-lookup"><span data-stu-id="f6757-112">Requirement</span></span> | <span data-ttu-id="f6757-113">值</span><span class="sxs-lookup"><span data-stu-id="f6757-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6757-114">版本</span><span class="sxs-lookup"><span data-stu-id="f6757-114">Version</span></span><br/> | <span data-ttu-id="f6757-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="f6757-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f6757-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="f6757-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f6757-117">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="f6757-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f6757-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6757-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6757-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6757-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6757-120">屬性</span><span class="sxs-lookup"><span data-stu-id="f6757-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




