---
title: 'MCI_HMS_SECOND 宏 (Mciapi) '
description: MCI \_ HMS \_ SECOND 宏會從包含「壓縮時數/分鐘/秒」參數的參數抓取秒鐘元件 (HMS) 資訊。
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844331"
---
# <a name="mci_hms_second-macro"></a><span data-ttu-id="e8133-104">MCI \_ HMS \_ 第二個宏</span><span class="sxs-lookup"><span data-stu-id="e8133-104">MCI\_HMS\_SECOND macro</span></span>

<span data-ttu-id="e8133-105">**MCI \_ HMS \_ SECOND** 宏會從包含「壓縮時數/分鐘/秒」參數的參數抓取秒鐘元件 (HMS) 資訊。</span><span class="sxs-lookup"><span data-stu-id="e8133-105">The **MCI\_HMS\_SECOND** macro retrieves the seconds component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8133-106">語法</span><span class="sxs-lookup"><span data-stu-id="e8133-106">Syntax</span></span>


```C++
BYTE MCI_HMS_SECOND(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="e8133-107">參數</span><span class="sxs-lookup"><span data-stu-id="e8133-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8133-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="e8133-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="e8133-109">HMS 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="e8133-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8133-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8133-110">Return value</span></span>

<span data-ttu-id="e8133-111">傳回所指定 HMS 資訊的秒陣列件。</span><span class="sxs-lookup"><span data-stu-id="e8133-111">Returns the seconds component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8133-112">備註</span><span class="sxs-lookup"><span data-stu-id="e8133-112">Remarks</span></span>

<span data-ttu-id="e8133-113">HMS 格式的時間以 **DWORD** 值表示，其中最小的位元組包含小時、下一個最不重要的位元組（包含分鐘），以及下一個最不重要的位元組（包含秒）。</span><span class="sxs-lookup"><span data-stu-id="e8133-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="e8133-114">最重要的位元組未使用。</span><span class="sxs-lookup"><span data-stu-id="e8133-114">The most significant byte is unused.</span></span>

<span data-ttu-id="e8133-115">**MCI \_ HMS \_ SECOND** 宏的定義如下：</span><span class="sxs-lookup"><span data-stu-id="e8133-115">The **MCI\_HMS\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
```



## <a name="requirements"></a><span data-ttu-id="e8133-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8133-116">Requirements</span></span>



| <span data-ttu-id="e8133-117">需求</span><span class="sxs-lookup"><span data-stu-id="e8133-117">Requirement</span></span> | <span data-ttu-id="e8133-118">值</span><span class="sxs-lookup"><span data-stu-id="e8133-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e8133-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8133-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8133-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8133-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e8133-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8133-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8133-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8133-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e8133-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e8133-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8133-124"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8133-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8133-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8133-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8133-126">Mci</span><span class="sxs-lookup"><span data-stu-id="e8133-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e8133-127">MCI 宏</span><span class="sxs-lookup"><span data-stu-id="e8133-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





