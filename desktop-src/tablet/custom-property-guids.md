---
description: 下列 (Guid) 的全域唯一識別碼，Windows 筆記本用來識別筆劃或繪圖屬性上的自訂屬性。
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: 自訂屬性 Guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987331"
---
# <a name="custom-property-guids"></a><span data-ttu-id="b3347-103">自訂屬性 Guid</span><span class="sxs-lookup"><span data-stu-id="b3347-103">Custom Property GUIDs</span></span>

<span data-ttu-id="b3347-104">下列 (Guid) 的全域唯一識別碼，Windows 筆記本用來識別筆劃或繪圖屬性上的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="b3347-104">The following globally unique identifiers (GUIDs) are used by Windows Journal to identify custom properties on strokes or drawing attributes.</span></span>

## <a name="guid_stroke_timestamp"></a><span data-ttu-id="b3347-105">GUID \_ 筆劃 \_ 時間戳記</span><span class="sxs-lookup"><span data-stu-id="b3347-105">GUID\_STROKE\_TIMESTAMP</span></span>


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



<span data-ttu-id="b3347-106">這是一個 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 結構，表示筆劃的建立時間或新增至檔的時間。</span><span class="sxs-lookup"><span data-stu-id="b3347-106">This is a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure that indicates the time at which the stroke was created or added to the document.</span></span>


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a><span data-ttu-id="b3347-107">GUID \_ 筆劃 \_ TIMEID</span><span class="sxs-lookup"><span data-stu-id="b3347-107">GUID\_STROKE\_TIMEID</span></span>


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



<span data-ttu-id="b3347-108">這是 **TIMEID** 結構。</span><span class="sxs-lookup"><span data-stu-id="b3347-108">This is a **TIMEID** structure.</span></span> <span data-ttu-id="b3347-109">它可讓您在貼上和卸載作業期間維持筆劃順序。</span><span class="sxs-lookup"><span data-stu-id="b3347-109">It allows stroke order to be maintained across paste and drop operations.</span></span> <span data-ttu-id="b3347-110">如果沒有 **TIMEID** 結構，在 [InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))中剪下和貼上的所有 [**IInkStrokeDisp 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的時間戳記都會相同。</span><span class="sxs-lookup"><span data-stu-id="b3347-110">Without the **TIMEID** structure, the timestamp for all [**IInkStrokeDisp Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects cut and pasted in a [InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) will be the same.</span></span>


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a><span data-ttu-id="b3347-111">GUID \_ 螢光筆</span><span class="sxs-lookup"><span data-stu-id="b3347-111">GUID\_HIGHLIGHTER</span></span>

<span data-ttu-id="b3347-112">這是 **布林** 值，其中 **TRUE**= 螢光筆筆墨， **FALSE**= 一般筆跡。</span><span class="sxs-lookup"><span data-stu-id="b3347-112">This is a **BOOL**, where **TRUE**=highlighter ink, **FALSE**=regular ink.</span></span> <span data-ttu-id="b3347-113">這會套用至繪圖屬性。</span><span class="sxs-lookup"><span data-stu-id="b3347-113">This is applied to drawing attributes.</span></span>


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a><span data-ttu-id="b3347-114">GUID \_ 筆墨 \_ 樣式 \_ 粗體</span><span class="sxs-lookup"><span data-stu-id="b3347-114">GUID\_INK\_STYLE\_BOLD</span></span>

<span data-ttu-id="b3347-115">這是 **布林** 值，其中 **TRUE**= bold 筆墨， **FALSE**= normal。</span><span class="sxs-lookup"><span data-stu-id="b3347-115">This is a **BOOL**, where **TRUE**=bold ink, **FALSE**=normal.</span></span> <span data-ttu-id="b3347-116">這會套用至繪圖屬性。</span><span class="sxs-lookup"><span data-stu-id="b3347-116">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a><span data-ttu-id="b3347-117">GUID \_ 筆墨 \_ 樣式 \_ 斜體</span><span class="sxs-lookup"><span data-stu-id="b3347-117">GUID\_INK\_STYLE\_ITALICS</span></span>

<span data-ttu-id="b3347-118">這是 **布林** 值，其中 **TRUE**= 斜體筆墨， **FALSE**= normal。</span><span class="sxs-lookup"><span data-stu-id="b3347-118">This is a **BOOL**, where **TRUE**=italicized ink, **FALSE**=normal.</span></span> <span data-ttu-id="b3347-119">這會套用至繪圖屬性。</span><span class="sxs-lookup"><span data-stu-id="b3347-119">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a><span data-ttu-id="b3347-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3347-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3347-121">**IJournalReader 介面**</span><span class="sxs-lookup"><span data-stu-id="b3347-121">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> </dl>

 

 
