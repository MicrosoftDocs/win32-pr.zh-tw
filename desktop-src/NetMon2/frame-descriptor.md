---
description: 框架 \_ 描述元結構提供有關原始框架的描述性資訊。
ms.assetid: f2fc256e-8e64-49c1-b2ad-ef656762d5c7
title: 'FRAME_DESCRIPTOR 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c327ce1568eec07aabe3334013dae8b720ab7446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973419"
---
# <a name="frame_descriptor-structure"></a><span data-ttu-id="a72b6-103">框架 \_ 描述元結構</span><span class="sxs-lookup"><span data-stu-id="a72b6-103">FRAME\_DESCRIPTOR structure</span></span>

<span data-ttu-id="a72b6-104">**框架 \_ 描述** 元結構提供有關原始框架的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="a72b6-104">The **FRAME\_DESCRIPTOR** structure provides descriptive information about raw frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="a72b6-105">語法</span><span class="sxs-lookup"><span data-stu-id="a72b6-105">Syntax</span></span>


```C++
typedef struct _FRAME_DESCRIPTOR {
  LPBYTE       FramePointer;
  __int64      TimeStamp;
  DWORD        FrameLength;
  DWORD        nBytesAvail;
  WORD         Etype;
  BYTE         Sap;
  BYTE         LowProtocol;
  WORD         LowProtocolOffset;
  GENERIC_PORT HighPort;
  WORD         HighProtocolOffset;
} FRAME_DESCRIPTOR, *LPFRAME_DESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="a72b6-106">成員</span><span class="sxs-lookup"><span data-stu-id="a72b6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a72b6-107">**FramePointer**</span><span class="sxs-lookup"><span data-stu-id="a72b6-107">**FramePointer**</span></span>
</dt> <dd>

<span data-ttu-id="a72b6-108">框架資料的指標。</span><span class="sxs-lookup"><span data-stu-id="a72b6-108">Pointer to frame data.</span></span>

</dd> <dt>

<span data-ttu-id="a72b6-109">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="a72b6-109">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="a72b6-110">畫面格的系統時間（以微秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a72b6-110">System time, in microseconds, when the frame was captured.</span></span> <span data-ttu-id="a72b6-111">這段時間通常用來判斷兩個畫面格之間的間隔時間。</span><span class="sxs-lookup"><span data-stu-id="a72b6-111">This time is typically used to determine the interval between the times two frames were captured.</span></span>

</dd> <dt>

<span data-ttu-id="a72b6-112">**FrameLength**</span><span class="sxs-lookup"><span data-stu-id="a72b6-112">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="a72b6-113">框架的長度。</span><span class="sxs-lookup"><span data-stu-id="a72b6-113">Length of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="a72b6-114">**nBytesAvail**</span><span class="sxs-lookup"><span data-stu-id="a72b6-114">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="a72b6-115">複製實際的框架長度。</span><span class="sxs-lookup"><span data-stu-id="a72b6-115">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="a72b6-116">**Etype**</span><span class="sxs-lookup"><span data-stu-id="a72b6-116">**Etype**</span></span>
</dt> <dd>

<span data-ttu-id="a72b6-117">Etype 名稱。</span><span class="sxs-lookup"><span data-stu-id="a72b6-117">Etype name.</span></span>

</dd> <dt>

<span data-ttu-id="a72b6-118">**Sap**</span><span class="sxs-lookup"><span data-stu-id="a72b6-118">**Sap**</span></span>
</dt> <dd>

<span data-ttu-id="a72b6-119">SAP 值。</span><span class="sxs-lookup"><span data-stu-id="a72b6-119">SAP value.</span></span>

</dd> <dt>

<span data-ttu-id="a72b6-120">**LowProtocol**</span><span class="sxs-lookup"><span data-stu-id="a72b6-120">**LowProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="a72b6-121">找到的通訊協定索引。</span><span class="sxs-lookup"><span data-stu-id="a72b6-121">Index of protocol found.</span></span>

</dd> <dt>

<span data-ttu-id="a72b6-122">**LowProtocolOffset**</span><span class="sxs-lookup"><span data-stu-id="a72b6-122">**LowProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="a72b6-123">從 **LowProtocol** 取得的通訊協定資料的位移。</span><span class="sxs-lookup"><span data-stu-id="a72b6-123">Offset to protocol data obtained from **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="a72b6-124">**HighPort**</span><span class="sxs-lookup"><span data-stu-id="a72b6-124">**HighPort**</span></span>
</dt> <dd>

<span data-ttu-id="a72b6-125">在 **LowProtocol** 中識別的高通訊協定埠。</span><span class="sxs-lookup"><span data-stu-id="a72b6-125">Port of high protocol identified in **LowProtocol**.</span></span>

</dd> <dt>

<span data-ttu-id="a72b6-126">**HighProtocolOffset**</span><span class="sxs-lookup"><span data-stu-id="a72b6-126">**HighProtocolOffset**</span></span>
</dt> <dd>

<span data-ttu-id="a72b6-127">從 **HighPort** 取得的通訊協定資料的位移。</span><span class="sxs-lookup"><span data-stu-id="a72b6-127">Offset to protocol data obtained from **HighPort**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a72b6-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a72b6-128">Requirements</span></span>



| <span data-ttu-id="a72b6-129">需求</span><span class="sxs-lookup"><span data-stu-id="a72b6-129">Requirement</span></span> | <span data-ttu-id="a72b6-130">值</span><span class="sxs-lookup"><span data-stu-id="a72b6-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a72b6-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a72b6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a72b6-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a72b6-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a72b6-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a72b6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a72b6-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a72b6-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a72b6-135">標頭</span><span class="sxs-lookup"><span data-stu-id="a72b6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a72b6-136"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="a72b6-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




