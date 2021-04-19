---
description: 安裝程式會將 WindowsVolume 屬性設定為 windows 資料夾的磁片區。
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: WindowsVolume 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000408"
---
# <a name="windowsvolume-property"></a><span data-ttu-id="f0cfa-103">WindowsVolume 屬性</span><span class="sxs-lookup"><span data-stu-id="f0cfa-103">WindowsVolume property</span></span>

<span data-ttu-id="f0cfa-104">安裝程式會將 **WindowsVolume** 屬性設定為 windows 資料夾的磁片區。</span><span class="sxs-lookup"><span data-stu-id="f0cfa-104">The installer sets the **WindowsVolume** property to the volume of the windows folder.</span></span> <span data-ttu-id="f0cfa-105">屬性一律以反斜線結尾。</span><span class="sxs-lookup"><span data-stu-id="f0cfa-105">The property always ends with a backslash.</span></span> <span data-ttu-id="f0cfa-106">這可以用來設定 Windows 資料夾所在磁片區的預設位置，因為 [**ROOTDRIVE**](rootdrive.md) 屬性不一定等於此磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f0cfa-106">This can be used to set the default location to the volume the Windows folder is on because the [**ROOTDRIVE**](rootdrive.md) property does not necessarily equal this drive.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0cfa-107">備註</span><span class="sxs-lookup"><span data-stu-id="f0cfa-107">Remarks</span></span>

<span data-ttu-id="f0cfa-108">請勿在 [目錄](directory-table.md)資料表的目錄資料行中使用 **WindowsVolume** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f0cfa-108">Do not use the **WindowsVolume** property in the Directory column of the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="f0cfa-109">[**WindowsFolder**](windowsfolder.md)屬性包含 Windows 資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="f0cfa-109">The [**WindowsFolder**](windowsfolder.md) property contains the path to the Windows folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0cfa-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0cfa-110">Requirements</span></span>



| <span data-ttu-id="f0cfa-111">需求</span><span class="sxs-lookup"><span data-stu-id="f0cfa-111">Requirement</span></span> | <span data-ttu-id="f0cfa-112">值</span><span class="sxs-lookup"><span data-stu-id="f0cfa-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0cfa-113">版本</span><span class="sxs-lookup"><span data-stu-id="f0cfa-113">Version</span></span><br/> | <span data-ttu-id="f0cfa-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="f0cfa-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f0cfa-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="f0cfa-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f0cfa-116">Windows Installer 在 Windows Server 2003 或 Windows XP 上，請參閱 Windows Installer Run-Time Windows Installer 版本所需的最低 Windows service pack 相關資訊的 [需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="f0cfa-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f0cfa-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0cfa-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0cfa-118">屬性</span><span class="sxs-lookup"><span data-stu-id="f0cfa-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




