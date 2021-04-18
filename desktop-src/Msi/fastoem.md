---
description: FASTOEM 屬性的設計目的是要讓 Oem 縮短為特定案例安裝 Windows Installer 應用程式所需的時間。
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: FASTOEM 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976251"
---
# <a name="fastoem-property"></a><span data-ttu-id="44606-103">FASTOEM 屬性</span><span class="sxs-lookup"><span data-stu-id="44606-103">FASTOEM property</span></span>

<span data-ttu-id="44606-104">**FASTOEM** 屬性的設計目的是要讓 oem 縮短為特定案例安裝 Windows Installer 應用程式所需的時間。</span><span class="sxs-lookup"><span data-stu-id="44606-104">The **FASTOEM** property is designed to enable OEMs to reduce the time it takes to install Windows Installer applications for a specific scenario.</span></span> <span data-ttu-id="44606-105">請勿將 **FASTOEM** 屬性撰寫至 [屬性資料表](property-table.md)。</span><span class="sxs-lookup"><span data-stu-id="44606-105">Do not author the **FASTOEM** property into the [Property Table](property-table.md).</span></span>

<span data-ttu-id="44606-106">只有在下列所有條件都成立時，才適用 **FASTOEM** 屬性：</span><span class="sxs-lookup"><span data-stu-id="44606-106">The **FASTOEM** property is only applicable if all of these conditions are true:</span></span>

-   <span data-ttu-id="44606-107">應用程式會安裝在與包含原始程式檔的資料夾相同的磁片區上。</span><span class="sxs-lookup"><span data-stu-id="44606-107">The application is being installed on the same volume as the folder containing the source files.</span></span>
-   <span data-ttu-id="44606-108">系統會在安裝後刪除來源檔案。</span><span class="sxs-lookup"><span data-stu-id="44606-108">The source files are deleted after the installation.</span></span>
-   <span data-ttu-id="44606-109">安裝期間不會顯示任何使用者介面。</span><span class="sxs-lookup"><span data-stu-id="44606-109">No user interface is displayed during the installation.</span></span> <span data-ttu-id="44606-110">[使用者介面層級](user-interface-levels.md)為 [無]。</span><span class="sxs-lookup"><span data-stu-id="44606-110">The [user interface level](user-interface-levels.md) is none.</span></span>
-   <span data-ttu-id="44606-111">安裝會在每一電腦的 [安裝內容](installation-context.md)中執行。</span><span class="sxs-lookup"><span data-stu-id="44606-111">The installation is performed in the per-machine [installation context](installation-context.md).</span></span>
-   <span data-ttu-id="44606-112">電腦上有足夠的空間可順利安裝。</span><span class="sxs-lookup"><span data-stu-id="44606-112">There is enough space on the computer for a successful installation.</span></span>
-   <span data-ttu-id="44606-113">這是第一次安裝。</span><span class="sxs-lookup"><span data-stu-id="44606-113">This is first time installation.</span></span> <span data-ttu-id="44606-114">安裝未公告、重新安裝、移除或執行系統管理安裝。</span><span class="sxs-lookup"><span data-stu-id="44606-114">The installation is not advertising, reinstalling, removing, or doing an administrative installation.</span></span>
-   <span data-ttu-id="44606-115">未安裝任何功能以從來源執行。</span><span class="sxs-lookup"><span data-stu-id="44606-115">No features are installed to run from source.</span></span>
-   <span data-ttu-id="44606-116">安裝套件未包含任何 [獨立元件](isolated-components.md)。</span><span class="sxs-lookup"><span data-stu-id="44606-116">The installation package contains no [isolated components](isolated-components.md).</span></span> <span data-ttu-id="44606-117">因為隔離的元件需要來源檔案保持在來源，所以 **FASTOEM** 屬性目前無法與隔離的元件一起使用。</span><span class="sxs-lookup"><span data-stu-id="44606-117">Because isolated components require source files to remain located at the source, the **FASTOEM** property cannot currently be used with isolated components.</span></span>

<span data-ttu-id="44606-118">如果上述所有條件都成立，則設定 **FASTOEM** 屬性可讓 Windows Installer 藉由執行下列動作來改善效能：</span><span class="sxs-lookup"><span data-stu-id="44606-118">If all of the previous conditions are true, setting the **FASTOEM** property enables Windows Installer to improve performance by doing the following:</span></span>

-   <span data-ttu-id="44606-119">移動而不是複製相同磁片區上的檔案。</span><span class="sxs-lookup"><span data-stu-id="44606-119">Move rather than copy files on the same volume.</span></span> <span data-ttu-id="44606-120">這並不保證會移動所有檔案，而不是複製。</span><span class="sxs-lookup"><span data-stu-id="44606-120">This does not guarantee that all files are moved rather than copied.</span></span> <span data-ttu-id="44606-121">請注意，如果電腦有多個硬碟，您必須將命令列上的 [**ROOTDRIVE**](rootdrive.md) 屬性初始化到包含安裝來源的相同磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="44606-121">Note that if the computer has multiple hard drives, you must initialize the [**ROOTDRIVE**](rootdrive.md) property on the command line to the same drive containing the installation source.</span></span>
-   <span data-ttu-id="44606-122">從應用程式的來源清單中省略此來源，讓後續的重新安裝或維護安裝預設為 [媒體資料表](media-table.md)中指定的 cd-rom 來源。</span><span class="sxs-lookup"><span data-stu-id="44606-122">Omit this source from the application's source list so that subsequent reinstallation or maintenance installations default to the CD-ROM sources specified in the [Media Table](media-table.md).</span></span>
-   <span data-ttu-id="44606-123">簡化檔案 [成本](file-costing.md)。</span><span class="sxs-lookup"><span data-stu-id="44606-123">Streamline [file costing](file-costing.md).</span></span>
-   <span data-ttu-id="44606-124">隱藏從 Windows Installer 傳送至用戶端的進度訊息。</span><span class="sxs-lookup"><span data-stu-id="44606-124">Suppress progress messages sent from Windows Installer to the client.</span></span>

## <a name="remarks"></a><span data-ttu-id="44606-125">備註</span><span class="sxs-lookup"><span data-stu-id="44606-125">Remarks</span></span>

<span data-ttu-id="44606-126">由於設定 **FASTOEM** 時不會傳送任何進度訊息，因此建議作者手動將 Timeout 的1800值寫入至金鑰</span><span class="sxs-lookup"><span data-stu-id="44606-126">Because no progress messages are sent when **FASTOEM** is set, it is recommended that authors manually write a value of 1800 for Timeout into the key</span></span>

<span data-ttu-id="44606-127">**HKLM** \\**軟體** \\**原則** \\**Microsoft** \\**Windows** \\**安裝程式** \\**Timeout**</span><span class="sxs-lookup"><span data-stu-id="44606-127">**HKLM**\\**SoftWare**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**Timeout**</span></span>

<span data-ttu-id="44606-128">Timeout 是 **REG \_ DWORD** 型別。</span><span class="sxs-lookup"><span data-stu-id="44606-128">Timeout is a **REG\_DWORD** type.</span></span>

<span data-ttu-id="44606-129">若要在 Windows 2000 主控台的 [新增或移除程式] 中顯示應用程式大小，您必須手動將 EstimatedSize 的值寫入機碼</span><span class="sxs-lookup"><span data-stu-id="44606-129">To display the size of the application in Add or Remove Programs in the Windows 2000 Control Panel, you must manually write the value of EstimatedSize into the key</span></span>

<span data-ttu-id="44606-130">**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**卸載** \\**< *產品* 代碼 >**</span><span class="sxs-lookup"><span data-stu-id="44606-130">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\**<*Product Code*>**</span></span>

<span data-ttu-id="44606-131">這是 **REG \_ DWORD** 型別，等於應用程式大小（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="44606-131">This is a **REG\_DWORD** type and equals to the size of the application in Kbytes.</span></span> <span data-ttu-id="44606-132">安裝程式不會自動寫入此值。</span><span class="sxs-lookup"><span data-stu-id="44606-132">The installer does not automatically write this value.</span></span>

<span data-ttu-id="44606-133">如果傳送給終端使用者的 CD-ROM 將應用程式的安裝套件儲存在 CD-ROM 的根目錄，請使用下列範例命令列。</span><span class="sxs-lookup"><span data-stu-id="44606-133">Use the following example command line if the CD-ROM shipped to end users stores the application's installation package at the root of the CD-ROM.</span></span> <span data-ttu-id="44606-134">請注意，.msi 檔案的 [Media 資料表](media-table.md) 中的磁片區標籤必須與 cd-rom 的磁片區標籤相符。</span><span class="sxs-lookup"><span data-stu-id="44606-134">Note that the volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span>

<span data-ttu-id="44606-135">**Msiexec/I C： \\ TempImage \\package.msi/qn/LE logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 ROOTDRIVE = C：\\**</span><span class="sxs-lookup"><span data-stu-id="44606-135">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 ROOTDRIVE=C:\\**</span></span>

<span data-ttu-id="44606-136">如果安裝套件不是位於傳送給使用者的 CD-ROM 根目錄，請使用下列範例命令列。</span><span class="sxs-lookup"><span data-stu-id="44606-136">Use the following example command line if the installation package is not located at the root of the CD-ROM shipped to end users.</span></span> <span data-ttu-id="44606-137">在此情況下，您必須將 [**MEDIAPACKAGEPATH**](mediapackagepath.md) 屬性設定為安裝套件的路徑。</span><span class="sxs-lookup"><span data-stu-id="44606-137">You must set the [**MEDIAPACKAGEPATH**](mediapackagepath.md) property in this case to the path to the installation package.</span></span> <span data-ttu-id="44606-138">.Msi 檔案的 [媒體資料表](media-table.md) 中的磁片區標籤必須符合 cd-rom 的磁片區標籤。</span><span class="sxs-lookup"><span data-stu-id="44606-138">The volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span> <span data-ttu-id="44606-139">在此情況下，請遵循此範例。</span><span class="sxs-lookup"><span data-stu-id="44606-139">In this case follow this example.</span></span>

<span data-ttu-id="44606-140">**Msiexec/I C： \\ TempImage \\package.msi/qn/LE logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 MEDIAPACKAGEPATH = C： \\ TempImage \\package.msi ROOTDRIVE = c：\\**</span><span class="sxs-lookup"><span data-stu-id="44606-140">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 MEDIAPACKAGEPATH=C:\\TempImage\\package.msi ROOTDRIVE=C:\\**</span></span>

## <a name="requirements"></a><span data-ttu-id="44606-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="44606-141">Requirements</span></span>



| <span data-ttu-id="44606-142">需求</span><span class="sxs-lookup"><span data-stu-id="44606-142">Requirement</span></span> | <span data-ttu-id="44606-143">值</span><span class="sxs-lookup"><span data-stu-id="44606-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44606-144">版本</span><span class="sxs-lookup"><span data-stu-id="44606-144">Version</span></span><br/> | <span data-ttu-id="44606-145">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="44606-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="44606-146">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="44606-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="44606-147">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="44606-147">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="44606-148">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="44606-148">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44606-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44606-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44606-150">屬性</span><span class="sxs-lookup"><span data-stu-id="44606-150">Properties</span></span>](properties.md)
</dt> </dl>

 

 




