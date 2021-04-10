---
title: 'MCIWNDM_GETPOSITION 訊息 (Vfw .h) '
description: MCIWNDM \_ GETPOSITION 訊息會抓取 MCI 裝置內容中目前位置的數值。
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843192"
---
# <a name="mciwndm_getposition-message"></a><span data-ttu-id="2eb20-104">MCIWNDM \_ GETPOSITION 訊息</span><span class="sxs-lookup"><span data-stu-id="2eb20-104">MCIWNDM\_GETPOSITION message</span></span>

<span data-ttu-id="2eb20-105">**MCIWNDM \_ GETPOSITION** 訊息會抓取 MCI 裝置內容中目前位置的數值。</span><span class="sxs-lookup"><span data-stu-id="2eb20-105">The **MCIWNDM\_GETPOSITION** message retrieves the numerical value of the current position within the content of the MCI device.</span></span> <span data-ttu-id="2eb20-106">這個宏也會在應用程式定義的緩衝區中，以字串形式提供目前的位置。</span><span class="sxs-lookup"><span data-stu-id="2eb20-106">This macro also provides the current position in string form in an application-defined buffer.</span></span> <span data-ttu-id="2eb20-107">您可以明確地傳送此訊息，或使用 [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) 或 [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="2eb20-107">You can send this message explicitly or by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) or [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="2eb20-108">參數</span><span class="sxs-lookup"><span data-stu-id="2eb20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb20-109"><span id="len"></span><span id="LEN"></span>*萊恩*</span><span class="sxs-lookup"><span data-stu-id="2eb20-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-110">緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2eb20-110">Size, in bytes, of the buffer.</span></span> <span data-ttu-id="2eb20-111">如果以 null 結尾的字串長度超過緩衝區，它就會被截斷。</span><span class="sxs-lookup"><span data-stu-id="2eb20-111">If the null-terminated string is longer than the buffer, it is truncated.</span></span> <span data-ttu-id="2eb20-112">使用零可禁止將位置抓取為字串。</span><span class="sxs-lookup"><span data-stu-id="2eb20-112">Use zero to inhibit retrieval of the position as a string.</span></span>

</dd> <dt>

<span data-ttu-id="2eb20-113"><span id="lp"></span><span id="LP"></span>*Lp*</span><span class="sxs-lookup"><span data-stu-id="2eb20-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="2eb20-114">用來傳回位置的應用程式定義緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="2eb20-114">Pointer to an application-defined buffer used to return the position.</span></span> <span data-ttu-id="2eb20-115">使用零可禁止將位置抓取為字串。</span><span class="sxs-lookup"><span data-stu-id="2eb20-115">Use zero to inhibit retrieval of the position as a string.</span></span> <span data-ttu-id="2eb20-116">如果裝置支援追蹤，則會以 TT： MM： SS： FF 格式傳回字串位置資訊，其中 TT 對應至曲目，MM 和 SS 對應到分鐘和秒，而 FF 對應至框架。</span><span class="sxs-lookup"><span data-stu-id="2eb20-116">If the device supports tracks, the string position information is returned in the form TT:MM:SS:FF where TT corresponds to tracks, MM and SS correspond to minutes and seconds, and FF corresponds to frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb20-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2eb20-117">Return Value</span></span>

<span data-ttu-id="2eb20-118">傳回對應至目前位置的整數。</span><span class="sxs-lookup"><span data-stu-id="2eb20-118">Returns an integer corresponding to the current position.</span></span> <span data-ttu-id="2eb20-119">Position 值的單位取決於目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="2eb20-119">The units for the position value depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb20-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2eb20-120">Requirements</span></span>



| <span data-ttu-id="2eb20-121">需求</span><span class="sxs-lookup"><span data-stu-id="2eb20-121">Requirement</span></span> | <span data-ttu-id="2eb20-122">值</span><span class="sxs-lookup"><span data-stu-id="2eb20-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2eb20-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2eb20-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb20-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eb20-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2eb20-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2eb20-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb20-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eb20-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2eb20-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2eb20-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eb20-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="2eb20-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb20-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2eb20-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb20-130">**MCIWndGetPosition**</span><span class="sxs-lookup"><span data-stu-id="2eb20-130">**MCIWndGetPosition**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[<span data-ttu-id="2eb20-131">**MCIWndGetPositionString**</span><span class="sxs-lookup"><span data-stu-id="2eb20-131">**MCIWndGetPositionString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





