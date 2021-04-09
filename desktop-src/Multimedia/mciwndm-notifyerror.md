---
title: 'MCIWNDM_NOTIFYERROR 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYERROR 訊息會通知應用程式的父視窗發生 MCI 錯誤。
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024967"
---
# <a name="mciwndm_notifyerror-message"></a><span data-ttu-id="f3bd1-104">MCIWNDM \_ NOTIFYERROR 訊息</span><span class="sxs-lookup"><span data-stu-id="f3bd1-104">MCIWNDM\_NOTIFYERROR message</span></span>

<span data-ttu-id="f3bd1-105">**MCIWNDM \_ NOTIFYERROR** 訊息會通知應用程式的父視窗發生 MCI 錯誤。</span><span class="sxs-lookup"><span data-stu-id="f3bd1-105">The **MCIWNDM\_NOTIFYERROR** message notifies the parent window of an application that an MCI error occurred.</span></span>


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a><span data-ttu-id="f3bd1-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3bd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3bd1-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span><span class="sxs-lookup"><span data-stu-id="f3bd1-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="f3bd1-108">MCIWnd 視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f3bd1-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="f3bd1-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*錯誤碼*</span><span class="sxs-lookup"><span data-stu-id="f3bd1-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span></span>
</dt> <dd>

<span data-ttu-id="f3bd1-110">MCI 錯誤的數值代碼。</span><span class="sxs-lookup"><span data-stu-id="f3bd1-110">Numerical code for the MCI error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3bd1-111">備註</span><span class="sxs-lookup"><span data-stu-id="f3bd1-111">Remarks</span></span>

<span data-ttu-id="f3bd1-112">您可以藉由指定 [MCIWNDF \_ NOTIFYERROR] 視窗樣式來啟用 MCI 錯誤通知。</span><span class="sxs-lookup"><span data-stu-id="f3bd1-112">You can enable MCI error notification by specifying the MCIWNDF\_NOTIFYERROR window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3bd1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3bd1-113">Requirements</span></span>



| <span data-ttu-id="f3bd1-114">需求</span><span class="sxs-lookup"><span data-stu-id="f3bd1-114">Requirement</span></span> | <span data-ttu-id="f3bd1-115">值</span><span class="sxs-lookup"><span data-stu-id="f3bd1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3bd1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3bd1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f3bd1-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3bd1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f3bd1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3bd1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f3bd1-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3bd1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f3bd1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f3bd1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3bd1-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3bd1-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





