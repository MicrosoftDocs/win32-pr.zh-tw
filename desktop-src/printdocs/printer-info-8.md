---
description: 印表機 \_ 資訊 \_ 8 結構會指定全域預設印表機設定。
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: 'PRINTER_INFO_8 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852224"
---
# <a name="printer_info_8-structure"></a><span data-ttu-id="5d56e-103">印表機 \_ 資訊 \_ 8 結構</span><span class="sxs-lookup"><span data-stu-id="5d56e-103">PRINTER\_INFO\_8 structure</span></span>

<span data-ttu-id="5d56e-104">**印表機 \_ 資訊 \_ 8** 結構會指定全域預設印表機設定。</span><span class="sxs-lookup"><span data-stu-id="5d56e-104">The **PRINTER\_INFO\_8** structure specifies the global default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d56e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5d56e-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="5d56e-106">成員</span><span class="sxs-lookup"><span data-stu-id="5d56e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d56e-107">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="5d56e-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="5d56e-108">用來定義全域預設印表機資料的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標，例如紙張方向和解析度。</span><span class="sxs-lookup"><span data-stu-id="5d56e-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the global default printer data such as the paper orientation and the resolution.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d56e-109">備註</span><span class="sxs-lookup"><span data-stu-id="5d56e-109">Remarks</span></span>

<span data-ttu-id="5d56e-110">全域預設值是由可供任何人使用之印表機的系統管理員所設定。</span><span class="sxs-lookup"><span data-stu-id="5d56e-110">The global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="5d56e-111">相反地，每個使用者的預設值將會影響特定使用者或使用該設定檔的其他人。</span><span class="sxs-lookup"><span data-stu-id="5d56e-111">In contrast, the per-user defaults will affect a particular user or anyone else who uses the profile.</span></span> <span data-ttu-id="5d56e-112">針對每個使用者預設，請使用 [**印表機 \_ 資訊 \_ 9**](printer-info-9.md)。</span><span class="sxs-lookup"><span data-stu-id="5d56e-112">For per-user defaults, use [**PRINTER\_INFO\_9**](printer-info-9.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d56e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d56e-113">Requirements</span></span>



| <span data-ttu-id="5d56e-114">需求</span><span class="sxs-lookup"><span data-stu-id="5d56e-114">Requirement</span></span> | <span data-ttu-id="5d56e-115">值</span><span class="sxs-lookup"><span data-stu-id="5d56e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d56e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d56e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5d56e-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d56e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5d56e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d56e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5d56e-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d56e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5d56e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5d56e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d56e-121"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5d56e-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5d56e-122">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="5d56e-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5d56e-123">**\_ 印表機 \_ 資訊 \_ 8W** (Unicode) 和 **\_ 印表機 \_ 資訊 \_ 8A** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="5d56e-123">**\_PRINTER\_INFO\_8W** (Unicode) and **\_PRINTER\_INFO\_8A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="5d56e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d56e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d56e-125">列印</span><span class="sxs-lookup"><span data-stu-id="5d56e-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5d56e-126">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="5d56e-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="5d56e-127">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="5d56e-127">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="5d56e-128">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="5d56e-128">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="5d56e-129">**印表機 \_ 資訊 \_ 9**</span><span class="sxs-lookup"><span data-stu-id="5d56e-129">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> </dl>

 

 




