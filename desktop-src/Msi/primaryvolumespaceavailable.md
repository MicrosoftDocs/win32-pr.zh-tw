---
description: 安裝程式會將 PrimaryVolumeSpaceAvailable 屬性的值設定為字串，該字串代表 PrimaryVolumePath 屬性所參考之磁片區上可用的位元組總數（單位為512）。
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: PrimaryVolumeSpaceAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998806"
---
# <a name="primaryvolumespaceavailable-property"></a><span data-ttu-id="42f40-103">PrimaryVolumeSpaceAvailable 屬性</span><span class="sxs-lookup"><span data-stu-id="42f40-103">PrimaryVolumeSpaceAvailable property</span></span>

<span data-ttu-id="42f40-104">安裝程式會將 **PrimaryVolumeSpaceAvailable** 屬性的值設定為字串，該字串代表 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考之磁片區上可用的位元組總數（單位為512）。</span><span class="sxs-lookup"><span data-stu-id="42f40-104">The installer sets the value of the **PrimaryVolumeSpaceAvailable** property to a string that represents the total number of bytes available, in units of 512, on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="42f40-105">備註</span><span class="sxs-lookup"><span data-stu-id="42f40-105">Remarks</span></span>

<span data-ttu-id="42f40-106">例如，如果 [**PrimaryVolumePath**](primaryvolumepath.md) 設定為 "D："，且磁片區 D：有446134272個位元組可用，則 **PrimaryVolumeSpaceAvailable** 會設定為871356。</span><span class="sxs-lookup"><span data-stu-id="42f40-106">For example, if [**PrimaryVolumePath**](primaryvolumepath.md) is set to "D:", and volume D: has 446,134,272 bytes free, **PrimaryVolumeSpaceAvailable** is set to 871356.</span></span>

<span data-ttu-id="42f40-107">注意：如果此值要顯示在靜態 [文字控制項](text-control.md)內，則可以使用 [FormatSize](formatsize-control-attribute.md) 位自動格式化，並以適當的單位（kb 或 mb）標記此數位。</span><span class="sxs-lookup"><span data-stu-id="42f40-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="42f40-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="42f40-108">Requirements</span></span>



| <span data-ttu-id="42f40-109">需求</span><span class="sxs-lookup"><span data-stu-id="42f40-109">Requirement</span></span> | <span data-ttu-id="42f40-110">值</span><span class="sxs-lookup"><span data-stu-id="42f40-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f40-111">版本</span><span class="sxs-lookup"><span data-stu-id="42f40-111">Version</span></span><br/> | <span data-ttu-id="42f40-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="42f40-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="42f40-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="42f40-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="42f40-114">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="42f40-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="42f40-115">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="42f40-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42f40-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42f40-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f40-117">屬性</span><span class="sxs-lookup"><span data-stu-id="42f40-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




