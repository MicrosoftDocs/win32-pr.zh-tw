---
description: 指定以 OpenPrinter2 開啟之印表機的控制碼快取。
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: 'PRINTER_OPTION_FLAGS 列舉 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194282"
---
# <a name="printer_option_flags-enumeration"></a><span data-ttu-id="37923-103">印表機 \_ 選項 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="37923-103">PRINTER\_OPTION\_FLAGS enumeration</span></span>

<span data-ttu-id="37923-104">指定以 [**OpenPrinter2**](openprinter2.md)開啟之印表機的控制碼快取。</span><span class="sxs-lookup"><span data-stu-id="37923-104">Specifies the caching of a handle for a printer opened with [**OpenPrinter2**](openprinter2.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="37923-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37923-105">Syntax</span></span>


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="37923-106">常數</span><span class="sxs-lookup"><span data-stu-id="37923-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="37923-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**印表機 \_ 選項 \_ 沒有快取 \_**</span><span class="sxs-lookup"><span data-stu-id="37923-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**PRINTER\_OPTION\_NO\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="37923-108">控制碼不會被快取。</span><span class="sxs-lookup"><span data-stu-id="37923-108">The handle is not cached.</span></span> <span data-ttu-id="37923-109">所有套用至 [**OpenPrinter2**](openprinter2.md) 所傳回之控制碼的函式都會移至遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="37923-109">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="37923-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**印表機 \_ 選項快取 \_**</span><span class="sxs-lookup"><span data-stu-id="37923-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**PRINTER\_OPTION\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="37923-111">會快取控制碼。</span><span class="sxs-lookup"><span data-stu-id="37923-111">The handle is cached.</span></span> <span data-ttu-id="37923-112">所有套用至 [**OpenPrinter2**](openprinter2.md) 所傳回之控制碼的函式都會移至本機快取。</span><span class="sxs-lookup"><span data-stu-id="37923-112">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the local cache.</span></span>

</dd> <dt>

<span data-ttu-id="37923-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**印表機 \_ 選項 \_ 用戶端 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="37923-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**PRINTER\_OPTION\_CLIENT\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="37923-114">[**SetPrinter**](setprinter.md)會使用 [**OpenPrinter2**](openprinter2.md)傳回的控制碼來重新命名印表機連接。</span><span class="sxs-lookup"><span data-stu-id="37923-114">The handle returned by [**OpenPrinter2**](openprinter2.md) can be used by [**SetPrinter**](setprinter.md) to rename the printer connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37923-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="37923-115">Requirements</span></span>



| <span data-ttu-id="37923-116">需求</span><span class="sxs-lookup"><span data-stu-id="37923-116">Requirement</span></span> | <span data-ttu-id="37923-117">值</span><span class="sxs-lookup"><span data-stu-id="37923-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37923-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37923-118">Minimum supported client</span></span><br/> | <span data-ttu-id="37923-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37923-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="37923-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37923-120">Minimum supported server</span></span><br/> | <span data-ttu-id="37923-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37923-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="37923-122">標頭</span><span class="sxs-lookup"><span data-stu-id="37923-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="37923-123"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="37923-123"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37923-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37923-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37923-125">列印</span><span class="sxs-lookup"><span data-stu-id="37923-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="37923-126">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="37923-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="37923-127">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="37923-127">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="37923-128">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="37923-128">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




