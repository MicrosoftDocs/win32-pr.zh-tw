---
description: MSIRESTARTMANAGERCONTROL 屬性會指定 Windows Installer 封裝是使用 [重新開機管理員] 或 [FilesInUse] 對話方塊功能。
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: MSIRESTARTMANAGERCONTROL 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976189"
---
# <a name="msirestartmanagercontrol-property"></a><span data-ttu-id="10d3e-103">MSIRESTARTMANAGERCONTROL 屬性</span><span class="sxs-lookup"><span data-stu-id="10d3e-103">MSIRESTARTMANAGERCONTROL property</span></span>

<span data-ttu-id="10d3e-104">**MSIRESTARTMANAGERCONTROL** 屬性會指定 Windows Installer 封裝是使用 [[重新開機管理員](../rstmgr/restart-manager-portal.md)] 或 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)功能。</span><span class="sxs-lookup"><span data-stu-id="10d3e-104">The **MSIRESTARTMANAGERCONTROL** Property specifies whether the Windows Installer package uses the [Restart Manager](../rstmgr/restart-manager-portal.md) or [FilesInUse Dialog](filesinuse-dialog.md) functionality.</span></span>

## <a name="value"></a><span data-ttu-id="10d3e-105">值</span><span class="sxs-lookup"><span data-stu-id="10d3e-105">Value</span></span>



| <span data-ttu-id="10d3e-106">值</span><span class="sxs-lookup"><span data-stu-id="10d3e-106">Value</span></span>                                                                                        | <span data-ttu-id="10d3e-107">意義</span><span class="sxs-lookup"><span data-stu-id="10d3e-107">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="10d3e-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="10d3e-108"><dt>0</dt></span></span> </dl>                 | <span data-ttu-id="10d3e-109">如果未設定屬性，則這是預設值。</span><span class="sxs-lookup"><span data-stu-id="10d3e-109">This is the default value if the property is not set.</span></span> <span data-ttu-id="10d3e-110">Windows Installer 一律會嘗試在 Windows Vista 上使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="10d3e-110">Windows Installer always attempts to use the [Restart Manager](../rstmgr/restart-manager-portal.md) on Windows Vista.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="10d3e-111"><dt>停用</dt></span><span class="sxs-lookup"><span data-stu-id="10d3e-111"><dt>"Disable"</dt></span></span> </dl>         | <span data-ttu-id="10d3e-112">停用 [重新開機管理員](../rstmgr/restart-manager-portal.md)與封裝的互動。</span><span class="sxs-lookup"><span data-stu-id="10d3e-112">Disables interaction of the package with the [Restart Manager](../rstmgr/restart-manager-portal.md).</span></span> <span data-ttu-id="10d3e-113">Windows Installer 使用 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)。</span><span class="sxs-lookup"><span data-stu-id="10d3e-113">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="10d3e-114"><dt>"DisableShutdown"</dt></span><span class="sxs-lookup"><span data-stu-id="10d3e-114"><dt>"DisableShutdown"</dt></span></span> </dl> | <span data-ttu-id="10d3e-115">Windows Installer 使用 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)。</span><span class="sxs-lookup"><span data-stu-id="10d3e-115">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="10d3e-116">這項設定會在安裝未撰寫為使用重新開機管理員的 Windows Installer 套件時，停用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 可減輕重新開機的嘗試。</span><span class="sxs-lookup"><span data-stu-id="10d3e-116">This setting disables attempts by the [Restart Manager](../rstmgr/restart-manager-portal.md) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="10d3e-117">安裝程式仍會使用重新開機管理員來偵測應用程式所使用的檔案。</span><span class="sxs-lookup"><span data-stu-id="10d3e-117">The installer still uses the Restart Manager to detect files in use by applications.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="10d3e-118">備註</span><span class="sxs-lookup"><span data-stu-id="10d3e-118">Remarks</span></span>

<span data-ttu-id="10d3e-119">如果 [重新開機管理員](../rstmgr/restart-manager-portal.md)無法使用或停用，則會忽略 **MSIRESTARTMANAGERCONTROL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="10d3e-119">The **MSIRESTARTMANAGERCONTROL** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

<span data-ttu-id="10d3e-120">您可以使用自訂轉換或升級來修改此屬性的值。</span><span class="sxs-lookup"><span data-stu-id="10d3e-120">The value of this property can be modified using customization transforms or upgrades.</span></span> <span data-ttu-id="10d3e-121">從自訂動作變更這個屬性的值沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="10d3e-121">Changing the value of this property from custom actions has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d3e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="10d3e-122">Requirements</span></span>



| <span data-ttu-id="10d3e-123">需求</span><span class="sxs-lookup"><span data-stu-id="10d3e-123">Requirement</span></span> | <span data-ttu-id="10d3e-124">值</span><span class="sxs-lookup"><span data-stu-id="10d3e-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d3e-125">版本</span><span class="sxs-lookup"><span data-stu-id="10d3e-125">Version</span></span><br/> | <span data-ttu-id="10d3e-126">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="10d3e-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="10d3e-127">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="10d3e-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="10d3e-128">如需 Windows Installer 版本所需的最低 service pack 資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="10d3e-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10d3e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10d3e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d3e-130">屬性</span><span class="sxs-lookup"><span data-stu-id="10d3e-130">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="10d3e-131">DisableAutomaticApplicationShutdown</span><span class="sxs-lookup"><span data-stu-id="10d3e-131">DisableAutomaticApplicationShutdown</span></span>](disableautomaticapplicationshutdown.md)
</dt> <dt>

[<span data-ttu-id="10d3e-132">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="10d3e-132">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
