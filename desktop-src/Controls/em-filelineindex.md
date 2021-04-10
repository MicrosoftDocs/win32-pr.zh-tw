---
title: 'EM_FILELINEINDEX 訊息 (CommCtrl .h) '
description: 取得多行編輯控制項中指定行第一個字元的字元索引，與螢幕上的線條顯示方式無關。
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104226"
---
# <a name="em_filelineindex-message-commctrlh"></a><span data-ttu-id="15946-104">EM_FILELINEINDEX 訊息 (CommCtrl .h) </span><span class="sxs-lookup"><span data-stu-id="15946-104">EM_FILELINEINDEX message (CommCtrl.h)</span></span>

<span data-ttu-id="15946-105">取得多行編輯控制項中指定行第一個字元的字元索引，與螢幕上的線條顯示方式無關。</span><span class="sxs-lookup"><span data-stu-id="15946-105">Gets the character index of the first character of a specified line in a multiline edit control, independently of how lines are displayed on the screen..</span></span> <span data-ttu-id="15946-106">字元索引是編輯控制項開頭的字元之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="15946-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="15946-107">參數</span><span class="sxs-lookup"><span data-stu-id="15946-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15946-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15946-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15946-109">以零為基底的行號。</span><span class="sxs-lookup"><span data-stu-id="15946-109">The zero-based line number.</span></span> <span data-ttu-id="15946-110">值-1 會指定包含插入號)  (行的目前行號。</span><span class="sxs-lookup"><span data-stu-id="15946-110">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="15946-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15946-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15946-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="15946-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15946-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="15946-113">Return value</span></span>

<span data-ttu-id="15946-114">傳回值是 *wParam* 參數中指定之線條的字元索引，與螢幕上的線條顯示方式無關，或者，如果指定的行號大於編輯控制項中的行數，則為-1。</span><span class="sxs-lookup"><span data-stu-id="15946-114">The return value is the character index of the line specified in the *wParam* parameter, independently of how lines are displayed on the screen, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="15946-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="15946-115">Requirements</span></span>



| <span data-ttu-id="15946-116">需求</span><span class="sxs-lookup"><span data-stu-id="15946-116">Requirement</span></span> | <span data-ttu-id="15946-117">值</span><span class="sxs-lookup"><span data-stu-id="15946-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15946-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15946-118">Minimum supported client</span></span><br/> | <span data-ttu-id="15946-119">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15946-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="15946-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15946-120">Minimum supported server</span></span><br/> | <span data-ttu-id="15946-121">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15946-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15946-122">標頭</span><span class="sxs-lookup"><span data-stu-id="15946-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="15946-123"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="15946-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15946-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15946-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15946-125">**EM \_ FILELINEFROMCHAR**</span><span class="sxs-lookup"><span data-stu-id="15946-125">**EM\_FILELINEFROMCHAR**</span></span>](em-filelinefromchar.md)
</dt> </dl>

 

 





