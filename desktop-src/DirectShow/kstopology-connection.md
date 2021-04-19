---
description: 本主題適用于 Windows XP Service Pack 2 或更新版本。 KSTOPOLOGY \_ 連接結構描述核心串流 (KS) 篩選器內的節點連接。 節點可以連接到篩選中的另一個節點，或連接到篩選器上的釘選。
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: 'KSTOPOLOGY_CONNECTION 結構 (Ks) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978800"
---
# <a name="kstopology_connection-structure"></a><span data-ttu-id="abf13-105">KSTOPOLOGY \_ 連接結構</span><span class="sxs-lookup"><span data-stu-id="abf13-105">KSTOPOLOGY\_CONNECTION structure</span></span>

<span data-ttu-id="abf13-106">本主題適用于 Windows XP Service Pack 2 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="abf13-106">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="abf13-107">**KSTOPOLOGY \_ 連接** 結構描述核心串流 (KS) 篩選器內的節點連接。</span><span class="sxs-lookup"><span data-stu-id="abf13-107">The **KSTOPOLOGY\_CONNECTION** structure describes a node connection within a kernel-streaming (KS) filter.</span></span> <span data-ttu-id="abf13-108">節點可以連接到篩選中的另一個節點，或連接到篩選器上的釘選。</span><span class="sxs-lookup"><span data-stu-id="abf13-108">A node can be connected to another node within the filter, or to a pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf13-109">語法</span><span class="sxs-lookup"><span data-stu-id="abf13-109">Syntax</span></span>


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a><span data-ttu-id="abf13-110">成員</span><span class="sxs-lookup"><span data-stu-id="abf13-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="abf13-111">**FromNode**</span><span class="sxs-lookup"><span data-stu-id="abf13-111">**FromNode**</span></span>
</dt> <dd>

<span data-ttu-id="abf13-112">連接中上游節點的索引。</span><span class="sxs-lookup"><span data-stu-id="abf13-112">Index of the upstream node in the connection.</span></span> <span data-ttu-id="abf13-113">如果上游連線是一個 pin，而不是節點，則值為 KSFILTER \_ node。</span><span class="sxs-lookup"><span data-stu-id="abf13-113">If the upstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="abf13-114">**FromNodePin**</span><span class="sxs-lookup"><span data-stu-id="abf13-114">**FromNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="abf13-115">如果 [ **FromNode** ] 欄位的值是 [KSFILTER] \_ 節點，則此欄位會指定上游釘選的索引。</span><span class="sxs-lookup"><span data-stu-id="abf13-115">If the value of the **FromNode** field is KSFILTER\_NODE, this field specifies the index of the upstream pin.</span></span> <span data-ttu-id="abf13-116">否則會忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="abf13-116">Otherwise, this field is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="abf13-117">**ToNode**</span><span class="sxs-lookup"><span data-stu-id="abf13-117">**ToNode**</span></span>
</dt> <dd>

<span data-ttu-id="abf13-118">連接中下游節點的索引。</span><span class="sxs-lookup"><span data-stu-id="abf13-118">Index of the downstream node in the connection.</span></span> <span data-ttu-id="abf13-119">如果下游連線是一個固定的，而不是節點，則值為 KSFILTER \_ node。</span><span class="sxs-lookup"><span data-stu-id="abf13-119">If the downstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="abf13-120">**ToNodePin**</span><span class="sxs-lookup"><span data-stu-id="abf13-120">**ToNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="abf13-121">如果 **ToNode** 欄位的值為 KSFILTER \_ 節點，則此欄位會指定下游 pin 的索引。</span><span class="sxs-lookup"><span data-stu-id="abf13-121">If the value of the **ToNode** field is KSFILTER\_NODE, this field specifies the index of the downstream pin.</span></span> <span data-ttu-id="abf13-122">否則會忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="abf13-122">Otherwise, this field is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abf13-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="abf13-123">Requirements</span></span>



| <span data-ttu-id="abf13-124">需求</span><span class="sxs-lookup"><span data-stu-id="abf13-124">Requirement</span></span> | <span data-ttu-id="abf13-125">值</span><span class="sxs-lookup"><span data-stu-id="abf13-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="abf13-126">標頭</span><span class="sxs-lookup"><span data-stu-id="abf13-126">Header</span></span><br/> | <dl> <span data-ttu-id="abf13-127"><dt>Ks. h</dt></span><span class="sxs-lookup"><span data-stu-id="abf13-127"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abf13-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abf13-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abf13-129">DirectShow 結構</span><span class="sxs-lookup"><span data-stu-id="abf13-129">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="abf13-130">**IKsTopologyInfo：： get \_ ConnectionInfo**</span><span class="sxs-lookup"><span data-stu-id="abf13-130">**IKsTopologyInfo::get\_ConnectionInfo**</span></span>](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




