---
description: ROOTDRIVE 屬性會指定安裝目的地目錄的預設磁片磁碟機。
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: ROOTDRIVE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990570"
---
# <a name="rootdrive-property"></a><span data-ttu-id="8ab6e-103">ROOTDRIVE 屬性</span><span class="sxs-lookup"><span data-stu-id="8ab6e-103">ROOTDRIVE property</span></span>

<span data-ttu-id="8ab6e-104">**ROOTDRIVE** 屬性會指定安裝目的地目錄的預設磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8ab6e-104">The **ROOTDRIVE** property specifies the default drive for the destination directory of the installation.</span></span> <span data-ttu-id="8ab6e-105">如果 [目錄資料表](directory-table.md) 的目錄資料行以未定義的屬性名稱來指出根目的地目錄，安裝程式就會使用 **ROOTDRIVE** 屬性的值來解析目的地目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="8ab6e-105">If the Directory column of the [Directory table](directory-table.md) indicates the root destination directory by a property name that is undefined, the installer uses the value of the **ROOTDRIVE** property to resolve the path to the destination directory.</span></span>

<span data-ttu-id="8ab6e-106">如果未在命令列上設定 **ROOTDRIVE** ，或在 [屬性工作表](property-table.md)中撰寫，則安裝程式會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8ab6e-106">If **ROOTDRIVE** is not set at a command line or authored into the [Property table](property-table.md), the installer sets this property.</span></span> <span data-ttu-id="8ab6e-107">在 [系統管理安裝](administrative-installation.md) 期間，安裝程式會將 **ROOTDRIVE** 設定為第一個可寫入的連線網路磁碟機機。</span><span class="sxs-lookup"><span data-stu-id="8ab6e-107">During an [administrative installation](administrative-installation.md) the installer sets **ROOTDRIVE** to the first connected network drive it finds that can be written to.</span></span> <span data-ttu-id="8ab6e-108">如果它不是系統管理安裝，或是安裝程式找不到任何網路磁碟機機，則安裝程式會將 **ROOTDRIVE** 設定為可寫入至具有最多可用空間的本機磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8ab6e-108">If it is not an administrative installation, or if the installer can find no network drives, the installer sets **ROOTDRIVE** to the local drive that can be written to having the most free space.</span></span>

<span data-ttu-id="8ab6e-109">這個屬性的值必須以 ' ' 結尾 \\ 。</span><span class="sxs-lookup"><span data-stu-id="8ab6e-109">The value for this property must end with '\\'.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ab6e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ab6e-110">Requirements</span></span>



| <span data-ttu-id="8ab6e-111">需求</span><span class="sxs-lookup"><span data-stu-id="8ab6e-111">Requirement</span></span> | <span data-ttu-id="8ab6e-112">值</span><span class="sxs-lookup"><span data-stu-id="8ab6e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ab6e-113">版本</span><span class="sxs-lookup"><span data-stu-id="8ab6e-113">Version</span></span><br/> | <span data-ttu-id="8ab6e-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="8ab6e-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8ab6e-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="8ab6e-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8ab6e-116">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="8ab6e-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8ab6e-117">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="8ab6e-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ab6e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ab6e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ab6e-119">屬性</span><span class="sxs-lookup"><span data-stu-id="8ab6e-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




