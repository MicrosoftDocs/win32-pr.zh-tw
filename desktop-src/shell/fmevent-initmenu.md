---
description: 當使用者從 [檔案管理員] 功能表列選取擴充功能的功能表時，傳送至擴充 DLL。 延伸模組可以使用此通知來初始化功能表項目。
title: 'FMEVENT_INITMENU 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 4bbb959feeb2c1bf99eaa999b4c51b69b0d0cf63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191048"
---
# <a name="fmevent_initmenu-message"></a><span data-ttu-id="d736b-104">FMEVENT \_ INITMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="d736b-104">FMEVENT\_INITMENU message</span></span>

<span data-ttu-id="d736b-105">當使用者從 [檔案管理員] 功能表列選取擴充功能的功能表時，傳送至擴充 DLL。</span><span class="sxs-lookup"><span data-stu-id="d736b-105">Sent to an extension DLL when the user selects the menu for the extension from the File Manager menu bar.</span></span> <span data-ttu-id="d736b-106">延伸模組可以使用此通知來初始化功能表項目。</span><span class="sxs-lookup"><span data-stu-id="d736b-106">The extension can use this notification to initialize menu items.</span></span>

## <a name="parameters"></a><span data-ttu-id="d736b-107">參數</span><span class="sxs-lookup"><span data-stu-id="d736b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d736b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d736b-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d736b-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="d736b-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d736b-110">*hmenu*</span><span class="sxs-lookup"><span data-stu-id="d736b-110">*hmenu*</span></span> 
</dt> <dd>

<span data-ttu-id="d736b-111">[檔案管理員] 功能表列的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d736b-111">A handle to the File Manager menu bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d736b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d736b-112">Return value</span></span>

<span data-ttu-id="d736b-113">如果延伸模組 DLL 處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="d736b-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d736b-114">備註</span><span class="sxs-lookup"><span data-stu-id="d736b-114">Remarks</span></span>

<span data-ttu-id="d736b-115">只有當使用者選取最上層功能表時，擴充 DLL 才會接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="d736b-115">An extension DLL receives this message only when the user selects the top-level menu.</span></span> <span data-ttu-id="d736b-116">如果延伸模組包含子功能表，則必須在初始化最上層功能表時將它們初始化。</span><span class="sxs-lookup"><span data-stu-id="d736b-116">If the extension contains submenus, it must initialize them at the same time it initializes the top-level menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="d736b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d736b-117">Requirements</span></span>



| <span data-ttu-id="d736b-118">需求</span><span class="sxs-lookup"><span data-stu-id="d736b-118">Requirement</span></span> | <span data-ttu-id="d736b-119">值</span><span class="sxs-lookup"><span data-stu-id="d736b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d736b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d736b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d736b-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d736b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d736b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d736b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d736b-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d736b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d736b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d736b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d736b-125"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="d736b-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d736b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d736b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d736b-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="d736b-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




