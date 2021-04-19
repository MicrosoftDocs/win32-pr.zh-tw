---
description: 驅動程式 \_ 資訊 \_ 1 結構會識別印表機驅動程式。
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: 'DRIVER_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 21301cdab4449d0a48254660d195d4f2507a80e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987766"
---
# <a name="driver_info_1-structure"></a><span data-ttu-id="50f52-103">驅動程式 \_ 資訊 \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="50f52-103">DRIVER\_INFO\_1 structure</span></span>

<span data-ttu-id="50f52-104">**驅動程式 \_ 資訊 \_ 1** 結構會識別印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="50f52-104">The **DRIVER\_INFO\_1** structure identifies a printer driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f52-105">語法</span><span class="sxs-lookup"><span data-stu-id="50f52-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="50f52-106">成員</span><span class="sxs-lookup"><span data-stu-id="50f52-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="50f52-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="50f52-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="50f52-108">指定印表機驅動程式名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="50f52-108">Pointer to a null-terminated string that specifies the name of a printer driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50f52-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="50f52-109">Requirements</span></span>



| <span data-ttu-id="50f52-110">需求</span><span class="sxs-lookup"><span data-stu-id="50f52-110">Requirement</span></span> | <span data-ttu-id="50f52-111">值</span><span class="sxs-lookup"><span data-stu-id="50f52-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f52-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50f52-112">Minimum supported client</span></span><br/> | <span data-ttu-id="50f52-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50f52-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="50f52-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50f52-114">Minimum supported server</span></span><br/> | <span data-ttu-id="50f52-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50f52-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="50f52-116">標頭</span><span class="sxs-lookup"><span data-stu-id="50f52-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="50f52-117"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="50f52-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="50f52-118">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="50f52-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="50f52-119">**\_ 驅動程式 \_ 資訊 \_ 1W** (Unicode) 和 **\_ 驅動程式 \_ 資訊 \_ 1a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="50f52-119">**\_DRIVER\_INFO\_1W** (Unicode) and **\_DRIVER\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="50f52-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50f52-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f52-121">列印</span><span class="sxs-lookup"><span data-stu-id="50f52-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="50f52-122">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="50f52-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="50f52-123">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="50f52-123">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

 




