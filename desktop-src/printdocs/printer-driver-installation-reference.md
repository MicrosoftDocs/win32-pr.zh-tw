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
# <a name="printer-driver-installation-reference"></a><span data-ttu-id="b91eb-103">印表機驅動程式安裝參考</span><span class="sxs-lookup"><span data-stu-id="b91eb-103">Printer Driver Installation Reference</span></span>

<span data-ttu-id="b91eb-104">本節中的功能會在電腦上安裝和設定印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b91eb-104">The functions in this section install and configure printer drivers on a computer.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b91eb-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="b91eb-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b91eb-106">函式</span><span class="sxs-lookup"><span data-stu-id="b91eb-106">Function</span></span></th>
<th><span data-ttu-id="b91eb-107">描述</span><span class="sxs-lookup"><span data-stu-id="b91eb-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b91eb-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-109"><a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a>函式會安裝本機埠監視器，並連結設定、資料和監視檔案。</span><span class="sxs-lookup"><span data-stu-id="b91eb-109">The <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> function installs a local port monitor and links the configuration, data, and monitor files.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-110"><a href="addport.md"><strong>AddPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-110"><a href="addport.md"><strong>AddPort</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-111"><a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a>函式會將埠的名稱新增至支援的埠清單。</span><span class="sxs-lookup"><span data-stu-id="b91eb-111">The <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="b91eb-112"><strong>AddPort</strong>函數是由埠監視器匯出。</span><span class="sxs-lookup"><span data-stu-id="b91eb-112">The <strong>AddPort</strong> function is exported by the port monitor.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-114"><a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a>函式會安裝本機或遠端印表機驅動程式，並產生設定、資料和驅動程式檔案的關聯。</span><span class="sxs-lookup"><span data-stu-id="b91eb-114">The <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span><br/> <span data-ttu-id="b91eb-115">若要在安裝或升級印表機驅動程式時有更大的彈性，請使用 <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> 函式，因為它允許嚴格升級、嚴格降級、複製較新的檔案，以及複製所有檔案 (無論檔案時間戳記) 。</span><span class="sxs-lookup"><span data-stu-id="b91eb-115">For more flexibility in installing or upgrading printer drivers, use the <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b91eb-116">不再建議您安裝不含驅動程式套件的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b91eb-116">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="b91eb-117">請改用 <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="b91eb-117">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-119"><a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a>函式會安裝本機或遠端印表機驅動程式，並連結設定、資料和驅動程式檔案。</span><span class="sxs-lookup"><span data-stu-id="b91eb-119">The <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="b91eb-120">除了擁有 <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>的功能之外，它也有一些選項可允許嚴格升級、嚴格降級、只複製較新的檔案，以及複製所有檔案 (無論檔案時間戳記) 。</span><span class="sxs-lookup"><span data-stu-id="b91eb-120">Besides having the capabilities of <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b91eb-121">不再建議您安裝不含驅動程式套件的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b91eb-121">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="b91eb-122">請改用 <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="b91eb-122">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-124"><a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a>函式會在指定的伺服器上安裝列印處理器，並將列印處理器名稱新增至支援的列印處理器清單。</span><span class="sxs-lookup"><span data-stu-id="b91eb-124">The <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-126"><a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a>函式會安裝本機列印提供者，並連結設定、資料和提供者檔案。</span><span class="sxs-lookup"><span data-stu-id="b91eb-126">The <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> function installs a local print provider and links the configuration, data, and provider files.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-128"><a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a>函式會報告是否已安裝具有指定 GUID、日期和版本的核心印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b91eb-128">The <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-130"><a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a>函式會移除<a href="addmonitor.md"><strong>AddMonitor</strong></a>函數所新增的埠監視器。</span><span class="sxs-lookup"><span data-stu-id="b91eb-130">The <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> function removes a port monitor added by the <a href="addmonitor.md"><strong>AddMonitor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-132"><a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a>函式會顯示一個對話方塊，可讓使用者刪除埠名稱。</span><span class="sxs-lookup"><span data-stu-id="b91eb-132">The <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> function displays a dialog box that allows the user to delete a port name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-134"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a>函數會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="b91eb-134">The <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span><br/> <span data-ttu-id="b91eb-135">若要刪除與驅動程式相關聯的檔案，以及從伺服器支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱，請使用 <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="b91eb-135">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> function.</span></span><br/> <span data-ttu-id="b91eb-136">只有當指定的環境未使用任何驅動程式版本時， <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a>才會刪除驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b91eb-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="b91eb-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> 可以刪除特定版本的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b91eb-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> can delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-139"><a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a>函式會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱，並刪除與驅動程式相關聯的檔案。</span><span class="sxs-lookup"><span data-stu-id="b91eb-139">The <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="b91eb-140">此函數也可以刪除驅動程式的特定版本。</span><span class="sxs-lookup"><span data-stu-id="b91eb-140">This function can also delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-142">從驅動程式存放區刪除印表機驅動程式套件。</span><span class="sxs-lookup"><span data-stu-id="b91eb-142">Deletes a printer driver package from the driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-144"><a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a>函式會移除<a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a>函數所新增的列印處理器。</span><span class="sxs-lookup"><span data-stu-id="b91eb-144">The <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> function removes a print processor added by the <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-146"><a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a>函式會移除<a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a>函數所新增的列印提供者。</span><span class="sxs-lookup"><span data-stu-id="b91eb-146">The <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> function removes a print provider added by the <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-148"><a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a>函式會抓取指定的伺服器上所安裝之埠監視器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b91eb-148">The <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> function retrieves information about the port monitors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-150"><a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a>函式會列舉可在指定的伺服器上列印的埠。</span><span class="sxs-lookup"><span data-stu-id="b91eb-150">The <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> function enumerates the ports that are available for printing on a specified server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-152"><a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a>函式會列舉安裝在指定印表機伺服器上的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b91eb-152">The <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> function enumerates the printer drivers installed on a specified printer server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-154"><a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a>函式會列舉指定列印處理器支援的資料類型。</span><span class="sxs-lookup"><span data-stu-id="b91eb-154">The <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> function enumerates the data types that a specified print processor supports.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-156"><a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a>函式會列舉安裝在指定伺服器上的列印處理器。</span><span class="sxs-lookup"><span data-stu-id="b91eb-156">The <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> function enumerates the print processors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-158">抓取指定的核心印表機驅動程式的 GUID、版本和日期，以及其套件的路徑。</span><span class="sxs-lookup"><span data-stu-id="b91eb-158">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-160"><a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a>函式會抓取指定印表機的驅動程式資料。</span><span class="sxs-lookup"><span data-stu-id="b91eb-160">The <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="b91eb-161">如果未在本機電腦上安裝驅動程式， <strong>GetPrinterDriver</strong> 會安裝該驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b91eb-161">If the driver is not installed on the local computer, <strong>GetPrinterDriver</strong> installs it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-163"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a>函式會抓取指定印表機的驅動程式資料。</span><span class="sxs-lookup"><span data-stu-id="b91eb-163">The <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="b91eb-164">如果未在本機電腦上安裝驅動程式， <strong>GetPrinterDriver2</strong> 會安裝該驅動程式，並在指定的視窗中顯示任何使用者介面。</span><span class="sxs-lookup"><span data-stu-id="b91eb-164">If the driver is not installed on the local computer, <strong>GetPrinterDriver2</strong> installs it and displays any user interface to the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-166"><a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a>函式會捕獲印表機驅動程式目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="b91eb-166">The <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> function retrieves the path of the printer-driver directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-168">抓取列印伺服器上指定之印表機驅動程式套件的路徑。</span><span class="sxs-lookup"><span data-stu-id="b91eb-168">Retrieves the path to the specified printer driver package on a print server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-170"><a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a>函式會在指定的伺服器上，捕獲列印處理器目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="b91eb-170">The <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> function retrieves the path to the print processor directory on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b91eb-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-172">從列印伺服器的驅動程式存放區中的驅動程式套件安裝印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b91eb-172">Installs a printer driver from a driver package that is in the print server's driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b91eb-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="b91eb-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="b91eb-174">將印表機驅動程式上傳至列印伺服器的驅動程式存放區，以便藉由呼叫 <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>來進行安裝。</span><span class="sxs-lookup"><span data-stu-id="b91eb-174">Uploads a printer driver to the print server's driver store so that it can be installed by calling <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

