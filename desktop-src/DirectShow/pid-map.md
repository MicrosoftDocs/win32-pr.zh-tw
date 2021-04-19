---
description: PID \_ 對應結構包含可識別 mpeg-2 傳輸資料流程封包識別碼的內容。
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: 'PID_MAP 結構 (Bdatypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983189"
---
# <a name="pid_map-structure"></a><span data-ttu-id="dd241-103">PID \_ 對應結構</span><span class="sxs-lookup"><span data-stu-id="dd241-103">PID\_MAP structure</span></span>

<span data-ttu-id="dd241-104">`PID_MAP`結構包含可識別 mpeg-2 傳輸資料流程封包識別碼的內容。</span><span class="sxs-lookup"><span data-stu-id="dd241-104">The `PID_MAP` structure contains identifies the contents of an MPEG-2 transport stream packet ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd241-105">語法</span><span class="sxs-lookup"><span data-stu-id="dd241-105">Syntax</span></span>


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a><span data-ttu-id="dd241-106">成員</span><span class="sxs-lookup"><span data-stu-id="dd241-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd241-107">**ulPID**</span><span class="sxs-lookup"><span data-stu-id="dd241-107">**ulPID**</span></span>
</dt> <dd>

<span data-ttu-id="dd241-108">指定 (PID 的封包識別碼) </span><span class="sxs-lookup"><span data-stu-id="dd241-108">Specifies the packet ID (PID)</span></span>

</dd> <dt>

<span data-ttu-id="dd241-109">**MediaSampleContent**</span><span class="sxs-lookup"><span data-stu-id="dd241-109">**MediaSampleContent**</span></span>
</dt> <dd>

<span data-ttu-id="dd241-110">以 [**媒體 \_ 範例 \_ 內容**](media-sample-content.md) 列舉型別指定封包內容的內容。</span><span class="sxs-lookup"><span data-stu-id="dd241-110">Specifies the contents of the packet payload, as a [**MEDIA\_SAMPLE\_CONTENT**](media-sample-content.md) enumeration type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd241-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd241-111">Requirements</span></span>



| <span data-ttu-id="dd241-112">需求</span><span class="sxs-lookup"><span data-stu-id="dd241-112">Requirement</span></span> | <span data-ttu-id="dd241-113">值</span><span class="sxs-lookup"><span data-stu-id="dd241-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd241-114">標頭</span><span class="sxs-lookup"><span data-stu-id="dd241-114">Header</span></span><br/> | <dl> <span data-ttu-id="dd241-115"><dt>Bdatypes (包含 Bdaiface) </dt></span><span class="sxs-lookup"><span data-stu-id="dd241-115"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd241-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd241-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd241-117">DirectShow 結構</span><span class="sxs-lookup"><span data-stu-id="dd241-117">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="dd241-118">**IEnumPIDMap 介面**</span><span class="sxs-lookup"><span data-stu-id="dd241-118">**IEnumPIDMap Interface**</span></span>](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 




