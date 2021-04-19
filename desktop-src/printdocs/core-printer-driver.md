---
description: 代表其他印表機驅動程式所依存的印表機驅動程式。
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: 'CORE_PRINTER_DRIVER 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997125"
---
# <a name="core_printer_driver-structure"></a><span data-ttu-id="38f87-103">核心 \_ 印表機 \_ 驅動程式結構</span><span class="sxs-lookup"><span data-stu-id="38f87-103">CORE\_PRINTER\_DRIVER structure</span></span>

<span data-ttu-id="38f87-104">代表其他印表機驅動程式所依存的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="38f87-104">Represents a printer driver on which other printer drivers depend.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f87-105">語法</span><span class="sxs-lookup"><span data-stu-id="38f87-105">Syntax</span></span>


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a><span data-ttu-id="38f87-106">成員</span><span class="sxs-lookup"><span data-stu-id="38f87-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="38f87-107">**CoreDriverGUID**</span><span class="sxs-lookup"><span data-stu-id="38f87-107">**CoreDriverGUID**</span></span>
</dt> <dd>

<span data-ttu-id="38f87-108">核心印表機驅動程式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="38f87-108">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="38f87-109">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="38f87-109">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="38f87-110">最新版本的核心印表機驅動程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="38f87-110">The date and time of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="38f87-111">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="38f87-111">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="38f87-112">最新版本的核心印表機驅動程式的版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="38f87-112">The version ID of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="38f87-113">**szPackageID \[ 最大 \_ 路徑\]**</span><span class="sxs-lookup"><span data-stu-id="38f87-113">**szPackageID\[MAX\_PATH\]**</span></span>
</dt> <dd>

<span data-ttu-id="38f87-114">包含核心印表機驅動程式之驅動程式套件的路徑。</span><span class="sxs-lookup"><span data-stu-id="38f87-114">The path to the driver package that contains the core printer driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38f87-115">備註</span><span class="sxs-lookup"><span data-stu-id="38f87-115">Remarks</span></span>

<span data-ttu-id="38f87-116">此結構可代表製造商的基礎驅動程式，而該驅動程式的驅動程式與各種印表機型號相依。</span><span class="sxs-lookup"><span data-stu-id="38f87-116">This structure can represent a manufacturer's base driver on which the drivers for various printer models are dependent.</span></span>

## <a name="requirements"></a><span data-ttu-id="38f87-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="38f87-117">Requirements</span></span>



| <span data-ttu-id="38f87-118">需求</span><span class="sxs-lookup"><span data-stu-id="38f87-118">Requirement</span></span> | <span data-ttu-id="38f87-119">值</span><span class="sxs-lookup"><span data-stu-id="38f87-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38f87-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38f87-120">Minimum supported client</span></span><br/> | <span data-ttu-id="38f87-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38f87-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="38f87-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38f87-122">Minimum supported server</span></span><br/> | <span data-ttu-id="38f87-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38f87-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="38f87-124">標頭</span><span class="sxs-lookup"><span data-stu-id="38f87-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="38f87-125"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="38f87-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="38f87-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="38f87-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="38f87-127">**\_ 核心 \_ 印表機 \_ DRIVERW** (Unicode) 和 **\_ 核心 \_ 印表機 \_ DRIVERA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="38f87-127">**\_CORE\_PRINTER\_DRIVERW** (Unicode) and **\_CORE\_PRINTER\_DRIVERA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="38f87-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38f87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f87-129">列印</span><span class="sxs-lookup"><span data-stu-id="38f87-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="38f87-130">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="38f87-130">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




