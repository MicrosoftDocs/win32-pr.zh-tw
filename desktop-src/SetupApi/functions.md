---
description: 下列函式是安裝程式 API 的一部分：
ms.assetid: 0a9518b7-f231-48f2-ba50-5b802f8ccaed
title: " (設定 API) 的函式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24051c52d7c7555e1e1b84c03fafd6faf6ad1b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976927"
---
# <a name="functions-setup-api"></a><span data-ttu-id="308ab-103"> (設定 API) 的函式</span><span class="sxs-lookup"><span data-stu-id="308ab-103">Functions (Setup API)</span></span>

<span data-ttu-id="308ab-104">\[這些函式可在 [需求] 區段中指出的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="308ab-104">\[These functions are available for use in the operating systems indicated in the Requirements sections.</span></span> <span data-ttu-id="308ab-105">在後續的版本中，我們可能會修改其功能或不再提供。</span><span class="sxs-lookup"><span data-stu-id="308ab-105">They may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="308ab-106">Setupapi.log 不應再用來安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="308ab-106">SetupAPI should no longer be used for installing applications.</span></span> <span data-ttu-id="308ab-107">相反地，請使用 Windows Installer 開發應用程式安裝程式。</span><span class="sxs-lookup"><span data-stu-id="308ab-107">Instead, use the Windows Installer for developing application installers.</span></span> <span data-ttu-id="308ab-108">Setupapi.log 會繼續用來安裝設備磁碟機。\]</span><span class="sxs-lookup"><span data-stu-id="308ab-108">SetupAPI continues to be used for installing device drivers.\]</span></span>

<span data-ttu-id="308ab-109">下列函式是安裝程式 API 的一部分：</span><span class="sxs-lookup"><span data-stu-id="308ab-109">The following functions are part of the Setup API:</span></span>

-   [<span data-ttu-id="308ab-110">**InstallHinfSection**</span><span class="sxs-lookup"><span data-stu-id="308ab-110">**InstallHinfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-installhinfsectiona)
-   [<span data-ttu-id="308ab-111">**SetupAddInstallSectionToDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-111">**SetupAddInstallSectionToDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)
-   [<span data-ttu-id="308ab-112">**SetupAddSectionToDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-112">**SetupAddSectionToDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)
-   [<span data-ttu-id="308ab-113">**SetupAddToDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-113">**SetupAddToDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)
-   [<span data-ttu-id="308ab-114">**SetupAddToSourceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-114">**SetupAddToSourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista)
-   [<span data-ttu-id="308ab-115">**SetupAdjustDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-115">**SetupAdjustDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)
-   [<span data-ttu-id="308ab-116">**SetupBackupError**</span><span class="sxs-lookup"><span data-stu-id="308ab-116">**SetupBackupError**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupbackuperrora)
-   [<span data-ttu-id="308ab-117">**SetupCancelTemporarySourceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-117">**SetupCancelTemporarySourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist)
-   [<span data-ttu-id="308ab-118">**SetupCloseFileQueue**</span><span class="sxs-lookup"><span data-stu-id="308ab-118">**SetupCloseFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)
-   [<span data-ttu-id="308ab-119">**SetupCloseInfFile**</span><span class="sxs-lookup"><span data-stu-id="308ab-119">**SetupCloseInfFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)
-   [<span data-ttu-id="308ab-120">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="308ab-120">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
-   [<span data-ttu-id="308ab-121">**SetupConfigureWmiFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="308ab-121">**SetupConfigureWmiFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupconfigurewmifrominfsectiona)
-   [<span data-ttu-id="308ab-122">**SetupCopyError**</span><span class="sxs-lookup"><span data-stu-id="308ab-122">**SetupCopyError**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)
-   [<span data-ttu-id="308ab-123">**SetupCopyOEMInf**</span><span class="sxs-lookup"><span data-stu-id="308ab-123">**SetupCopyOEMInf**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyoeminfa)
-   [<span data-ttu-id="308ab-124">**SetupCreateDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-124">**SetupCreateDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)
-   [<span data-ttu-id="308ab-125">**SetupDecompressOrCopyFile**</span><span class="sxs-lookup"><span data-stu-id="308ab-125">**SetupDecompressOrCopyFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea)
-   [<span data-ttu-id="308ab-126">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="308ab-126">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
-   [<span data-ttu-id="308ab-127">**SetupDeleteError**</span><span class="sxs-lookup"><span data-stu-id="308ab-127">**SetupDeleteError**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)
-   [<span data-ttu-id="308ab-128">**SetupDestroyDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-128">**SetupDestroyDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)
-   [<span data-ttu-id="308ab-129">**SetupDuplicateDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-129">**SetupDuplicateDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)
-   [<span data-ttu-id="308ab-130">**SetupEnumInfSections**</span><span class="sxs-lookup"><span data-stu-id="308ab-130">**SetupEnumInfSections**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupenuminfsectionsa)
-   [<span data-ttu-id="308ab-131">**SetupFindFirstLine**</span><span class="sxs-lookup"><span data-stu-id="308ab-131">**SetupFindFirstLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)
-   [<span data-ttu-id="308ab-132">**SetupFindNextLine**</span><span class="sxs-lookup"><span data-stu-id="308ab-132">**SetupFindNextLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)
-   [<span data-ttu-id="308ab-133">**SetupFindNextMatchLine**</span><span class="sxs-lookup"><span data-stu-id="308ab-133">**SetupFindNextMatchLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)
-   [<span data-ttu-id="308ab-134">**SetupFreeSourceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-134">**SetupFreeSourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista)
-   [<span data-ttu-id="308ab-135">**SetupGetBinaryField**</span><span class="sxs-lookup"><span data-stu-id="308ab-135">**SetupGetBinaryField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)
-   [<span data-ttu-id="308ab-136">**SetupGetFieldCount**</span><span class="sxs-lookup"><span data-stu-id="308ab-136">**SetupGetFieldCount**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfieldcount)
-   [<span data-ttu-id="308ab-137">**SetupGetFileCompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="308ab-137">**SetupGetFileCompressionInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)
-   [<span data-ttu-id="308ab-138">**SetupGetFileCompressionInfoEx**</span><span class="sxs-lookup"><span data-stu-id="308ab-138">**SetupGetFileCompressionInfoEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoexa)
-   [<span data-ttu-id="308ab-139">**SetupGetFileQueueCount**</span><span class="sxs-lookup"><span data-stu-id="308ab-139">**SetupGetFileQueueCount**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilequeuecount)
-   [<span data-ttu-id="308ab-140">**SetupGetFileQueueFlags**</span><span class="sxs-lookup"><span data-stu-id="308ab-140">**SetupGetFileQueueFlags**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilequeueflags)
-   [<span data-ttu-id="308ab-141">**SetupGetInfFileList**</span><span class="sxs-lookup"><span data-stu-id="308ab-141">**SetupGetInfFileList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista)
-   [<span data-ttu-id="308ab-142">**SetupGetInfInformation**</span><span class="sxs-lookup"><span data-stu-id="308ab-142">**SetupGetInfInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)
-   [<span data-ttu-id="308ab-143">**SetupGetIntField**</span><span class="sxs-lookup"><span data-stu-id="308ab-143">**SetupGetIntField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)
-   [<span data-ttu-id="308ab-144">**SetupGetLineByIndex**</span><span class="sxs-lookup"><span data-stu-id="308ab-144">**SetupGetLineByIndex**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)
-   [<span data-ttu-id="308ab-145">**SetupGetLineCount**</span><span class="sxs-lookup"><span data-stu-id="308ab-145">**SetupGetLineCount**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinecounta)
-   [<span data-ttu-id="308ab-146">**SetupGetLineText**</span><span class="sxs-lookup"><span data-stu-id="308ab-146">**SetupGetLineText**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)
-   [<span data-ttu-id="308ab-147">**SetupGetMultiSzField**</span><span class="sxs-lookup"><span data-stu-id="308ab-147">**SetupGetMultiSzField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)
-   [<span data-ttu-id="308ab-148">**SetupGetSourceFileLocation**</span><span class="sxs-lookup"><span data-stu-id="308ab-148">**SetupGetSourceFileLocation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)
-   [<span data-ttu-id="308ab-149">**SetupGetSourceFileSize**</span><span class="sxs-lookup"><span data-stu-id="308ab-149">**SetupGetSourceFileSize**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)
-   [<span data-ttu-id="308ab-150">**SetupGetSourceInfo**</span><span class="sxs-lookup"><span data-stu-id="308ab-150">**SetupGetSourceInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)
-   [<span data-ttu-id="308ab-151">**SetupGetStringField**</span><span class="sxs-lookup"><span data-stu-id="308ab-151">**SetupGetStringField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)
-   [<span data-ttu-id="308ab-152">**SetupGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="308ab-152">**SetupGetTargetPath**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)
-   [<span data-ttu-id="308ab-153">**SetupInitDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="308ab-153">**SetupInitDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)
-   [<span data-ttu-id="308ab-154">**SetupInitDefaultQueueCallbackEx**</span><span class="sxs-lookup"><span data-stu-id="308ab-154">**SetupInitDefaultQueueCallbackEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)
-   [<span data-ttu-id="308ab-155">**SetupInitializeFileLog**</span><span class="sxs-lookup"><span data-stu-id="308ab-155">**SetupInitializeFileLog**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga)
-   [<span data-ttu-id="308ab-156">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="308ab-156">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
-   [<span data-ttu-id="308ab-157">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="308ab-157">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
-   [<span data-ttu-id="308ab-158">**SetupInstallFilesFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="308ab-158">**SetupInstallFilesFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)
-   [<span data-ttu-id="308ab-159">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="308ab-159">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
-   [<span data-ttu-id="308ab-160">**SetupInstallServicesFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="308ab-160">**SetupInstallServicesFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona)
-   [<span data-ttu-id="308ab-161">**SetupInstallServicesFromInfSectionEx**</span><span class="sxs-lookup"><span data-stu-id="308ab-161">**SetupInstallServicesFromInfSectionEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectionexa)
-   [<span data-ttu-id="308ab-162">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="308ab-162">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
-   [<span data-ttu-id="308ab-163">**SetupLogFile**</span><span class="sxs-lookup"><span data-stu-id="308ab-163">**SetupLogFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea)
-   [<span data-ttu-id="308ab-164">**SetupLogError**</span><span class="sxs-lookup"><span data-stu-id="308ab-164">**SetupLogError**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuplogerrora)
-   [<span data-ttu-id="308ab-165">**SetupOpenAppendInfFile**</span><span class="sxs-lookup"><span data-stu-id="308ab-165">**SetupOpenAppendInfFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)
-   [<span data-ttu-id="308ab-166">**SetupOpenFileQueue**</span><span class="sxs-lookup"><span data-stu-id="308ab-166">**SetupOpenFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)
-   [<span data-ttu-id="308ab-167">**SetupOpenInfFile**</span><span class="sxs-lookup"><span data-stu-id="308ab-167">**SetupOpenInfFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea)
-   [<span data-ttu-id="308ab-168">**SetupOpenMasterInf**</span><span class="sxs-lookup"><span data-stu-id="308ab-168">**SetupOpenMasterInf**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenmasterinf)
-   [<span data-ttu-id="308ab-169">**SetupPromptForDisk**</span><span class="sxs-lookup"><span data-stu-id="308ab-169">**SetupPromptForDisk**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)
-   [<span data-ttu-id="308ab-170">**SetupPromptReboot**</span><span class="sxs-lookup"><span data-stu-id="308ab-170">**SetupPromptReboot**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)
-   [<span data-ttu-id="308ab-171">**SetupQueryDrivesInDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-171">**SetupQueryDrivesInDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)
-   [<span data-ttu-id="308ab-172">**SetupQueryFileLog**</span><span class="sxs-lookup"><span data-stu-id="308ab-172">**SetupQueryFileLog**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga)
-   [<span data-ttu-id="308ab-173">**SetupQueryInfFileInformation**</span><span class="sxs-lookup"><span data-stu-id="308ab-173">**SetupQueryInfFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)
-   [<span data-ttu-id="308ab-174">**SetupQueryInfOriginalFileInformation**</span><span class="sxs-lookup"><span data-stu-id="308ab-174">**SetupQueryInfOriginalFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinforiginalfileinformationa)
-   [<span data-ttu-id="308ab-175">**SetupQueryInfVersionInformation**</span><span class="sxs-lookup"><span data-stu-id="308ab-175">**SetupQueryInfVersionInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)
-   [<span data-ttu-id="308ab-176">**SetupQuerySourceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-176">**SetupQuerySourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista)
-   [<span data-ttu-id="308ab-177">**SetupQuerySpaceRequiredOnDrive**</span><span class="sxs-lookup"><span data-stu-id="308ab-177">**SetupQuerySpaceRequiredOnDrive**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)
-   [<span data-ttu-id="308ab-178">**SetupQueueCopy**</span><span class="sxs-lookup"><span data-stu-id="308ab-178">**SetupQueueCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)
-   [<span data-ttu-id="308ab-179">**SetupQueueCopyIndirect**</span><span class="sxs-lookup"><span data-stu-id="308ab-179">**SetupQueueCopyIndirect**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopyindirecta)
-   [<span data-ttu-id="308ab-180">**SetupQueueCopySection**</span><span class="sxs-lookup"><span data-stu-id="308ab-180">**SetupQueueCopySection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)
-   [<span data-ttu-id="308ab-181">**SetupQueueDefaultCopy**</span><span class="sxs-lookup"><span data-stu-id="308ab-181">**SetupQueueDefaultCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)
-   [<span data-ttu-id="308ab-182">**SetupQueueDelete**</span><span class="sxs-lookup"><span data-stu-id="308ab-182">**SetupQueueDelete**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)
-   [<span data-ttu-id="308ab-183">**SetupQueueDeleteSection**</span><span class="sxs-lookup"><span data-stu-id="308ab-183">**SetupQueueDeleteSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)
-   [<span data-ttu-id="308ab-184">**SetupQueueRename**</span><span class="sxs-lookup"><span data-stu-id="308ab-184">**SetupQueueRename**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)
-   [<span data-ttu-id="308ab-185">**SetupQueueRenameSection**</span><span class="sxs-lookup"><span data-stu-id="308ab-185">**SetupQueueRenameSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)
-   [<span data-ttu-id="308ab-186">**SetupRemoveFileLogEntry**</span><span class="sxs-lookup"><span data-stu-id="308ab-186">**SetupRemoveFileLogEntry**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)
-   [<span data-ttu-id="308ab-187">**SetupRemoveFromDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-187">**SetupRemoveFromDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)
-   [<span data-ttu-id="308ab-188">**SetupRemoveFromSourceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-188">**SetupRemoveFromSourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista)
-   [<span data-ttu-id="308ab-189">**SetupRemoveInstallSectionFromDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-189">**SetupRemoveInstallSectionFromDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista)
-   [<span data-ttu-id="308ab-190">**SetupRemoveSectionFromDiskSpaceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-190">**SetupRemoveSectionFromDiskSpaceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)
-   [<span data-ttu-id="308ab-191">**SetupRenameError**</span><span class="sxs-lookup"><span data-stu-id="308ab-191">**SetupRenameError**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)
-   [<span data-ttu-id="308ab-192">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="308ab-192">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
-   [<span data-ttu-id="308ab-193">**SetupSetDirectoryId**</span><span class="sxs-lookup"><span data-stu-id="308ab-193">**SetupSetDirectoryId**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryida)
-   [<span data-ttu-id="308ab-194">**SetupSetDirectoryIdEx**</span><span class="sxs-lookup"><span data-stu-id="308ab-194">**SetupSetDirectoryIdEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryidexa)
-   [<span data-ttu-id="308ab-195">**SetupSetFileQueueAlternatePlatform**</span><span class="sxs-lookup"><span data-stu-id="308ab-195">**SetupSetFileQueueAlternatePlatform**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetfilequeuealternateplatforma)
-   [<span data-ttu-id="308ab-196">**SetupSetFileQueueFlags**</span><span class="sxs-lookup"><span data-stu-id="308ab-196">**SetupSetFileQueueFlags**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetfilequeueflags)
-   [<span data-ttu-id="308ab-197">**SetupSetPlatformPathOverride**</span><span class="sxs-lookup"><span data-stu-id="308ab-197">**SetupSetPlatformPathOverride**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea)
-   [<span data-ttu-id="308ab-198">**SetupSetSourceList**</span><span class="sxs-lookup"><span data-stu-id="308ab-198">**SetupSetSourceList**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista)
-   [<span data-ttu-id="308ab-199">**SetupTermDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="308ab-199">**SetupTermDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback)
-   [<span data-ttu-id="308ab-200">**SetupTerminateFileLog**</span><span class="sxs-lookup"><span data-stu-id="308ab-200">**SetupTerminateFileLog**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog)
-   [<span data-ttu-id="308ab-201">**SetupUninstallNewlyCopiedInfs**</span><span class="sxs-lookup"><span data-stu-id="308ab-201">**SetupUninstallNewlyCopiedInfs**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupuninstallnewlycopiedinfs)
-   [<span data-ttu-id="308ab-202">**SetupUninstallOEMInf**</span><span class="sxs-lookup"><span data-stu-id="308ab-202">**SetupUninstallOEMInf**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupuninstalloeminfa)
-   [<span data-ttu-id="308ab-203">**SetupVerifyInfFile**</span><span class="sxs-lookup"><span data-stu-id="308ab-203">**SetupVerifyInfFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupverifyinffilea)

 

 



