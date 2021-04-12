---
title: 'EM_FILELINEFROMCHAR 訊息 (CommCtrl .h) '
description: 取得在多行編輯控制項中包含指定字元索引的行索引，與螢幕上的線條顯示方式無關。
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_FILELINEFROMCHAR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465717"
---
# <a name="em_filelinefromchar-message"></a><span data-ttu-id="cb6dd-104">EM \_ FILELINEFROMCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="cb6dd-104">EM\_FILELINEFROMCHAR message</span></span>

<span data-ttu-id="cb6dd-105">取得在多行編輯控制項中包含指定字元索引的行索引，與螢幕上的線條顯示方式無關。</span><span class="sxs-lookup"><span data-stu-id="cb6dd-105">Gets the index of the line that contains the specified character index in a multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="cb6dd-106">字元索引是編輯控制項開頭的字元之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="cb6dd-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb6dd-107">參數</span><span class="sxs-lookup"><span data-stu-id="cb6dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb6dd-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb6dd-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb6dd-109">要取出其數位的行中所含字元的字元索引。</span><span class="sxs-lookup"><span data-stu-id="cb6dd-109">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="cb6dd-110">如果此參數為-1， **EM \_ FILELINEFROMCHAR** 會抓取目前行的行號， (包含插入號) 的行號，或者，如果有選取範圍，則為包含選取範圍開頭之行的行號。</span><span class="sxs-lookup"><span data-stu-id="cb6dd-110">If this parameter is -1, **EM\_FILELINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="cb6dd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb6dd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb6dd-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="cb6dd-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb6dd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb6dd-113">Return value</span></span>

<span data-ttu-id="cb6dd-114">傳回值是行的以零為起始的行號，其中包含 *wParam* 指定的字元索引，與螢幕上的線條顯示方式無關。</span><span class="sxs-lookup"><span data-stu-id="cb6dd-114">The return value is the zero-based line number of the line containing the character index specified by *wParam*, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb6dd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb6dd-115">Requirements</span></span>



| <span data-ttu-id="cb6dd-116">需求</span><span class="sxs-lookup"><span data-stu-id="cb6dd-116">Requirement</span></span> | <span data-ttu-id="cb6dd-117">值</span><span class="sxs-lookup"><span data-stu-id="cb6dd-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6dd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb6dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb6dd-119">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb6dd-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb6dd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb6dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb6dd-121">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb6dd-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb6dd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="cb6dd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb6dd-123"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb6dd-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb6dd-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb6dd-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb6dd-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="cb6dd-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb6dd-126">**EM \_ FILELINEINDEX**</span><span class="sxs-lookup"><span data-stu-id="cb6dd-126">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





