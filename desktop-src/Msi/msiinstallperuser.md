---
description: 使用者可以在安裝時，透過使用者介面或命令列來設定 MSIINSTALLPERUSER 和 ALLUSERS 屬性，以要求 Windows Installer 為目前的使用者或電腦的所有使用者安裝雙重用途的封裝。
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: MSIINSTALLPERUSER 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998721"
---
# <a name="msiinstallperuser-property"></a><span data-ttu-id="1faa6-103">MSIINSTALLPERUSER 屬性</span><span class="sxs-lookup"><span data-stu-id="1faa6-103">MSIINSTALLPERUSER property</span></span>

<span data-ttu-id="1faa6-104">使用者可以在安裝時，透過使用者介面或命令列來設定 **MSIINSTALLPERUSER** 和 [**ALLUSERS**](allusers.md) 屬性，以要求 Windows Installer 為目前的使用者或電腦的所有使用者安裝雙重用途的封裝。</span><span class="sxs-lookup"><span data-stu-id="1faa6-104">The **MSIINSTALLPERUSER** and the [**ALLUSERS**](allusers.md) properties can be set by the user at installation time, through the user interface or on a command line, to request that the Windows Installer install a dual-purpose package for the current user or all users of the computer.</span></span> <span data-ttu-id="1faa6-105">若要使用 **MSIINSTALLPERUSER** 屬性， [**ALLUSERS**](allusers.md) 屬性的值必須是2，而封裝必須經過撰寫，才能安裝到每位使用者或每一電腦的內容中。</span><span class="sxs-lookup"><span data-stu-id="1faa6-105">To use the **MSIINSTALLPERUSER** property, the value of the [**ALLUSERS**](allusers.md) property must be 2 and the package has to have been authored to be capable of installation into either the per-user or a per-machine context.</span></span> <span data-ttu-id="1faa6-106">如需撰寫雙重用途封裝的相關資訊，請參閱 [單一封裝撰寫](single-package-authoring.md)。</span><span class="sxs-lookup"><span data-stu-id="1faa6-106">For information about authoring a dual-purpose package, see [Single Package Authoring](single-package-authoring.md).</span></span> <span data-ttu-id="1faa6-107">如果 **ALLUSERS** 屬性的值不等於2，就會忽略 **MSIINSTALLPERUSER** 屬性的值，而且不會影響安裝。</span><span class="sxs-lookup"><span data-stu-id="1faa6-107">If the value of the **ALLUSERS** property does not equal 2, the value of the **MSIINSTALLPERUSER** property is ignored and has no effect on the installation.</span></span> <span data-ttu-id="1faa6-108">使用 Windows Installer 4.5 或更早版本安裝封裝時，會忽略 **MSIINSTALLPERUSER** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1faa6-108">The value of **MSIINSTALLPERUSER** property is ignored when installing the package using Windows Installer 4.5 or earlier.</span></span>

<span data-ttu-id="1faa6-109">若要要求 Windows Installer 在每部電腦 [安裝內容](installation-context.md)中安裝雙重用途套件，使用者可以使用撰寫的使用者介面或命令列，將 **MSIINSTALLPERUSER** 屬性的值設定為空字串 ( "" ) 以及 [**ALLUSERS**](allusers.md) 屬性的值設定為2。</span><span class="sxs-lookup"><span data-stu-id="1faa6-109">To request that the Windows Installer install the dual-purpose package in the per-machine [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to an empty string ("") and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="1faa6-110">若要要求 Windows Installer 在每個使用者 [安裝內容](installation-context.md)中安裝雙重用途封裝，使用者可以使用撰寫的使用者介面或命令列，將 **MSIINSTALLPERUSER** 屬性的值設定為1，並將 [**ALLUSERS**](allusers.md) 屬性的值設定為2。</span><span class="sxs-lookup"><span data-stu-id="1faa6-110">To request that the Windows Installer install the dual-purpose package in the per-user [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to 1 and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="1faa6-111">如果 [**ALLUSERS**](allusers.md) 屬性的值不等於2，Windows Installer 會忽略 **MSIINSTALLPERUSER** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1faa6-111">If the value of the [**ALLUSERS**](allusers.md) property does not equal 2, the Windows Installer ignores the value of the **MSIINSTALLPERUSER** property.</span></span> <span data-ttu-id="1faa6-112">如果 Windows Installer 將應用程式安裝在每部電腦的內容中，它會將 **ALLUSERS** 屬性的值重設為1。</span><span class="sxs-lookup"><span data-stu-id="1faa6-112">If Windows Installer installs the application in the per-machine context, it resets the value of the **ALLUSERS** property to 1.</span></span> <span data-ttu-id="1faa6-113">如果 Windows Installer 將應用程式安裝在每個使用者的內容中，它會將 **ALLUSERS** 屬性的值重設為空字串 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="1faa6-113">If Windows Installer installs the application in the per-user context, it resets the value of the **ALLUSERS** property to an empty string ("").</span></span> <span data-ttu-id="1faa6-114">針對每位使用者安裝的應用程式，會收到每個使用者的所有更新或修復，以及每部電腦安裝的應用程式每一電腦的更新或修復。</span><span class="sxs-lookup"><span data-stu-id="1faa6-114">Applications that have been installed per-user therefore receive all updates or repairs on a per-user basis and applications installed per-machine receive updates or repairs on a per-machine basis.</span></span>

<span data-ttu-id="1faa6-115">**[Windows Installer 4.5 或更早](not-supported-in-windows-installer-4-5.md)版本：** Windows Installer 5.0 之前的版本會忽略 **MSIINSTALLPERUSER** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1faa6-115">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** The **MSIINSTALLPERUSER** property is ignored by versions earlier than Windows Installer 5.0.</span></span>

## <a name="default-value"></a><span data-ttu-id="1faa6-116">預設值</span><span class="sxs-lookup"><span data-stu-id="1faa6-116">Default Value</span></span>

<span data-ttu-id="1faa6-117">建議的預設安裝內容為每位使用者提供的雙重用途套件。</span><span class="sxs-lookup"><span data-stu-id="1faa6-117">The recommended default installation context is per-user for a dual-purpose package.</span></span> <span data-ttu-id="1faa6-118">在雙重用途封裝的 [屬性工作表](property-table.md) 中，Author MSIINSTALLPERUSER = 1 和 ALLUSERS = 2，以指定每位使用者作為預設安裝內容。</span><span class="sxs-lookup"><span data-stu-id="1faa6-118">Author MSIINSTALLPERUSER=1 and ALLUSERS=2 in the [Property table](property-table.md) of the dual-purpose package to specify per-user as the default installation context.</span></span>

## <a name="remarks"></a><span data-ttu-id="1faa6-119">備註</span><span class="sxs-lookup"><span data-stu-id="1faa6-119">Remarks</span></span>

<span data-ttu-id="1faa6-120">您可以將值設為空字串 ( "" ) ，MSIINSTALLPERUSER = ""，以確定尚未設定 **MSIINSTALLPERUSER** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1faa6-120">You can ensure the **MSIINSTALLPERUSER** property has not been set by setting its value to an empty string (""), MSIINSTALLPERUSER="".</span></span>

<span data-ttu-id="1faa6-121">安裝內容會決定 [**DesktopFolder**](desktopfolder.md)、 [**ProgramMenuFolder**](programmenufolder.md)、 [**StartMenuFolder**](startmenufolder.md)、 [**StartupFolder**](startupfolder.md)、 [**TemplateFolder**](templatefolder.md)、 [**AdminToolsFolder**](admintoolsfolder.md)、 [**ProgramFilesFolder**](programfilesfolder.md)、 [**CommonFilesFolder**](commonfilesfolder.md)、 [**ProgramFiles64Folder**](programfiles64folder.md)和 [**CommonFiles64Folder**](commonfiles64folder.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1faa6-121">The installation context determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="1faa6-122">安裝內容會決定登錄的部分，其中登錄 [表](registry-table.md) 和 [RemoveRegistry 資料表](removeregistry-table.md)中的專案（在根資料行中為-1）會寫入或移除。</span><span class="sxs-lookup"><span data-stu-id="1faa6-122">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span> <span data-ttu-id="1faa6-123">如需安裝內容的詳細資訊，請參閱 [安裝內容](installation-context.md)。</span><span class="sxs-lookup"><span data-stu-id="1faa6-123">For information about the installation context, see [Installation Context](installation-context.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1faa6-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1faa6-124">Requirements</span></span>



| <span data-ttu-id="1faa6-125">需求</span><span class="sxs-lookup"><span data-stu-id="1faa6-125">Requirement</span></span> | <span data-ttu-id="1faa6-126">值</span><span class="sxs-lookup"><span data-stu-id="1faa6-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1faa6-127">版本</span><span class="sxs-lookup"><span data-stu-id="1faa6-127">Version</span></span><br/> | <span data-ttu-id="1faa6-128">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="1faa6-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1faa6-129">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="1faa6-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1faa6-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1faa6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1faa6-131">屬性</span><span class="sxs-lookup"><span data-stu-id="1faa6-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="1faa6-132">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="1faa6-132">**ALLUSERS**</span></span>](allusers.md)
</dt> <dt>

[<span data-ttu-id="1faa6-133">安裝內容</span><span class="sxs-lookup"><span data-stu-id="1faa6-133">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="1faa6-134">單一套件撰寫</span><span class="sxs-lookup"><span data-stu-id="1faa6-134">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




