---
description: 深入瞭解： EtwEventWrite 函數
title: EtwEventWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 149f611dfb298749befca805509e05fa2dec497a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025968"
---
# <a name="etweventwrite-function"></a><span data-ttu-id="e43ee-103">EtwEventWrite 函式</span><span class="sxs-lookup"><span data-stu-id="e43ee-103">EtwEventWrite function</span></span>

<span data-ttu-id="e43ee-104">[EtwEventWrite 函式和它所傳回的結構是作業系統的內部，而且可能會從某個 Windows 版本變更為另一個版本。]</span><span class="sxs-lookup"><span data-stu-id="e43ee-104">[The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="e43ee-105">將基本事件寫入至會話。</span><span class="sxs-lookup"><span data-stu-id="e43ee-105">Writes a basic event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="e43ee-106">語法</span><span class="sxs-lookup"><span data-stu-id="e43ee-106">Syntax</span></span>

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="e43ee-107">參數</span><span class="sxs-lookup"><span data-stu-id="e43ee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e43ee-108">*RegHandle*</span><span class="sxs-lookup"><span data-stu-id="e43ee-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="e43ee-109">提供者的 RegHandle。</span><span class="sxs-lookup"><span data-stu-id="e43ee-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="e43ee-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="e43ee-110">*EventDescriptor*</span></span>
</dt> <dd>

<span data-ttu-id="e43ee-111">要記錄之事件的事件描述項。</span><span class="sxs-lookup"><span data-stu-id="e43ee-111">Event descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="e43ee-112">*UserDataCount*</span><span class="sxs-lookup"><span data-stu-id="e43ee-112">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="e43ee-113">使用者資料項目數目。</span><span class="sxs-lookup"><span data-stu-id="e43ee-113">Number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="e43ee-114">*UserData*</span><span class="sxs-lookup"><span data-stu-id="e43ee-114">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="e43ee-115">使用者資料項目陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="e43ee-115">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e43ee-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e43ee-116">Return value</span></span>

<span data-ttu-id="e43ee-117">Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e43ee-117">A Win32 error code.</span></span>


## <a name="remarks"></a><span data-ttu-id="e43ee-118">備註</span><span class="sxs-lookup"><span data-stu-id="e43ee-118">Remarks</span></span>

<span data-ttu-id="e43ee-119">EtwEventWrite 函式和它所傳回的結構是作業系統的內部，而且可能會從某個 Windows 版本變更為另一個。</span><span class="sxs-lookup"><span data-stu-id="e43ee-119">The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="e43ee-120">若要維持應用程式的相容性，最好改為使用公用函數。</span><span class="sxs-lookup"><span data-stu-id="e43ee-120">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="e43ee-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e43ee-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e43ee-122">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="e43ee-122">**Target Platform**</span></span> | <span data-ttu-id="e43ee-123">Windows</span><span class="sxs-lookup"><span data-stu-id="e43ee-123">Windows</span></span> |
| <span data-ttu-id="e43ee-124">**標頭**</span><span class="sxs-lookup"><span data-stu-id="e43ee-124">**Header**</span></span> | <span data-ttu-id="e43ee-125">ntetw。h</span><span class="sxs-lookup"><span data-stu-id="e43ee-125">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="e43ee-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e43ee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e43ee-127">EventWrite</span><span class="sxs-lookup"><span data-stu-id="e43ee-127">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="e43ee-128">EventWriteEx</span><span class="sxs-lookup"><span data-stu-id="e43ee-128">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
