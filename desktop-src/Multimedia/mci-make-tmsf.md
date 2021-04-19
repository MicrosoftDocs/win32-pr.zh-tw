---
title: 'MCI_MAKE_TMSF 宏 (Mciapi) '
description: MCI \_ MAKE \_ TMSF 宏會從指定的曲目、分、秒和框架值，以封裝的曲目/分鐘/秒/框架 (TMSF) 格式來建立時間值。
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968799"
---
# <a name="mci_make_tmsf-macro"></a><span data-ttu-id="f871e-104">MCI \_ MAKE \_ TMSF 宏</span><span class="sxs-lookup"><span data-stu-id="f871e-104">MCI\_MAKE\_TMSF macro</span></span>

<span data-ttu-id="f871e-105">**MCI \_ MAKE \_ TMSF** 宏會從指定的曲目、分、秒和框架值，以封裝的曲目/分鐘/秒/框架 (TMSF) 格式來建立時間值。</span><span class="sxs-lookup"><span data-stu-id="f871e-105">The **MCI\_MAKE\_TMSF** macro creates a time value in packed tracks/minutes/seconds/frames (TMSF) format from the given tracks, minutes, seconds, and frames values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f871e-106">語法</span><span class="sxs-lookup"><span data-stu-id="f871e-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="f871e-107">參數</span><span class="sxs-lookup"><span data-stu-id="f871e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f871e-108">*tracks*</span><span class="sxs-lookup"><span data-stu-id="f871e-108">*tracks*</span></span> 
</dt> <dd>

<span data-ttu-id="f871e-109">曲目數目。</span><span class="sxs-lookup"><span data-stu-id="f871e-109">Number of tracks.</span></span>

</dd> <dt>

<span data-ttu-id="f871e-110">*分鐘*</span><span class="sxs-lookup"><span data-stu-id="f871e-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="f871e-111">分鐘數。</span><span class="sxs-lookup"><span data-stu-id="f871e-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="f871e-112">*seconds*</span><span class="sxs-lookup"><span data-stu-id="f871e-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="f871e-113">秒數。</span><span class="sxs-lookup"><span data-stu-id="f871e-113">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="f871e-114">*框架*</span><span class="sxs-lookup"><span data-stu-id="f871e-114">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="f871e-115">畫面格數目。</span><span class="sxs-lookup"><span data-stu-id="f871e-115">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f871e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f871e-116">Return value</span></span>

<span data-ttu-id="f871e-117">以壓縮的 TMSF 格式傳回時間。</span><span class="sxs-lookup"><span data-stu-id="f871e-117">Returns the time in packed TMSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="f871e-118">備註</span><span class="sxs-lookup"><span data-stu-id="f871e-118">Remarks</span></span>

<span data-ttu-id="f871e-119">TMSF 格式的時間是以 **DWORD** 值來表示，其中包含最不重要的位元組，其中包含追蹤、下一個最不重要的位元組包含分鐘、下一個最不重要的位元組（包含秒），以及最重要的位元組（包含框架）。</span><span class="sxs-lookup"><span data-stu-id="f871e-119">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="f871e-120">**MCI \_ MAKE \_ TMSF** 宏的定義如下：</span><span class="sxs-lookup"><span data-stu-id="f871e-120">The **MCI\_MAKE\_TMSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="f871e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f871e-121">Requirements</span></span>



| <span data-ttu-id="f871e-122">需求</span><span class="sxs-lookup"><span data-stu-id="f871e-122">Requirement</span></span> | <span data-ttu-id="f871e-123">值</span><span class="sxs-lookup"><span data-stu-id="f871e-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f871e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f871e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f871e-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f871e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f871e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f871e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f871e-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f871e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f871e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f871e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f871e-129"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f871e-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f871e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f871e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f871e-131">Mci</span><span class="sxs-lookup"><span data-stu-id="f871e-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f871e-132">MCI 宏</span><span class="sxs-lookup"><span data-stu-id="f871e-132">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





