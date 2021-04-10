---
title: 'TB_GETBUTTONINFO 訊息 (Commctrl .h) '
description: 抓取工具列中按鈕的擴充資訊。
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- TB_GETBUTTONINFO message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106601"
---
# <a name="tb_getbuttoninfo-message"></a><span data-ttu-id="d357b-104">TB \_ GETBUTTONINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="d357b-104">TB\_GETBUTTONINFO message</span></span>

<span data-ttu-id="d357b-105">抓取工具列中按鈕的擴充資訊。</span><span class="sxs-lookup"><span data-stu-id="d357b-105">Retrieves extended information for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d357b-106">參數</span><span class="sxs-lookup"><span data-stu-id="d357b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d357b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d357b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d357b-108">按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="d357b-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="d357b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d357b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d357b-110">接收按鈕資訊之 [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d357b-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that receives the button information.</span></span> <span data-ttu-id="d357b-111">在傳送此訊息之前，必須先填入此結構的 **cbSize** 和 **dwMask** 成員。</span><span class="sxs-lookup"><span data-stu-id="d357b-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d357b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d357b-112">Return value</span></span>

<span data-ttu-id="d357b-113">傳回按鈕的以零為起始的索引; 如果發生錯誤，則為-1。</span><span class="sxs-lookup"><span data-stu-id="d357b-113">Returns the zero-based index of the button, or -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="d357b-114">備註</span><span class="sxs-lookup"><span data-stu-id="d357b-114">Remarks</span></span>

<span data-ttu-id="d357b-115">當您使用 [**TB \_ ADDBUTTONS**](tb-addbuttons.md) 或 [**tb \_ INSERTBUTTON**](tb-insertbutton.md) 將按鈕放在工具列上時，按鈕文字通常是由其字串集區索引所指定。</span><span class="sxs-lookup"><span data-stu-id="d357b-115">When you use [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) to place buttons on the toolbar, the button text is commonly specified by its string pool index.</span></span> <span data-ttu-id="d357b-116">**TB \_GETBUTTONINFO** 將不會取得此字串。</span><span class="sxs-lookup"><span data-stu-id="d357b-116">**TB\_GETBUTTONINFO** will not retrieve this string.</span></span> <span data-ttu-id="d357b-117">若要使用 **tb \_ GETBUTTONINFO** 來抓取按鈕文字，您必須先設定具有 [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)的文字字串。</span><span class="sxs-lookup"><span data-stu-id="d357b-117">To use **TB\_GETBUTTONINFO** to retrieve button text, you must first set the text string with [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md).</span></span> <span data-ttu-id="d357b-118">將按鈕文字設定為 [TB] **\_ SETBUTTONINFO** 之後，就無法再使用字串集區索引。</span><span class="sxs-lookup"><span data-stu-id="d357b-118">Once you have set the button text with **TB\_SETBUTTONINFO**, you can no longer use the string pool index.</span></span>

## <a name="requirements"></a><span data-ttu-id="d357b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d357b-119">Requirements</span></span>



| <span data-ttu-id="d357b-120">需求</span><span class="sxs-lookup"><span data-stu-id="d357b-120">Requirement</span></span> | <span data-ttu-id="d357b-121">值</span><span class="sxs-lookup"><span data-stu-id="d357b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d357b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d357b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d357b-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d357b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d357b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d357b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d357b-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d357b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d357b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d357b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d357b-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d357b-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d357b-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d357b-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d357b-129">**TB \_GETBUTTONINFOW** (Unicode) 和 **TB \_ GETBUTTONINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d357b-129">**TB\_GETBUTTONINFOW** (Unicode) and **TB\_GETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="d357b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d357b-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="d357b-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="d357b-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d357b-132">**TB \_ SETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="d357b-132">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="d357b-133">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="d357b-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> </dl>

 

 





