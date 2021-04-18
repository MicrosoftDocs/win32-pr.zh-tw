---
title: 'TB_ADDSTRING 訊息 (Commctrl .h) '
description: 將新字串加入至工具列的字串集區。
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- TB_ADDSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968600"
---
# <a name="tb_addstring-message"></a><span data-ttu-id="146b9-104">TB \_ ADDSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="146b9-104">TB\_ADDSTRING message</span></span>

<span data-ttu-id="146b9-105">將新字串加入至工具列的字串集區。</span><span class="sxs-lookup"><span data-stu-id="146b9-105">Adds a new string to the toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="146b9-106">參數</span><span class="sxs-lookup"><span data-stu-id="146b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="146b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="146b9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="146b9-108">具有包含字串資源之可執行檔的模組實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="146b9-108">Handle to the module instance with an executable file that contains the string resource.</span></span> <span data-ttu-id="146b9-109">如果 *lParam* 改為指向具有一或多個字串的字元陣列，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="146b9-109">If *lParam* instead points to a character array with one or more strings, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="146b9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="146b9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="146b9-111">字串資源的資源識別碼，或 TCHAR 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="146b9-111">Resource identifier for the string resource, or a pointer to a TCHAR array.</span></span> <span data-ttu-id="146b9-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="146b9-112">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="146b9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="146b9-113">Return value</span></span>

<span data-ttu-id="146b9-114">如果成功，則傳回第一個新字串的索引，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="146b9-114">Returns the index of the first new string if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="146b9-115">備註</span><span class="sxs-lookup"><span data-stu-id="146b9-115">Remarks</span></span>

<span data-ttu-id="146b9-116">如果 *wParam* 為 **Null**，則 *lParam* 會指向具有一或多個以 Null 終止之字串的字元陣列。</span><span class="sxs-lookup"><span data-stu-id="146b9-116">If *wParam* is **NULL**, *lParam* points to a character array with one or more null-terminated strings.</span></span> <span data-ttu-id="146b9-117">陣列中的最後一個字串必須以兩個 null 字元做為結束。</span><span class="sxs-lookup"><span data-stu-id="146b9-117">The last string in the array must be terminated with two null characters.</span></span>

<span data-ttu-id="146b9-118">如果 *wParam* 為應用程式的 HINSTANCE，或包含字串資源的其他模組，則 *lParam* 是字串的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="146b9-118">If *wParam* is the HINSTANCE of the application or of another module containing a string resource, *lParam* is the resource identifier of the string.</span></span> <span data-ttu-id="146b9-119">字串中的每個專案都必須以任意分隔字元開頭，且字串必須以兩個這類字元結尾。</span><span class="sxs-lookup"><span data-stu-id="146b9-119">Each item in the string must begin with an arbitrary separator character, and the string must end with two such characters.</span></span> <span data-ttu-id="146b9-120">例如，三個按鈕的文字可能會以 "/New/Open/Save//" 形式出現在字串資料表中。</span><span class="sxs-lookup"><span data-stu-id="146b9-120">For example, the text for three buttons might appear in the string table as "/New/Open/Save//".</span></span> <span data-ttu-id="146b9-121">訊息會在工具列的字串集區中傳回 "New" 的索引，而其他專案則是在連續的位置。</span><span class="sxs-lookup"><span data-stu-id="146b9-121">The message returns the index of "New" in the toolbar's string pool, and the other items are in consecutive positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="146b9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="146b9-122">Requirements</span></span>



| <span data-ttu-id="146b9-123">需求</span><span class="sxs-lookup"><span data-stu-id="146b9-123">Requirement</span></span> | <span data-ttu-id="146b9-124">值</span><span class="sxs-lookup"><span data-stu-id="146b9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="146b9-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="146b9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="146b9-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="146b9-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="146b9-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="146b9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="146b9-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="146b9-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="146b9-129">標頭</span><span class="sxs-lookup"><span data-stu-id="146b9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="146b9-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="146b9-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="146b9-131">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="146b9-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="146b9-132">**TB \_ADDSTRINGW** (Unicode) 和 **TB \_ ADDSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="146b9-132">**TB\_ADDSTRINGW** (Unicode) and **TB\_ADDSTRINGA** (ANSI)</span></span><br/>                 |



 

 





