---
description: 傳回框架中指定之通訊協定的位移。
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: 'GetProtocolStartOffset 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973217"
---
# <a name="getprotocolstartoffset-function"></a><span data-ttu-id="61b24-103">GetProtocolStartOffset 函式</span><span class="sxs-lookup"><span data-stu-id="61b24-103">GetProtocolStartOffset function</span></span>

<span data-ttu-id="61b24-104">**GetProtocolStartOffset** 函式會傳回框架中指定之通訊協定的位移。</span><span class="sxs-lookup"><span data-stu-id="61b24-104">The **GetProtocolStartOffset** function returns the offset of a specified protocol in the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b24-105">語法</span><span class="sxs-lookup"><span data-stu-id="61b24-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="61b24-106">參數</span><span class="sxs-lookup"><span data-stu-id="61b24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61b24-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="61b24-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="61b24-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="61b24-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="61b24-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="61b24-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="61b24-110">通訊協定名稱，例如 TCP。</span><span class="sxs-lookup"><span data-stu-id="61b24-110">The Protocol name, such as TCP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61b24-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="61b24-111">Return value</span></span>

<span data-ttu-id="61b24-112">如果函式成功，則傳回值會是要搜尋的通訊協定開頭的 **DWORD** 位移，表示通訊協定是框架中的第一個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="61b24-112">If the function is successful, the return value is a **DWORD** offset to the beginning of the protocol being searched for   a return value of zero indicates the protocol is the first protocol in the frame.</span></span>

<span data-ttu-id="61b24-113">如果函式不成功，則此通訊協定不在框架中，傳回值為-1。</span><span class="sxs-lookup"><span data-stu-id="61b24-113">If the function is unsuccessful, the protocol is not in the frame, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="61b24-114">備註</span><span class="sxs-lookup"><span data-stu-id="61b24-114">Remarks</span></span>

<span data-ttu-id="61b24-115">當提供框架的控制碼時，此函式會傳回框架中指定之通訊協定的位移。</span><span class="sxs-lookup"><span data-stu-id="61b24-115">When given the handle to a frame, this function returns the offset to a specified protocol in the frame.</span></span> <span data-ttu-id="61b24-116">例如，若要判斷框架是否為 DNS 框架，DNS 剖析器需要 TCP 通訊協定的埠位址。</span><span class="sxs-lookup"><span data-stu-id="61b24-116">For example, to determine whether the frame is a DNS frame, the DNS parser requires the port address of the TCP protocol.</span></span> <span data-ttu-id="61b24-117">DNS 剖析器會以 TCP 作為 *ProtocolName* 值來呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="61b24-117">The DNS parser would call this function with TCP as the *ProtocolName* value.</span></span> <span data-ttu-id="61b24-118">如果 TCP 通訊協定可以辨識框架，則會傳回從框架開頭到 TCP 框架開頭的 **單字** 位移。</span><span class="sxs-lookup"><span data-stu-id="61b24-118">If the frame is recognized by the TCP protocol, the **WORD** offset from the beginning of the frame to the beginning of the TCP frame is returned.</span></span> <span data-ttu-id="61b24-119">如果沒有 TCP 通訊協定，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="61b24-119">If there is no TCP protocol, the return value is zero.</span></span>

<span data-ttu-id="61b24-120">此函數會尋找框架中的通訊協定開頭。</span><span class="sxs-lookup"><span data-stu-id="61b24-120">This function finds the beginning of a protocol in a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b24-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="61b24-121">Requirements</span></span>



| <span data-ttu-id="61b24-122">需求</span><span class="sxs-lookup"><span data-stu-id="61b24-122">Requirement</span></span> | <span data-ttu-id="61b24-123">值</span><span class="sxs-lookup"><span data-stu-id="61b24-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="61b24-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61b24-124">Minimum supported client</span></span><br/> | <span data-ttu-id="61b24-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61b24-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="61b24-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61b24-126">Minimum supported server</span></span><br/> | <span data-ttu-id="61b24-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61b24-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="61b24-128">標頭</span><span class="sxs-lookup"><span data-stu-id="61b24-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="61b24-129"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="61b24-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="61b24-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="61b24-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="61b24-131"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="61b24-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="61b24-132">DLL</span><span class="sxs-lookup"><span data-stu-id="61b24-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61b24-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61b24-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




