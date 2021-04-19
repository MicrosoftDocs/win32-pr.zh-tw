---
description: 安裝程式會將 System64Folder 屬性設定為預先定義之 System64 資料夾的完整路徑。 現有的 System64Folder 屬性會設定為對應的32位資料夾。
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: System64Folder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995966"
---
# <a name="system64folder-property"></a><span data-ttu-id="49d39-104">System64Folder 屬性</span><span class="sxs-lookup"><span data-stu-id="49d39-104">System64Folder property</span></span>

<span data-ttu-id="49d39-105">安裝程式會將 **System64Folder** 屬性設定為預先定義之 System64 資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="49d39-105">The installer sets the **System64Folder** property to the full path to the predefined System64 folder.</span></span> <span data-ttu-id="49d39-106">現有的 **System64Folder** 屬性會設定為對應的32位資料夾。</span><span class="sxs-lookup"><span data-stu-id="49d39-106">The existing **System64Folder** property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="49d39-107">備註</span><span class="sxs-lookup"><span data-stu-id="49d39-107">Remarks</span></span>

<span data-ttu-id="49d39-108">安裝程式會在64位 Windows 上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="49d39-108">The installer sets this property on 64-bit Windows.</span></span> <span data-ttu-id="49d39-109">例如，在64位的 Windows 上，此值可能是 C： \\ Window \\ System32。</span><span class="sxs-lookup"><span data-stu-id="49d39-109">For example, on 64-bit Windows, the value may be C:\\Window\\System32.</span></span> <span data-ttu-id="49d39-110">這個屬性不會用於32位的 Windows 上。</span><span class="sxs-lookup"><span data-stu-id="49d39-110">This property is not used on 32-bit Windows.</span></span>

<span data-ttu-id="49d39-111">此資料夾通常是 Windows 資料夾的子目錄。</span><span class="sxs-lookup"><span data-stu-id="49d39-111">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="49d39-112">不過，它會在設定共用視窗時位於伺服器上。</span><span class="sxs-lookup"><span data-stu-id="49d39-112">However, it resides on a server when configured for Shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="49d39-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="49d39-113">Requirements</span></span>



| <span data-ttu-id="49d39-114">需求</span><span class="sxs-lookup"><span data-stu-id="49d39-114">Requirement</span></span> | <span data-ttu-id="49d39-115">值</span><span class="sxs-lookup"><span data-stu-id="49d39-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49d39-116">版本</span><span class="sxs-lookup"><span data-stu-id="49d39-116">Version</span></span><br/> | <span data-ttu-id="49d39-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="49d39-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="49d39-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="49d39-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="49d39-119">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="49d39-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="49d39-120">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="49d39-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49d39-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49d39-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d39-122">屬性</span><span class="sxs-lookup"><span data-stu-id="49d39-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




