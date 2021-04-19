---
description: 代表呼叫堆疊上框架的相關資訊。
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CallStackFrame 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbe527c59a64e91f46a390344ea576c7560ef1f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971105"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span data-ttu-id="1c9a9-103"><span id="vspixengine.callstackframe"></span>CallStackFrame 結構</span><span class="sxs-lookup"><span data-stu-id="1c9a9-103"><span id="vspixengine.callstackframe"></span>CallStackFrame structure</span></span>

<span data-ttu-id="1c9a9-104">代表呼叫堆疊上框架的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-104">Represents information about a frame on the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c9a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c9a9-105">Syntax</span></span>


```C++
} CallStackFrame;
```

## <a name="members"></a><span data-ttu-id="1c9a9-106">成員</span><span class="sxs-lookup"><span data-stu-id="1c9a9-106">Members</span></span>

<span data-ttu-id="1c9a9-107">**functionName**</span><span class="sxs-lookup"><span data-stu-id="1c9a9-107">**functionName**</span></span>  
<span data-ttu-id="1c9a9-108">COM 字串，其中包含相關聯的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-108">A COM string containing the name of the associated function.</span></span>

<span data-ttu-id="1c9a9-109">**sourceFile**</span><span class="sxs-lookup"><span data-stu-id="1c9a9-109">**sourceFile**</span></span>  
<span data-ttu-id="1c9a9-110">COM 字串，其中包含相關原始程式檔的 filepath。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-110">A COM string containing the filepath of the associated source file.</span></span>

<span data-ttu-id="1c9a9-111">**moduleName**</span><span class="sxs-lookup"><span data-stu-id="1c9a9-111">**moduleName**</span></span>  
<span data-ttu-id="1c9a9-112">COM 字串，其中包含相關聯程式碼模組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-112">A COM string containing the name of the associated code module.</span></span>

<span data-ttu-id="1c9a9-113">**lineNumber**</span><span class="sxs-lookup"><span data-stu-id="1c9a9-113">**lineNumber**</span></span>  
<span data-ttu-id="1c9a9-114">關聯的行號。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-114">The associated line number.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c9a9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c9a9-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1c9a9-116">標頭</span><span class="sxs-lookup"><span data-stu-id="1c9a9-116">Header</span></span></p></td><td><span data-ttu-id="1c9a9-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="1c9a9-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



