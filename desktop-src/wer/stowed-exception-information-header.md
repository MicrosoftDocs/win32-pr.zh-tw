---
title: STOWED_EXCEPTION_INFORMATION_HEADER 結構
description: 包含識別父結構的資訊。
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- STOWED_EXCEPTION_INFORMATION_HEADER 結構 Windows 錯誤報告
- PSTOWED_EXCEPTION_INFORMATION_HEADER 結構指標 Windows 錯誤報告
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025404"
---
# <a name="stowed_exception_information_header-structure"></a><span data-ttu-id="ce119-105">STOWED \_ 例外狀況 \_ 資訊 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="ce119-105">STOWED\_EXCEPTION\_INFORMATION\_HEADER structure</span></span>

<span data-ttu-id="ce119-106">包含識別父結構的資訊。</span><span class="sxs-lookup"><span data-stu-id="ce119-106">Contains info that identifies the parent structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce119-107">語法</span><span class="sxs-lookup"><span data-stu-id="ce119-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a><span data-ttu-id="ce119-108">成員</span><span class="sxs-lookup"><span data-stu-id="ce119-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce119-109">**大小**</span><span class="sxs-lookup"><span data-stu-id="ce119-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="ce119-110">類型： **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce119-110">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ce119-111">父結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce119-111">Size, in bytes, of the parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce119-112">**簽名**</span><span class="sxs-lookup"><span data-stu-id="ce119-112">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="ce119-113">類型： **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce119-113">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="ce119-114">指定父結構簽章的32位值。</span><span class="sxs-lookup"><span data-stu-id="ce119-114">A 32-bit value that specifies the signature of the parent structure.</span></span>



| <span data-ttu-id="ce119-115">值</span><span class="sxs-lookup"><span data-stu-id="ce119-115">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="ce119-116">意義</span><span class="sxs-lookup"><span data-stu-id="ce119-116">Meaning</span></span>                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <span data-ttu-id="ce119-117"><dt>**STOWED \_例外狀況 \_ 資訊 \_ V1 \_ 簽名碼**</dt> <dt>' SE01 '</dt></span><span class="sxs-lookup"><span data-stu-id="ce119-117"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V1\_SIGNATURE**</dt> <dt>'SE01'</dt></span></span> </dl> | <span data-ttu-id="ce119-118">這個值表示父系是 **STOWED \_ 例外狀況 \_ 資訊 \_ V1** 結構。</span><span class="sxs-lookup"><span data-stu-id="ce119-118">This value indicates that the parent is a **STOWED\_EXCEPTION\_INFORMATION\_V1** structure.</span></span><br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <span data-ttu-id="ce119-119"><dt>**STOWED \_例外狀況 \_ 資訊 \_ V2 \_ 簽名碼**</dt> <dt>' SE02 '</dt></span><span class="sxs-lookup"><span data-stu-id="ce119-119"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V2\_SIGNATURE**</dt> <dt>'SE02'</dt></span></span> </dl> | <span data-ttu-id="ce119-120">這個值表示父系是 [**STOWED \_ 例外狀況 \_ 資訊 \_ V2**](stowed-exception-information-v2.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="ce119-120">This value indicates that the parent is a [**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) structure.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce119-121">備註</span><span class="sxs-lookup"><span data-stu-id="ce119-121">Remarks</span></span>

<span data-ttu-id="ce119-122">[**STOWED \_例外狀況 \_ 資訊 \_ V2**](stowed-exception-information-v2.md) 和 **STOWED 例外狀況 \_ \_ 資訊 \_ 標頭** 目前未定義于可公開取得的標頭中，因此您必須先在原始程式碼中定義它們，然後才能使用它們。</span><span class="sxs-lookup"><span data-stu-id="ce119-122">[**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) and **STOWED\_EXCEPTION\_INFORMATION\_HEADER** currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="ce119-123">**STOWED \_ 例外狀況 \_ 資訊 \_ V1** 結構與此結構相同，但不包含 **NestedExceptionType** 和 **NestedException** 成員。</span><span class="sxs-lookup"><span data-stu-id="ce119-123">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce119-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce119-124">Requirements</span></span>



| <span data-ttu-id="ce119-125">需求</span><span class="sxs-lookup"><span data-stu-id="ce119-125">Requirement</span></span> | <span data-ttu-id="ce119-126">值</span><span class="sxs-lookup"><span data-stu-id="ce119-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="ce119-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce119-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ce119-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce119-128">Windows 8 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ce119-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce119-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ce119-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce119-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ce119-131">標頭</span><span class="sxs-lookup"><span data-stu-id="ce119-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce119-132"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="ce119-132"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce119-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce119-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce119-134">**STOWED \_ 例外狀況 \_ 資訊 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="ce119-134">**STOWED\_EXCEPTION\_INFORMATION\_V2**</span></span>](stowed-exception-information-v2.md)
</dt> </dl>

 

