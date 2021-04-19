---
description: 安裝程式會將 PrimaryVolumeSpaceRequired 屬性的值設定為字串，此字串代表 PrimaryVolumePath 屬性所參考之磁片區上所有選定功能所需的總位元組數。
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: PrimaryVolumeSpaceRequired 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001225"
---
# <a name="primaryvolumespacerequired-property"></a><span data-ttu-id="e54bd-103">PrimaryVolumeSpaceRequired 屬性</span><span class="sxs-lookup"><span data-stu-id="e54bd-103">PrimaryVolumeSpaceRequired property</span></span>

<span data-ttu-id="e54bd-104">安裝程式會將 **PrimaryVolumeSpaceRequired** 屬性的值設定為字串，此字串代表 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考之磁片區上所有選定功能所需的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="e54bd-104">The installer sets the value of the **PrimaryVolumeSpaceRequired** property to a string representing the total number of bytes required by all selected features on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span> <span data-ttu-id="e54bd-105">如同 [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) 屬性，此數位會以512個位元組的單位表示。</span><span class="sxs-lookup"><span data-stu-id="e54bd-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="e54bd-106">備註</span><span class="sxs-lookup"><span data-stu-id="e54bd-106">Remarks</span></span>

<span data-ttu-id="e54bd-107">注意：如果此值要顯示在靜態 [文字控制項](text-control.md)內，則可以使用 [FormatSize](formatsize-control-attribute.md) 位自動格式化，並以適當的單位（kb 或 mb）標記此數位。</span><span class="sxs-lookup"><span data-stu-id="e54bd-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e54bd-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="e54bd-108">Requirements</span></span>



| <span data-ttu-id="e54bd-109">需求</span><span class="sxs-lookup"><span data-stu-id="e54bd-109">Requirement</span></span> | <span data-ttu-id="e54bd-110">值</span><span class="sxs-lookup"><span data-stu-id="e54bd-110">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e54bd-111">版本</span><span class="sxs-lookup"><span data-stu-id="e54bd-111">Version</span></span><br/> | <span data-ttu-id="e54bd-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e54bd-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e54bd-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0。</span><span class="sxs-lookup"><span data-stu-id="e54bd-113">Windows Installer 4.0 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e54bd-114">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="e54bd-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e54bd-115">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="e54bd-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e54bd-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e54bd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54bd-117">屬性</span><span class="sxs-lookup"><span data-stu-id="e54bd-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




