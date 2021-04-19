---
description: 驅動程式實際的畫面格。
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: '畫面格結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b4ff8d66f88b18988cbb33bbcd8196cc01177b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970574"
---
# <a name="frame-structure"></a><span data-ttu-id="215b3-103">框架結構</span><span class="sxs-lookup"><span data-stu-id="215b3-103">FRAME structure</span></span>

<span data-ttu-id="215b3-104">**框架** 結構是驅動程式的實際畫面。</span><span class="sxs-lookup"><span data-stu-id="215b3-104">The **FRAME** structure is an actual frame from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="215b3-105">語法</span><span class="sxs-lookup"><span data-stu-id="215b3-105">Syntax</span></span>


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a><span data-ttu-id="215b3-106">成員</span><span class="sxs-lookup"><span data-stu-id="215b3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="215b3-107">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="215b3-107">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="215b3-108">捕捉開始與捕獲框架時間之間的經過時間（以微秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="215b3-108">Elapsed time, in microseconds, between the start of the capture and the time when the frame was captured.</span></span>

</dd> <dt>

<span data-ttu-id="215b3-109">**FrameLength**</span><span class="sxs-lookup"><span data-stu-id="215b3-109">**FrameLength**</span></span>
</dt> <dd>

<span data-ttu-id="215b3-110">MAC 框架長度。</span><span class="sxs-lookup"><span data-stu-id="215b3-110">MAC frame length.</span></span>

</dd> <dt>

<span data-ttu-id="215b3-111">**nBytesAvail**</span><span class="sxs-lookup"><span data-stu-id="215b3-111">**nBytesAvail**</span></span>
</dt> <dd>

<span data-ttu-id="215b3-112">複製實際的框架長度。</span><span class="sxs-lookup"><span data-stu-id="215b3-112">Actual frame length copied.</span></span>

</dd> <dt>

<span data-ttu-id="215b3-113">**MacFrame**</span><span class="sxs-lookup"><span data-stu-id="215b3-113">**MacFrame**</span></span>
</dt> <dd>

<span data-ttu-id="215b3-114">框架資料。</span><span class="sxs-lookup"><span data-stu-id="215b3-114">Frame data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="215b3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="215b3-115">Requirements</span></span>



| <span data-ttu-id="215b3-116">需求</span><span class="sxs-lookup"><span data-stu-id="215b3-116">Requirement</span></span> | <span data-ttu-id="215b3-117">值</span><span class="sxs-lookup"><span data-stu-id="215b3-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="215b3-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="215b3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="215b3-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="215b3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="215b3-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="215b3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="215b3-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="215b3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="215b3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="215b3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="215b3-123"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="215b3-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




