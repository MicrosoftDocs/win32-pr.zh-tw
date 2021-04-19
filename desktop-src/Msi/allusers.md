---
Description: ALLUSERS 屬性會設定封裝的安裝內容。
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: ALLUSERS 屬性
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987831"
---
# <a name="allusers-property"></a><span data-ttu-id="d3ba3-103">ALLUSERS 屬性</span><span class="sxs-lookup"><span data-stu-id="d3ba3-103">ALLUSERS property</span></span>

<span data-ttu-id="d3ba3-104">**ALLUSERS** 屬性會設定封裝的安裝內容。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-104">The **ALLUSERS** property configures the installation context of the package.</span></span> <span data-ttu-id="d3ba3-105">Windows Installer 會根據使用者的存取權限來執行每個使用者安裝或個別電腦安裝、是否需要較高的許可權才能安裝應用程式、 **ALLUSERS** 屬性的值、 [**MSIINSTALLPERUSER**](msiinstallperuser.md) 屬性的值和作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-105">The Windows Installer performs a per-user installation or per-machine installation depending on the access privileges of the user, whether elevated privileges are required to install the application, the value of the **ALLUSERS** property, the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property and the version of the operating system.</span></span>

<span data-ttu-id="d3ba3-106">在安裝時， **ALLUSERS** 屬性的值會決定 [安裝內容](installation-context.md)。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-106">The value of the **ALLUSERS** property, at installation time, determines the [installation context](installation-context.md).</span></span>

-   <span data-ttu-id="d3ba3-107">**ALLUSERS** 屬性值1會指定每部電腦的安裝內容。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-107">An **ALLUSERS** property value of 1 specifies the per-machine installation context.</span></span>
-   <span data-ttu-id="d3ba3-108">空字串 ( "" ) 指定每個使用者安裝內容的 **ALLUSERS** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-108">An **ALLUSERS** property value of an empty string ("") specifies the per-user installation context.</span></span>
-   <span data-ttu-id="d3ba3-109">如果 **allusers** 屬性的值設定為2，Windows Installer 一律會將 **allusers** 屬性的值重設為1，然後執行每一電腦安裝，或是將 **allusers** 屬性的值重設為空字串 ( "" ) 並執行每個使用者安裝。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-109">If the value of the **ALLUSERS** property is set to 2, the Windows Installer always resets the value of the **ALLUSERS** property to 1 and performs a per-machine installation or it resets the value of the **ALLUSERS** property to an empty string ("") and performs a per-user installation.</span></span> <span data-ttu-id="d3ba3-110">ALLUSERS = 2 的值可讓系統重設 **allusers** 的值和安裝內容，取決於使用者的許可權和 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-110">The value ALLUSERS=2 enables the system to reset the value of **ALLUSERS**, and the installation context, dependent upon the user's privileges and the version of Windows.</span></span>

    <span data-ttu-id="d3ba3-111">**Windows 7：** 將 **ALLUSERS** 屬性設定為2，即可使用 [**MSIINSTALLPERUSER**](msiinstallperuser.md) 屬性來指定安裝內容。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-111">**Windows 7:** Set the **ALLUSERS** property to 2 to use the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property to specify the installation context.</span></span> <span data-ttu-id="d3ba3-112">針對每部電腦安裝，將 **MSIINSTALLPERUSER** 屬性設定為空字串 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-112">Set the **MSIINSTALLPERUSER** property to an empty string ("") for a per-machine installation.</span></span> <span data-ttu-id="d3ba3-113">針對每個使用者安裝，將 **MSIINSTALLPERUSER** 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-113">Set the **MSIINSTALLPERUSER** property to 1 for a per-user installation.</span></span> <span data-ttu-id="d3ba3-114">如果封裝已依照 [單一套件撰寫](single-package-authoring.md)中所述的開發指導方針撰寫，則擁有使用者存取權的使用者可以安裝到每個使用者的內容中，而不需要提供 UAC 認證。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-114">If the package has been written following the development guidelines described in [Single Package Authoring](single-package-authoring.md), users having user access can install into the per-user context without having to provide UAC credentials.</span></span> <span data-ttu-id="d3ba3-115">如果使用者具有使用者存取權限，則只有在 [UAC] 對話方塊中提供系統管理員認證時，安裝程式才會執行個別電腦安裝。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-115">If the user has user access privileges, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span>

    <span data-ttu-id="d3ba3-116">**Windows Vista：** 將 **ALLUSERS** 屬性設定為2，Windows Installer 符合 (UAC) 的 [*使用者帳戶控制*](u-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-116">**Windows Vista:** Set the **ALLUSERS** property to 2 and Windows Installer complies with [*User Account Control*](u-gly.md) (UAC).</span></span> <span data-ttu-id="d3ba3-117">如果使用者具有使用者存取權限，以及 ALLUSERS = 2，則安裝程式只會在提供系統管理員認證給 UAC 對話方塊時執行每部電腦安裝。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-117">If the user has user access privileges, and ALLUSERS=2, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span> <span data-ttu-id="d3ba3-118">如果啟用 UAC 且未提供正確的系統管理員認證，則安裝會失敗並出現錯誤，指出需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-118">If UAC is enabled and the correct Admin credentials are not provided, the installation fails with an error stating that administrator privileges are required.</span></span> <span data-ttu-id="d3ba3-119">如果登錄機碼、群組原則或控制台停用 UAC，則不會顯示 UAC 對話方塊，且安裝會失敗，並出現錯誤訊息，指出需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-119">If UAC is disabled by the registry key, group policy, or the control panel, the UAC dialog box is not displayed and the installation fails with an error stating that administrator privileges are required.</span></span>

    <span data-ttu-id="d3ba3-120">**WINDOWS XP：** 如果使用者具有使用者存取權限，請將 **ALLUSERS** 屬性設定為2，Windows Installer 執行每個使用者安裝。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-120">**Windows XP:** Set the **ALLUSERS** property to 2 and Windows Installer performs a per-user installation if the user has user access privileges.</span></span>

-   <span data-ttu-id="d3ba3-121">如果 **ALLUSERS** 屬性的值不等於2，Windows Installer 會忽略 [**MSIINSTALLPERUSER**](msiinstallperuser.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-121">If the value of the **ALLUSERS** property does not equal 2, the Windows Installer ignores the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property.</span></span>

## <a name="example"></a><span data-ttu-id="d3ba3-122">範例</span><span class="sxs-lookup"><span data-stu-id="d3ba3-122">Example</span></span>

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

<span data-ttu-id="d3ba3-123">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-123">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) on GitHub.</span></span>

## <a name="default-value"></a><span data-ttu-id="d3ba3-124">預設值</span><span class="sxs-lookup"><span data-stu-id="d3ba3-124">Default Value</span></span>

<span data-ttu-id="d3ba3-125">建議的預設安裝內容為每位使用者。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-125">The recommended default installation context is per-user.</span></span> <span data-ttu-id="d3ba3-126">如果未設定 **ALLUSERS** ，安裝程式會執行每個使用者安裝。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-126">If **ALLUSERS** is not set, the installer does a per-user installation.</span></span> <span data-ttu-id="d3ba3-127">您可以將值設為空字串 ( "" ) ，ALLUSERS = ""，以確定尚未設定 **ALLUSERS** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-127">You can ensure the **ALLUSERS** property has not been set by setting its value to an empty string (""), ALLUSERS="".</span></span>

## <a name="remarks"></a><span data-ttu-id="d3ba3-128">備註</span><span class="sxs-lookup"><span data-stu-id="d3ba3-128">Remarks</span></span>

<span data-ttu-id="d3ba3-129">[安裝內容](installation-context.md)會決定 [**DesktopFolder**](desktopfolder.md)、 [**ProgramMenuFolder**](programmenufolder.md)、 [**StartMenuFolder**](startmenufolder.md)、 [**StartupFolder**](startupfolder.md)、 [**TemplateFolder**](templatefolder.md)、 [**AdminToolsFolder**](admintoolsfolder.md)、 [**ProgramFilesFolder**](programfilesfolder.md)、 [**CommonFilesFolder**](commonfilesfolder.md)、 [**ProgramFiles64Folder**](programfiles64folder.md)和 [**CommonFiles64Folder**](commonfiles64folder.md)屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-129">The [installation context](installation-context.md) determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="d3ba3-130">安裝內容會決定登錄的部分，其中登錄 [表](registry-table.md) 和 [RemoveRegistry 資料表](removeregistry-table.md)中的專案（在根資料行中為-1）會寫入或移除。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-130">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ba3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3ba3-131">Requirements</span></span>



| <span data-ttu-id="d3ba3-132">需求</span><span class="sxs-lookup"><span data-stu-id="d3ba3-132">Requirement</span></span> | <span data-ttu-id="d3ba3-133">值</span><span class="sxs-lookup"><span data-stu-id="d3ba3-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ba3-134">版本</span><span class="sxs-lookup"><span data-stu-id="d3ba3-134">Version</span></span><br/> | <span data-ttu-id="d3ba3-135">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d3ba3-136">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d3ba3-137">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d3ba3-138">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="d3ba3-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3ba3-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3ba3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ba3-140">屬性</span><span class="sxs-lookup"><span data-stu-id="d3ba3-140">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d3ba3-141">**MSIINSTALLPERUSER**</span><span class="sxs-lookup"><span data-stu-id="d3ba3-141">**MSIINSTALLPERUSER**</span></span>](msiinstallperuser.md)
</dt> <dt>

[<span data-ttu-id="d3ba3-142">安裝內容</span><span class="sxs-lookup"><span data-stu-id="d3ba3-142">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="d3ba3-143">單一套件撰寫</span><span class="sxs-lookup"><span data-stu-id="d3ba3-143">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




