---
description: HANDOFFENTRY 結構會在 HANDOFFTABLE 結構中定義特定的通訊協定專案。
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: 'HANDOFFENTRY 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510971"
---
# <a name="handoffentry-structure"></a><span data-ttu-id="26090-103">HANDOFFENTRY 結構</span><span class="sxs-lookup"><span data-stu-id="26090-103">HANDOFFENTRY structure</span></span>

<span data-ttu-id="26090-104">**HANDOFFENTRY** 結構會在 **HANDOFFTABLE** 結構中定義特定的通訊協定專案。</span><span class="sxs-lookup"><span data-stu-id="26090-104">The **HANDOFFENTRY** structure defines a specific protocol entry in a **HANDOFFTABLE** structure.</span></span>

<span data-ttu-id="26090-105">根據使用者在呼叫 [**CreateHandoffTable**](createhandofftable.md) 函式時提供的 .ini 檔中的資訊，網路監視器填入此結構。</span><span class="sxs-lookup"><span data-stu-id="26090-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span> <span data-ttu-id="26090-106">應用程式絕對不應明確修改此結構。</span><span class="sxs-lookup"><span data-stu-id="26090-106">This structure should never be explicitly modified by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="26090-107">語法</span><span class="sxs-lookup"><span data-stu-id="26090-107">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="26090-108">成員</span><span class="sxs-lookup"><span data-stu-id="26090-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="26090-109">**hoe \_ sig**</span><span class="sxs-lookup"><span data-stu-id="26090-109">**hoe\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="26090-110">將此專案識別為遞交資料表專案的簽章。</span><span class="sxs-lookup"><span data-stu-id="26090-110">Signature that identifies this entry as a handoff table entry.</span></span>

</dd> <dt>

<span data-ttu-id="26090-111">**hoe \_ ProtIdentNumber**</span><span class="sxs-lookup"><span data-stu-id="26090-111">**hoe\_ProtIdentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="26090-112">使用者提供的 .ini 檔案所提供的通訊協定編號。</span><span class="sxs-lookup"><span data-stu-id="26090-112">Protocol number provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="26090-113">**hoe \_ ProtocolHandle**</span><span class="sxs-lookup"><span data-stu-id="26090-113">**hoe\_ProtocolHandle**</span></span>
</dt> <dd>

<span data-ttu-id="26090-114">使用由使用者提供的 .ini 檔案提供的通訊協定名稱建立的通訊協定控制碼。</span><span class="sxs-lookup"><span data-stu-id="26090-114">Handle of protocol created using the protocol name provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="26090-115">**hoe \_ ProtocolData**</span><span class="sxs-lookup"><span data-stu-id="26090-115">**hoe\_ProtocolData**</span></span>
</dt> <dd>

<span data-ttu-id="26090-116">使用者提供的 .ini 檔案所提供的通訊協定實例資料。</span><span class="sxs-lookup"><span data-stu-id="26090-116">Protocol instance data provided by user supplied .ini file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26090-117">備註</span><span class="sxs-lookup"><span data-stu-id="26090-117">Remarks</span></span>

<span data-ttu-id="26090-118">當網路監視器建立遞交資料表時，網路監視器會填入此結構。</span><span class="sxs-lookup"><span data-stu-id="26090-118">This structure is filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

## <a name="requirements"></a><span data-ttu-id="26090-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="26090-119">Requirements</span></span>



| <span data-ttu-id="26090-120">需求</span><span class="sxs-lookup"><span data-stu-id="26090-120">Requirement</span></span> | <span data-ttu-id="26090-121">值</span><span class="sxs-lookup"><span data-stu-id="26090-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26090-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26090-122">Minimum supported client</span></span><br/> | <span data-ttu-id="26090-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26090-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="26090-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26090-124">Minimum supported server</span></span><br/> | <span data-ttu-id="26090-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26090-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="26090-126">標頭</span><span class="sxs-lookup"><span data-stu-id="26090-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="26090-127"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="26090-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26090-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26090-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26090-129">HANDOFFTABLE</span><span class="sxs-lookup"><span data-stu-id="26090-129">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




