---
description: 代表印表機選項。
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: 'PRINTER_OPTIONS 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993196"
---
# <a name="printer_options-structure"></a><span data-ttu-id="4145e-103">印表機 \_ 選項結構</span><span class="sxs-lookup"><span data-stu-id="4145e-103">PRINTER\_OPTIONS structure</span></span>

<span data-ttu-id="4145e-104">代表印表機選項。</span><span class="sxs-lookup"><span data-stu-id="4145e-104">Represents printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="4145e-105">語法</span><span class="sxs-lookup"><span data-stu-id="4145e-105">Syntax</span></span>


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="4145e-106">成員</span><span class="sxs-lookup"><span data-stu-id="4145e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4145e-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="4145e-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="4145e-108">**印表機 \_ 選項** 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="4145e-108">The size of the **PRINTER\_OPTIONS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="4145e-109">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="4145e-109">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4145e-110">一組 [**印表機 \_ 選項 \_ 旗標**](printer-option-flags.md) ，指定其他函式將如何使用 [**OpenPrinter2**](openprinter2.md) 所傳回之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4145e-110">A set of [**PRINTER\_OPTION\_FLAGS**](printer-option-flags.md) that specifies how the handle to a printer returned by [**OpenPrinter2**](openprinter2.md) will be used by other functions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4145e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="4145e-111">Requirements</span></span>



| <span data-ttu-id="4145e-112">需求</span><span class="sxs-lookup"><span data-stu-id="4145e-112">Requirement</span></span> | <span data-ttu-id="4145e-113">值</span><span class="sxs-lookup"><span data-stu-id="4145e-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4145e-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4145e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4145e-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4145e-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4145e-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4145e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4145e-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4145e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4145e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="4145e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4145e-119"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4145e-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4145e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4145e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4145e-121">列印</span><span class="sxs-lookup"><span data-stu-id="4145e-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4145e-122">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="4145e-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4145e-123">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="4145e-123">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="4145e-124">**印表機 \_ 選項 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="4145e-124">**PRINTER\_OPTION\_FLAGS**</span></span>](printer-option-flags.md)
</dt> </dl>

 

 




