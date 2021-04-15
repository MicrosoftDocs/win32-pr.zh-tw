---
title: 'MCIWNDM_GETFILENAME 訊息 (Vfw .h) '
description: MCIWNDM \_ GETFILENAME 訊息會抓取 MCI 裝置目前所使用的檔案名。 您可以使用 MCIWndGetFileName 宏明確地傳送此訊息。
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- MCIWNDM_GETFILENAME message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508340"
---
# <a name="mciwndm_getfilename-message"></a><span data-ttu-id="a5002-105">MCIWNDM \_ GETFILENAME 訊息</span><span class="sxs-lookup"><span data-stu-id="a5002-105">MCIWNDM\_GETFILENAME message</span></span>

<span data-ttu-id="a5002-106">**MCIWNDM \_ GETFILENAME** 訊息會抓取 MCI 裝置目前所使用的檔案名。</span><span class="sxs-lookup"><span data-stu-id="a5002-106">The **MCIWNDM\_GETFILENAME** message retrieves the filename currently used by an MCI device.</span></span> <span data-ttu-id="a5002-107">您可以使用 [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a5002-107">You can send this message explicitly or by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span>


```C++
MCIWNDM_GETFILENAME 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="a5002-108">參數</span><span class="sxs-lookup"><span data-stu-id="a5002-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5002-109"><span id="len"></span><span id="LEN"></span>*萊恩*</span><span class="sxs-lookup"><span data-stu-id="a5002-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="a5002-110">緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a5002-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a5002-111"><span id="lp"></span><span id="LP"></span>*Lp*</span><span class="sxs-lookup"><span data-stu-id="a5002-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="a5002-112">應用程式定義之緩衝區的指標，以傳回檔案名。</span><span class="sxs-lookup"><span data-stu-id="a5002-112">Pointer to an application-defined buffer to return the filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5002-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5002-113">Return Value</span></span>

<span data-ttu-id="a5002-114">如果成功則傳回零; 否則傳回1。</span><span class="sxs-lookup"><span data-stu-id="a5002-114">Returns zero if successful or 1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5002-115">備註</span><span class="sxs-lookup"><span data-stu-id="a5002-115">Remarks</span></span>

<span data-ttu-id="a5002-116">如果包含檔案名的以 null 終止的字串長度超過緩衝區，MCIWnd 會截斷檔案名。</span><span class="sxs-lookup"><span data-stu-id="a5002-116">If the null-terminated string containing the filename is longer than the buffer, MCIWnd truncates the filename.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5002-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5002-117">Requirements</span></span>



| <span data-ttu-id="a5002-118">需求</span><span class="sxs-lookup"><span data-stu-id="a5002-118">Requirement</span></span> | <span data-ttu-id="a5002-119">值</span><span class="sxs-lookup"><span data-stu-id="a5002-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a5002-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5002-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a5002-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5002-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a5002-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5002-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a5002-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5002-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a5002-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a5002-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5002-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="a5002-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5002-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5002-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5002-127">**MCIWndGetFileName**</span><span class="sxs-lookup"><span data-stu-id="a5002-127">**MCIWndGetFileName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 





