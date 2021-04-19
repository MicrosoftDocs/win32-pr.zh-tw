---
description: PROVIDOR \_ INFO \_ 2 結構會將列印提供者附加至列印提供者順序清單。
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: 'PROVIDOR_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980603"
---
# <a name="providor_info_2-structure"></a><span data-ttu-id="f7e42-103">PROVIDOR \_ INFO \_ 2 結構</span><span class="sxs-lookup"><span data-stu-id="f7e42-103">PROVIDOR\_INFO\_2 structure</span></span>

<span data-ttu-id="f7e42-104">**PROVIDOR \_ INFO \_ 2** 結構會將列印提供者附加至列印提供者順序清單。</span><span class="sxs-lookup"><span data-stu-id="f7e42-104">The **PROVIDOR\_INFO\_2** structure appends a print provider to the print provider order list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e42-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7e42-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="f7e42-106">成員</span><span class="sxs-lookup"><span data-stu-id="f7e42-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f7e42-107">**pOrder**</span><span class="sxs-lookup"><span data-stu-id="f7e42-107">**pOrder**</span></span>
</dt> <dd>

<span data-ttu-id="f7e42-108">以 null 結束的字串指標，指定列印提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7e42-108">Pointer to a null-terminated string that specifies the name of the print provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7e42-109">備註</span><span class="sxs-lookup"><span data-stu-id="f7e42-109">Remarks</span></span>

<span data-ttu-id="f7e42-110">呼叫 [**AddPrintProvidor**](addprintprovidor.md)（層級2）時，會使用這個結構，將指定的列印提供者加入至列印提供者順序清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="f7e42-110">This structure is used when calling [**AddPrintProvidor**](addprintprovidor.md), level 2, to add the specified print provider to the end of the print provider order list.</span></span> <span data-ttu-id="f7e42-111">如果呼叫成功，則會立即將提供者用於路由。</span><span class="sxs-lookup"><span data-stu-id="f7e42-111">The provider is immediately used for routing if the call succeeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e42-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7e42-112">Requirements</span></span>



| <span data-ttu-id="f7e42-113">需求</span><span class="sxs-lookup"><span data-stu-id="f7e42-113">Requirement</span></span> | <span data-ttu-id="f7e42-114">值</span><span class="sxs-lookup"><span data-stu-id="f7e42-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e42-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7e42-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e42-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7e42-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f7e42-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7e42-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e42-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7e42-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f7e42-119">標頭</span><span class="sxs-lookup"><span data-stu-id="f7e42-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7e42-120"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f7e42-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f7e42-121">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f7e42-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f7e42-122">**\_ PROVIDOR \_ Info \_ 2w** (Unicode) 和 **\_ PROVIDOR \_ INFO \_ 2a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f7e42-122">**\_PROVIDOR\_INFO\_2W** (Unicode) and **\_PROVIDOR\_INFO\_2A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="f7e42-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7e42-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e42-124">列印</span><span class="sxs-lookup"><span data-stu-id="f7e42-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f7e42-125">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="f7e42-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f7e42-126">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="f7e42-126">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




