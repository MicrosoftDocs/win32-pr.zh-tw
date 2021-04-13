---
title: 'MCIWNDM_GETDEVICE 訊息 (Vfw .h) '
description: MCIWNDM \_ GETDEVICE 訊息會抓取目前開啟之 MCI 裝置的名稱。 您可以使用 MCIWndGetDevice 宏明確地傳送此訊息。
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- MCIWNDM_GETDEVICE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464520"
---
# <a name="mciwndm_getdevice-message"></a><span data-ttu-id="5835d-105">MCIWNDM \_ GETDEVICE 訊息</span><span class="sxs-lookup"><span data-stu-id="5835d-105">MCIWNDM\_GETDEVICE message</span></span>

<span data-ttu-id="5835d-106">**MCIWNDM \_ GETDEVICE** 訊息會抓取目前開啟之 MCI 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5835d-106">The **MCIWNDM\_GETDEVICE** message retrieves the name of the currently open MCI device.</span></span> <span data-ttu-id="5835d-107">您可以使用 [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="5835d-107">You can send this message explicitly or by using the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span>


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="5835d-108">參數</span><span class="sxs-lookup"><span data-stu-id="5835d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5835d-109"><span id="len"></span><span id="LEN"></span>*萊恩*</span><span class="sxs-lookup"><span data-stu-id="5835d-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="5835d-110">緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5835d-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5835d-111"><span id="lp"></span><span id="LP"></span>*Lp*</span><span class="sxs-lookup"><span data-stu-id="5835d-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="5835d-112">應用程式定義之緩衝區的指標，以傳回裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="5835d-112">Pointer to an application-defined buffer to return the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5835d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5835d-113">Return Value</span></span>

<span data-ttu-id="5835d-114">如果成功則傳回零，否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="5835d-114">Returns zero if successful or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5835d-115">備註</span><span class="sxs-lookup"><span data-stu-id="5835d-115">Remarks</span></span>

<span data-ttu-id="5835d-116">如果包含裝置名稱的以 null 終止的字串長度超過緩衝區，MCIWnd 會將它截斷。</span><span class="sxs-lookup"><span data-stu-id="5835d-116">If the null-terminated string containing the device name is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5835d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5835d-117">Requirements</span></span>



| <span data-ttu-id="5835d-118">需求</span><span class="sxs-lookup"><span data-stu-id="5835d-118">Requirement</span></span> | <span data-ttu-id="5835d-119">值</span><span class="sxs-lookup"><span data-stu-id="5835d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5835d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5835d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5835d-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5835d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5835d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5835d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5835d-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5835d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5835d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5835d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5835d-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="5835d-125"><dt>Vfw.h</dt></span></span> </dl> |



 

 





