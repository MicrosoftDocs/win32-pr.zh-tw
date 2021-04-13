---
description: IWordInfo 介面是日文專用的語言資源元件。 物件會剖析文字並識別個別的單字，並傳回字串中的文字，或傳回字典 (根) 形式的字串文字中的單字。
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: IWordInfo 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510405"
---
# <a name="iwordinfo-interface"></a><span data-ttu-id="819e5-104">IWordInfo 介面</span><span class="sxs-lookup"><span data-stu-id="819e5-104">IWordInfo interface</span></span>

<span data-ttu-id="819e5-105">\[此介面已淘汰，且在 Windows Vista 上不受支援。\]</span><span class="sxs-lookup"><span data-stu-id="819e5-105">\[This interface is obsolete and is not supported on Windows Vista.\]</span></span>

<span data-ttu-id="819e5-106">**IWordInfo** 介面是日文專用的語言資源元件。</span><span class="sxs-lookup"><span data-stu-id="819e5-106">The **IWordInfo** interface is a Japanese-specific language resource component.</span></span> <span data-ttu-id="819e5-107">物件會剖析文字並識別個別的單字，並傳回字串中的文字，或傳回字典 (根) 形式的字串文字中的單字。</span><span class="sxs-lookup"><span data-stu-id="819e5-107">The object parses text and identifies individual words, returning either the words in the string or returns the dictionary (root) forms of the words in the text of the string.</span></span>

## <a name="members"></a><span data-ttu-id="819e5-108">成員</span><span class="sxs-lookup"><span data-stu-id="819e5-108">Members</span></span>

<span data-ttu-id="819e5-109">**IWordInfo** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="819e5-109">The **IWordInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="819e5-110">**IWordInfo** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="819e5-110">**IWordInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="819e5-111">方法</span><span class="sxs-lookup"><span data-stu-id="819e5-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="819e5-112">方法</span><span class="sxs-lookup"><span data-stu-id="819e5-112">Methods</span></span>

<span data-ttu-id="819e5-113">**IWordInfo** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="819e5-113">The **IWordInfo** interface has these methods.</span></span>



| <span data-ttu-id="819e5-114">方法</span><span class="sxs-lookup"><span data-stu-id="819e5-114">Method</span></span>        | <span data-ttu-id="819e5-115">描述</span><span class="sxs-lookup"><span data-stu-id="819e5-115">Description</span></span>                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="819e5-116">**BreakText**</span><span class="sxs-lookup"><span data-stu-id="819e5-116">**BreakText**</span></span> | <span data-ttu-id="819e5-117">剖析文字以識別單字，並將結果提供給 [WordSink](/previous-versions//ms691570(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="819e5-117">Parses text to identify words and provides the results to the [WordSink](/previous-versions//ms691570(v=vs.85)) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="819e5-118">備註</span><span class="sxs-lookup"><span data-stu-id="819e5-118">Remarks</span></span>

<span data-ttu-id="819e5-119">這個介面是用來針對要分析的文字，取得日文斷詞或字典表單。</span><span class="sxs-lookup"><span data-stu-id="819e5-119">This interface is used to retrieve Japanese word breaks or dictionary forms for the text to be analyzed.</span></span> <span data-ttu-id="819e5-120">單字的字典形式是單字的 uninflected 形式。</span><span class="sxs-lookup"><span data-stu-id="819e5-120">The dictionary form of a word is the uninflected form of the word.</span></span>

## <a name="requirements"></a><span data-ttu-id="819e5-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="819e5-121">Requirements</span></span>



| <span data-ttu-id="819e5-122">需求</span><span class="sxs-lookup"><span data-stu-id="819e5-122">Requirement</span></span> | <span data-ttu-id="819e5-123">值</span><span class="sxs-lookup"><span data-stu-id="819e5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="819e5-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="819e5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="819e5-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="819e5-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="819e5-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="819e5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="819e5-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="819e5-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="819e5-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="819e5-128">End of client support</span></span><br/>    | <span data-ttu-id="819e5-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="819e5-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="819e5-130">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="819e5-130">End of server support</span></span><br/>    | <span data-ttu-id="819e5-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="819e5-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="819e5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="819e5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="819e5-133"><dt>Msir3jp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="819e5-133"><dt>Msir3jp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="819e5-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="819e5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="819e5-135">**WordInfo**</span><span class="sxs-lookup"><span data-stu-id="819e5-135">**WordInfo**</span></span>](wordinfo-coclass.md)
</dt> <dt>

<span data-ttu-id="819e5-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="819e5-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span></span>
</dt> </dl>

 

 
