---
title: 'MCIWNDM_NOTIFYPOS 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYPOS 訊息會通知應用程式的父視窗，該視窗的位置已變更。
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934878"
---
# <a name="mciwndm_notifypos-message"></a><span data-ttu-id="62854-104">MCIWNDM \_ NOTIFYPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="62854-104">MCIWNDM\_NOTIFYPOS message</span></span>

<span data-ttu-id="62854-105">**MCIWNDM \_ NOTIFYPOS** 訊息會通知應用程式的父視窗，該視窗的位置已變更。</span><span class="sxs-lookup"><span data-stu-id="62854-105">The **MCIWNDM\_NOTIFYPOS** message notifies the parent window of an application that the window position has changed.</span></span>


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a><span data-ttu-id="62854-106">參數</span><span class="sxs-lookup"><span data-stu-id="62854-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62854-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span><span class="sxs-lookup"><span data-stu-id="62854-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="62854-108">MCIWnd 視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="62854-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="62854-109"><span id="pos"></span><span id="POS"></span>*Pos*</span><span class="sxs-lookup"><span data-stu-id="62854-109"><span id="pos"></span><span id="POS"></span>*pos*</span></span>
</dt> <dd>

<span data-ttu-id="62854-110">描述新的位置。</span><span class="sxs-lookup"><span data-stu-id="62854-110">Describes the new position.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62854-111">備註</span><span class="sxs-lookup"><span data-stu-id="62854-111">Remarks</span></span>

<span data-ttu-id="62854-112">您可以藉由指定 MCIWNDF NOTIFYPOS 視窗樣式，在 MCIWnd 視窗的位置啟用變更的通知 \_ 。</span><span class="sxs-lookup"><span data-stu-id="62854-112">You can enable notification of changes in the position of an MCIWnd window by specifying the MCIWNDF\_NOTIFYPOS window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="62854-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="62854-113">Requirements</span></span>



| <span data-ttu-id="62854-114">需求</span><span class="sxs-lookup"><span data-stu-id="62854-114">Requirement</span></span> | <span data-ttu-id="62854-115">值</span><span class="sxs-lookup"><span data-stu-id="62854-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62854-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62854-116">Minimum supported client</span></span><br/> | <span data-ttu-id="62854-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62854-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="62854-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62854-118">Minimum supported server</span></span><br/> | <span data-ttu-id="62854-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62854-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="62854-120">標頭</span><span class="sxs-lookup"><span data-stu-id="62854-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="62854-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="62854-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





