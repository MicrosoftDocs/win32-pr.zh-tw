---
title: 'MCIWNDM_NOTIFYSIZE 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYSIZE 訊息會通知應用程式的父視窗，視窗大小已變更。
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- MCIWNDM_NOTIFYSIZE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094383"
---
# <a name="mciwndm_notifysize-message"></a><span data-ttu-id="fa5fb-104">MCIWNDM \_ NOTIFYSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="fa5fb-104">MCIWNDM\_NOTIFYSIZE message</span></span>

<span data-ttu-id="fa5fb-105">**MCIWNDM \_ NOTIFYSIZE** 訊息會通知應用程式的父視窗，視窗大小已變更。</span><span class="sxs-lookup"><span data-stu-id="fa5fb-105">The **MCIWNDM\_NOTIFYSIZE** message notifies the parent window of an application that the window size has changed.</span></span>


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="fa5fb-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa5fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa5fb-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span><span class="sxs-lookup"><span data-stu-id="fa5fb-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="fa5fb-108">MCIWnd 視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fa5fb-108">Handle to the MCIWnd window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa5fb-109">備註</span><span class="sxs-lookup"><span data-stu-id="fa5fb-109">Remarks</span></span>

<span data-ttu-id="fa5fb-110">您可以藉由指定 MCIWNDF NOTIFYSIZE 視窗樣式，來啟用 MCIWnd 視窗大小變更的通知 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fa5fb-110">You can enable notification of changes in the size of an MCIWnd window by specifying the MCIWNDF\_NOTIFYSIZE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa5fb-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa5fb-111">Requirements</span></span>



| <span data-ttu-id="fa5fb-112">需求</span><span class="sxs-lookup"><span data-stu-id="fa5fb-112">Requirement</span></span> | <span data-ttu-id="fa5fb-113">值</span><span class="sxs-lookup"><span data-stu-id="fa5fb-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fa5fb-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa5fb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fa5fb-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa5fb-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fa5fb-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa5fb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fa5fb-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa5fb-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fa5fb-118">標頭</span><span class="sxs-lookup"><span data-stu-id="fa5fb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa5fb-119"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa5fb-119"><dt>Vfw.h</dt></span></span> </dl> |



 

 





