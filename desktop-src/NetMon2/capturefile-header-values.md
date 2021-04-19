---
description: 定義網路監視器標頭檔結構。
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: 'CAPTUREFILE_HEADER_VALUES 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974664"
---
# <a name="capturefile_header_values-structure"></a><span data-ttu-id="8ccc5-103">CAPTUREFILE \_ 標頭 \_ 值結構</span><span class="sxs-lookup"><span data-stu-id="8ccc5-103">CAPTUREFILE\_HEADER\_VALUES structure</span></span>

<span data-ttu-id="8ccc5-104">**CAPTUREFILE \_ 標頭 \_ 值** 結構會定義網路監視器標頭檔結構。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-104">The **CAPTUREFILE\_HEADER\_VALUES** structure defines the Network Monitor header file structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ccc5-105">語法</span><span class="sxs-lookup"><span data-stu-id="8ccc5-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a><span data-ttu-id="8ccc5-106">成員</span><span class="sxs-lookup"><span data-stu-id="8ccc5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ccc5-107">**簽名**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-107">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-108">唯一識別碼： ' GMBU。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-108">Unique identifier: 'GMBU.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-109">**BCDVerMinor**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-109">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-110">二進位、編碼的十進位 (次要) 。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-110">Binary, coded decimal (minor).</span></span> <span data-ttu-id="8ccc5-111">此成員的值應該是零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-111">The value of this member should be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-112">**BCDVerMajor**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-112">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-113">二進位編碼的 decimal (主要) 。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-113">Binary coded decimal (major).</span></span> <span data-ttu-id="8ccc5-114">此值應該是2。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-114">This value should be 2.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-116">拓撲類型。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-116">Topology type.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-117">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-118">拍攝時間。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-118">Time of capture.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-119">**FrameTableOffset**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-119">**FrameTableOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-120">框架索引表。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-120">Frame index table.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-121">**FrameTableLength**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-121">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-122">框架索引資料表大小。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-122">Frame index table size.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-123">**UserDataOffset**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-123">**UserDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-124">使用者資料位移。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-124">User data offset.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-125">**UserDataLength**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-125">**UserDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-126">使用者資料長度。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-126">User data length.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-127">**CommentDataOffset**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-127">**CommentDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-128">批註資料位移。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-128">Comment data offset.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-129">**CommentDataLength**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-129">**CommentDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-130">批註資料的長度。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-130">Length of comment data.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-131">**StatisticsOffset**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-131">**StatisticsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-132">**統計資料** 結構的位移。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-132">Offset to the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-133">**StatisticsLength**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-133">**StatisticsLength**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-134">**統計資料** 結構的長度。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-134">Length of the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-135">**NetworkInfoOffset**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-135">**NetworkInfoOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-136">**NETWORKINFO** 結構的位移。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-136">Offset to the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-137">**NetworkInfoLength**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-137">**NetworkInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-138">**NETWORKINFO** 結構的長度。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-138">Length of the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-139">**ConversationStatsOffset**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-139">**ConversationStatsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-140">未使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-140">This member is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ccc5-141">**ConversationStatsLength**</span><span class="sxs-lookup"><span data-stu-id="8ccc5-141">**ConversationStatsLength**</span></span>
</dt> <dd>

<span data-ttu-id="8ccc5-142">未使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="8ccc5-142">This member is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ccc5-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ccc5-143">Requirements</span></span>



| <span data-ttu-id="8ccc5-144">需求</span><span class="sxs-lookup"><span data-stu-id="8ccc5-144">Requirement</span></span> | <span data-ttu-id="8ccc5-145">值</span><span class="sxs-lookup"><span data-stu-id="8ccc5-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8ccc5-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ccc5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8ccc5-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ccc5-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8ccc5-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ccc5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8ccc5-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ccc5-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8ccc5-150">標頭</span><span class="sxs-lookup"><span data-stu-id="8ccc5-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ccc5-151"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="8ccc5-151"><dt>Netmon.h</dt></span></span> </dl> |



 

 




