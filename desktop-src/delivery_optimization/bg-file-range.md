---
title: 'BG_FILE_RANGE 結構 (>deliveryoptimization .h) '
description: BG_FILE_RANGE 結構會識別要從檔案下載的位元組範圍。
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- BG_FILE_RANGE 結構
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385093"
---
# <a name="bg_file_range-structure"></a><span data-ttu-id="371b2-104">BG_FILE_RANGE 結構</span><span class="sxs-lookup"><span data-stu-id="371b2-104">BG_FILE_RANGE structure</span></span>

<span data-ttu-id="371b2-105">**BG_FILE_RANGE** 結構會識別要從檔案下載的位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="371b2-105">The **BG_FILE_RANGE** structure identifies a range of bytes to download from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="371b2-106">語法</span><span class="sxs-lookup"><span data-stu-id="371b2-106">Syntax</span></span>


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a><span data-ttu-id="371b2-107">成員</span><span class="sxs-lookup"><span data-stu-id="371b2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="371b2-108">**InitialOffset**</span><span class="sxs-lookup"><span data-stu-id="371b2-108">**InitialOffset**</span></span>
</dt> <dd>

<span data-ttu-id="371b2-109">從檔案下載的位元組範圍開頭以零為基底的位移。</span><span class="sxs-lookup"><span data-stu-id="371b2-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

</dd> <dt>

<span data-ttu-id="371b2-110">**長度**</span><span class="sxs-lookup"><span data-stu-id="371b2-110">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="371b2-111">範圍的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="371b2-111">The length of the range, in bytes.</span></span> <span data-ttu-id="371b2-112">請勿指定零位元組長度。</span><span class="sxs-lookup"><span data-stu-id="371b2-112">Do not specify a zero byte length.</span></span> <span data-ttu-id="371b2-113">若要指出範圍延伸至檔案結尾，請指定 **BG_LENGTH_TO_EOF**。</span><span class="sxs-lookup"><span data-stu-id="371b2-113">To indicate that the range extends to the end of the file, specify **BG_LENGTH_TO_EOF**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="371b2-114">備註</span><span class="sxs-lookup"><span data-stu-id="371b2-114">Remarks</span></span>

<span data-ttu-id="371b2-115">範圍必須存在於檔案中，否則會產生 **DO_E_INVALID_RANGE** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="371b2-115">The range must exist in the file or DO generates an **DO_E_INVALID_RANGE** error.</span></span>

## <a name="requirements"></a><span data-ttu-id="371b2-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="371b2-116">Requirements</span></span>



| <span data-ttu-id="371b2-117">需求</span><span class="sxs-lookup"><span data-stu-id="371b2-117">Requirement</span></span> | <span data-ttu-id="371b2-118">值</span><span class="sxs-lookup"><span data-stu-id="371b2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="371b2-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="371b2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="371b2-120">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="371b2-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="371b2-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="371b2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="371b2-122">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="371b2-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="371b2-123">標頭</span><span class="sxs-lookup"><span data-stu-id="371b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="371b2-124"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="371b2-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="371b2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="371b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="371b2-126">**IBackgroundCopyFile2::GetFileRanges**</span><span class="sxs-lookup"><span data-stu-id="371b2-126">**IBackgroundCopyFile2::GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





