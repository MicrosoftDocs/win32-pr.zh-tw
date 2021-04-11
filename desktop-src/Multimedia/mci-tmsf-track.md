---
title: 'MCI_TMSF_TRACK 宏 (Mciapi) '
description: MCI \_ TMSF \_ TRACK 宏會從包含封裝曲目/分鐘/秒/畫面格的參數抓取 TRACK 元件， (TMSF) 資訊。
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8512169d0e5b3d6892dd1bf615a220143e6d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843696"
---
# <a name="mci_tmsf_track-macro"></a><span data-ttu-id="a8fc3-104">MCI \_ TMSF \_ TRACK 宏</span><span class="sxs-lookup"><span data-stu-id="a8fc3-104">MCI\_TMSF\_TRACK macro</span></span>

<span data-ttu-id="a8fc3-105">**MCI \_ TMSF \_ TRACK** 宏會從包含封裝曲目/分鐘/秒/畫面格的參數抓取 TRACK 元件， (TMSF) 資訊。</span><span class="sxs-lookup"><span data-stu-id="a8fc3-105">The **MCI\_TMSF\_TRACK** macro retrieves the tracks component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8fc3-106">語法</span><span class="sxs-lookup"><span data-stu-id="a8fc3-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_TRACK(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="a8fc3-107">參數</span><span class="sxs-lookup"><span data-stu-id="a8fc3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8fc3-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="a8fc3-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="a8fc3-109">TMSF 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="a8fc3-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8fc3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8fc3-110">Return value</span></span>

<span data-ttu-id="a8fc3-111">傳回所指定 TMSF 資訊的「追蹤」元件。</span><span class="sxs-lookup"><span data-stu-id="a8fc3-111">Returns the tracks component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8fc3-112">備註</span><span class="sxs-lookup"><span data-stu-id="a8fc3-112">Remarks</span></span>

<span data-ttu-id="a8fc3-113">TMSF 格式的時間是以 **DWORD** 值來表示，其中包含最不重要的位元組，其中包含追蹤、下一個最不重要的位元組包含分鐘、下一個最不重要的位元組（包含秒），以及最重要的位元組（包含框架）。</span><span class="sxs-lookup"><span data-stu-id="a8fc3-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="a8fc3-114">**MCI \_ TMSF \_ TRACK** 巨集定義如下：</span><span class="sxs-lookup"><span data-stu-id="a8fc3-114">The **MCI\_TMSF\_TRACK** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
```



## <a name="requirements"></a><span data-ttu-id="a8fc3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8fc3-115">Requirements</span></span>



| <span data-ttu-id="a8fc3-116">需求</span><span class="sxs-lookup"><span data-stu-id="a8fc3-116">Requirement</span></span> | <span data-ttu-id="a8fc3-117">值</span><span class="sxs-lookup"><span data-stu-id="a8fc3-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fc3-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8fc3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8fc3-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8fc3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a8fc3-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8fc3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8fc3-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8fc3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a8fc3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a8fc3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8fc3-123"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8fc3-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8fc3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8fc3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8fc3-125">Mci</span><span class="sxs-lookup"><span data-stu-id="a8fc3-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a8fc3-126">MCI 宏</span><span class="sxs-lookup"><span data-stu-id="a8fc3-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





