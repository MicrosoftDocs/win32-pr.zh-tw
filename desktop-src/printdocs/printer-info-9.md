---
description: 印表機 \_ 資訊 \_ 9 結構會指定每位使用者的預設印表機設定。
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: 'PRINTER_INFO_9 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980673"
---
# <a name="printer_info_9-structure"></a><span data-ttu-id="e47a7-103">印表機 \_ 資訊 \_ 9 結構</span><span class="sxs-lookup"><span data-stu-id="e47a7-103">PRINTER\_INFO\_9 structure</span></span>

<span data-ttu-id="e47a7-104">**印表機 \_ 資訊 \_ 9** 結構會指定每位使用者的預設印表機設定。</span><span class="sxs-lookup"><span data-stu-id="e47a7-104">The **PRINTER\_INFO\_9** structure specifies the per-user default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="e47a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="e47a7-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a><span data-ttu-id="e47a7-106">成員</span><span class="sxs-lookup"><span data-stu-id="e47a7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e47a7-107">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="e47a7-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="e47a7-108">用來定義每個使用者預設印表機資料的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標，例如紙張方向和解析度。</span><span class="sxs-lookup"><span data-stu-id="e47a7-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the per-user default printer data such as the paper orientation and the resolution.</span></span> <span data-ttu-id="e47a7-109">**DEVMODE** 會儲存在使用者的登錄中。</span><span class="sxs-lookup"><span data-stu-id="e47a7-109">The **DEVMODE** is stored in the user's registry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e47a7-110">備註</span><span class="sxs-lookup"><span data-stu-id="e47a7-110">Remarks</span></span>

<span data-ttu-id="e47a7-111">每個使用者預設值只會影響特定使用者或使用此設定檔的任何人。</span><span class="sxs-lookup"><span data-stu-id="e47a7-111">The per-user defaults will affect only a particular user or anyone who uses the profile.</span></span> <span data-ttu-id="e47a7-112">相反地，全域預設值是由可供任何人使用的印表機管理員設定。</span><span class="sxs-lookup"><span data-stu-id="e47a7-112">In contrast, the global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="e47a7-113">若為全域預設值，請使用 [**印表機 \_ 資訊 \_ 8**](printer-info-8.md)。</span><span class="sxs-lookup"><span data-stu-id="e47a7-113">For global defaults, use [**PRINTER\_INFO\_8**](printer-info-8.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e47a7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e47a7-114">Requirements</span></span>



| <span data-ttu-id="e47a7-115">需求</span><span class="sxs-lookup"><span data-stu-id="e47a7-115">Requirement</span></span> | <span data-ttu-id="e47a7-116">值</span><span class="sxs-lookup"><span data-stu-id="e47a7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e47a7-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e47a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e47a7-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e47a7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e47a7-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e47a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e47a7-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e47a7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e47a7-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e47a7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e47a7-122"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e47a7-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e47a7-123">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e47a7-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e47a7-124">**\_ 印表機 \_ 資訊 \_ 9W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 9A** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e47a7-124">**\_PRINTER\_INFO\_9W** (Unicode) and **\_PRINTER\_INFO\_9A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="e47a7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e47a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e47a7-126">列印</span><span class="sxs-lookup"><span data-stu-id="e47a7-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e47a7-127">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="e47a7-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e47a7-128">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="e47a7-128">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="e47a7-129">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="e47a7-129">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="e47a7-130">**印表機 \_ 資訊 \_ 8**</span><span class="sxs-lookup"><span data-stu-id="e47a7-130">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> </dl>

 

 




