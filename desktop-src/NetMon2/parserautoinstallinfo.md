---
description: ParserAutoInstallInfo export 函數會識別位於 DLL 中的剖析器或剖析器。 ParserAutoInstallInfo 應該在所有剖析器 Dll 中實作為。
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: 'ParserAutoInstallInfo 回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318072"
---
# <a name="parserautoinstallinfo-callback-function"></a><span data-ttu-id="e8754-104">ParserAutoInstallInfo 回呼函式</span><span class="sxs-lookup"><span data-stu-id="e8754-104">ParserAutoInstallInfo callback function</span></span>

<span data-ttu-id="e8754-105">**ParserAutoInstallInfo** export 函數會識別位於 DLL 中的剖析器或剖析器。</span><span class="sxs-lookup"><span data-stu-id="e8754-105">The **ParserAutoInstallInfo** export function identifies the parser, or parsers that are located in a DLL.</span></span> <span data-ttu-id="e8754-106">**ParserAutoInstallInfo** 應該在所有剖析器 dll 中實作為。</span><span class="sxs-lookup"><span data-stu-id="e8754-106">**ParserAutoInstallInfo** should be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8754-107">語法</span><span class="sxs-lookup"><span data-stu-id="e8754-107">Syntax</span></span>


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a><span data-ttu-id="e8754-108">參數</span><span class="sxs-lookup"><span data-stu-id="e8754-108">Parameters</span></span>

<span data-ttu-id="e8754-109">這個回呼函數沒有參數。</span><span class="sxs-lookup"><span data-stu-id="e8754-109">This callback function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8754-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8754-110">Return value</span></span>

<span data-ttu-id="e8754-111">如果函式成功，則傳回值會是用來描述 DLL 中剖析器的 [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="e8754-111">If the function is successful, the return value is a [PF\_PARSERDLLINFO](pf-parserdllinfo.md) structure that describes the parsers in the DLL.</span></span>

<span data-ttu-id="e8754-112">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e8754-112">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8754-113">備註</span><span class="sxs-lookup"><span data-stu-id="e8754-113">Remarks</span></span>

<span data-ttu-id="e8754-114">當網路監視器第一次載入時，它會呼叫 **ParserAutoInstallInfo** (（如果存在的話）) 自動安裝每個剖析器，然後列舉剖析器子目錄中的所有剖析器 dll。</span><span class="sxs-lookup"><span data-stu-id="e8754-114">When Network Monitor loads for the first time, it calls **ParserAutoInstallInfo** (if it exists) to automatically install each parser, and then enumerate all the parser DLLs in the parser subdirectory.</span></span>

<span data-ttu-id="e8754-115">在 **PF \_ PARSERDLLINFO** 結構中傳回的資訊包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="e8754-115">The information returned in the **PF\_PARSERDLLINFO** structure includes the following:</span></span>

-   <span data-ttu-id="e8754-116">DLL 中的剖析器數目 (通常是一個) 。</span><span class="sxs-lookup"><span data-stu-id="e8754-116">The number of parsers in the DLL (typically one).</span></span>
-   <span data-ttu-id="e8754-117">每個剖析器偵測到的通訊協定名稱和簡短描述。</span><span class="sxs-lookup"><span data-stu-id="e8754-117">The name and a brief description of the protocol that each parser detects.</span></span>
-   <span data-ttu-id="e8754-118">每個通訊協定都有選擇性的說明檔。</span><span class="sxs-lookup"><span data-stu-id="e8754-118">An optional Help file for each protocol.</span></span>
-   <span data-ttu-id="e8754-119">每個通訊協定前面的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e8754-119">The protocols that precede each protocol.</span></span>
-   <span data-ttu-id="e8754-120">遵循每個通訊協定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e8754-120">The protocols that follow each protocol.</span></span>

<span data-ttu-id="e8754-121">每個剖析器 DLL 都應該包含一個剖析器。</span><span class="sxs-lookup"><span data-stu-id="e8754-121">Each parser DLL should contain one parser.</span></span> <span data-ttu-id="e8754-122">不過，網路監視器可讓您建立包含一個以上剖析器的 DLL。</span><span class="sxs-lookup"><span data-stu-id="e8754-122">However, Network Monitor allows you to create a DLL that contains more than one parser.</span></span> <span data-ttu-id="e8754-123">例如，tcpip.dll 是具有一個以上剖析器的網路監視器 DLL。</span><span class="sxs-lookup"><span data-stu-id="e8754-123">For example, tcpip.dll is a Network Monitor DLL with more than one parser.</span></span>



| <span data-ttu-id="e8754-124">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="e8754-124">For information on</span></span>                                               | <span data-ttu-id="e8754-125">請參閱</span><span class="sxs-lookup"><span data-stu-id="e8754-125">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e8754-126">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="e8754-126">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="e8754-127">解析 器</span><span class="sxs-lookup"><span data-stu-id="e8754-127">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="e8754-128">剖析器 DLL 中包含的進入點。</span><span class="sxs-lookup"><span data-stu-id="e8754-128">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="e8754-129">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="e8754-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="e8754-130">如何執行 **ParserAutoInstallInfo**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="e8754-130">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="e8754-131">執行 ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="e8754-131">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="e8754-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8754-132">Requirements</span></span>



| <span data-ttu-id="e8754-133">需求</span><span class="sxs-lookup"><span data-stu-id="e8754-133">Requirement</span></span> | <span data-ttu-id="e8754-134">值</span><span class="sxs-lookup"><span data-stu-id="e8754-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e8754-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8754-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e8754-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8754-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e8754-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8754-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e8754-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8754-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e8754-139">標頭</span><span class="sxs-lookup"><span data-stu-id="e8754-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8754-140"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e8754-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8754-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8754-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8754-142">PF \_ PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="e8754-142">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




