---
description: LARGEINT 資料類型會定義大型 \_ 整數值。
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: 'LARGEINT (Netmon. h) '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967773"
---
# <a name="largeint"></a><span data-ttu-id="32e15-103">LARGEINT</span><span class="sxs-lookup"><span data-stu-id="32e15-103">LARGEINT</span></span>

<span data-ttu-id="32e15-104">**LARGEINT** 資料類型會定義 [**大型 \_ 整數**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)值。</span><span class="sxs-lookup"><span data-stu-id="32e15-104">The **LARGEINT** datatype defines a [**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) value.</span></span>


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a><span data-ttu-id="32e15-105">備註</span><span class="sxs-lookup"><span data-stu-id="32e15-105">Remarks</span></span>

<span data-ttu-id="32e15-106">[**Set**](set.md)結構的 **lpLargeIntTable** 成員會指向定義一個或多個 LARGEINT 值的 **集合** 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="32e15-106">The **lpLargeIntTable** member of the [**SET**](set.md) structure points to an array of **SET** structures that define one or more LARGEINT values.</span></span> <span data-ttu-id="32e15-107">當指定這種類型的 **集合** 結構時，網路監視器會顯示下列其中一個標籤，其中包含在通訊協定封包中找到的每個 LARGEINT 值。</span><span class="sxs-lookup"><span data-stu-id="32e15-107">When this type of **SET** structure is specified, Network Monitor displays one of the following labels with each LARGEINT value that it finds in the protocol packet.</span></span>

-   <span data-ttu-id="32e15-108">符合設定的值。</span><span class="sxs-lookup"><span data-stu-id="32e15-108">Matches set value.</span></span> <span data-ttu-id="32e15-109">LARGEINT 值會包含在集合中。</span><span class="sxs-lookup"><span data-stu-id="32e15-109">The LARGEINT value is included in the set.</span></span>
-   <span data-ttu-id="32e15-110">未知的設定值。</span><span class="sxs-lookup"><span data-stu-id="32e15-110">Unknown set value.</span></span> <span data-ttu-id="32e15-111">LARGEINT 值未包含在集合中。</span><span class="sxs-lookup"><span data-stu-id="32e15-111">The LARGEINT value is not included in the set.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e15-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="32e15-112">Requirements</span></span>



| <span data-ttu-id="32e15-113">需求</span><span class="sxs-lookup"><span data-stu-id="32e15-113">Requirement</span></span> | <span data-ttu-id="32e15-114">值</span><span class="sxs-lookup"><span data-stu-id="32e15-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="32e15-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32e15-115">Minimum supported client</span></span><br/> | <span data-ttu-id="32e15-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32e15-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="32e15-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32e15-117">Minimum supported server</span></span><br/> | <span data-ttu-id="32e15-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32e15-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="32e15-119">標頭</span><span class="sxs-lookup"><span data-stu-id="32e15-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="32e15-120"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="32e15-120"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e15-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32e15-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e15-122">SET</span><span class="sxs-lookup"><span data-stu-id="32e15-122">SET</span></span>](set.md)
</dt> </dl>

 

