---
description: FindPreviousFrame 函式會在目前的捕獲內容中尋找符合篩選準則的上一個畫面格。
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: 'FindPreviousFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936633"
---
# <a name="findpreviousframe-function"></a><span data-ttu-id="7ee08-103">FindPreviousFrame 函式</span><span class="sxs-lookup"><span data-stu-id="7ee08-103">FindPreviousFrame function</span></span>

<span data-ttu-id="7ee08-104">**FindPreviousFrame** 函式會在目前的捕獲內容中尋找符合篩選準則的上一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="7ee08-104">The **FindPreviousFrame** function finds the previous frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee08-105">語法</span><span class="sxs-lookup"><span data-stu-id="7ee08-105">Syntax</span></span>


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="7ee08-106">參數</span><span class="sxs-lookup"><span data-stu-id="7ee08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ee08-107">*hCurrentFrame*</span><span class="sxs-lookup"><span data-stu-id="7ee08-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee08-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7ee08-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="7ee08-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="7ee08-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee08-110">通訊協定名稱，例如 TCP。</span><span class="sxs-lookup"><span data-stu-id="7ee08-110">Protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="7ee08-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="7ee08-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee08-112">搜尋之框架的目的地位址。</span><span class="sxs-lookup"><span data-stu-id="7ee08-112">Destination address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="7ee08-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="7ee08-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee08-114">搜尋之框架的來源位址。</span><span class="sxs-lookup"><span data-stu-id="7ee08-114">Source address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="7ee08-115">*ProtocolOffset*</span><span class="sxs-lookup"><span data-stu-id="7ee08-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee08-116">接收通訊協定位移的 **單字** 指標。</span><span class="sxs-lookup"><span data-stu-id="7ee08-116">Pointer to a **WORD** that receives the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="7ee08-117">*OriginalFrameNumber*</span><span class="sxs-lookup"><span data-stu-id="7ee08-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee08-118">搜尋起點。</span><span class="sxs-lookup"><span data-stu-id="7ee08-118">Starting point of the search.</span></span> <span data-ttu-id="7ee08-119">根據預設，此函式會從 *OriginalFrameNumber* 起始點搜尋反向1000的畫面格。</span><span class="sxs-lookup"><span data-stu-id="7ee08-119">By default, this function searches backward 1,000 frames from *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="7ee08-120">您可以藉由將這一行新增至 Nmapi.ini 檔案（位於網路監視器目錄中），來變更搜尋後距離 \\ 。</span><span class="sxs-lookup"><span data-stu-id="7ee08-120">You can change the search-back distance by adding this line to the Nmapi.ini file, which is located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="7ee08-121">MAXLOOKBACK =<new lookback distance></span><span class="sxs-lookup"><span data-stu-id="7ee08-121">MAXLOOKBACK=<new lookback distance></span></span>

</dd> <dt>

<span data-ttu-id="7ee08-122">*LowestFrame*</span><span class="sxs-lookup"><span data-stu-id="7ee08-122">*LowestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee08-123">所搜尋之捕捉中的最小框架編號。</span><span class="sxs-lookup"><span data-stu-id="7ee08-123">Lowest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ee08-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ee08-124">Return value</span></span>

<span data-ttu-id="7ee08-125">如果函式成功，則傳回值會是上一個框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7ee08-125">If the function is successful, the return value is a handle to the previous frame.</span></span>

<span data-ttu-id="7ee08-126">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7ee08-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ee08-127">備註</span><span class="sxs-lookup"><span data-stu-id="7ee08-127">Remarks</span></span>

<span data-ttu-id="7ee08-128">Capture 篩選器主要是由 *ProtocolName* 所定義，這是唯一需要的篩選器輸入;您可以新增 *DestinationAddress* 和 *SourceAddress* 資訊來提高捕捉速度。</span><span class="sxs-lookup"><span data-stu-id="7ee08-128">The capture filter is defined primarily by *ProtocolName*, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* information to increase the capture speed.</span></span>

<span data-ttu-id="7ee08-129">*ProtocolOffset* 會傳回給呼叫剖析器，它會將此 **DWORD** 新增至透過 [ParserTemporaryLockFrame](parsertemporarylockframe.md)) 鎖定框架 (所傳回的指標，以取得所搜尋之通訊協定的 LPBYTE。</span><span class="sxs-lookup"><span data-stu-id="7ee08-129">*ProtocolOffset* is returned to the calling parser, which adds this **DWORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the LPBYTE of the protocol that is being searched for.</span></span> <span data-ttu-id="7ee08-130">傳回時，傳遞篩選器的 HFRAME 會提供給剖析器。</span><span class="sxs-lookup"><span data-stu-id="7ee08-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="7ee08-131">如果剖析器發現框架不是正在搜尋的框架，剖析器可以將這個 HFRAME 交給 **FindPreviousFrame** 函式，以取得下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="7ee08-131">If the parser finds that the frame is not the one that is being sought, the parser can hand this HFRAME back to the **FindPreviousFrame** function to retrieve the next frame.</span></span> <span data-ttu-id="7ee08-132">來源和目的地位址（非必要）可以傳入做為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7ee08-132">The source and destination addresses, which are not required, can be passed in as **NULL**.</span></span> <span data-ttu-id="7ee08-133">使用時，這些位址可以是類型的 \_ IP 位址 \_ ，而不只是 MAC 類型。</span><span class="sxs-lookup"><span data-stu-id="7ee08-133">When used, these addresses can be of type ADDRESS\_TYPE\_IP, and so on, not just MAC types.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee08-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ee08-134">Requirements</span></span>



| <span data-ttu-id="7ee08-135">需求</span><span class="sxs-lookup"><span data-stu-id="7ee08-135">Requirement</span></span> | <span data-ttu-id="7ee08-136">值</span><span class="sxs-lookup"><span data-stu-id="7ee08-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee08-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ee08-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7ee08-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ee08-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7ee08-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ee08-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7ee08-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ee08-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7ee08-141">標頭</span><span class="sxs-lookup"><span data-stu-id="7ee08-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ee08-142"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="7ee08-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7ee08-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ee08-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ee08-144"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ee08-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ee08-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7ee08-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ee08-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ee08-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




