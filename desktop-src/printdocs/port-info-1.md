---
description: 埠 \_ 資訊 \_ 1 結構會識別支援的印表機埠。
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: 'PORT_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d64e7dfa29cbe6b3f7efd3aaa0076851aea0311b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981566"
---
# <a name="port_info_1-structure"></a><span data-ttu-id="a9643-103">埠 \_ 資訊 \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="a9643-103">PORT\_INFO\_1 structure</span></span>

<span data-ttu-id="a9643-104">**埠 \_ 資訊 \_ 1** 結構會識別支援的印表機埠。</span><span class="sxs-lookup"><span data-stu-id="a9643-104">The **PORT\_INFO\_1** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9643-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9643-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a><span data-ttu-id="a9643-106">成員</span><span class="sxs-lookup"><span data-stu-id="a9643-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9643-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="a9643-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="a9643-108">識別支援之印表機埠 (以 null 終止的字串指標，例如 "LPT1：" ) 。</span><span class="sxs-lookup"><span data-stu-id="a9643-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9643-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9643-109">Requirements</span></span>



| <span data-ttu-id="a9643-110">需求</span><span class="sxs-lookup"><span data-stu-id="a9643-110">Requirement</span></span> | <span data-ttu-id="a9643-111">值</span><span class="sxs-lookup"><span data-stu-id="a9643-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9643-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9643-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a9643-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9643-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a9643-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9643-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a9643-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9643-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a9643-116">標頭</span><span class="sxs-lookup"><span data-stu-id="a9643-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9643-117"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a9643-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a9643-118">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a9643-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a9643-119">**\_ 埠 \_ 資訊 \_ 1W** (Unicode) 和 **\_ 埠 \_ 資訊 \_ 1a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a9643-119">**\_PORT\_INFO\_1W** (Unicode) and **\_PORT\_INFO\_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="a9643-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9643-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9643-121">列印</span><span class="sxs-lookup"><span data-stu-id="a9643-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a9643-122">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="a9643-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a9643-123">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="a9643-123">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




