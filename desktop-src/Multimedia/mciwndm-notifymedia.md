---
title: 'MCIWNDM_NOTIFYMEDIA 訊息 (Vfw .h) '
description: MCIWNDM \_ NOTIFYMEDIA 訊息會通知應用程式的父視窗已變更。
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685820"
---
# <a name="mciwndm_notifymedia-message"></a><span data-ttu-id="91392-104">MCIWNDM \_ NOTIFYMEDIA 訊息</span><span class="sxs-lookup"><span data-stu-id="91392-104">MCIWNDM\_NOTIFYMEDIA message</span></span>

<span data-ttu-id="91392-105">**MCIWNDM \_ NOTIFYMEDIA** 訊息會通知應用程式的父視窗已變更。</span><span class="sxs-lookup"><span data-stu-id="91392-105">The **MCIWNDM\_NOTIFYMEDIA** message notifies the parent window of an application that the media has changed.</span></span>


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="91392-106">參數</span><span class="sxs-lookup"><span data-stu-id="91392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91392-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span><span class="sxs-lookup"><span data-stu-id="91392-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="91392-108">MCIWnd 視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="91392-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="91392-109"><span id="lp"></span><span id="LP"></span>*Lp*</span><span class="sxs-lookup"><span data-stu-id="91392-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="91392-110">以 null 結束的字串指標，其中包含新的檔案名。</span><span class="sxs-lookup"><span data-stu-id="91392-110">Pointer to a null-terminated string containing the new filename.</span></span> <span data-ttu-id="91392-111">如果媒體正在關閉，則會指定 null 字串。</span><span class="sxs-lookup"><span data-stu-id="91392-111">If the media is closing, it specifies a null string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91392-112">備註</span><span class="sxs-lookup"><span data-stu-id="91392-112">Remarks</span></span>

<span data-ttu-id="91392-113">您可以藉由指定 [MCIWNDF \_ NOTIFYMEDIA] 視窗樣式，來啟用媒體變更的通知。</span><span class="sxs-lookup"><span data-stu-id="91392-113">You can enable notification of media changes by specifying the MCIWNDF\_NOTIFYMEDIA window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="91392-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="91392-114">Requirements</span></span>



| <span data-ttu-id="91392-115">需求</span><span class="sxs-lookup"><span data-stu-id="91392-115">Requirement</span></span> | <span data-ttu-id="91392-116">值</span><span class="sxs-lookup"><span data-stu-id="91392-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="91392-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91392-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91392-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91392-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="91392-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91392-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91392-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91392-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="91392-121">標頭</span><span class="sxs-lookup"><span data-stu-id="91392-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="91392-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="91392-122"><dt>Vfw.h</dt></span></span> </dl> |



 

 





