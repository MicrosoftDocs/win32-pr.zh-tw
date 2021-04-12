---
description: 包含印表機驅動程式資訊。
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: 'DRIVER_INFO_8 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320612"
---
# <a name="driver_info_8-structure"></a><span data-ttu-id="b75cd-103">驅動程式 \_ 資訊 \_ 8 結構</span><span class="sxs-lookup"><span data-stu-id="b75cd-103">DRIVER\_INFO\_8 structure</span></span>

<span data-ttu-id="b75cd-104">包含印表機驅動程式資訊。</span><span class="sxs-lookup"><span data-stu-id="b75cd-104">Contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b75cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="b75cd-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_8 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="b75cd-106">成員</span><span class="sxs-lookup"><span data-stu-id="b75cd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b75cd-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="b75cd-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-108">寫入驅動程式的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="b75cd-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="b75cd-109">支援的值為3。</span><span class="sxs-lookup"><span data-stu-id="b75cd-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="b75cd-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-111">以 null 結束的字串指標，指定驅動程式的名稱 (例如，QMS 810) 。</span><span class="sxs-lookup"><span data-stu-id="b75cd-111">A pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="b75cd-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-113">以 null 結束的字串指標，指定驅動程式所撰寫的環境 (例如，Windows x86、Windows IA64 和 Windows x64。</span><span class="sxs-lookup"><span data-stu-id="b75cd-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="b75cd-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-115">以 null 結束的字串指標，指定包含設備磁碟機之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\Pscript.dll) 。</span><span class="sxs-lookup"><span data-stu-id="b75cd-115">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="b75cd-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-117">以 null 結束的字串指標，這個字串會指定包含驅動程式資料之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\ Qms810) 。</span><span class="sxs-lookup"><span data-stu-id="b75cd-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="b75cd-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-119">以 null 結束的字串指標，指定設備磁碟機設定動態連結程式庫的檔案名或完整路徑和檔案名 (例如 C： \\ 驅動程式 \\Pscrptui.dll) 。</span><span class="sxs-lookup"><span data-stu-id="b75cd-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="b75cd-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-121">以 null 結束的字串指標，指定設備磁碟機的說明檔的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\ Pscrptui .hlp) 。</span><span class="sxs-lookup"><span data-stu-id="b75cd-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="b75cd-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-123">MultiSZ 緩衝區的指標，其中包含以 null 終止之字串的序列。</span><span class="sxs-lookup"><span data-stu-id="b75cd-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="b75cd-124">緩衝區中每個以 null 結束的字串都包含驅動程式相依的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b75cd-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="b75cd-125">字串序列會以空的零長度字串來終止。</span><span class="sxs-lookup"><span data-stu-id="b75cd-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="b75cd-126">如果 **pDependentFiles** 不是 **Null** ，而且不包含任何檔案名，則會指向包含兩個空字串的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b75cd-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="b75cd-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-128">指定語言監視器 (之以 null 結束的字串指標，例如「PJL 監視器」 ) 。</span><span class="sxs-lookup"><span data-stu-id="b75cd-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="b75cd-129">這個成員可以是 **Null** ，而且只能針對能夠進行雙向通訊的印表機指定。</span><span class="sxs-lookup"><span data-stu-id="b75cd-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="b75cd-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-131">以 null 結束的字串指標，指定列印工作的預設資料類型 (例如 "EMF" ) 。</span><span class="sxs-lookup"><span data-stu-id="b75cd-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="b75cd-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-133">以 null 結束的字串指標，這個字串會指定與此驅動程式相容的先前印表機驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="b75cd-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="b75cd-134">例如，OldName1 \\ 0OldName2 \\ 0 \\ 0。</span><span class="sxs-lookup"><span data-stu-id="b75cd-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-135">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="b75cd-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-136">驅動程式套件的日期，以驅動程式檔案中的程式碼為程式碼。</span><span class="sxs-lookup"><span data-stu-id="b75cd-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-137">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="b75cd-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-138">驅動程式的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="b75cd-138">The version number of the driver.</span></span> <span data-ttu-id="b75cd-139">這是來自驅動程式的版本結構。</span><span class="sxs-lookup"><span data-stu-id="b75cd-139">This comes from the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-140">**pszMfgName**</span><span class="sxs-lookup"><span data-stu-id="b75cd-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-141">指定制造商名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="b75cd-141">A pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-142">**pszOEMUrl**</span><span class="sxs-lookup"><span data-stu-id="b75cd-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-143">指定制造商 URL 之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="b75cd-143">A pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-144">**pszHardwareID**</span><span class="sxs-lookup"><span data-stu-id="b75cd-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-145">以 null 結束的字串指標，指定印表機驅動程式的硬體識別碼。</span><span class="sxs-lookup"><span data-stu-id="b75cd-145">A pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-146">**pszProvider**</span><span class="sxs-lookup"><span data-stu-id="b75cd-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-147">以 null 結束的字串指標，指定印表機驅動程式的提供者 (例如「Microsoft Windows 2000」 ) 。</span><span class="sxs-lookup"><span data-stu-id="b75cd-147">A pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000").</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-148">**pszPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="b75cd-148">**pszPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-149">以 null 結束的字串指標，指定列印處理器 (例如 "WinPrint" ) 。</span><span class="sxs-lookup"><span data-stu-id="b75cd-149">A pointer to a null-terminated string that specifies the print processor (for example, "WinPrint").</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-150">**pszVendorSetup**</span><span class="sxs-lookup"><span data-stu-id="b75cd-150">**pszVendorSetup**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-151">以 null 結束的字串指標，指定廠商的驅動程式安裝 DLL 和進入點。</span><span class="sxs-lookup"><span data-stu-id="b75cd-151">A pointer to a null-terminated string that specifies the vendor's driver setup DLL and entry point.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-152">**pszzColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="b75cd-152">**pszzColorProfiles**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-153">以 null 結束的字串指標，指定與驅動程式相關聯的色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="b75cd-153">A pointer to a null-terminated string that specifies the color profiles associated with the driver.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-154">**pszInfPath**</span><span class="sxs-lookup"><span data-stu-id="b75cd-154">**pszInfPath**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-155">以 null 結束的字串指標，指定驅動程式的 .inf 檔案在驅動程式存放區中的路徑。</span><span class="sxs-lookup"><span data-stu-id="b75cd-155">A pointer to a null-terminated string that specifies the path to the driver's .inf file in the driver store.</span></span> <span data-ttu-id="b75cd-156"> (請參閱 [備註]。如果要將驅動程式 \_ 資訊 \_ 8 傳遞給 [**AddPrinterDriver**](addprinterdriver.md)或 [**AddPrinterDriverEx**](addprinterdriverex.md)，請 ) 此值必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="b75cd-156">(See Remarks.) This must be **NULL** if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-157">**dwPrinterDriverAttributes**</span><span class="sxs-lookup"><span data-stu-id="b75cd-157">**dwPrinterDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-158">印表機驅動程式的屬性旗標。</span><span class="sxs-lookup"><span data-stu-id="b75cd-158">Attribute flags for printer drivers.</span></span> <span data-ttu-id="b75cd-159">如果即將將驅動程式 \_ 資訊 \_ 8 傳遞給 [**AddPrinterDriver**](addprinterdriver.md) 或 [**AddPrinterDriverEx**](addprinterdriverex.md)，這就必須是0。</span><span class="sxs-lookup"><span data-stu-id="b75cd-159">This must be 0 if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span> <span data-ttu-id="b75cd-160">否則，它可以是下列旗標的任意組合：</span><span class="sxs-lookup"><span data-stu-id="b75cd-160">Otherwise, it can be any combination of the following flags:</span></span>



| <span data-ttu-id="b75cd-161">旗標名稱/值</span><span class="sxs-lookup"><span data-stu-id="b75cd-161">Flag name/value</span></span>                                                         | <span data-ttu-id="b75cd-162">意義</span><span class="sxs-lookup"><span data-stu-id="b75cd-162">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="b75cd-163">最低 OS</span><span class="sxs-lookup"><span data-stu-id="b75cd-163">Minimum OS</span></span>                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="b75cd-164">印表機 \_ 驅動程式 \_ 套件 \_ 感知</span><span class="sxs-lookup"><span data-stu-id="b75cd-164">PRINTER\_DRIVER\_PACKAGE\_AWARE</span></span><br/> <span data-ttu-id="b75cd-165">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b75cd-165">0x00000001</span></span><br/>        | <span data-ttu-id="b75cd-166">印表機驅動程式是驅動程式套件的一部分。</span><span class="sxs-lookup"><span data-stu-id="b75cd-166">The printer driver is part of a driver package.</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="b75cd-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b75cd-167">Windows Vista</span></span>                                          |
| <span data-ttu-id="b75cd-168">印表機 \_ 驅動程式 \_ XPS</span><span class="sxs-lookup"><span data-stu-id="b75cd-168">PRINTER\_DRIVER\_XPS</span></span><br/> <span data-ttu-id="b75cd-169">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b75cd-169">0x00000002</span></span><br/>                   | <span data-ttu-id="b75cd-170">印表機驅動程式支援 [XML 檔規格：總覽](/previous-versions/windows/hardware/design/dn641615(v=vs.85))和產品行為中所述的 Microsoft XPS 格式 [，<27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)。</span><span class="sxs-lookup"><span data-stu-id="b75cd-170">The printer driver supports the Microsoft XPS format described in the [XML Paper Specification: Overview](/previous-versions/windows/hardware/design/dn641615(v=vs.85)), and also in [Product Behavior, section <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span>                        | <span data-ttu-id="b75cd-171">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b75cd-171">Windows 8</span></span><br/> <span data-ttu-id="b75cd-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b75cd-172">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="b75cd-173">印表機 \_ 驅動程式 \_ 沙箱 \_ 已啟用</span><span class="sxs-lookup"><span data-stu-id="b75cd-173">PRINTER\_DRIVER\_SANDBOX\_ENABLED</span></span><br/> <span data-ttu-id="b75cd-174">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b75cd-174">0x00000004</span></span><br/>      | <span data-ttu-id="b75cd-175">印表機驅動程式與 [印表機驅動程式隔離](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)相容。</span><span class="sxs-lookup"><span data-stu-id="b75cd-175">The printer driver is compatible with [printer driver isolation](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span> <span data-ttu-id="b75cd-176">如需詳細資訊，請參閱 [產品行為 <28>一節 ](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)。</span><span class="sxs-lookup"><span data-stu-id="b75cd-176">For more information, see [Product Behavior, section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span> | <span data-ttu-id="b75cd-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b75cd-177">Windows 7</span></span><br/> <span data-ttu-id="b75cd-178">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b75cd-178">Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="b75cd-179">印表機 \_ 驅動程式 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="b75cd-179">PRINTER\_DRIVER\_CLASS</span></span><br/> <span data-ttu-id="b75cd-180">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b75cd-180">0x00000008</span></span><br/>                 | <span data-ttu-id="b75cd-181">印表機驅動程式是 [類別的印表機驅動程式](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)。</span><span class="sxs-lookup"><span data-stu-id="b75cd-181">The printer driver is a [class printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                       | <span data-ttu-id="b75cd-182">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b75cd-182">Windows 8</span></span><br/> <span data-ttu-id="b75cd-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b75cd-183">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="b75cd-184">衍生的印表機 \_ 驅動程式 \_</span><span class="sxs-lookup"><span data-stu-id="b75cd-184">PRINTER\_DRIVER\_DERIVED</span></span><br/> <span data-ttu-id="b75cd-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b75cd-185">0x00000010</span></span><br/>               | <span data-ttu-id="b75cd-186">印表機驅動程式是 [衍生的印表機驅動程式](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)。</span><span class="sxs-lookup"><span data-stu-id="b75cd-186">The printer driver is a [derived printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                   | <span data-ttu-id="b75cd-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b75cd-187">Windows 8</span></span><br/> <span data-ttu-id="b75cd-188">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b75cd-188">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="b75cd-189">印表機 \_ 驅動程式 \_ 無法 \_ 共用</span><span class="sxs-lookup"><span data-stu-id="b75cd-189">PRINTER\_DRIVER\_NOT\_SHAREABLE</span></span><br/> <span data-ttu-id="b75cd-190">0x00000020</span><span class="sxs-lookup"><span data-stu-id="b75cd-190">0x00000020</span></span><br/>        | <span data-ttu-id="b75cd-191">無法共用使用此印表機驅動程式的印表機。</span><span class="sxs-lookup"><span data-stu-id="b75cd-191">Printers using this printer driver cannot be shared.</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="b75cd-192">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b75cd-192">Windows 8</span></span><br/> <span data-ttu-id="b75cd-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b75cd-193">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="b75cd-194">印表機 \_ 驅動程式 \_ 類別 \_ 傳真</span><span class="sxs-lookup"><span data-stu-id="b75cd-194">PRINTER\_DRIVER\_CATEGORY\_FAX</span></span><br/> <span data-ttu-id="b75cd-195">0x00000040</span><span class="sxs-lookup"><span data-stu-id="b75cd-195">0x00000040</span></span><br/>         | <span data-ttu-id="b75cd-196">印表機驅動程式的目的是要與 [傳真印表機](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b75cd-196">The printer driver is intended for use with [fax printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                    | <span data-ttu-id="b75cd-197">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b75cd-197">Windows 8</span></span><br/> <span data-ttu-id="b75cd-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b75cd-198">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="b75cd-199">印表機 \_ 驅動程式 \_ 類別檔案 \_</span><span class="sxs-lookup"><span data-stu-id="b75cd-199">PRINTER\_DRIVER\_CATEGORY\_FILE</span></span><br/> <span data-ttu-id="b75cd-200">0x00000080</span><span class="sxs-lookup"><span data-stu-id="b75cd-200">0x00000080</span></span><br/>        | <span data-ttu-id="b75cd-201">印表機驅動程式的目的是要與檔案 [印表機](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b75cd-201">The printer driver is intended for use with [file printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                  | <span data-ttu-id="b75cd-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b75cd-202">Windows 8</span></span><br/> <span data-ttu-id="b75cd-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b75cd-203">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="b75cd-204">印表機 \_ 驅動程式 \_ 類別 \_ 虛擬</span><span class="sxs-lookup"><span data-stu-id="b75cd-204">PRINTER\_DRIVER\_CATEGORY\_VIRTUAL</span></span><br/> <span data-ttu-id="b75cd-205">0x00000100</span><span class="sxs-lookup"><span data-stu-id="b75cd-205">0x00000100</span></span><br/>     | <span data-ttu-id="b75cd-206">印表機驅動程式的目的是要搭配 [虛擬印表機](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)使用。</span><span class="sxs-lookup"><span data-stu-id="b75cd-206">The printer driver is intended for use with [virtual printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="b75cd-207">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b75cd-207">Windows 8</span></span><br/> <span data-ttu-id="b75cd-208">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b75cd-208">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="b75cd-209">印表機 \_ 驅動程式 \_ 類別 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="b75cd-209">PRINTER\_DRIVER\_CATEGORY\_SERVICE</span></span><br/> <span data-ttu-id="b75cd-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="b75cd-210">0x00000200</span></span><br/>     | <span data-ttu-id="b75cd-211">印表機驅動程式的目的是要與 [服務印表機](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)一起使用。</span><span class="sxs-lookup"><span data-stu-id="b75cd-211">The printer driver is intended for use with [service printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="b75cd-212">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b75cd-212">Windows 8</span></span><br/> <span data-ttu-id="b75cd-213">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b75cd-213">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="b75cd-214">\_需要印表機驅動程式 \_ 軟 \_ 重設 \_</span><span class="sxs-lookup"><span data-stu-id="b75cd-214">PRINTER\_DRIVER\_SOFT\_RESET\_REQUIRED</span></span><br/> <span data-ttu-id="b75cd-215">0x00000400</span><span class="sxs-lookup"><span data-stu-id="b75cd-215">0x00000400</span></span><br/> | <span data-ttu-id="b75cd-216">使用此印表機驅動程式的印表機應遵循 USB 裝置類別定義中所述的指導方針。</span><span class="sxs-lookup"><span data-stu-id="b75cd-216">Printers that use this printer driver should follow the guidelines outlined in the USB Device Class Definition.</span></span> <span data-ttu-id="b75cd-217">如需詳細資訊，請參閱 [產品行為，第 <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span><span class="sxs-lookup"><span data-stu-id="b75cd-217">For more information, see [Product Behavior, section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span></span>                                                                      | <span data-ttu-id="b75cd-218">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b75cd-218">Windows 8</span></span><br/> <span data-ttu-id="b75cd-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b75cd-219">Windows Server 2012</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="b75cd-220">**pszzCoreDriverDependencies**</span><span class="sxs-lookup"><span data-stu-id="b75cd-220">**pszzCoreDriverDependencies**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-221">以 null 終止的多字串指標，指定驅動程式相依的所有核心印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b75cd-221">A pointer to a null-terminated multi-string that specifies all the core printer drivers that the driver depends on.</span></span> <span data-ttu-id="b75cd-222">如果即將將 **驅動程式 \_ 資訊 \_ 8** 傳遞給 [**AddPrinterDriver**](addprinterdriver.md)或 [**AddPrinterDriverEx**](addprinterdriverex.md)，這就必須是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b75cd-222">This must be **NULL** if the **DRIVER\_INFO\_8** is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-223">**ftMinInboxDriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="b75cd-223">**ftMinInboxDriverVerDate**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-224">Windows 隨附的任何驅動程式和此驅動程式相依的最早允許日期。</span><span class="sxs-lookup"><span data-stu-id="b75cd-224">The earliest allowed date of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> <dt>

<span data-ttu-id="b75cd-225">**dwlMinInboxDriverVerVersion**</span><span class="sxs-lookup"><span data-stu-id="b75cd-225">**dwlMinInboxDriverVerVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b75cd-226">隨附于 Windows 以及此驅動程式所相依之任何驅動程式的最早允許版本。</span><span class="sxs-lookup"><span data-stu-id="b75cd-226">The earliest allowed version of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b75cd-227">備註</span><span class="sxs-lookup"><span data-stu-id="b75cd-227">Remarks</span></span>

<span data-ttu-id="b75cd-228">這些成員的字串包含在用來新增驅動程式的 .inf 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b75cd-228">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="b75cd-229">規格需求</span><span class="sxs-lookup"><span data-stu-id="b75cd-229">Requirements</span></span>



| <span data-ttu-id="b75cd-230">需求</span><span class="sxs-lookup"><span data-stu-id="b75cd-230">Requirement</span></span> | <span data-ttu-id="b75cd-231">值</span><span class="sxs-lookup"><span data-stu-id="b75cd-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b75cd-232">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b75cd-232">Minimum supported client</span></span><br/> | <span data-ttu-id="b75cd-233">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b75cd-233">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b75cd-234">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b75cd-234">Minimum supported server</span></span><br/> | <span data-ttu-id="b75cd-235">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b75cd-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b75cd-236">標頭</span><span class="sxs-lookup"><span data-stu-id="b75cd-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="b75cd-237"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b75cd-237"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b75cd-238">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b75cd-238">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b75cd-239">**\_ 驅動程式 \_ 資訊 \_ 8W** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 8A** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b75cd-239">**\_DRIVER\_INFO\_8W** (Unicode) and **\_DRIVER\_INFO\_8A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="b75cd-240">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b75cd-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75cd-241">列印</span><span class="sxs-lookup"><span data-stu-id="b75cd-241">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b75cd-242">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="b75cd-242">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b75cd-243">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="b75cd-243">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="b75cd-244">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="b75cd-244">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

