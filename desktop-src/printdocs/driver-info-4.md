---
description: 驅動程式 \_ 資訊 \_ 4 結構包含印表機驅動程式資訊。
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: 'DRIVER_INFO_4 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b737947b19e93a6b8de0563128a0f1be412101ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192600"
---
# <a name="driver_info_4-structure"></a><span data-ttu-id="ce905-103">驅動程式 \_ 資訊 \_ 4 結構</span><span class="sxs-lookup"><span data-stu-id="ce905-103">DRIVER\_INFO\_4 structure</span></span>

<span data-ttu-id="ce905-104">**驅動程式 \_ 資訊 \_ 4** 結構包含印表機驅動程式資訊。</span><span class="sxs-lookup"><span data-stu-id="ce905-104">The **DRIVER\_INFO\_4** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce905-105">語法</span><span class="sxs-lookup"><span data-stu-id="ce905-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_4 {
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
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="ce905-106">成員</span><span class="sxs-lookup"><span data-stu-id="ce905-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce905-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="ce905-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-108">寫入驅動程式的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="ce905-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="ce905-109">支援的值為3。</span><span class="sxs-lookup"><span data-stu-id="ce905-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="ce905-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="ce905-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-111">以 null 結束的字串指標，指定驅動程式的名稱 (例如 "QMS 810" ) 。</span><span class="sxs-lookup"><span data-stu-id="ce905-111">Pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="ce905-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="ce905-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-113">以 null 結束的字串指標，指定寫入驅動程式的環境 (例如，Windows x86、Windows IA64 和 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="ce905-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="ce905-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="ce905-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-115">以 null 結束的字串指標，指定包含設備磁碟機之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\Pscript.dll) 。</span><span class="sxs-lookup"><span data-stu-id="ce905-115">Pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="ce905-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="ce905-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-117">以 null 結束的字串指標，指定包含驅動程式資料之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\ Qms810) 。</span><span class="sxs-lookup"><span data-stu-id="ce905-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="ce905-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="ce905-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-119">以 null 結束的字串指標，指定設備磁碟機設定動態連結程式庫的檔案名或完整路徑和檔案名 (例如 C： \\ 驅動程式 \\Pscrptui.dll) 。</span><span class="sxs-lookup"><span data-stu-id="ce905-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="ce905-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="ce905-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-121">以 null 結束的字串指標，指定設備磁碟機的說明檔的檔案名或完整路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="ce905-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="ce905-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="ce905-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-123">MultiSZ 緩衝區的指標，其中包含以 null 終止之字串的序列。</span><span class="sxs-lookup"><span data-stu-id="ce905-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="ce905-124">緩衝區中每個以 null 結束的字串都包含驅動程式相依的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ce905-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="ce905-125">字串序列會以空的零長度字串來終止。</span><span class="sxs-lookup"><span data-stu-id="ce905-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="ce905-126">如果 **pDependentFiles** 不是 **Null** ，而且不包含任何檔案名，則會指向包含兩個空字串的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ce905-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="ce905-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="ce905-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-128">指定語言監視器 (之以 null 結束的字串指標，例如 PJL 監視器) 。</span><span class="sxs-lookup"><span data-stu-id="ce905-128">A pointer to a null-terminated string that specifies a language monitor (for example, PJL monitor).</span></span> <span data-ttu-id="ce905-129">這個成員可以是 **Null** ，而且只能針對能夠進行雙向通訊的印表機指定。</span><span class="sxs-lookup"><span data-stu-id="ce905-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="ce905-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="ce905-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-131">以 null 結束的字串指標，指定列印工作的預設資料類型 (例如，EMF) 。</span><span class="sxs-lookup"><span data-stu-id="ce905-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, EMF).</span></span>

</dd> <dt>

<span data-ttu-id="ce905-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="ce905-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="ce905-133">以 null 結束的字串指標，這個字串會指定與此驅動程式相容的先前印表機驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="ce905-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="ce905-134">例如，OldName1 \\ 0OldName2 \\ 0 \\ 0。</span><span class="sxs-lookup"><span data-stu-id="ce905-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce905-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce905-135">Requirements</span></span>



| <span data-ttu-id="ce905-136">需求</span><span class="sxs-lookup"><span data-stu-id="ce905-136">Requirement</span></span> | <span data-ttu-id="ce905-137">值</span><span class="sxs-lookup"><span data-stu-id="ce905-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce905-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce905-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ce905-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce905-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ce905-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce905-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ce905-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce905-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ce905-142">標頭</span><span class="sxs-lookup"><span data-stu-id="ce905-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce905-143"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ce905-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ce905-144">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="ce905-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ce905-145">**\_ 驅動程式 \_ 資訊 \_ 4W** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 4a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="ce905-145">**\_DRIVER\_INFO\_4W** (Unicode) and **\_DRIVER\_INFO\_4A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="ce905-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce905-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce905-147">列印</span><span class="sxs-lookup"><span data-stu-id="ce905-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ce905-148">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="ce905-148">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ce905-149">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ce905-149">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="ce905-150">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="ce905-150">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="ce905-151">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ce905-151">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




