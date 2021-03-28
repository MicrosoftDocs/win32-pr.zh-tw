---
description: 當使用者在 [檔案管理員目錄] 視窗或 [搜尋結果] 視窗中選取檔案名時，傳送至擴充 DLL。
title: 'FMEVENT_SELCHANGE 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: 4b05bca54f75bd48b5e710e31c31e5f0f56a2597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510787"
---
# <a name="fmevent_selchange-message"></a><span data-ttu-id="23ef0-103">FMEVENT \_ SELCHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="23ef0-103">FMEVENT\_SELCHANGE message</span></span>

<span data-ttu-id="23ef0-104">當使用者在 [檔案管理員目錄] 視窗或 [搜尋結果] 視窗中選取檔案名時，傳送至擴充 DLL。</span><span class="sxs-lookup"><span data-stu-id="23ef0-104">Sent to an extension DLL when the user selects a file name in the File Manager directory window or Search Results window.</span></span>

## <a name="parameters"></a><span data-ttu-id="23ef0-105">參數</span><span class="sxs-lookup"><span data-stu-id="23ef0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23ef0-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23ef0-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="23ef0-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="23ef0-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="23ef0-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23ef0-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="23ef0-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="23ef0-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23ef0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="23ef0-110">Return value</span></span>

<span data-ttu-id="23ef0-111">如果延伸模組 DLL 處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="23ef0-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="23ef0-112">備註</span><span class="sxs-lookup"><span data-stu-id="23ef0-112">Remarks</span></span>

<span data-ttu-id="23ef0-113">目錄視窗的樹狀結構部分中的變更不會產生此訊息。</span><span class="sxs-lookup"><span data-stu-id="23ef0-113">Changes in the tree portion of the directory window do not produce this message.</span></span>

<span data-ttu-id="23ef0-114">因為使用者可以多次變更選取專案，所以擴充 DLL 必須在處理此訊息之後立即傳回，以避免讓使用者的選取程式變慢。</span><span class="sxs-lookup"><span data-stu-id="23ef0-114">Because the user can change the selection many times, the extension DLL must return promptly after processing this message to avoid slowing the selection process for the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="23ef0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="23ef0-115">Requirements</span></span>



| <span data-ttu-id="23ef0-116">需求</span><span class="sxs-lookup"><span data-stu-id="23ef0-116">Requirement</span></span> | <span data-ttu-id="23ef0-117">值</span><span class="sxs-lookup"><span data-stu-id="23ef0-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23ef0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23ef0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="23ef0-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23ef0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="23ef0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23ef0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="23ef0-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23ef0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="23ef0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="23ef0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="23ef0-123"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="23ef0-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ef0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23ef0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ef0-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="23ef0-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




