---
title: IMAPI.EXE 介面
description: 下表會識別並簡短描述 C/c + + 開發人員和相關聯的腳本物件所使用的介面。 在資料表中的物件名稱前面加上 \ 0034; IMAPI2。 \ 0034;在腳本中建立物件時，完整限定物件名稱。
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac989a9871b761a1f1700ec599cc51affd30b2e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "106968884"
---
# <a name="imapi-interfaces"></a><span data-ttu-id="7474b-105">IMAPI.EXE 介面</span><span class="sxs-lookup"><span data-stu-id="7474b-105">IMAPI Interfaces</span></span>

<span data-ttu-id="7474b-106">下表會識別並簡短描述 C/c + + 開發人員和相關聯的腳本物件所使用的介面。</span><span class="sxs-lookup"><span data-stu-id="7474b-106">The following tables identify and briefly describe the interfaces used C/C++ developers and the associated scripting object.</span></span> <span data-ttu-id="7474b-107">在資料表中的物件名稱前面加上 "IMAPI2"。</span><span class="sxs-lookup"><span data-stu-id="7474b-107">Prefix the object name in the table with "IMAPI2."</span></span> <span data-ttu-id="7474b-108">在腳本中建立物件時，完整限定物件名稱。</span><span class="sxs-lookup"><span data-stu-id="7474b-108">to fully qualify the object name when creating the object in script.</span></span>

<span data-ttu-id="7474b-109">下表列出與裝置、燒錄引擎和格式寫入器和橡皮擦相關聯的介面。</span><span class="sxs-lookup"><span data-stu-id="7474b-109">The following table lists the interfaces associated with devices, the burn engine, and the format writers and eraser.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7474b-110">介面</span><span class="sxs-lookup"><span data-stu-id="7474b-110">Interface</span></span></td>
<td><span data-ttu-id="7474b-111">Object</span><span class="sxs-lookup"><span data-stu-id="7474b-111">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-112">低層級的燒錄引擎。</span><span class="sxs-lookup"><span data-stu-id="7474b-112">Low-level burn engine.</span></span>
<ul>
<li><span data-ttu-id="7474b-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span></span></li>
<li><span data-ttu-id="7474b-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span></span></li>
<li><span data-ttu-id="7474b-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-116">MsftWriteEngine2</span><span class="sxs-lookup"><span data-stu-id="7474b-116">MsftWriteEngine2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-117">主要影像寫入器。</span><span class="sxs-lookup"><span data-stu-id="7474b-117">Main image writer.</span></span>
<ul>
<li><span data-ttu-id="7474b-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span></span></li>
<li><span data-ttu-id="7474b-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span></span></li>
<li><span data-ttu-id="7474b-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-121">MsftDiscFormat2Data</span><span class="sxs-lookup"><span data-stu-id="7474b-121">MsftDiscFormat2Data</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-122">光碟橡皮擦。</span><span class="sxs-lookup"><span data-stu-id="7474b-122">Disc eraser.</span></span>
<ul>
<li><span data-ttu-id="7474b-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span></span></li>
<li><span data-ttu-id="7474b-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-125">MsftDiscFormat2Erase</span><span class="sxs-lookup"><span data-stu-id="7474b-125">MsftDiscFormat2Erase</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-126">原始影像寫入器。</span><span class="sxs-lookup"><span data-stu-id="7474b-126">Raw image writer.</span></span>
<ul>
<li><span data-ttu-id="7474b-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span></span></li>
<li><span data-ttu-id="7474b-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span></span></li>
<li><span data-ttu-id="7474b-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-130">MsftDiscFormat2RawCD</span><span class="sxs-lookup"><span data-stu-id="7474b-130">MsftDiscFormat2RawCD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-131">單次追蹤影像寫入器。</span><span class="sxs-lookup"><span data-stu-id="7474b-131">Track-At-Once image writer.</span></span>
<ul>
<li><span data-ttu-id="7474b-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span></span></li>
<li><span data-ttu-id="7474b-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span></span></li>
<li><span data-ttu-id="7474b-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-135">MsftDiscFormat2TrackAtOnce</span><span class="sxs-lookup"><span data-stu-id="7474b-135">MsftDiscFormat2TrackAtOnce</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-136">列舉系統硬體清單中的光碟裝置。</span><span class="sxs-lookup"><span data-stu-id="7474b-136">Enumeration of disc devices in the system hardware list.</span></span>
<ul>
<li><span data-ttu-id="7474b-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-138">MsftDiscMaster2</span><span class="sxs-lookup"><span data-stu-id="7474b-138">MsftDiscMaster2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-139">MsftDiscMaster2 物件的通知委派。</span><span class="sxs-lookup"><span data-stu-id="7474b-139">Notification delegate for the MsftDiscMaster2 object.</span></span>
<ul>
<li><span data-ttu-id="7474b-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-141">DDiscMaster2Events</span><span class="sxs-lookup"><span data-stu-id="7474b-141">DDiscMaster2Events</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-142">個別錄製裝置。</span><span class="sxs-lookup"><span data-stu-id="7474b-142">Individual recording device.</span></span>
<ul>
<li><span data-ttu-id="7474b-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span></span></li>
<li><span data-ttu-id="7474b-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-145">MsftDiscRecorder2</span><span class="sxs-lookup"><span data-stu-id="7474b-145">MsftDiscRecorder2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-146">裝置寫入屬性，包括媒體類型、書寫速度，以及角度速度控制項的類型。</span><span class="sxs-lookup"><span data-stu-id="7474b-146">Device writing attributes, including the media type, writing speed, and type of angular velocity control.</span></span>
<ul>
<li><span data-ttu-id="7474b-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-148">MsftWriteSpeedDescriptor</span><span class="sxs-lookup"><span data-stu-id="7474b-148">MsftWriteSpeedDescriptor</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7474b-149">下表列出檔案系統介面。</span><span class="sxs-lookup"><span data-stu-id="7474b-149">The following table lists the file system interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7474b-150">介面</span><span class="sxs-lookup"><span data-stu-id="7474b-150">Interface</span></span></td>
<td><span data-ttu-id="7474b-151">Object</span><span class="sxs-lookup"><span data-stu-id="7474b-151">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-152">開機映射串流和屬性，用於整合光碟映射中的可開機映射。</span><span class="sxs-lookup"><span data-stu-id="7474b-152">Boot image stream and properties for integrating the bootable image in the disc image.</span></span>
<ul>
<li><span data-ttu-id="7474b-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-154">BootOptions</span><span class="sxs-lookup"><span data-stu-id="7474b-154">BootOptions</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-155">檔案系統映射和屬性。</span><span class="sxs-lookup"><span data-stu-id="7474b-155">File system image and properties.</span></span> <span data-ttu-id="7474b-156">此物件包含所有的追蹤，以及開機映射和結果影像的參考。</span><span class="sxs-lookup"><span data-stu-id="7474b-156">This object includes all tracks, and references to the boot image and result image.</span></span>
<ul>
<li><span data-ttu-id="7474b-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span></span></li>
<li><span data-ttu-id="7474b-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span></span></li>
<li><span data-ttu-id="7474b-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span></span></li>
<li><span data-ttu-id="7474b-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span></span></li>
<li><span data-ttu-id="7474b-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-162">CFileSystemImage</span><span class="sxs-lookup"><span data-stu-id="7474b-162">CFileSystemImage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-163">檔案系統物件所提供之資料流程的容器。</span><span class="sxs-lookup"><span data-stu-id="7474b-163">Container of the data stream provided by the file system object.</span></span>
<ul>
<li><span data-ttu-id="7474b-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-165">FileSystemImageResult</span><span class="sxs-lookup"><span data-stu-id="7474b-165">FileSystemImageResult</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-166">檔案系統映射中的目錄專案。</span><span class="sxs-lookup"><span data-stu-id="7474b-166">Directory item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="7474b-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span></span></li>
<li><span data-ttu-id="7474b-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-169">FsiDirectoryItem</span><span class="sxs-lookup"><span data-stu-id="7474b-169">FsiDirectoryItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-170">檔案系統映射中的檔案專案。</span><span class="sxs-lookup"><span data-stu-id="7474b-170">File item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="7474b-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span></span></li>
<li><span data-ttu-id="7474b-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-173">FsiFileItem</span><span class="sxs-lookup"><span data-stu-id="7474b-173">FsiFileItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-174">包含檔案和目錄專案通用屬性的介面。</span><span class="sxs-lookup"><span data-stu-id="7474b-174">Interface containing properties common to both file and directory items.</span></span>
<ul>
<li><span data-ttu-id="7474b-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-176">FsiItem</span><span class="sxs-lookup"><span data-stu-id="7474b-176">FsiItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-177">建立原始 CD 映射。</span><span class="sxs-lookup"><span data-stu-id="7474b-177">RAW CD image creation.</span></span>
<ul>
<li><span data-ttu-id="7474b-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span></span></li>
<li><span data-ttu-id="7474b-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-180">MsftRawCDImageCreator</span><span class="sxs-lookup"><span data-stu-id="7474b-180">MsftRawCDImageCreator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-181">串流物件協助程式物件來串連多個資料流程。</span><span class="sxs-lookup"><span data-stu-id="7474b-181">Stream object helper object to concatenate multiple streams.</span></span>
<ul>
<li><span data-ttu-id="7474b-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-183">MsftStreamConcatenate</span><span class="sxs-lookup"><span data-stu-id="7474b-183">MsftStreamConcatenate</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-184">交錯串流以新增至光碟影像。</span><span class="sxs-lookup"><span data-stu-id="7474b-184">Interleaved stream to add to the disc image.</span></span>
<ul>
<li><span data-ttu-id="7474b-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-186">MsftStreamInterleave</span><span class="sxs-lookup"><span data-stu-id="7474b-186">MsftStreamInterleave</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-187">虛擬隨機產生的資料流程。</span><span class="sxs-lookup"><span data-stu-id="7474b-187">Pseudo-random generated stream.</span></span>
<ul>
<li><span data-ttu-id="7474b-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-189">MsftStreamPrgn001</span><span class="sxs-lookup"><span data-stu-id="7474b-189">MsftStreamPrgn001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-190"><strong>MsftStreamZero</strong>腳本物件不會實作為介面。</span><span class="sxs-lookup"><span data-stu-id="7474b-190">The <strong>MsftStreamZero</strong> scripting object is not implemented as an interface.</span></span></td>
<td><span data-ttu-id="7474b-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7474b-192">下表列出 helper 介面。</span><span class="sxs-lookup"><span data-stu-id="7474b-192">The following table lists helper interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7474b-193">介面</span><span class="sxs-lookup"><span data-stu-id="7474b-193">Interface</span></span></td>
<td><span data-ttu-id="7474b-194">Object</span><span class="sxs-lookup"><span data-stu-id="7474b-194">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-195">檔案系統映射內的磁區範圍集合。</span><span class="sxs-lookup"><span data-stu-id="7474b-195">Collection of sector ranges within a file system image.</span></span>
<ul>
<li><span data-ttu-id="7474b-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span></span></li>
<li><span data-ttu-id="7474b-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-198">沒有對應的物件</span><span class="sxs-lookup"><span data-stu-id="7474b-198">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-199">燒錄驗證支援。</span><span class="sxs-lookup"><span data-stu-id="7474b-199">Burn verification support.</span></span>
<ul>
<li><span data-ttu-id="7474b-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-201">沒有對應的物件</span><span class="sxs-lookup"><span data-stu-id="7474b-201">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-202">C/c + + 應用程式的 FsiItems 列舉值。</span><span class="sxs-lookup"><span data-stu-id="7474b-202">Enumerator of FsiItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="7474b-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-204">EnumFsiItems</span><span class="sxs-lookup"><span data-stu-id="7474b-204">EnumFsiItems</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-205">C/c + + 應用程式的 ProgressItems 列舉值。</span><span class="sxs-lookup"><span data-stu-id="7474b-205">Enumerator of ProgressItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="7474b-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-207">EnumProgressItems</span><span class="sxs-lookup"><span data-stu-id="7474b-207">EnumProgressItems</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="7474b-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-209">FsiFileItem2</span><span class="sxs-lookup"><span data-stu-id="7474b-209">FsiFileItem2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-210">.iso 影像驗證支援。</span><span class="sxs-lookup"><span data-stu-id="7474b-210">.iso image verification support.</span></span>
<ul>
<li><span data-ttu-id="7474b-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-212">沒有對應的物件</span><span class="sxs-lookup"><span data-stu-id="7474b-212">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-213">多個會話支援。</span><span class="sxs-lookup"><span data-stu-id="7474b-213">Multiple session support.</span></span>
<ul>
<li><span data-ttu-id="7474b-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-215">沒有對應的物件</span><span class="sxs-lookup"><span data-stu-id="7474b-215">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-216">連續多重會話支援。</span><span class="sxs-lookup"><span data-stu-id="7474b-216">Sequential multiple session support.</span></span>
<ul>
<li><span data-ttu-id="7474b-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span></span></li>
<li><span data-ttu-id="7474b-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-219">MsftMultisessionSequential</span><span class="sxs-lookup"><span data-stu-id="7474b-219">MsftMultisessionSequential</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7474b-220">結果影像中的檔案名和相關聯的區塊。</span><span class="sxs-lookup"><span data-stu-id="7474b-220">File name and associated blocks in the result image.</span></span>
<ul>
<li><span data-ttu-id="7474b-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-222">ProgressItem</span><span class="sxs-lookup"><span data-stu-id="7474b-222">ProgressItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7474b-223">結果影像清單，依檔案名和相關聯的區塊細分。</span><span class="sxs-lookup"><span data-stu-id="7474b-223">Result image listing, broken down by file name and associated blocks.</span></span>
<ul>
<li><span data-ttu-id="7474b-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="7474b-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="7474b-225">ProgressItems</span><span class="sxs-lookup"><span data-stu-id="7474b-225">ProgressItems</span></span></td>
</tr>
</tbody>
</table>



 

 

 




