---
description: HRECOWORDLIST 控制碼可用來管理您附加至辨識器內容的字組清單。 您可以使用單字清單來改善辨識結果。
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: 'HRECOWORDLIST 控制碼 (Recapis .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511709"
---
# <a name="hrecowordlist-handle"></a><span data-ttu-id="b14c4-104">HRECOWORDLIST 控制碼</span><span class="sxs-lookup"><span data-stu-id="b14c4-104">HRECOWORDLIST Handle</span></span>

<span data-ttu-id="b14c4-105">**HRECOWORDLIST** 控制碼可用來管理您附加至辨識器內容的字組清單。</span><span class="sxs-lookup"><span data-stu-id="b14c4-105">An **HRECOWORDLIST** handle is used to manage a word list you attach to a recognizer context.</span></span> <span data-ttu-id="b14c4-106">您可以使用單字清單來改善辨識結果。</span><span class="sxs-lookup"><span data-stu-id="b14c4-106">You use a word list to improve recognition results.</span></span>


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a><span data-ttu-id="b14c4-107">備註</span><span class="sxs-lookup"><span data-stu-id="b14c4-107">Remarks</span></span>

<span data-ttu-id="b14c4-108">下列函數使用 **HRECOWORDLIST**。</span><span class="sxs-lookup"><span data-stu-id="b14c4-108">The following function use an **HRECOWORDLIST**.</span></span>



| <span data-ttu-id="b14c4-109">函式</span><span class="sxs-lookup"><span data-stu-id="b14c4-109">Function</span></span>                                         | <span data-ttu-id="b14c4-110">描述</span><span class="sxs-lookup"><span data-stu-id="b14c4-110">Description</span></span>                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="b14c4-111">**AddWordsToWordList**</span><span class="sxs-lookup"><span data-stu-id="b14c4-111">**AddWordsToWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | <span data-ttu-id="b14c4-112">將一或多個單字加入至單字清單。</span><span class="sxs-lookup"><span data-stu-id="b14c4-112">Adds one or more words to the word list.</span></span><br/> |
| [<span data-ttu-id="b14c4-113">**DestroyWordList**</span><span class="sxs-lookup"><span data-stu-id="b14c4-113">**DestroyWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | <span data-ttu-id="b14c4-114">終結目前的字組清單。</span><span class="sxs-lookup"><span data-stu-id="b14c4-114">Destroys the current word list.</span></span><br/>          |
| [<span data-ttu-id="b14c4-115">**MakeWordList**</span><span class="sxs-lookup"><span data-stu-id="b14c4-115">**MakeWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | <span data-ttu-id="b14c4-116">建立字組清單。</span><span class="sxs-lookup"><span data-stu-id="b14c4-116">Creates a word list.</span></span><br/>                     |



 

## <a name="requirements"></a><span data-ttu-id="b14c4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b14c4-117">Requirements</span></span>



| <span data-ttu-id="b14c4-118">需求</span><span class="sxs-lookup"><span data-stu-id="b14c4-118">Requirement</span></span> | <span data-ttu-id="b14c4-119">值</span><span class="sxs-lookup"><span data-stu-id="b14c4-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b14c4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b14c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b14c4-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b14c4-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="b14c4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b14c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b14c4-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="b14c4-123">None supported</span></span><br/>                                                            |
| <span data-ttu-id="b14c4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b14c4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b14c4-125"><dt>Recapis。h</dt></span><span class="sxs-lookup"><span data-stu-id="b14c4-125"><dt>Recapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b14c4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b14c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b14c4-127">**SetWordList 函式**</span><span class="sxs-lookup"><span data-stu-id="b14c4-127">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




