---
description: 本節中的功能會在電腦上安裝和設定印表機驅動程式。
ms.assetid: e6aa8963-aa1a-4313-bc24-2aeb4f4b93c4
title: 印表機驅動程式安裝參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1613725ec5c7e2dbb06710bff706ec5aa7e32dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987646"
---
# <a name="printer-driver-installation-reference"></a>印表機驅動程式安裝參考

本節中的功能會在電腦上安裝和設定印表機驅動程式。

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="addmonitor.md"><strong>AddMonitor</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a>函式會安裝本機埠監視器，並連結設定、資料和監視檔案。<br/></td>
</tr>
<tr class="even">
<td><a href="addport.md"><strong>AddPort</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a>函式會將埠的名稱新增至支援的埠清單。 <strong>AddPort</strong>函數是由埠監視器匯出。<br/></td>
</tr>
<tr class="odd">
<td><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a>函式會安裝本機或遠端印表機驅動程式，並產生設定、資料和驅動程式檔案的關聯。<br/> 若要在安裝或升級印表機驅動程式時有更大的彈性，請使用 <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> 函式，因為它允許嚴格升級、嚴格降級、複製較新的檔案，以及複製所有檔案 (無論檔案時間戳記) 。<br/>
<blockquote>
[!Note]<br />
不再建議您安裝不含驅動程式套件的印表機驅動程式。 請改用 <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> 。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a>函式會安裝本機或遠端印表機驅動程式，並連結設定、資料和驅動程式檔案。 除了擁有 <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>的功能之外，它也有一些選項可允許嚴格升級、嚴格降級、只複製較新的檔案，以及複製所有檔案 (無論檔案時間戳記) 。<br/>
<blockquote>
[!Note]<br />
不再建議您安裝不含驅動程式套件的印表機驅動程式。 請改用 <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> 。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a>函式會在指定的伺服器上安裝列印處理器，並將列印處理器名稱新增至支援的列印處理器清單。<br/></td>
</tr>
<tr class="even">
<td><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a>函式會安裝本機列印提供者，並連結設定、資料和提供者檔案。<br/></td>
</tr>
<tr class="odd">
<td><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a>函式會報告是否已安裝具有指定 GUID、日期和版本的核心印表機驅動程式。<br/></td>
</tr>
<tr class="even">
<td><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a>函式會移除<a href="addmonitor.md"><strong>AddMonitor</strong></a>函數所新增的埠監視器。<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteport.md"><strong>DeletePort</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a>函式會顯示一個對話方塊，可讓使用者刪除埠名稱。<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a>函數會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱。<br/> 若要刪除與驅動程式相關聯的檔案，以及從伺服器支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱，請使用 <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> 函數。<br/> 只有當指定的環境未使用任何驅動程式版本時， <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a>才會刪除驅動程式。 <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> 可以刪除特定版本的驅動程式。<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a>函式會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱，並刪除與驅動程式相關聯的檔案。 此函數也可以刪除驅動程式的特定版本。<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a><br/></td>
<td>從驅動程式存放區刪除印表機驅動程式套件。<br/></td>
</tr>
<tr class="odd">
<td><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a>函式會移除<a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a>函數所新增的列印處理器。<br/></td>
</tr>
<tr class="even">
<td><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a>函式會移除<a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a>函數所新增的列印提供者。<br/></td>
</tr>
<tr class="odd">
<td><a href="enummonitors.md"><strong>EnumMonitors</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a>函式會抓取指定的伺服器上所安裝之埠監視器的相關資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="enumports.md"><strong>EnumPorts</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a>函式會列舉可在指定的伺服器上列印的埠。<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a>函式會列舉安裝在指定印表機伺服器上的印表機驅動程式。<br/></td>
</tr>
<tr class="even">
<td><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a>函式會列舉指定列印處理器支援的資料類型。<br/></td>
</tr>
<tr class="odd">
<td><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a>函式會列舉安裝在指定伺服器上的列印處理器。<br/></td>
</tr>
<tr class="even">
<td><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a><br/></td>
<td>抓取指定的核心印表機驅動程式的 GUID、版本和日期，以及其套件的路徑。<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a>函式會抓取指定印表機的驅動程式資料。 如果未在本機電腦上安裝驅動程式， <strong>GetPrinterDriver</strong> 會安裝該驅動程式。<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a><br/></td>
<td><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a>函式會抓取指定印表機的驅動程式資料。 如果未在本機電腦上安裝驅動程式， <strong>GetPrinterDriver2</strong> 會安裝該驅動程式，並在指定的視窗中顯示任何使用者介面。<br/></td>
</tr>
<tr class="odd">
<td><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a>函式會捕獲印表機驅動程式目錄的路徑。<br/></td>
</tr>
<tr class="even">
<td><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a><br/></td>
<td>抓取列印伺服器上指定之印表機驅動程式套件的路徑。<br/></td>
</tr>
<tr class="odd">
<td><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a><br/></td>
<td><a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a>函式會在指定的伺服器上，捕獲列印處理器目錄的路徑。<br/></td>
</tr>
<tr class="even">
<td><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a><br/></td>
<td>從列印伺服器的驅動程式存放區中的驅動程式套件安裝印表機驅動程式。<br/></td>
</tr>
<tr class="odd">
<td><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a><br/></td>
<td>將印表機驅動程式上傳至列印伺服器的驅動程式存放區，以便藉由呼叫 <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>來進行安裝。<br/></td>
</tr>
</tbody>
</table>



 

 

