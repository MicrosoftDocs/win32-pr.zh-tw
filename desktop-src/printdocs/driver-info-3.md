---
description: 驅動程式 \_ 資訊 \_ 3 結構包含印表機驅動程式資訊。
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: 'DRIVER_INFO_3 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 64509977a85bc33cb13dac4e6ba2817502c06cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996930"
---
# <a name="driver_info_3-structure"></a><span data-ttu-id="1778e-103">驅動程式 \_ 資訊 \_ 3 結構</span><span class="sxs-lookup"><span data-stu-id="1778e-103">DRIVER\_INFO\_3 structure</span></span>

<span data-ttu-id="1778e-104">**驅動程式 \_ 資訊 \_ 3** 結構包含印表機驅動程式資訊。</span><span class="sxs-lookup"><span data-stu-id="1778e-104">The **DRIVER\_INFO\_3** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1778e-105">語法</span><span class="sxs-lookup"><span data-stu-id="1778e-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_3 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="1778e-106">成員</span><span class="sxs-lookup"><span data-stu-id="1778e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1778e-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="1778e-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1778e-108">寫入驅動程式的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="1778e-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="1778e-109">支援的值為3和4，分別代表 V3 和 V4 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="1778e-109">The supported values are 3 and 4, which represent the V3 and V4 drivers, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="1778e-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="1778e-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="1778e-111">以 null 結束的字串指標，指定驅動程式的名稱 (例如 "QMS 810" ) 。</span><span class="sxs-lookup"><span data-stu-id="1778e-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="1778e-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="1778e-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="1778e-113">以 null 結束的字串指標，指定寫入驅動程式的環境 (例如，Windows x86、Windows IA64 和 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="1778e-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="1778e-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="1778e-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="1778e-115">以 null 結束的字串指標，指定包含設備磁碟機之檔案的檔案名或完整路徑和檔案名 (例如 "C： \\ 驅動程式 \\Pscript.dll" ) 。</span><span class="sxs-lookup"><span data-stu-id="1778e-115">A pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "C:\\DRIVERS\\Pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="1778e-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="1778e-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="1778e-117">以 null 結束的字串指標，指定包含驅動程式資料之檔案的檔案名或完整路徑和檔案名 (例如 "C： \\ 驅動程式 \\ Qms810" ) 。</span><span class="sxs-lookup"><span data-stu-id="1778e-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "C:\\DRIVERS\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="1778e-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="1778e-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="1778e-119">以 null 結束的字串指標，指定設備磁碟機設定動態連結程式庫的檔案名或完整路徑和檔案名 (例如 "C： \\ 驅動程式 \\Pscrptui.dll" ) 。</span><span class="sxs-lookup"><span data-stu-id="1778e-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, "C:\\DRIVERS\\Pscrptui.dll").</span></span>

</dd> <dt>

<span data-ttu-id="1778e-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="1778e-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="1778e-121">以 null 終止的字串指標，指定設備磁碟機的說明檔的檔案名或完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="1778e-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="1778e-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="1778e-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="1778e-123">MultiSZ 緩衝區的指標，其中包含以 null 終止之字串的序列。</span><span class="sxs-lookup"><span data-stu-id="1778e-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="1778e-124">緩衝區中每個以 null 結束的字串都包含驅動程式相依的檔案名。</span><span class="sxs-lookup"><span data-stu-id="1778e-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="1778e-125">字串序列會以空的零長度字串來終止。</span><span class="sxs-lookup"><span data-stu-id="1778e-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="1778e-126">如果 **pDependentFiles** 不是 **Null** ，而且不包含任何檔案名，則會指向包含兩個空字串的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1778e-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="1778e-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="1778e-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="1778e-128">指定語言監視器 (之以 null 結束的字串指標，例如「PJL 監視器」 ) 。</span><span class="sxs-lookup"><span data-stu-id="1778e-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="1778e-129">這個成員可以是 **Null** ，而且只能針對能夠進行雙向通訊的印表機指定。</span><span class="sxs-lookup"><span data-stu-id="1778e-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="1778e-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="1778e-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="1778e-131">以 null 結束的字串指標，指定列印工作的預設資料類型 (例如 "EMF" ) 。</span><span class="sxs-lookup"><span data-stu-id="1778e-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1778e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="1778e-132">Requirements</span></span>



| <span data-ttu-id="1778e-133">需求</span><span class="sxs-lookup"><span data-stu-id="1778e-133">Requirement</span></span> | <span data-ttu-id="1778e-134">值</span><span class="sxs-lookup"><span data-stu-id="1778e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1778e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1778e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1778e-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1778e-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1778e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1778e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1778e-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1778e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1778e-139">標頭</span><span class="sxs-lookup"><span data-stu-id="1778e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1778e-140"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1778e-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1778e-141">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1778e-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1778e-142">**\_ 驅動程式 \_ 資訊 \_ 3w 法** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 3a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1778e-142">**\_DRIVER\_INFO\_3W** (Unicode) and **\_DRIVER\_INFO\_3A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="1778e-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1778e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1778e-144">列印</span><span class="sxs-lookup"><span data-stu-id="1778e-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1778e-145">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="1778e-145">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="1778e-146">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1778e-146">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="1778e-147">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="1778e-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="1778e-148">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1778e-148">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




