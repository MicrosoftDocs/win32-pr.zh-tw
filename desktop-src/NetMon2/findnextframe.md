---
description: 在目前的捕獲內容中尋找符合篩選準則的下一個畫面格。
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: 'FindNextFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510979"
---
# <a name="findnextframe-function"></a><span data-ttu-id="8d20c-103">FindNextFrame 函式</span><span class="sxs-lookup"><span data-stu-id="8d20c-103">FindNextFrame function</span></span>

<span data-ttu-id="8d20c-104">**FindNextFrame** 函式會在目前的捕獲內容中尋找符合篩選準則的下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="8d20c-104">The **FindNextFrame** function finds the next frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d20c-105">語法</span><span class="sxs-lookup"><span data-stu-id="8d20c-105">Syntax</span></span>


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="8d20c-106">參數</span><span class="sxs-lookup"><span data-stu-id="8d20c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d20c-107">*hCurrentFrame*</span><span class="sxs-lookup"><span data-stu-id="8d20c-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="8d20c-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8d20c-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="8d20c-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="8d20c-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="8d20c-110">通訊協定名稱，例如 TCP。</span><span class="sxs-lookup"><span data-stu-id="8d20c-110">The protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="8d20c-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="8d20c-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="8d20c-112">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="8d20c-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="8d20c-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="8d20c-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="8d20c-114">來源位址。</span><span class="sxs-lookup"><span data-stu-id="8d20c-114">The source address.</span></span>

</dd> <dt>

<span data-ttu-id="8d20c-115">*ProtocolOffset*</span><span class="sxs-lookup"><span data-stu-id="8d20c-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="8d20c-116">將接收通訊協定位移的 **單字** 指標。</span><span class="sxs-lookup"><span data-stu-id="8d20c-116">A pointer to a **WORD** that will receive the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="8d20c-117">*OriginalFrameNumber*</span><span class="sxs-lookup"><span data-stu-id="8d20c-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="8d20c-118">搜尋的起點。</span><span class="sxs-lookup"><span data-stu-id="8d20c-118">The starting point of the search.</span></span> <span data-ttu-id="8d20c-119">根據預設，此函式會從 *OriginalFrameNumber* 起點搜尋向前1000的畫面格。</span><span class="sxs-lookup"><span data-stu-id="8d20c-119">By default, this function searches forward 1,000 frames from the *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="8d20c-120">若要變更向前搜尋的距離，請將這一行新增至位於網路監視器目錄中的 Nmapi.ini 檔案 \\ 。</span><span class="sxs-lookup"><span data-stu-id="8d20c-120">To change the search-forward distance, add this line to the Nmapi.ini file, located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="8d20c-121">MAXLOOKBACK =<new lookforward distance></span><span class="sxs-lookup"><span data-stu-id="8d20c-121">MAXLOOKBACK=<new lookforward distance></span></span>

</dd> <dt>

<span data-ttu-id="8d20c-122">*HighestFrame*</span><span class="sxs-lookup"><span data-stu-id="8d20c-122">*HighestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="8d20c-123">在捕捉中搜尋的最大框架編號。</span><span class="sxs-lookup"><span data-stu-id="8d20c-123">The highest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d20c-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d20c-124">Return value</span></span>

<span data-ttu-id="8d20c-125">如果函式成功，則傳回值是下一個框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8d20c-125">If the function is successful, the return value is a handle to the next frame.</span></span>

<span data-ttu-id="8d20c-126">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d20c-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d20c-127">備註</span><span class="sxs-lookup"><span data-stu-id="8d20c-127">Remarks</span></span>

<span data-ttu-id="8d20c-128">Capture 篩選器主要由 *ProtocolName* 參數定義，這是唯一必要的篩選輸入;您可以新增 *DestinationAddress* 和 *SourceAddress* 資料，以提高捕獲速度。</span><span class="sxs-lookup"><span data-stu-id="8d20c-128">The capture filter is defined primarily by the *ProtocolName* parameter, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* data to increase the capture speed.</span></span>

<span data-ttu-id="8d20c-129">*ProtocolOffset* 指標會傳回給呼叫剖析器，它會使用 [ParserTemporaryLockFrame](parsertemporarylockframe.md)) 來鎖定框架 (，以將該 **字** 組新增至所傳回的指標，以取得所搜尋的通訊協定 **LPBYTE** 。</span><span class="sxs-lookup"><span data-stu-id="8d20c-129">The *ProtocolOffset* pointer is returned to the calling parser, which adds the **WORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the **LPBYTE** of the protocol searched for.</span></span> <span data-ttu-id="8d20c-130">傳回時，傳遞篩選器的 HFRAME 會提供給剖析器。</span><span class="sxs-lookup"><span data-stu-id="8d20c-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="8d20c-131">如果剖析器發現這個框架不是搜尋的畫面格，剖析器可以將 HFRAME 交給 **FindNextFrame** 函式，以取得下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="8d20c-131">If the parser finds that this frame is not the one sought, the parser can hand the HFRAME back to the **FindNextFrame** function to get the next frame.</span></span> <span data-ttu-id="8d20c-132">來源和目的地位址不是必要的，而且可以傳遞為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d20c-132">The source and destination addresses are not required and can be passed as **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d20c-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d20c-133">Requirements</span></span>



| <span data-ttu-id="8d20c-134">需求</span><span class="sxs-lookup"><span data-stu-id="8d20c-134">Requirement</span></span> | <span data-ttu-id="8d20c-135">值</span><span class="sxs-lookup"><span data-stu-id="8d20c-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8d20c-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d20c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8d20c-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d20c-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8d20c-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d20c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8d20c-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d20c-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8d20c-140">標頭</span><span class="sxs-lookup"><span data-stu-id="8d20c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d20c-141"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="8d20c-141"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8d20c-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d20c-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d20c-143"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d20c-143"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d20c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8d20c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d20c-145"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d20c-145"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




