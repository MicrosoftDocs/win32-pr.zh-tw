---
description: 當使用者從 [檔案管理員] 的 [View] 功能表選擇 [重新整理] 命令時，會傳送至擴充 DLL。 延伸模組可以使用此通知來更新其功能表。
title: 'FMEVENT_USER_REFRESH 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: c3c4596b0ea589545c6e59953b9c7b5977e07b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973224"
---
# <a name="fmevent_user_refresh-message"></a><span data-ttu-id="6d6d3-104">FMEVENT \_ 使用者重新整理 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="6d6d3-104">FMEVENT\_USER\_REFRESH message</span></span>

<span data-ttu-id="6d6d3-105">當使用者從 [檔案管理員] 的 [ **View** ] 功能表選擇 [重新整理 **] 命令時，會** 傳送至擴充 DLL。</span><span class="sxs-lookup"><span data-stu-id="6d6d3-105">Sent to an extension DLL when the user chooses the **Refresh** command from the **View** menu in File Manager.</span></span> <span data-ttu-id="6d6d3-106">延伸模組可以使用此通知來更新其功能表。</span><span class="sxs-lookup"><span data-stu-id="6d6d3-106">The extension can use this notification to update its menu.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d6d3-107">參數</span><span class="sxs-lookup"><span data-stu-id="6d6d3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d6d3-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d6d3-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6d6d3-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6d6d3-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6d6d3-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d6d3-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6d6d3-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6d6d3-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d6d3-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d6d3-112">Return value</span></span>

<span data-ttu-id="6d6d3-113">如果延伸模組 DLL 處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="6d6d3-113">An extension DLL should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d6d3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d6d3-114">Requirements</span></span>



| <span data-ttu-id="6d6d3-115">需求</span><span class="sxs-lookup"><span data-stu-id="6d6d3-115">Requirement</span></span> | <span data-ttu-id="6d6d3-116">值</span><span class="sxs-lookup"><span data-stu-id="6d6d3-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d6d3-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d6d3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6d6d3-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d6d3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6d6d3-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d6d3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6d6d3-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d6d3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6d6d3-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6d6d3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d6d3-122"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d6d3-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d6d3-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d6d3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d6d3-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="6d6d3-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




