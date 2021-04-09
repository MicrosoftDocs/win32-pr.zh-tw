---
title: 'MCI_MAKE_HMS 宏 (Mciapi) '
description: MCI \_ MAKE \_ HMS 宏會將時間值從指定的時數、分鐘數和秒數值以 [壓縮時數/分鐘/秒] (HMS) 格式建立。
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686318"
---
# <a name="mci_make_hms-macro"></a><span data-ttu-id="572dd-104">MCI \_ MAKE \_ HMS 宏</span><span class="sxs-lookup"><span data-stu-id="572dd-104">MCI\_MAKE\_HMS macro</span></span>

<span data-ttu-id="572dd-105">**MCI \_ MAKE \_ HMS** 宏會將時間值從指定的時數、分鐘數和秒數值以 [壓縮時數/分鐘/秒] (HMS) 格式建立。</span><span class="sxs-lookup"><span data-stu-id="572dd-105">The **MCI\_MAKE\_HMS** macro creates a time value in packed hours/minutes/seconds (HMS) format from the given hours, minutes, and seconds values.</span></span>

## <a name="syntax"></a><span data-ttu-id="572dd-106">語法</span><span class="sxs-lookup"><span data-stu-id="572dd-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a><span data-ttu-id="572dd-107">參數</span><span class="sxs-lookup"><span data-stu-id="572dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="572dd-108">*小時*</span><span class="sxs-lookup"><span data-stu-id="572dd-108">*hours*</span></span> 
</dt> <dd>

<span data-ttu-id="572dd-109">時數。</span><span class="sxs-lookup"><span data-stu-id="572dd-109">Number of hours.</span></span>

</dd> <dt>

<span data-ttu-id="572dd-110">*分鐘*</span><span class="sxs-lookup"><span data-stu-id="572dd-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="572dd-111">分鐘數。</span><span class="sxs-lookup"><span data-stu-id="572dd-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="572dd-112">*seconds*</span><span class="sxs-lookup"><span data-stu-id="572dd-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="572dd-113">秒數。</span><span class="sxs-lookup"><span data-stu-id="572dd-113">Number of seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="572dd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="572dd-114">Return value</span></span>

<span data-ttu-id="572dd-115">以壓縮的 HMS 格式傳回時間。</span><span class="sxs-lookup"><span data-stu-id="572dd-115">Returns the time in packed HMS format.</span></span>

## <a name="remarks"></a><span data-ttu-id="572dd-116">備註</span><span class="sxs-lookup"><span data-stu-id="572dd-116">Remarks</span></span>

<span data-ttu-id="572dd-117">HMS 格式的時間以 **DWORD** 值表示，其中最小的位元組包含小時、下一個最不重要的位元組（包含分鐘），以及下一個最不重要的位元組（包含秒）。</span><span class="sxs-lookup"><span data-stu-id="572dd-117">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="572dd-118">最重要的位元組未使用。</span><span class="sxs-lookup"><span data-stu-id="572dd-118">The most significant byte is unused.</span></span>

<span data-ttu-id="572dd-119">**MCI \_ MAKE \_ HMS** 宏的定義如下：</span><span class="sxs-lookup"><span data-stu-id="572dd-119">The **MCI\_MAKE\_HMS** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="572dd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="572dd-120">Requirements</span></span>



| <span data-ttu-id="572dd-121">需求</span><span class="sxs-lookup"><span data-stu-id="572dd-121">Requirement</span></span> | <span data-ttu-id="572dd-122">值</span><span class="sxs-lookup"><span data-stu-id="572dd-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="572dd-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="572dd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="572dd-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="572dd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="572dd-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="572dd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="572dd-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="572dd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="572dd-127">標頭</span><span class="sxs-lookup"><span data-stu-id="572dd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="572dd-128"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="572dd-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="572dd-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="572dd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="572dd-130">Mci</span><span class="sxs-lookup"><span data-stu-id="572dd-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="572dd-131">MCI 宏</span><span class="sxs-lookup"><span data-stu-id="572dd-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





