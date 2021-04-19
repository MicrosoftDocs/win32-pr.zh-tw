---
description: PRIMARYFOLDER 是全域屬性，可讓作者指定主要資料夾以進行安裝。
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: PRIMARYFOLDER 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987037"
---
# <a name="primaryfolder-property"></a><span data-ttu-id="7f686-103">PRIMARYFOLDER 屬性</span><span class="sxs-lookup"><span data-stu-id="7f686-103">PRIMARYFOLDER property</span></span>

<span data-ttu-id="7f686-104">**PRIMARYFOLDER** 是全域屬性，可讓作者指定主要資料夾以進行安裝。</span><span class="sxs-lookup"><span data-stu-id="7f686-104">The **PRIMARYFOLDER** is a global property that allows the author to designate a primary folder for the installation.</span></span> <span data-ttu-id="7f686-105">這個屬性的值必須是存在於 [目錄資料表](directory-table.md)中之目錄的索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="7f686-105">The value for this property must be the key name of a directory that exists in the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="7f686-106">安裝程式會在設定 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性、 [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) 屬性、 [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) 屬性和 [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) 屬性的值時，使用主要資料夾的解析路徑來決定要使用的磁片區。</span><span class="sxs-lookup"><span data-stu-id="7f686-106">The installer uses the resolved path of the primary folder to determine which volume to use when setting the values of the [**PrimaryVolumePath**](primaryvolumepath.md) property, [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) property, and [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) property.</span></span> <span data-ttu-id="7f686-107">安裝程式會將這些後面的屬性值提供給使用者介面中的使用者，以協助他們管理磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="7f686-107">The installer provides the values of these latter properties to users in the user interface to help them manage disk space.</span></span> <span data-ttu-id="7f686-108">通常封裝作者可以選取最大的資料夾做為主要資料夾。</span><span class="sxs-lookup"><span data-stu-id="7f686-108">Commonly package authors can select the largest folder as the primary folder.</span></span>

<span data-ttu-id="7f686-109">這個屬性的值必須是 [目錄資料表](directory-table.md)中所找到目錄記錄的索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="7f686-109">The value for this property must be the key name of a directory record found in the [Directory table](directory-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f686-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f686-110">Requirements</span></span>



| <span data-ttu-id="7f686-111">需求</span><span class="sxs-lookup"><span data-stu-id="7f686-111">Requirement</span></span> | <span data-ttu-id="7f686-112">值</span><span class="sxs-lookup"><span data-stu-id="7f686-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f686-113">版本</span><span class="sxs-lookup"><span data-stu-id="7f686-113">Version</span></span><br/> | <span data-ttu-id="7f686-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="7f686-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7f686-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="7f686-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7f686-116">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="7f686-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7f686-117">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="7f686-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f686-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f686-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f686-119">屬性</span><span class="sxs-lookup"><span data-stu-id="7f686-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




