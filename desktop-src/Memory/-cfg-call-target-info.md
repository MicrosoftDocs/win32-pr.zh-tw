---
description: 代表控制流程防護 (CFG) 的呼叫目標相關資訊。
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: 'CFG_CALL_TARGET_INFO 結構 (Ntmmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974267"
---
# <a name="cfg_call_target_info-structure"></a><span data-ttu-id="42a67-103">CFG \_ 呼叫 \_ 目標 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="42a67-103">CFG\_CALL\_TARGET\_INFO structure</span></span>

<span data-ttu-id="42a67-104">代表控制流程防護 (CFG) 的呼叫目標相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42a67-104">Represents information about call targets for Control Flow Guard (CFG).</span></span>

## <a name="syntax"></a><span data-ttu-id="42a67-105">語法</span><span class="sxs-lookup"><span data-stu-id="42a67-105">Syntax</span></span>


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="42a67-106">成員</span><span class="sxs-lookup"><span data-stu-id="42a67-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="42a67-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="42a67-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="42a67-108">相對於所提供之 (開始) 虛擬位址的位移。</span><span class="sxs-lookup"><span data-stu-id="42a67-108">Offset relative to a provided (start) virtual address.</span></span> <span data-ttu-id="42a67-109">此位移應為16位元組對齊。</span><span class="sxs-lookup"><span data-stu-id="42a67-109">This offset should be 16 byte aligned.</span></span>

</dd> <dt>

<span data-ttu-id="42a67-110">**旗標**</span><span class="sxs-lookup"><span data-stu-id="42a67-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="42a67-111">描述要在位址上執行之作業的旗標。</span><span class="sxs-lookup"><span data-stu-id="42a67-111">Flags describing the operation to be performed on the address.</span></span> <span data-ttu-id="42a67-112">如果已設定 **cfg \_ 呼叫 \_ 目標 \_ 有效** ，則會將位址標示為適用于 CFG。</span><span class="sxs-lookup"><span data-stu-id="42a67-112">If **CFG\_CALL\_TARGET\_VALID** is set, then the address will be marked valid for CFG.</span></span> <span data-ttu-id="42a67-113">否則，它會標示為不正確呼叫目標。</span><span class="sxs-lookup"><span data-stu-id="42a67-113">Otherwise, it will be marked an invalid call target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42a67-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="42a67-114">Requirements</span></span>



| <span data-ttu-id="42a67-115">需求</span><span class="sxs-lookup"><span data-stu-id="42a67-115">Requirement</span></span> | <span data-ttu-id="42a67-116">值</span><span class="sxs-lookup"><span data-stu-id="42a67-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42a67-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42a67-117">Minimum supported client</span></span><br/> | <span data-ttu-id="42a67-118">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42a67-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="42a67-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42a67-119">Minimum supported server</span></span><br/> | <span data-ttu-id="42a67-120">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42a67-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42a67-121">標頭</span><span class="sxs-lookup"><span data-stu-id="42a67-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a67-122"><dt>Ntmmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="42a67-122"><dt>Ntmmapi.h</dt></span></span> </dl> |



 

 




