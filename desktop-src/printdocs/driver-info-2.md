---
description: 驅動程式 \_ 資訊 \_ 2 結構會識別印表機驅動程式、驅動程式版本號碼、寫入驅動程式的環境、儲存驅動程式的檔案名等等。
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: 'DRIVER_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976872"
---
# <a name="driver_info_2-structure"></a><span data-ttu-id="ce3c2-103">驅動程式 \_ 資訊 \_ 2 結構</span><span class="sxs-lookup"><span data-stu-id="ce3c2-103">DRIVER\_INFO\_2 structure</span></span>

<span data-ttu-id="ce3c2-104">**驅動程式 \_ 資訊 \_ 2** 結構會識別印表機驅動程式、驅動程式版本號碼、寫入驅動程式的環境、儲存驅動程式的檔案名等等。</span><span class="sxs-lookup"><span data-stu-id="ce3c2-104">The **DRIVER\_INFO\_2** structure identifies a printer driver, the driver version number, the environment for which the driver was written, the name of the file in which the driver is stored, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce3c2-105">語法</span><span class="sxs-lookup"><span data-stu-id="ce3c2-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="ce3c2-106">成員</span><span class="sxs-lookup"><span data-stu-id="ce3c2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce3c2-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="ce3c2-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ce3c2-108">寫入驅動程式的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="ce3c2-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="ce3c2-109">支援的值為3。</span><span class="sxs-lookup"><span data-stu-id="ce3c2-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="ce3c2-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="ce3c2-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="ce3c2-111">以 null 結束的字串指標，指定驅動程式的名稱 (例如 "QMS 810" ) 。</span><span class="sxs-lookup"><span data-stu-id="ce3c2-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="ce3c2-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="ce3c2-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="ce3c2-113">以 null 結束的字串指標，指定寫入驅動程式的環境 (例如，Windows x86、Windows IA64 和 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="ce3c2-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="ce3c2-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="ce3c2-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="ce3c2-115">以 null 結束的字串指標，指定包含設備磁碟機之檔案的檔案名或完整路徑和檔案名 (例如 "c： \\ 驅動程式 \\pscript.dll" ) 。</span><span class="sxs-lookup"><span data-stu-id="ce3c2-115">A pointer to null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "c:\\drivers\\pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="ce3c2-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="ce3c2-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="ce3c2-117">以 null 結束的字串指標，指定包含驅動程式資料之檔案的檔案名或完整路徑和檔案名 (例如 "c： \\ 驅動程式 \\ Qms810" ) 。</span><span class="sxs-lookup"><span data-stu-id="ce3c2-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "c:\\drivers\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="ce3c2-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="ce3c2-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="ce3c2-119">以 null 結束的字串指標，指定設備磁碟機設定 .dll 的檔案名或完整路徑和檔案名 (例如 "c： driver \\ \\Pscrptui.dll" ) 。</span><span class="sxs-lookup"><span data-stu-id="ce3c2-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device-driver's configuration .dll (for example, "c:\\drivers\\Pscrptui.dll").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce3c2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce3c2-120">Requirements</span></span>



| <span data-ttu-id="ce3c2-121">需求</span><span class="sxs-lookup"><span data-stu-id="ce3c2-121">Requirement</span></span> | <span data-ttu-id="ce3c2-122">值</span><span class="sxs-lookup"><span data-stu-id="ce3c2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce3c2-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce3c2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ce3c2-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce3c2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ce3c2-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce3c2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ce3c2-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce3c2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ce3c2-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ce3c2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce3c2-128"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ce3c2-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ce3c2-129">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="ce3c2-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ce3c2-130">**\_ 驅動程式 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 2a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="ce3c2-130">**\_DRIVER\_INFO\_2W** (Unicode) and **\_DRIVER\_INFO\_2A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="ce3c2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce3c2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3c2-132">列印</span><span class="sxs-lookup"><span data-stu-id="ce3c2-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ce3c2-133">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="ce3c2-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ce3c2-134">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ce3c2-134">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="ce3c2-135">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ce3c2-135">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




