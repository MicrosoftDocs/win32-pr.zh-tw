---
description: 驅動程式 \_ 資訊 \_ 5 結構包含印表機驅動程式資訊。
ms.assetid: 6fb63a9f-5227-46a3-97dc-8de1968e9d63
title: 'DRIVER_INFO_5 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_5
- _DRIVER_INFO_5A
- _DRIVER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 11281e69b70b2d87d354138a6313c8bca6673944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984724"
---
# <a name="driver_info_5-structure"></a><span data-ttu-id="f6633-103">驅動程式 \_ 資訊 \_ 5 結構</span><span class="sxs-lookup"><span data-stu-id="f6633-103">DRIVER\_INFO\_5 structure</span></span>

<span data-ttu-id="f6633-104">**驅動程式 \_ 資訊 \_ 5** 結構包含印表機驅動程式資訊。</span><span class="sxs-lookup"><span data-stu-id="f6633-104">The **DRIVER\_INFO\_5** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6633-105">語法</span><span class="sxs-lookup"><span data-stu-id="f6633-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_5 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  DWORD  dwDriverAttributes;
  DWORD  dwConfigVersion;
  DWORD  dwDriverVersion;
} DRIVER_INFO_5, *PDRIVER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="f6633-106">成員</span><span class="sxs-lookup"><span data-stu-id="f6633-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f6633-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="f6633-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f6633-108">寫入驅動程式的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="f6633-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="f6633-109">支援的值為3。</span><span class="sxs-lookup"><span data-stu-id="f6633-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="f6633-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="f6633-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="f6633-111">以 null 結束的字串指標，指定驅動程式的名稱 (例如，QMS 810) 。</span><span class="sxs-lookup"><span data-stu-id="f6633-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="f6633-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="f6633-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="f6633-113">以 null 結束的字串指標，指定寫入驅動程式的環境 (例如，Windows x86、Windows IA64 和 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="f6633-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="f6633-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="f6633-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="f6633-115">指標，指向以 null 終止的字串，這個字串會指定包含設備磁碟機之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\Pscript.dll) 。</span><span class="sxs-lookup"><span data-stu-id="f6633-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="f6633-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="f6633-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="f6633-117">以 null 結束的字串指標，指定包含驅動程式資料之檔案的檔案名或完整路徑和檔案名 (例如，C： \\ 驅動程式 \\ Qms810) 。</span><span class="sxs-lookup"><span data-stu-id="f6633-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="f6633-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="f6633-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="f6633-119">以 null 結束的字串指標，指定設備磁碟機設定動態連結程式庫的檔案名或完整路徑和檔案名 (例如 C： \\ 驅動程式 \\Pscrptui.dll) 。</span><span class="sxs-lookup"><span data-stu-id="f6633-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="f6633-120">**dwDriverAttributes**</span><span class="sxs-lookup"><span data-stu-id="f6633-120">**dwDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="f6633-121">驅動程式屬性，例如 UMPD/KMPD。</span><span class="sxs-lookup"><span data-stu-id="f6633-121">Driver attributes, like UMPD/KMPD.</span></span>

</dd> <dt>

<span data-ttu-id="f6633-122">**dwConfigVersion**</span><span class="sxs-lookup"><span data-stu-id="f6633-122">**dwConfigVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f6633-123">自上次重新開機多工緩衝處理器之後，此驅動程式的設定檔已升級或降級的次數。</span><span class="sxs-lookup"><span data-stu-id="f6633-123">Number of times the configuration file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> <dt>

<span data-ttu-id="f6633-124">**dwDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="f6633-124">**dwDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f6633-125">自上次重新開機多工緩衝處理器之後，此驅動程式的驅動程式檔案已升級或降級的次數。</span><span class="sxs-lookup"><span data-stu-id="f6633-125">Number of times the driver file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6633-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6633-126">Requirements</span></span>



| <span data-ttu-id="f6633-127">需求</span><span class="sxs-lookup"><span data-stu-id="f6633-127">Requirement</span></span> | <span data-ttu-id="f6633-128">值</span><span class="sxs-lookup"><span data-stu-id="f6633-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6633-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6633-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f6633-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6633-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f6633-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6633-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f6633-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6633-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f6633-133">標頭</span><span class="sxs-lookup"><span data-stu-id="f6633-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6633-134"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f6633-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f6633-135">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f6633-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f6633-136">**\_ 驅動 \_ 程式 \_ 資訊** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 5a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f6633-136">**\_DRIVER\_INFO\_5W** (Unicode) and **\_DRIVER\_INFO\_5A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="f6633-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6633-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6633-138">列印</span><span class="sxs-lookup"><span data-stu-id="f6633-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f6633-139">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="f6633-139">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f6633-140">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="f6633-140">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="f6633-141">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="f6633-141">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="f6633-142">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="f6633-142">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




