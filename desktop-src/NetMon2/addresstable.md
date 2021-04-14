---
description: ADDRESSTABLE 結構包含位址配對的表格。
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: 'ADDRESSTABLE 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469288"
---
# <a name="addresstable-structure"></a><span data-ttu-id="7f7b8-103">ADDRESSTABLE 結構</span><span class="sxs-lookup"><span data-stu-id="7f7b8-103">ADDRESSTABLE structure</span></span>

<span data-ttu-id="7f7b8-104">**ADDRESSTABLE** 結構包含位址配對的表格。</span><span class="sxs-lookup"><span data-stu-id="7f7b8-104">The **ADDRESSTABLE** structure contains a table of address pairs.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f7b8-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f7b8-105">Syntax</span></span>


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a><span data-ttu-id="7f7b8-106">成員</span><span class="sxs-lookup"><span data-stu-id="7f7b8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f7b8-107">**nAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="7f7b8-107">**nAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="7f7b8-108">**AddressPair** 陣列中的位址組數目。</span><span class="sxs-lookup"><span data-stu-id="7f7b8-108">Number of address pairs in the **AddressPair** array.</span></span>

</dd> <dt>

<span data-ttu-id="7f7b8-109">**nNonMacAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="7f7b8-109">**nNonMacAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="7f7b8-110">非 MAC 位址組的數目。</span><span class="sxs-lookup"><span data-stu-id="7f7b8-110">Number of non-MAC address pairs.</span></span>

</dd> <dt>

<span data-ttu-id="7f7b8-111">**AddressPair**</span><span class="sxs-lookup"><span data-stu-id="7f7b8-111">**AddressPair**</span></span>
</dt> <dd>

<span data-ttu-id="7f7b8-112">位址組的陣列。</span><span class="sxs-lookup"><span data-stu-id="7f7b8-112">Array of address pairs.</span></span> <span data-ttu-id="7f7b8-113">請注意，您最多隻能為每個 ADDRESSTABLE 結構儲存八個位址組。</span><span class="sxs-lookup"><span data-stu-id="7f7b8-113">Note that you may only store up to eight address pairs per ADDRESSTABLE structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f7b8-114">備註</span><span class="sxs-lookup"><span data-stu-id="7f7b8-114">Remarks</span></span>

<span data-ttu-id="7f7b8-115">使用此結構作為 capture 篩選器結構處理的一部分。</span><span class="sxs-lookup"><span data-stu-id="7f7b8-115">Use this structure as part of the capture filter construction process.</span></span> <span data-ttu-id="7f7b8-116">如需有關如何執行此結構的詳細資訊，請參閱「 [捕獲篩選準則](capture-filters.md)」。</span><span class="sxs-lookup"><span data-stu-id="7f7b8-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f7b8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f7b8-117">Requirements</span></span>



| <span data-ttu-id="7f7b8-118">需求</span><span class="sxs-lookup"><span data-stu-id="7f7b8-118">Requirement</span></span> | <span data-ttu-id="7f7b8-119">值</span><span class="sxs-lookup"><span data-stu-id="7f7b8-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7f7b8-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f7b8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7f7b8-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f7b8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7f7b8-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f7b8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7f7b8-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f7b8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7f7b8-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7f7b8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f7b8-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="7f7b8-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f7b8-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f7b8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f7b8-127">ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="7f7b8-127">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="7f7b8-128">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="7f7b8-128">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




