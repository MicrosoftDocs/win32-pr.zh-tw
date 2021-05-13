---
description: 由檔案管理員延伸模組所傳送，可在 [active 檔案管理員] 視窗中取出所選檔案的計數 (目錄視窗或 [搜尋結果] 視窗) 。
title: 'FM_GETSELCOUNT 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNT
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0d43bf37-863c-45cc-94ea-5b2aedba5353
ms.openlocfilehash: 727e098a98ecfe4a4349ebcf9c6f931a8579b70d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842369"
---
# <a name="fm_getselcount-message"></a><span data-ttu-id="73043-103">FM \_ GETSELCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="73043-103">FM\_GETSELCOUNT message</span></span>

<span data-ttu-id="73043-104">由檔案管理員延伸模組所傳送，可在 [active 檔案管理員] 視窗中取出所選檔案的計數 (目錄視窗或 [搜尋結果] 視窗) 。</span><span class="sxs-lookup"><span data-stu-id="73043-104">Sent by a File Manager extension to retrieve a count of the selected files in the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="73043-105">參數</span><span class="sxs-lookup"><span data-stu-id="73043-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73043-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73043-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="73043-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="73043-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="73043-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73043-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="73043-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="73043-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73043-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="73043-110">Return value</span></span>

<span data-ttu-id="73043-111">傳回選取的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="73043-111">Returns the number of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="73043-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="73043-112">Requirements</span></span>



| <span data-ttu-id="73043-113">需求</span><span class="sxs-lookup"><span data-stu-id="73043-113">Requirement</span></span> | <span data-ttu-id="73043-114">值</span><span class="sxs-lookup"><span data-stu-id="73043-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73043-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73043-115">Minimum supported client</span></span><br/> | <span data-ttu-id="73043-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73043-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="73043-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73043-117">Minimum supported server</span></span><br/> | <span data-ttu-id="73043-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73043-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="73043-119">標頭</span><span class="sxs-lookup"><span data-stu-id="73043-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="73043-120"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="73043-120"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73043-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73043-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73043-122">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="73043-122">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="73043-123">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="73043-123">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="73043-124">**FM \_ GETSELCOUNTLFN**</span><span class="sxs-lookup"><span data-stu-id="73043-124">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




