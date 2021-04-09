---
title: '新功能 (IMAPI.EXE) '
description: 下表指出每個映射主控 API 版本的新功能。
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77abc9db0c9d976eef632034a5620520bb29d73d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103681491"
---
# <a name="whats-new-image-mastering-api"></a><span data-ttu-id="c9738-103">新功能：映射主控 API</span><span class="sxs-lookup"><span data-stu-id="c9738-103">What's New: Image Mastering API</span></span>

<span data-ttu-id="c9738-104">下表指出每個映射主控 API 版本的新功能。</span><span class="sxs-lookup"><span data-stu-id="c9738-104">The following table identifies what is new for each release of the Image Mastering API.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9738-105">版本</span><span class="sxs-lookup"><span data-stu-id="c9738-105">Version</span></span></th>
<th><span data-ttu-id="c9738-106">功能描述</span><span class="sxs-lookup"><span data-stu-id="c9738-106">Description of features</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9738-107">版本2。0</span><span class="sxs-lookup"><span data-stu-id="c9738-107">Version 2.0</span></span></td>
<td><span data-ttu-id="c9738-108">大部分的 API 都經過重新設計。</span><span class="sxs-lookup"><span data-stu-id="c9738-108">Much of the API has been redesigned.</span></span> <span data-ttu-id="c9738-109">版本2.0 仍提供大部分的1.0 版功能。</span><span class="sxs-lookup"><span data-stu-id="c9738-109">Most of the version 1.0 functionality is still available in version 2.0.</span></span> <span data-ttu-id="c9738-110">我們鼓勵這些撰寫映射主控應用程式或執行新的裝置和格式開發，以使用版本2.0，而不是1.0 版。</span><span class="sxs-lookup"><span data-stu-id="c9738-110">Those writing image mastering applications or performing new device and format development are encouraged to use version 2.0 instead of version 1.0.</span></span><br/> <span data-ttu-id="c9738-111">IMAPI.EXE 2.0 包含在 Windows Vista 中。</span><span class="sxs-lookup"><span data-stu-id="c9738-111">IMAPI 2.0 is included in Windows Vista.</span></span> <span data-ttu-id="c9738-112">針對 Windows XP 和 Windows Server 2003 啟用相同的功能需要安裝 <a href="https://support.microsoft.com/kb/932716">KB932716</a> 更新套件。</span><span class="sxs-lookup"><span data-stu-id="c9738-112">Enabling the same functionality for Windows XP and Windows Server 2003 requires the installation of the <a href="https://support.microsoft.com/kb/932716">KB932716</a> update package.</span></span><br/> <span data-ttu-id="c9738-113">Point-Release 附注：</span><span class="sxs-lookup"><span data-stu-id="c9738-113">Point-Release Notes:</span></span><br/>
<ul>
<li><span data-ttu-id="c9738-114">Windows Vista Service Pack 1 (SP1) 和 Windows Server 2008 中引進了透過 <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a> 介面提供多重開機支援的更新。</span><span class="sxs-lookup"><span data-stu-id="c9738-114">An update offering multi-boot support via the <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a> interface was introduced in Windows Vista with Service Pack 1 (SP1) and Windows Server 2008.</span></span><br/></li>
<li><span data-ttu-id="c9738-115">一項功能更新供應專案可支援 BD-R\BD-RE 格式、映射建立時的原始 CD 光碟，以及 <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Windows Feature Pack For Storage</a>中包含的燒錄驗證。</span><span class="sxs-lookup"><span data-stu-id="c9738-115">A feature update offering mastering support for the BD-R\BD-RE format, RAW CD Disc-at-Once image creation, as well as burn verification was included in the <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Windows Feature Pack for Storage</a>.</span></span> <span data-ttu-id="c9738-116">Windows Vista （含 SP1）、Windows XP Service Pack 2 (SP2) 和更新版本，以及 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本都支援此功能更新。</span><span class="sxs-lookup"><span data-stu-id="c9738-116">This feature update is supported on Windows Vista with SP1, Windows XP with Service Pack 2 (SP2) and later, and Windows Server 2003 with Service Pack 1 (SP1) and later.</span></span> <span data-ttu-id="c9738-117">此外，這些功能都包含在 Windows 7 和 Windows Server 2008 中。</span><span class="sxs-lookup"><span data-stu-id="c9738-117">Additionally, these features are included in Windows 7 and Windows Server 2008.</span></span><br/></li>
<li><span data-ttu-id="c9738-118">Windows 7 和 Windows Server 2008 原生的 IMAPI.EXE 2.0 功能包括音訊 cd 的「Gapless 燒錄」，以及燒錄作業期間的「雙隱藏」消除。</span><span class="sxs-lookup"><span data-stu-id="c9738-118">IMAPI 2.0 features native to Windows 7 and Windows Server 2008 include 'Gapless Burning' for audio cds and the elimination of 'Double Stashing' during burn operations.</span></span> <span data-ttu-id="c9738-119">雙隱藏是在較大的燒錄作業內進行的程式，在此作業中，每個檔案在燒錄到光碟之前都隱藏。使用最新版本的 IMAPI.EXE 2.0 時，會選擇性地選擇隱藏的檔案，並將其餘的檔案 (大部分的大型檔案) 非隱藏。</span><span class="sxs-lookup"><span data-stu-id="c9738-119">Double Stashing is a process, within the larger burn operation, in which every file is stashed before being burned to disc. With the latest version of IMAPI 2.0, files are selectively choosen for stashing, leaving the remaining files (mostly large files) non-stashed.</span></span> <span data-ttu-id="c9738-120">最終結果會儲存磁碟空間和作業時間。</span><span class="sxs-lookup"><span data-stu-id="c9738-120">The end result is saved disk space and operation time.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9738-121">版本 1.0</span><span class="sxs-lookup"><span data-stu-id="c9738-121">Version 1.0</span></span></td>
<td><span data-ttu-id="c9738-122">初始版本。</span><span class="sxs-lookup"><span data-stu-id="c9738-122">Initial release.</span></span> <span data-ttu-id="c9738-123">讓應用程式階段，並將簡單的音訊或資料影像燒錄到 CD-R 和 cd-rw 裝置。</span><span class="sxs-lookup"><span data-stu-id="c9738-123">Lets an application stage and burn a simple audio or data image to CD-R and CD-RW devices.</span></span> <span data-ttu-id="c9738-124">API 支援 Redbook 音訊和資料光碟的 Joliet 和 ISO 9660 格式。</span><span class="sxs-lookup"><span data-stu-id="c9738-124">The API supports the Joliet and ISO 9660 format for Redbook audio and data discs.</span></span> <span data-ttu-id="c9738-125">如需1.0 版的相關資訊，請參閱 <a href="imapiv1.md">IMAPIv1 支援</a>。包含在 Windows XP 中。</span><span class="sxs-lookup"><span data-stu-id="c9738-125">For information on version 1.0, see <a href="imapiv1.md">IMAPIv1 Support</a>.Included in Windows XP.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="version-20"></a><span data-ttu-id="c9738-126">版本2。0</span><span class="sxs-lookup"><span data-stu-id="c9738-126">Version 2.0</span></span>

-   <span data-ttu-id="c9738-127">允許應用程式燒錄至 DVD-R、DVD + R、DVD RW、DVD + RW、DVD + DL、DVD DL 和 DVD-ROM、bd 和 BD 媒體格式。</span><span class="sxs-lookup"><span data-stu-id="c9738-127">Allows applications to burn to the DVD-R, DVD+R, DVD-RW, DVD+RW, DVD+DL, DVD-DL, and DVD-RAM, BD-R, and BD-RE media formats.</span></span>
-   <span data-ttu-id="c9738-128">允許同時錄製至多個磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c9738-128">Allows recording to multiple drives at the same time.</span></span> <span data-ttu-id="c9738-129">在1.0 版中，IMAPI.EXE 一次只能使用一部系統上的燒錄機。</span><span class="sxs-lookup"><span data-stu-id="c9738-129">In version 1.0, only one recorder on the system could be used by IMAPI at one time.</span></span> <span data-ttu-id="c9738-130">如果您在 Windows Vista 上執行1.0 版的應用程式，其他應用程式可能會同時在系統中的其他磁片磁碟機上使用 IMAPI.EXE 1.0 或2.0 介面。</span><span class="sxs-lookup"><span data-stu-id="c9738-130">If you run a version 1.0 application on Windows Vista, other applications may concurrently use IMAPI 1.0 or 2.0 interfaces on other drives in the system.</span></span> <span data-ttu-id="c9738-131">雖然這通常會被視為一項優點，但依賴單一系統燒錄機行為的應用程式可能需要較小的更新。</span><span class="sxs-lookup"><span data-stu-id="c9738-131">While this is generally seen as a benefit, applications which relied upon the single system burner behavior may require minor updates.</span></span>
-   <span data-ttu-id="c9738-132">當錄製器將資訊寫入光碟時，會拒絕對錄製器的存取。否則，此錄製器可供其他用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="c9738-132">Access to a recorder is denied when the recorder is writing information to the disc. Otherwise, the recorder is available to other clients.</span></span>
-   <span data-ttu-id="c9738-133">在用戶端電腦上支援一個以上的隱藏檔案，而版本1.0 只允許一個全系統的隱藏檔案。</span><span class="sxs-lookup"><span data-stu-id="c9738-133">Supports more than one stash file on a client computer whereas version 1.0 allowed only one system-wide stash file.</span></span>
-   <span data-ttu-id="c9738-134">在 Windows Vista 中，1.0 版不再包含服務或核心模式的元件。</span><span class="sxs-lookup"><span data-stu-id="c9738-134">On Windows Vista, version 1.0 no longer contains service or kernel-mode components.</span></span> <span data-ttu-id="c9738-135">不過， [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) 介面仍會使用 ioctl 磁片 \_ \_ 獨佔 \_ 存取，而 ioctl \_ SCSI \_ 會 \_ 透過 \_ 直接命令傳遞，以管理特定磁片磁碟機裝置的存取或通訊。</span><span class="sxs-lookup"><span data-stu-id="c9738-135">However, the [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface still uses the IOCTL\_CDROM\_EXCLUSIVE\_ACCESS and IOCTL\_SCSI\_PASS\_THROUGH\_DIRECT commands to manage access or communication to specific drive devices.</span></span>
-   <span data-ttu-id="c9738-136">在 Windows Vista 上，版本1.0 介面現在會呼叫2.0 版介面。</span><span class="sxs-lookup"><span data-stu-id="c9738-136">On Windows Vista, the version 1.0 interfaces now call the version 2.0 interfaces.</span></span>
-   <span data-ttu-id="c9738-137">隨附于 Windows Vista SP1 和 Windows Server 2008 的 IMAPI.EXE 版本2.0 透過 [**IFileSystemImage2**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2) 介面提供多重開機支援。</span><span class="sxs-lookup"><span data-stu-id="c9738-137">Included with Windows Vista with SP1 and Windows Server 2008, IMAPI vesion 2.0 offers multiboot support via the [**IFileSystemImage2**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2) interface.</span></span>
-   <span data-ttu-id="c9738-138">允許針對音訊 Cd 使用「Gapless 燒錄」。</span><span class="sxs-lookup"><span data-stu-id="c9738-138">Allows the use of 'Gapless Burning' for audio CDs.</span></span> <span data-ttu-id="c9738-139">使用 Gapless 燒錄，可以移除音訊播放軌之間的聲音間距。</span><span class="sxs-lookup"><span data-stu-id="c9738-139">With Gapless Burning, the audible gap between audio tracks can be removed.</span></span>
-   <span data-ttu-id="c9738-140">已將 ' Double 隱藏 ' 取代為特別選取檔案進行隱藏的處理常式，並將其餘的檔案保留 (大部分的大型檔案) 非隱藏。</span><span class="sxs-lookup"><span data-stu-id="c9738-140">Replaced 'Double Stashing' with a process that specifically selects files for stashing, and leaves the remaining files (mostly large files) non-stashed.</span></span> <span data-ttu-id="c9738-141">最終結果會儲存磁碟空間和作業時間。</span><span class="sxs-lookup"><span data-stu-id="c9738-141">The end result is saved disk space and operation time.</span></span>
-   <span data-ttu-id="c9738-142">使用 [適用于儲存體的 Windows Feature Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)，可透過 [**IBurnVerification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification)存取的屬性提供燒錄驗證選項。</span><span class="sxs-lookup"><span data-stu-id="c9738-142">With the [Windows Feature Pack for Storage](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05), burn verification options have been made available with a property accessed via [**IBurnVerification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification).</span></span>
