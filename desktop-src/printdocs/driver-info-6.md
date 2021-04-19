---
description: 驅動程式 \_ 資訊 \_ 6 結構包含印表機驅動程式資訊。
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: 'DRIVER_INFO_6 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969341"
---
# <a name="driver_info_6-structure"></a><span data-ttu-id="5c577-103">驅動程式 \_ 資訊 \_ 6 結構</span><span class="sxs-lookup"><span data-stu-id="5c577-103">DRIVER\_INFO\_6 structure</span></span>

<span data-ttu-id="5c577-104">**驅動程式 \_ 資訊 \_ 6** 結構包含印表機驅動程式資訊。</span><span class="sxs-lookup"><span data-stu-id="5c577-104">The **DRIVER\_INFO\_6** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c577-105">語法</span><span class="sxs-lookup"><span data-stu-id="5c577-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_6 {
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
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="5c577-106">成員</span><span class="sxs-lookup"><span data-stu-id="5c577-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c577-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="5c577-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-108">寫入驅動程式的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="5c577-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="5c577-109">支援的值為3。</span><span class="sxs-lookup"><span data-stu-id="5c577-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="5c577-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="5c577-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-111">以 null 結束的字串指標，指定驅動程式的名稱 (例如，QMS 810) 。</span><span class="sxs-lookup"><span data-stu-id="5c577-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="5c577-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="5c577-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-113">以 null 結束的字串指標，指定寫入驅動程式的環境 (例如 Windows NT x86、Windows IA64 和 Windows x64。</span><span class="sxs-lookup"><span data-stu-id="5c577-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows NT x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="5c577-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="5c577-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-115">指標，指向以 null 終止的字串，這個字串會指定包含設備磁碟機之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\Pscript.dll) 。</span><span class="sxs-lookup"><span data-stu-id="5c577-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="5c577-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="5c577-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-117">以 null 結束的字串指標，指定包含驅動程式資料之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\ Qms810) 。</span><span class="sxs-lookup"><span data-stu-id="5c577-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="5c577-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="5c577-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-119">以 null 結束的字串指標，指定設備磁碟機設定動態連結程式庫的檔案名或完整路徑和檔案名 (例如 C： \\ 驅動程式 \\Pscrptui.dll) 。</span><span class="sxs-lookup"><span data-stu-id="5c577-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="5c577-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="5c577-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-121">以 null 結束的字串指標，指定設備磁碟機的說明檔的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\ Pscrptui .hlp) 。</span><span class="sxs-lookup"><span data-stu-id="5c577-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="5c577-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="5c577-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-123">MultiSZ 緩衝區的指標，其中包含以 null 終止之字串的序列。</span><span class="sxs-lookup"><span data-stu-id="5c577-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="5c577-124">緩衝區中每個以 null 結束的字串都包含驅動程式相依的檔案名。</span><span class="sxs-lookup"><span data-stu-id="5c577-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="5c577-125">字串序列會以空的零長度字串來終止。</span><span class="sxs-lookup"><span data-stu-id="5c577-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="5c577-126">如果 **pDependentFiles** 不是 **Null** ，而且不包含任何檔案名，則會指向包含兩個空字串的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5c577-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="5c577-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="5c577-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-128">指定語言監視器 (之以 null 結束的字串指標，例如「PJL 監視器」 ) 。</span><span class="sxs-lookup"><span data-stu-id="5c577-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="5c577-129">這個成員可以是 **Null** ，而且只能針對能夠進行雙向通訊的印表機指定。</span><span class="sxs-lookup"><span data-stu-id="5c577-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="5c577-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="5c577-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-131">以 null 結束的字串指標，指定列印工作的預設資料類型 (例如 "EMF" ) 。</span><span class="sxs-lookup"><span data-stu-id="5c577-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="5c577-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="5c577-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-133">以 null 結束的字串指標，這個字串會指定與此驅動程式相容的先前印表機驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="5c577-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="5c577-134">例如，OldName1 \\ 0OldName2 \\ 0 \\ 0。</span><span class="sxs-lookup"><span data-stu-id="5c577-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="5c577-135">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="5c577-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-136">驅動程式套件的日期，以驅動程式檔案中的程式碼為程式碼。</span><span class="sxs-lookup"><span data-stu-id="5c577-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="5c577-137">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="5c577-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-138">驅動程式的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="5c577-138">Version number of the driver.</span></span> <span data-ttu-id="5c577-139">這就是驅動程式的版本結構。</span><span class="sxs-lookup"><span data-stu-id="5c577-139">This comes out of the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="5c577-140">**pszMfgName**</span><span class="sxs-lookup"><span data-stu-id="5c577-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-141">指定制造商名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="5c577-141">Pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="5c577-142">**pszOEMUrl**</span><span class="sxs-lookup"><span data-stu-id="5c577-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-143">指定制造商 URL 之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="5c577-143">Pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="5c577-144">**pszHardwareID**</span><span class="sxs-lookup"><span data-stu-id="5c577-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-145">以 null 結束的字串指標，指定印表機驅動程式的硬體識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c577-145">Pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="5c577-146">**pszProvider**</span><span class="sxs-lookup"><span data-stu-id="5c577-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="5c577-147">以 null 結束的字串指標，指定印表機驅動程式的提供者 (例如「Microsoft Windows 2000」 ) </span><span class="sxs-lookup"><span data-stu-id="5c577-147">Pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000")</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c577-148">備註</span><span class="sxs-lookup"><span data-stu-id="5c577-148">Remarks</span></span>

<span data-ttu-id="5c577-149">這些成員的字串包含在用來新增驅動程式的 .inf 檔案中。</span><span class="sxs-lookup"><span data-stu-id="5c577-149">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

<span data-ttu-id="5c577-150">如果您呼叫 [**AddPrinterDriver**](addprinterdriver.md) 或 [**AddPrinterDriverEx**](addprinterdriverex.md) （其 *層級* 不等於6），然後呼叫 [**GetPrinterDriver**](getprinterdriver.md) 或 [**EnumPrinterDrivers**](enumprinterdrivers.md) ， *且層級* 等於6，則會傳回 **驅動程式 \_ 資訊 \_ 6** 結構，並將 **PszMfgName**、 **pszOEMUrl**、 **pszHardwareID** 和 **pszProvider** 設為 **Null**、 **dwlDriverVersion** 設定為0，而 **ftDriverDate** 設定為 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="5c577-150">If you call [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md) with *Level* not equal to 6, and then you call [**GetPrinterDriver**](getprinterdriver.md) or [**EnumPrinterDrivers**](enumprinterdrivers.md) with *Level* equal to 6, the **DRIVER\_INFO\_6** structure is returned with **pszMfgName**, **pszOEMUrl**, **pszHardwareID**, and **pszProvider** set to **NULL**, **dwlDriverVersion** set to 0, and **ftDriverDate** set to (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c577-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c577-151">Requirements</span></span>



| <span data-ttu-id="5c577-152">需求</span><span class="sxs-lookup"><span data-stu-id="5c577-152">Requirement</span></span> | <span data-ttu-id="5c577-153">值</span><span class="sxs-lookup"><span data-stu-id="5c577-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c577-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c577-154">Minimum supported client</span></span><br/> | <span data-ttu-id="5c577-155">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c577-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c577-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c577-156">Minimum supported server</span></span><br/> | <span data-ttu-id="5c577-157">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c577-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5c577-158">標頭</span><span class="sxs-lookup"><span data-stu-id="5c577-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c577-159"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5c577-159"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5c577-160">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="5c577-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5c577-161">**\_ 驅動程式 \_ 資訊 \_ 6W** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 6a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="5c577-161">**\_DRIVER\_INFO\_6W** (Unicode) and **\_DRIVER\_INFO\_6A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="5c577-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c577-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c577-163">列印</span><span class="sxs-lookup"><span data-stu-id="5c577-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5c577-164">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="5c577-164">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="5c577-165">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="5c577-165">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="5c577-166">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="5c577-166">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="5c577-167">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="5c577-167">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="5c577-168">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="5c577-168">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




