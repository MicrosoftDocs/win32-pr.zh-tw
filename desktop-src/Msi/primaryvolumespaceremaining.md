---
description: 如果已安裝所有目前選取的功能，則安裝程式會將 PrimaryVolumeSpaceRemaining 屬性的值設為字串，代表 PrimaryVolumePath 屬性所參考的磁片區上剩餘的位元組總數。
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: PrimaryVolumeSpaceRemaining 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976280"
---
# <a name="primaryvolumespaceremaining-property"></a><span data-ttu-id="7b7c6-103">PrimaryVolumeSpaceRemaining 屬性</span><span class="sxs-lookup"><span data-stu-id="7b7c6-103">PrimaryVolumeSpaceRemaining property</span></span>

<span data-ttu-id="7b7c6-104">如果已安裝所有目前選取的功能，則安裝程式會將 **PrimaryVolumeSpaceRemaining** 屬性的值設為字串，代表 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考的磁片區上剩餘的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="7b7c6-104">The installer sets the value of the **PrimaryVolumeSpaceRemaining** property to a string representing the total number of bytes remaining on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property, if all currently selected features were installed.</span></span> <span data-ttu-id="7b7c6-105">如同 [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) 屬性，此數位會以512個位元組的單位表示。</span><span class="sxs-lookup"><span data-stu-id="7b7c6-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b7c6-106">備註</span><span class="sxs-lookup"><span data-stu-id="7b7c6-106">Remarks</span></span>

<span data-ttu-id="7b7c6-107">注意：如果此值要顯示在靜態 [文字控制項](text-control.md)內，則可以使用 [FormatSize](formatsize-control-attribute.md) 位自動格式化，並以適當的單位（kb 或 mb）標記此數位。</span><span class="sxs-lookup"><span data-stu-id="7b7c6-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b7c6-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b7c6-108">Requirements</span></span>



| <span data-ttu-id="7b7c6-109">需求</span><span class="sxs-lookup"><span data-stu-id="7b7c6-109">Requirement</span></span> | <span data-ttu-id="7b7c6-110">值</span><span class="sxs-lookup"><span data-stu-id="7b7c6-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b7c6-111">版本</span><span class="sxs-lookup"><span data-stu-id="7b7c6-111">Version</span></span><br/> | <span data-ttu-id="7b7c6-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="7b7c6-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7b7c6-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="7b7c6-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7b7c6-114">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7b7c6-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b7c6-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b7c6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b7c6-116">屬性</span><span class="sxs-lookup"><span data-stu-id="7b7c6-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




