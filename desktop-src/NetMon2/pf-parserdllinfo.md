---
description: PF \_ PARSERDLLINFO 結構會定義位於剖析器 DLL 中的剖析器。
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: 'PF_PARSERDLLINFO 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944639"
---
# <a name="pf_parserdllinfo-structure"></a><span data-ttu-id="2b75a-103">PF \_ PARSERDLLINFO 結構</span><span class="sxs-lookup"><span data-stu-id="2b75a-103">PF\_PARSERDLLINFO structure</span></span>

<span data-ttu-id="2b75a-104">**PF \_ PARSERDLLINFO** 結構會定義位於剖析器 DLL 中的剖析器。</span><span class="sxs-lookup"><span data-stu-id="2b75a-104">The **PF\_PARSERDLLINFO** structure defines the parsers located in the parser DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b75a-105">語法</span><span class="sxs-lookup"><span data-stu-id="2b75a-105">Syntax</span></span>


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a><span data-ttu-id="2b75a-106">成員</span><span class="sxs-lookup"><span data-stu-id="2b75a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b75a-107">**nParsers**</span><span class="sxs-lookup"><span data-stu-id="2b75a-107">**nParsers**</span></span>
</dt> <dd>

<span data-ttu-id="2b75a-108">剖析器 DLL 中的剖析器數目。</span><span class="sxs-lookup"><span data-stu-id="2b75a-108">Number of parsers in the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="2b75a-109">**ParserInfo**</span><span class="sxs-lookup"><span data-stu-id="2b75a-109">**ParserInfo**</span></span>
</dt> <dd>

<span data-ttu-id="2b75a-110">[PF \_ PARSERINFO](pf-parserinfo.md)結構的陣列，描述剖析器 DLL 中的每個剖析器。</span><span class="sxs-lookup"><span data-stu-id="2b75a-110">Array of [PF\_PARSERINFO](pf-parserinfo.md) structures that describe each parser in the parser DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b75a-111">備註</span><span class="sxs-lookup"><span data-stu-id="2b75a-111">Remarks</span></span>

<span data-ttu-id="2b75a-112">在剖析器 DLL 中執行的 [ParserAutoInstallInfo](parserautoinstallinfo.md)匯出函數會傳回 **PF \_ PARSERDLLINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="2b75a-112">The **PF\_PARSERDLLINFO** structure is returned by the [ParserAutoInstallInfo](parserautoinstallinfo.md) export function that is implemented in the parser DLL.</span></span> <span data-ttu-id="2b75a-113">**ParserAutoInstallInfo** 函式會識別 DLL 中的剖析器數目，並使用 [PF \_ PARSERINFO](pf-parserinfo.md)結構的陣列來描述每個剖析器。</span><span class="sxs-lookup"><span data-stu-id="2b75a-113">The **ParserAutoInstallInfo** function identifies the number of parsers in the DLL, and uses an array of [PF\_PARSERINFO](pf-parserinfo.md) structures to describe each parser.</span></span>

<span data-ttu-id="2b75a-114">您 \_ 必須使用 **HeapAlloc** 來配置 PF PARSERDLLINFO 結構。</span><span class="sxs-lookup"><span data-stu-id="2b75a-114">The PF\_PARSERDLLINFO structure must be allocated using **HeapAlloc**.</span></span>



| <span data-ttu-id="2b75a-115">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="2b75a-115">For information on</span></span>                                               | <span data-ttu-id="2b75a-116">請參閱</span><span class="sxs-lookup"><span data-stu-id="2b75a-116">See</span></span>                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="2b75a-117">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="2b75a-117">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="2b75a-118">解析 器</span><span class="sxs-lookup"><span data-stu-id="2b75a-118">Parsers</span></span>](parsers.md)                                                      |
| <span data-ttu-id="2b75a-119">剖析器 DLL 中包含的進入點。</span><span class="sxs-lookup"><span data-stu-id="2b75a-119">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="2b75a-120">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="2b75a-120">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                      |
| <span data-ttu-id="2b75a-121">如何執行 **ParserAutoInstallInfo**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="2b75a-121">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="2b75a-122">執行 ParserAutoIstallInfo</span><span class="sxs-lookup"><span data-stu-id="2b75a-122">Implementing ParserAutoIstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="2b75a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b75a-123">Requirements</span></span>



| <span data-ttu-id="2b75a-124">需求</span><span class="sxs-lookup"><span data-stu-id="2b75a-124">Requirement</span></span> | <span data-ttu-id="2b75a-125">值</span><span class="sxs-lookup"><span data-stu-id="2b75a-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2b75a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b75a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2b75a-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b75a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2b75a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b75a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2b75a-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b75a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2b75a-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2b75a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b75a-131"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="2b75a-131"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b75a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b75a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b75a-133">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="2b75a-133">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="2b75a-134">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="2b75a-134">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> </dl>

 

 




