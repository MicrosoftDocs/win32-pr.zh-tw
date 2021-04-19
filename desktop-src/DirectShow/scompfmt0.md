---
description: 包含智慧 recompression 的格式資訊。
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: 'SCompFmt0 結構 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990628"
---
# <a name="scompfmt0-structure"></a><span data-ttu-id="83b41-103">SCompFmt0 結構</span><span class="sxs-lookup"><span data-stu-id="83b41-103">SCompFmt0 structure</span></span>

> [!Note]  
> <span data-ttu-id="83b41-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="83b41-104">\[Deprecated.</span></span> <span data-ttu-id="83b41-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="83b41-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="83b41-106">包含智慧 recompression 的格式資訊。</span><span class="sxs-lookup"><span data-stu-id="83b41-106">Contains format information for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b41-107">語法</span><span class="sxs-lookup"><span data-stu-id="83b41-107">Syntax</span></span>


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a><span data-ttu-id="83b41-108">成員</span><span class="sxs-lookup"><span data-stu-id="83b41-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="83b41-109">**nFormatId**</span><span class="sxs-lookup"><span data-stu-id="83b41-109">**nFormatId**</span></span>
</dt> <dd>

<span data-ttu-id="83b41-110">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="83b41-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="83b41-111">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="83b41-111">**MediaType**</span></span>
</dt> <dd>

<span data-ttu-id="83b41-112">[**AM \_描述 \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) 壓縮格式的媒體類型結構。</span><span class="sxs-lookup"><span data-stu-id="83b41-112">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that describes the compression format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83b41-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="83b41-113">Requirements</span></span>



| <span data-ttu-id="83b41-114">需求</span><span class="sxs-lookup"><span data-stu-id="83b41-114">Requirement</span></span> | <span data-ttu-id="83b41-115">值</span><span class="sxs-lookup"><span data-stu-id="83b41-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83b41-116">標頭</span><span class="sxs-lookup"><span data-stu-id="83b41-116">Header</span></span><br/> | <dl> <span data-ttu-id="83b41-117"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="83b41-117"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83b41-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83b41-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b41-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="83b41-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[<span data-ttu-id="83b41-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="83b41-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




