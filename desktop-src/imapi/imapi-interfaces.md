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
# <a name="imapi-interfaces"></a>IMAPI.EXE 介面

下表會識別並簡短描述 C/c + + 開發人員和相關聯的腳本物件所使用的介面。 在資料表中的物件名稱前面加上 "IMAPI2"。 在腳本中建立物件時，完整限定物件名稱。

下表列出與裝置、燒錄引擎和格式寫入器和橡皮擦相關聯的介面。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>介面</td>
<td>Object</td>
</tr>
<tr class="even">
<td>低層級的燒錄引擎。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></li>
</ul></td>
<td>MsftWriteEngine2</td>
</tr>
<tr class="odd">
<td>主要影像寫入器。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2Data</td>
</tr>
<tr class="even">
<td>光碟橡皮擦。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></li>
</ul></td>
<td>MsftDiscFormat2Erase</td>
</tr>
<tr class="odd">
<td>原始影像寫入器。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2RawCD</td>
</tr>
<tr class="even">
<td>單次追蹤影像寫入器。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2TrackAtOnce</td>
</tr>
<tr class="odd">
<td>列舉系統硬體清單中的光碟裝置。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></li>
</ul></td>
<td>MsftDiscMaster2</td>
</tr>
<tr class="even">
<td>MsftDiscMaster2 物件的通知委派。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></li>
</ul></td>
<td>DDiscMaster2Events</td>
</tr>
<tr class="odd">
<td>個別錄製裝置。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></li>
</ul></td>
<td>MsftDiscRecorder2</td>
</tr>
<tr class="even">
<td>裝置寫入屬性，包括媒體類型、書寫速度，以及角度速度控制項的類型。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></li>
</ul></td>
<td>MsftWriteSpeedDescriptor</td>
</tr>
</tbody>
</table>



 

下表列出檔案系統介面。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>介面</td>
<td>Object</td>
</tr>
<tr class="even">
<td>開機映射串流和屬性，用於整合光碟映射中的可開機映射。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></li>
</ul></td>
<td>BootOptions</td>
</tr>
<tr class="odd">
<td>檔案系統映射和屬性。 此物件包含所有的追蹤，以及開機映射和結果影像的參考。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></li>
</ul></td>
<td>CFileSystemImage</td>
</tr>
<tr class="even">
<td>檔案系統物件所提供之資料流程的容器。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></li>
</ul></td>
<td>FileSystemImageResult</td>
</tr>
<tr class="odd">
<td>檔案系統映射中的目錄專案。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></li>
</ul></td>
<td>FsiDirectoryItem</td>
</tr>
<tr class="even">
<td>檔案系統映射中的檔案專案。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></li>
</ul></td>
<td>FsiFileItem</td>
</tr>
<tr class="odd">
<td>包含檔案和目錄專案通用屬性的介面。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></li>
</ul></td>
<td>FsiItem</td>
</tr>
<tr class="even">
<td>建立原始 CD 映射。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></li>
</ul></td>
<td>MsftRawCDImageCreator</td>
</tr>
<tr class="odd">
<td>串流物件協助程式物件來串連多個資料流程。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></li>
</ul></td>
<td>MsftStreamConcatenate</td>
</tr>
<tr class="even">
<td>交錯串流以新增至光碟影像。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></li>
</ul></td>
<td>MsftStreamInterleave</td>
</tr>
<tr class="odd">
<td>虛擬隨機產生的資料流程。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></li>
</ul></td>
<td>MsftStreamPrgn001</td>
</tr>
<tr class="even">
<td><strong>MsftStreamZero</strong>腳本物件不會實作為介面。</td>
<td><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></td>
</tr>
</tbody>
</table>



 

下表列出 helper 介面。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>介面</td>
<td>Object</td>
</tr>
<tr class="even">
<td>檔案系統映射內的磁區範圍集合。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></li>
</ul></td>
<td>沒有對應的物件</td>
</tr>
<tr class="odd">
<td>燒錄驗證支援。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></li>
</ul></td>
<td>沒有對應的物件</td>
</tr>
<tr class="even">
<td>C/c + + 應用程式的 FsiItems 列舉值。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></li>
</ul></td>
<td>EnumFsiItems</td>
</tr>
<tr class="odd">
<td>C/c + + 應用程式的 ProgressItems 列舉值。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></li>
</ul></td>
<td>EnumProgressItems</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></li>
</ul></td>
<td>FsiFileItem2</td>
</tr>
<tr class="odd">
<td>.iso 影像驗證支援。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></li>
</ul></td>
<td>沒有對應的物件</td>
</tr>
<tr class="even">
<td>多個會話支援。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></li>
</ul></td>
<td>沒有對應的物件</td>
</tr>
<tr class="odd">
<td>連續多重會話支援。
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></li>
</ul></td>
<td>MsftMultisessionSequential</td>
</tr>
<tr class="even">
<td>結果影像中的檔案名和相關聯的區塊。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></li>
</ul></td>
<td>ProgressItem</td>
</tr>
<tr class="odd">
<td>結果影像清單，依檔案名和相關聯的區塊細分。
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></li>
</ul></td>
<td>ProgressItems</td>
</tr>
</tbody>
</table>



 

 

 




