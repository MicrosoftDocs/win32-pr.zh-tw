---
description: EXPERTFRAMEDESCRIPTOR 結構包含框架的相關資訊。 當專家成功呼叫 ExpertGetFrame 函式時，網路監視器會將 EXPERTFRAMEDESCRIPTOR 結構傳回給專家。
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: 'EXPERTFRAMEDESCRIPTOR 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468756"
---
# <a name="expertframedescriptor-structure"></a><span data-ttu-id="ab1a5-104">EXPERTFRAMEDESCRIPTOR 結構</span><span class="sxs-lookup"><span data-stu-id="ab1a5-104">EXPERTFRAMEDESCRIPTOR structure</span></span>

<span data-ttu-id="ab1a5-105">**EXPERTFRAMEDESCRIPTOR** 結構包含框架的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-105">The **EXPERTFRAMEDESCRIPTOR** structure contains information about a frame.</span></span> <span data-ttu-id="ab1a5-106">當專家成功呼叫 [**ExpertGetFrame**](expertgetframe.md) 函式時，網路監視器會將 **EXPERTFRAMEDESCRIPTOR** 結構傳回給專家。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-106">When the expert calls the [**ExpertGetFrame**](expertgetframe.md) function successfully, Network Monitor passes the **EXPERTFRAMEDESCRIPTOR** structure back to the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1a5-107">語法</span><span class="sxs-lookup"><span data-stu-id="ab1a5-107">Syntax</span></span>


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="ab1a5-108">成員</span><span class="sxs-lookup"><span data-stu-id="ab1a5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ab1a5-109">**FrameNumber**</span><span class="sxs-lookup"><span data-stu-id="ab1a5-109">**FrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="ab1a5-110">指定框架的數目。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-110">Number of a specified frame.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a5-111">**hFrame**</span><span class="sxs-lookup"><span data-stu-id="ab1a5-111">**hFrame**</span></span>
</dt> <dd>

<span data-ttu-id="ab1a5-112">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-112">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a5-113">**pFrame**</span><span class="sxs-lookup"><span data-stu-id="ab1a5-113">**pFrame**</span></span>
</dt> <dd>

<span data-ttu-id="ab1a5-114">原始框架的指標。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-114">Pointer to a raw frame.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a5-115">**lpRecognizeDataTable**</span><span class="sxs-lookup"><span data-stu-id="ab1a5-115">**lpRecognizeDataTable**</span></span>
</dt> <dd>

<span data-ttu-id="ab1a5-116">資料表，指出每個剖析器識別資料開始的位置。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-116">Table that indicates where each parser identifies the start of the data.</span></span>

</dd> <dt>

<span data-ttu-id="ab1a5-117">**lpPropertyTable**</span><span class="sxs-lookup"><span data-stu-id="ab1a5-117">**lpPropertyTable**</span></span>
</dt> <dd>

<span data-ttu-id="ab1a5-118">剖析器所識別的框架屬性資料表。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-118">Table of frame properties that the parser identifies.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab1a5-119">備註</span><span class="sxs-lookup"><span data-stu-id="ab1a5-119">Remarks</span></span>

<span data-ttu-id="ab1a5-120">如果專家在 \_ \_ 呼叫 [**EXPERTGETFRAME**](expertgetframe.md)時指定 FLAGS 附加屬性，則每個 [**PROPERTYINST**](propertyinst.md)結構中的 **szPropertyText** 成員都是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-120">If the expert specifies FLAGS\_ATTACH\_PROPERTIES when calling [**ExpertGetFrame**](expertgetframe.md), then the **szPropertyText** member in each [**PROPERTYINST**](propertyinst.md) structure is **NULL**.</span></span>

<span data-ttu-id="ab1a5-121">如果專家在呼叫 ExpertGetFrame 函式時未指定 FLAGS \_ 附加 \_ 屬性，則在傳回時， [](expertgetframe.md) **lpPropertyTable** 成員會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-121">If the expert does not specify FLAGS\_ATTACH\_PROPERTIES when calling the [**ExpertGetFrame**](expertgetframe.md) function, then the **lpPropertyTable** member is **NULL** on return.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab1a5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab1a5-122">Requirements</span></span>



| <span data-ttu-id="ab1a5-123">需求</span><span class="sxs-lookup"><span data-stu-id="ab1a5-123">Requirement</span></span> | <span data-ttu-id="ab1a5-124">值</span><span class="sxs-lookup"><span data-stu-id="ab1a5-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1a5-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab1a5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ab1a5-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab1a5-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ab1a5-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab1a5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ab1a5-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab1a5-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ab1a5-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ab1a5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab1a5-130"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="ab1a5-130"><dt>Netmon.h</dt></span></span> </dl> |



 

 




