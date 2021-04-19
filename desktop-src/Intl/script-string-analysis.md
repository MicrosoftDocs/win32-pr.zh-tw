---
description: 定義字串的部分或全部字元屬性、圖像、前進寬度、x 和 y 位置、字元對圖像對應等等。
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: 'SCRIPT_STRING_ANALYSIS (Usp10) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991913"
---
# <a name="script_string_analysis"></a><span data-ttu-id="98df8-103">腳本 \_ 字串 \_ 分析</span><span class="sxs-lookup"><span data-stu-id="98df8-103">SCRIPT\_STRING\_ANALYSIS</span></span>

<span data-ttu-id="98df8-104">定義字串的部分或全部字元屬性、圖像、前進寬度、x 和 y 位置、字元對圖像對應等等。</span><span class="sxs-lookup"><span data-stu-id="98df8-104">Defines some or all of the character attributes, glyphs, advance widths, x and y positions, character-to-glyph mappings, and so forth, for a string.</span></span>


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a><span data-ttu-id="98df8-105">備註</span><span class="sxs-lookup"><span data-stu-id="98df8-105">Remarks</span></span>

<span data-ttu-id="98df8-106">這是 [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)動態配置及取出的不透明結構。</span><span class="sxs-lookup"><span data-stu-id="98df8-106">This is an opaque structure that is allocated dynamically and retrieved by [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span></span> <span data-ttu-id="98df8-107">所有其他 \**ScriptString \** _ 函式也需要此功能。</span><span class="sxs-lookup"><span data-stu-id="98df8-107">It is required for all other \**ScriptString\** _ functions, as well.</span></span>

<span data-ttu-id="98df8-108">因為分析可能很大，所以您的應用程式必須在完成字串後立即呼叫 [_ *ScriptStringFree* \*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) 。</span><span class="sxs-lookup"><span data-stu-id="98df8-108">Since the analysis can be large, it is important for your application to call [_ *ScriptStringFree*\*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) as soon as it has finished with the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="98df8-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="98df8-109">Requirements</span></span>



| <span data-ttu-id="98df8-110">需求</span><span class="sxs-lookup"><span data-stu-id="98df8-110">Requirement</span></span> | <span data-ttu-id="98df8-111">值</span><span class="sxs-lookup"><span data-stu-id="98df8-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98df8-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98df8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="98df8-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98df8-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="98df8-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98df8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="98df8-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98df8-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="98df8-116">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="98df8-116">Redistributable</span></span><br/>          | <span data-ttu-id="98df8-117">Internet Explorer 5 或更新版本于 windows Me/98/95</span><span class="sxs-lookup"><span data-stu-id="98df8-117">Internet Explorer 5 or later onWindows Me/98/95</span></span><br/>                         |
| <span data-ttu-id="98df8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="98df8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="98df8-119"><dt>Usp10。h</dt></span><span class="sxs-lookup"><span data-stu-id="98df8-119"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98df8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98df8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98df8-121">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="98df8-121">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="98df8-122">Uniscribe 結構</span><span class="sxs-lookup"><span data-stu-id="98df8-122">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="98df8-123">**ScriptStringAnalyse**</span><span class="sxs-lookup"><span data-stu-id="98df8-123">**ScriptStringAnalyse**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[<span data-ttu-id="98df8-124">**ScriptStringFree**</span><span class="sxs-lookup"><span data-stu-id="98df8-124">**ScriptStringFree**</span></span>](script-string-analysis.md)
</dt> </dl>

 

 




