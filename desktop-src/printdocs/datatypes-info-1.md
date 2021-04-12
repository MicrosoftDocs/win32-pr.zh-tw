---
description: 資料類型 \_ 資訊 \_ 1 結構包含用來記錄列印工作之資料類型的相關資訊。
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: 'DATATYPES_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e7259f6559220697538774fef8d2460318df84c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192725"
---
# <a name="datatypes_info_1-structure"></a><span data-ttu-id="bada9-103">資料類型 \_ 資訊 \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="bada9-103">DATATYPES\_INFO\_1 structure</span></span>

<span data-ttu-id="bada9-104">資料 **類型 \_ 資訊 \_ 1** 結構包含用來記錄列印工作之資料類型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bada9-104">The **DATATYPES\_INFO\_1** structure contains information about the data type used to record a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="bada9-105">語法</span><span class="sxs-lookup"><span data-stu-id="bada9-105">Syntax</span></span>


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a><span data-ttu-id="bada9-106">成員</span><span class="sxs-lookup"><span data-stu-id="bada9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bada9-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="bada9-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="bada9-108">以 null 結束的字串指標，識別用來記錄列印工作的資料類型。</span><span class="sxs-lookup"><span data-stu-id="bada9-108">Pointer to a null-terminated string that identifies the data type used to record a print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bada9-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="bada9-109">Requirements</span></span>



| <span data-ttu-id="bada9-110">需求</span><span class="sxs-lookup"><span data-stu-id="bada9-110">Requirement</span></span> | <span data-ttu-id="bada9-111">值</span><span class="sxs-lookup"><span data-stu-id="bada9-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bada9-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bada9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bada9-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bada9-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bada9-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bada9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bada9-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bada9-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bada9-116">標頭</span><span class="sxs-lookup"><span data-stu-id="bada9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="bada9-117"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bada9-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bada9-118">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="bada9-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bada9-119">**\_ 資料類型 \_ 資訊 \_ 1W** (Unicode) 和 **\_ 資料類型 \_ 資訊 \_ 1a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="bada9-119">**\_DATATYPES\_INFO\_1W** (Unicode) and **\_DATATYPES\_INFO\_1A** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="bada9-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bada9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bada9-121">列印</span><span class="sxs-lookup"><span data-stu-id="bada9-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bada9-122">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="bada9-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="bada9-123">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="bada9-123">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




