---
description: 如果以應用程式傳送的安裝套件不是客戶所收到 CD-ROM 的根目錄，則必須在命令列上將 MEDIAPACKAGEPATH 屬性設定為 CD-ROM 上應用程式的相對路徑。例如，如果媒體上封裝的路徑是 E： \\ MyPath \\My.msi，則使用 MEDIAPACKAGEPATH =&\# 0034; \\MyPath \\ & \# 0034;。系統管理員可以從系統管理安裝點建立 CD-ROMs。 如果在新的 CD-ROM 上變更安裝根目錄的位置，則必須將 MEDIAPACKAGEPATH 屬性設為要從此媒體安裝的新路徑。 CD-ROM 上的位置與套件中指定的來源不同，無法使用。 不過，在從運送媒體建立系統管理安裝點時，並不需要使用此屬性。
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: MEDIAPACKAGEPATH 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000458"
---
# <a name="mediapackagepath-property"></a><span data-ttu-id="7ed48-106">MEDIAPACKAGEPATH 屬性</span><span class="sxs-lookup"><span data-stu-id="7ed48-106">MEDIAPACKAGEPATH property</span></span>

<span data-ttu-id="7ed48-107">如果以應用程式傳送的安裝套件不是客戶所收到 CD-ROM 的根目錄，則必須在命令列上將 **MEDIAPACKAGEPATH** 屬性設定為 cd-rom 上應用程式的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="7ed48-107">If the installation package shipping with an application is not at the root of the CD-ROM that customers receive, the **MEDIAPACKAGEPATH** property must be set on the command line to the relative path of the application on the CD-ROM.</span></span>

<span data-ttu-id="7ed48-108">例如，如果媒體上封裝的路徑是 E： \\ MyPath \\My.msi，則使用 MEDIAPACKAGEPATH = " \\ MyPath \\ "。</span><span class="sxs-lookup"><span data-stu-id="7ed48-108">For example, if the path to the package on the media is E:\\MyPath\\My.msi, then use MEDIAPACKAGEPATH="\\MyPath\\".</span></span>

<span data-ttu-id="7ed48-109">系統管理員可以從系統管理安裝點建立 CD-ROMs。</span><span class="sxs-lookup"><span data-stu-id="7ed48-109">Administrators may create CD-ROMs from an administrative installation point.</span></span> <span data-ttu-id="7ed48-110">如果在新的 CD-ROM 上變更安裝根目錄的位置，則必須將 **MEDIAPACKAGEPATH** 屬性設為要從此媒體安裝的新路徑。</span><span class="sxs-lookup"><span data-stu-id="7ed48-110">If the location of the root of the installation is changed on the new CD-ROMs, the **MEDIAPACKAGEPATH** property must be set to the new path to install from this media.</span></span> <span data-ttu-id="7ed48-111">CD-ROM 上的位置與套件中指定的來源不同，無法使用。</span><span class="sxs-lookup"><span data-stu-id="7ed48-111">A source with a location on the CD-ROM different than what is specified in the package is unusable.</span></span> <span data-ttu-id="7ed48-112">不過，在從運送媒體建立系統管理安裝點時，並不需要使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="7ed48-112">It is not necessary, however, to use this property when creating an administrative installation point from shipping media.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ed48-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ed48-113">Requirements</span></span>



| <span data-ttu-id="7ed48-114">需求</span><span class="sxs-lookup"><span data-stu-id="7ed48-114">Requirement</span></span> | <span data-ttu-id="7ed48-115">值</span><span class="sxs-lookup"><span data-stu-id="7ed48-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed48-116">版本</span><span class="sxs-lookup"><span data-stu-id="7ed48-116">Version</span></span><br/> | <span data-ttu-id="7ed48-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="7ed48-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7ed48-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="7ed48-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7ed48-119">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="7ed48-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7ed48-120">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="7ed48-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ed48-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ed48-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed48-122">屬性</span><span class="sxs-lookup"><span data-stu-id="7ed48-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




