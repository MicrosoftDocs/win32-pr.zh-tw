---
title: 'MCI_TMSF_FRAME 宏 (Mciapi) '
description: MCI \_ TMSF \_ FRAME 宏會從包含封裝曲目/分鐘/秒/畫面格的參數抓取畫面元件， (TMSF) 資訊。
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- MCI_TMSF_FRAME 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685596"
---
# <a name="mci_tmsf_frame-macro"></a><span data-ttu-id="8fc06-104">MCI \_ TMSF \_ FRAME 宏</span><span class="sxs-lookup"><span data-stu-id="8fc06-104">MCI\_TMSF\_FRAME macro</span></span>

<span data-ttu-id="8fc06-105">**MCI \_ TMSF \_ FRAME** 宏會從包含封裝曲目/分鐘/秒/畫面格的參數抓取畫面元件， (TMSF) 資訊。</span><span class="sxs-lookup"><span data-stu-id="8fc06-105">The **MCI\_TMSF\_FRAME** macro retrieves the frames component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc06-106">語法</span><span class="sxs-lookup"><span data-stu-id="8fc06-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_FRAME(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="8fc06-107">參數</span><span class="sxs-lookup"><span data-stu-id="8fc06-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc06-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="8fc06-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc06-109">TMSF 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="8fc06-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc06-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fc06-110">Return value</span></span>

<span data-ttu-id="8fc06-111">傳回所指定 TMSF 資訊的框架元件。</span><span class="sxs-lookup"><span data-stu-id="8fc06-111">Returns the frames component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fc06-112">備註</span><span class="sxs-lookup"><span data-stu-id="8fc06-112">Remarks</span></span>

<span data-ttu-id="8fc06-113">TMSF 格式的時間是以 **DWORD** 值來表示，其中包含最不重要的位元組，其中包含追蹤、下一個最不重要的位元組包含分鐘、下一個最不重要的位元組（包含秒），以及最重要的位元組（包含框架）。</span><span class="sxs-lookup"><span data-stu-id="8fc06-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="8fc06-114">**MCI \_ TMSF \_ FRAME** 宏的定義如下：</span><span class="sxs-lookup"><span data-stu-id="8fc06-114">The **MCI\_TMSF\_FRAME** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
```



## <a name="requirements"></a><span data-ttu-id="8fc06-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fc06-115">Requirements</span></span>



| <span data-ttu-id="8fc06-116">需求</span><span class="sxs-lookup"><span data-stu-id="8fc06-116">Requirement</span></span> | <span data-ttu-id="8fc06-117">值</span><span class="sxs-lookup"><span data-stu-id="8fc06-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc06-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fc06-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc06-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fc06-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8fc06-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fc06-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc06-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fc06-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8fc06-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8fc06-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fc06-123"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc06-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc06-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fc06-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc06-125">Mci</span><span class="sxs-lookup"><span data-stu-id="8fc06-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8fc06-126">MCI 宏</span><span class="sxs-lookup"><span data-stu-id="8fc06-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





