---
description: PRINTPROCESSOR \_ INFO \_ 1 結構會指定已安裝的列印處理器名稱。
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: 'PRINTPROCESSOR_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985683"
---
# <a name="printprocessor_info_1-structure"></a><span data-ttu-id="bc660-103">PRINTPROCESSOR \_ INFO \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="bc660-103">PRINTPROCESSOR\_INFO\_1 structure</span></span>

<span data-ttu-id="bc660-104">**PRINTPROCESSOR \_ INFO \_ 1** 結構會指定已安裝的列印處理器名稱。</span><span class="sxs-lookup"><span data-stu-id="bc660-104">The **PRINTPROCESSOR\_INFO\_1** structure specifies the name of an installed print processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc660-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc660-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="bc660-106">成員</span><span class="sxs-lookup"><span data-stu-id="bc660-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc660-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="bc660-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="bc660-108">指定已安裝之列印處理器名稱的以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="bc660-108">Pointer to a null-terminated string that specifies the name of an installed print processor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc660-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc660-109">Requirements</span></span>



| <span data-ttu-id="bc660-110">需求</span><span class="sxs-lookup"><span data-stu-id="bc660-110">Requirement</span></span> | <span data-ttu-id="bc660-111">值</span><span class="sxs-lookup"><span data-stu-id="bc660-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc660-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc660-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bc660-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc660-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bc660-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc660-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bc660-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc660-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bc660-116">標頭</span><span class="sxs-lookup"><span data-stu-id="bc660-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc660-117"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bc660-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bc660-118">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="bc660-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bc660-119">**\_ PRINTPROCESSOR \_ Info \_ 1W** (Unicode) 和 **\_ PRINTPROCESSOR \_ info \_ 1a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="bc660-119">**\_PRINTPROCESSOR\_INFO\_1W** (Unicode) and **\_PRINTPROCESSOR\_INFO\_1A** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="bc660-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc660-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc660-121">列印</span><span class="sxs-lookup"><span data-stu-id="bc660-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bc660-122">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="bc660-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="bc660-123">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="bc660-123">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

 




