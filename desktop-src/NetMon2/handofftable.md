---
description: HANDOFFTABLE 結構會定義出交付資料表的通訊協定。
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: 'HANDOFFTABLE 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991685"
---
# <a name="handofftable-structure"></a><span data-ttu-id="e6132-103">HANDOFFTABLE 結構</span><span class="sxs-lookup"><span data-stu-id="e6132-103">HANDOFFTABLE structure</span></span>

<span data-ttu-id="e6132-104">**HANDOFFTABLE** 結構會定義出交付資料表的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e6132-104">The **HANDOFFTABLE** structure defines the protocols of a handoff table.</span></span>

<span data-ttu-id="e6132-105">根據使用者在呼叫 [**CreateHandoffTable**](createhandofftable.md) 函式時提供的 .ini 檔中的資訊，網路監視器填入此結構。</span><span class="sxs-lookup"><span data-stu-id="e6132-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6132-106">語法</span><span class="sxs-lookup"><span data-stu-id="e6132-106">Syntax</span></span>


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a><span data-ttu-id="e6132-107">成員</span><span class="sxs-lookup"><span data-stu-id="e6132-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6132-108">**熱 \_ sig**</span><span class="sxs-lookup"><span data-stu-id="e6132-108">**hot\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="e6132-109">將此資料表識別為遞交資料表的簽章。</span><span class="sxs-lookup"><span data-stu-id="e6132-109">Signature that identifies this table as a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="e6132-110">**熱 \_ NumEntries**</span><span class="sxs-lookup"><span data-stu-id="e6132-110">**hot\_NumEntries**</span></span>
</dt> <dd>

<span data-ttu-id="e6132-111">網路監視器加入至遞交資料表的專案數目。</span><span class="sxs-lookup"><span data-stu-id="e6132-111">Number of entries that Network Monitor added to the handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="e6132-112">**熱門 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="e6132-112">**hot\_Entries**</span></span>
</dt> <dd>

<span data-ttu-id="e6132-113">提交資料表。</span><span class="sxs-lookup"><span data-stu-id="e6132-113">Handoff table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6132-114">備註</span><span class="sxs-lookup"><span data-stu-id="e6132-114">Remarks</span></span>

<span data-ttu-id="e6132-115">當網路監視器建立一個遞交資料表時，網路監視器會填入此結構及其相關聯的 HANDOFFENTRY 結構。</span><span class="sxs-lookup"><span data-stu-id="e6132-115">This structure, and its associated HANDOFFENTRY structures, are filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

<span data-ttu-id="e6132-116">當呼叫 [**CreateHandoffTable**](createhandofftable.md) 時，會在應用程式提供的 .ini 檔案中提供建立遞交資料表時所使用的通訊協定資訊。</span><span class="sxs-lookup"><span data-stu-id="e6132-116">The protocol information that is used when creating a handoff table is provided in an .ini file supplied by the application when [**CreateHandoffTable**](createhandofftable.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6132-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6132-117">Requirements</span></span>



| <span data-ttu-id="e6132-118">需求</span><span class="sxs-lookup"><span data-stu-id="e6132-118">Requirement</span></span> | <span data-ttu-id="e6132-119">值</span><span class="sxs-lookup"><span data-stu-id="e6132-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e6132-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6132-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e6132-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6132-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e6132-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6132-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e6132-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6132-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e6132-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e6132-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6132-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e6132-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6132-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6132-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6132-127">HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="e6132-127">HANDOFFENTRY</span></span>](handoffentry.md)
</dt> <dt>

[<span data-ttu-id="e6132-128">CreateHandoffTable</span><span class="sxs-lookup"><span data-stu-id="e6132-128">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> </dl>

 

 




