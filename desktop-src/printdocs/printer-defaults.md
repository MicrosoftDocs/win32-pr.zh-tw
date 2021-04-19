---
description: 印表機 \_ 預設結構會指定印表機的預設資料類型、環境、初始化資料和存取權限。
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: 'PRINTER_DEFAULTS 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998304"
---
# <a name="printer_defaults-structure"></a><span data-ttu-id="e03a1-103">印表機 \_ 預設結構</span><span class="sxs-lookup"><span data-stu-id="e03a1-103">PRINTER\_DEFAULTS structure</span></span>

<span data-ttu-id="e03a1-104">**印表機 \_ 預設** 結構會指定印表機的預設資料類型、環境、初始化資料和存取權限。</span><span class="sxs-lookup"><span data-stu-id="e03a1-104">The **PRINTER\_DEFAULTS** structure specifies the default data type, environment, initialization data, and access rights for a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e03a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="e03a1-105">Syntax</span></span>


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a><span data-ttu-id="e03a1-106">成員</span><span class="sxs-lookup"><span data-stu-id="e03a1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e03a1-107">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="e03a1-107">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="e03a1-108">以 null 結束的字串指標，指定印表機的預設資料類型。</span><span class="sxs-lookup"><span data-stu-id="e03a1-108">Pointer to a null-terminated string that specifies the default data type for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="e03a1-109">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="e03a1-109">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="e03a1-110">用來識別印表機預設環境和初始化資料的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="e03a1-110">Pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that identifies the default environment and initialization data for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="e03a1-111">**DesiredAccess**</span><span class="sxs-lookup"><span data-stu-id="e03a1-111">**DesiredAccess**</span></span>
</dt> <dd>

<span data-ttu-id="e03a1-112">指定印表機所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="e03a1-112">Specifies desired access rights for a printer.</span></span> <span data-ttu-id="e03a1-113">[**OpenPrinter**](openprinter.md)函式會使用這個成員來設定印表機的存取權限。</span><span class="sxs-lookup"><span data-stu-id="e03a1-113">The [**OpenPrinter**](openprinter.md) function uses this member to set access rights to the printer.</span></span> <span data-ttu-id="e03a1-114">這些許可權可能會影響 [**SetPrinter**](setprinter.md) 和 [**DeletePrinter**](deleteprinter.md) 函數的操作。</span><span class="sxs-lookup"><span data-stu-id="e03a1-114">These rights can affect the operation of the [**SetPrinter**](setprinter.md) and [**DeletePrinter**](deleteprinter.md) functions.</span></span> <span data-ttu-id="e03a1-115">存取權限可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="e03a1-115">The access rights can be one of the following.</span></span>



| <span data-ttu-id="e03a1-116">值</span><span class="sxs-lookup"><span data-stu-id="e03a1-116">Value</span></span>                                       | <span data-ttu-id="e03a1-117">意義</span><span class="sxs-lookup"><span data-stu-id="e03a1-117">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e03a1-118">印表機 \_ 存取 \_ 管理</span><span class="sxs-lookup"><span data-stu-id="e03a1-118">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="e03a1-119">執行管理工作，例如 [**SetPrinter**](setprinter.md)所提供的工作。</span><span class="sxs-lookup"><span data-stu-id="e03a1-119">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="e03a1-120">印表機 \_ 存取 \_ 使用</span><span class="sxs-lookup"><span data-stu-id="e03a1-120">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="e03a1-121">執行基本列印工作。</span><span class="sxs-lookup"><span data-stu-id="e03a1-121">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="e03a1-122">印表機 \_ 存取 \_ 管理 \_ 受限</span><span class="sxs-lookup"><span data-stu-id="e03a1-122">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="e03a1-123">執行管理工作，例如 [**SetPrinter**](setprinter.md) 和 [**SetPrinterData**](setprinterdata.md)所提供的工作。</span><span class="sxs-lookup"><span data-stu-id="e03a1-123">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="e03a1-124">從 Windows 8.1 開始，可以使用這個值。</span><span class="sxs-lookup"><span data-stu-id="e03a1-124">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="e03a1-125">印表機 \_ 所有 \_ 存取</span><span class="sxs-lookup"><span data-stu-id="e03a1-125">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="e03a1-126">若要執行所有管理工作和基本列印工作，除了同步處理 (請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights) ) 。</span><span class="sxs-lookup"><span data-stu-id="e03a1-126">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights) ).</span></span>                                   |
| <span data-ttu-id="e03a1-127">一般安全性值，例如寫入 \_ DAC</span><span class="sxs-lookup"><span data-stu-id="e03a1-127">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="e03a1-128">允許特定的控制存取權限。</span><span class="sxs-lookup"><span data-stu-id="e03a1-128">To allow specific control access rights.</span></span> <span data-ttu-id="e03a1-129">請參閱 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="e03a1-129">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e03a1-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e03a1-130">Requirements</span></span>



| <span data-ttu-id="e03a1-131">需求</span><span class="sxs-lookup"><span data-stu-id="e03a1-131">Requirement</span></span> | <span data-ttu-id="e03a1-132">值</span><span class="sxs-lookup"><span data-stu-id="e03a1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e03a1-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e03a1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e03a1-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e03a1-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e03a1-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e03a1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e03a1-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e03a1-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e03a1-137">標頭</span><span class="sxs-lookup"><span data-stu-id="e03a1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e03a1-138"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e03a1-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e03a1-139">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e03a1-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e03a1-140">**\_ 印表機 \_ DEFAULTSW** (Unicode) 和 **\_ 印表機 \_ DEFAULTSA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e03a1-140">**\_PRINTER\_DEFAULTSW** (Unicode) and **\_PRINTER\_DEFAULTSA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="e03a1-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e03a1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e03a1-142">列印</span><span class="sxs-lookup"><span data-stu-id="e03a1-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e03a1-143">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="e03a1-143">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e03a1-144">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="e03a1-144">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="e03a1-145">**版**</span><span class="sxs-lookup"><span data-stu-id="e03a1-145">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="e03a1-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e03a1-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="e03a1-147">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="e03a1-147">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

