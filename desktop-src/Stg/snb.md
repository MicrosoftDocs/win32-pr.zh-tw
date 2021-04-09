---
title: 'SNB (Objidl.idl) '
description: 字串名稱區塊 (SNB) 是指向字串指標陣列的指標，而這些指標是以 Null 指標結尾。
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- 瑞士 央行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934148"
---
# <a name="snb"></a><span data-ttu-id="c9051-104">瑞士 央行</span><span class="sxs-lookup"><span data-stu-id="c9051-104">SNB</span></span>

<span data-ttu-id="c9051-105">字串名稱區塊 (**SNB**) 是指向字串指標陣列的指標，而這些指標是以 **Null** 指標結尾。</span><span class="sxs-lookup"><span data-stu-id="c9051-105">A string name block (**SNB**) is a pointer to an array of pointers to strings, that ends in a **NULL** pointer.</span></span> <span data-ttu-id="c9051-106">[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)介面和開啟儲存體物件的函式呼叫會使用字串名稱區塊。</span><span class="sxs-lookup"><span data-stu-id="c9051-106">String name blocks are used by the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and by function calls that open storage objects.</span></span> <span data-ttu-id="c9051-107">字串指向所包含的儲存物件或要在開啟的呼叫中排除的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c9051-107">The strings point to contained storage objects or streams that are to be excluded in the open calls.</span></span>


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

<span data-ttu-id="c9051-108">**瑞士 央行**</span><span class="sxs-lookup"><span data-stu-id="c9051-108">**SNB**</span></span>
</dt> <dd>

<span data-ttu-id="c9051-109">\[\_ (wireSNB) 的有線封送處理\]</span><span class="sxs-lookup"><span data-stu-id="c9051-109">\[wire\_marshal(wireSNB)\]</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9051-110">備註</span><span class="sxs-lookup"><span data-stu-id="c9051-110">Remarks</span></span>

<span data-ttu-id="c9051-111">**SNB** 的建立方式是配置連續的記憶體區塊，其中字串的指標後面接著 **Null** 指標，後面接著實際的字串。</span><span class="sxs-lookup"><span data-stu-id="c9051-111">The **SNB** should be created by allocating a contiguous block of memory in which the pointers to strings are followed by a **NULL** pointer, which is then followed by the actual strings.</span></span>

<span data-ttu-id="c9051-112">**SNB** 的封送處理是以這種方式建立的 **SNB** 為基礎。</span><span class="sxs-lookup"><span data-stu-id="c9051-112">The marshaling of an **SNB** is based on the assumption that the **SNB** that was passed in was created in this way.</span></span> <span data-ttu-id="c9051-113">雖然可以透過其他方式來儲存，但以這種方式建立的 **SNB** 有一個優點，就是只需要一個配置作業和一個釋出記憶體給所有字串。</span><span class="sxs-lookup"><span data-stu-id="c9051-113">Although it could be stored in other ways, the **SNB** created in this manner has the advantage of requiring only one allocation operation and one freeing of memory for all the strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9051-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9051-114">Requirements</span></span>



| <span data-ttu-id="c9051-115">需求</span><span class="sxs-lookup"><span data-stu-id="c9051-115">Requirement</span></span> | <span data-ttu-id="c9051-116">值</span><span class="sxs-lookup"><span data-stu-id="c9051-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9051-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9051-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c9051-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9051-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c9051-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9051-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c9051-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9051-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c9051-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c9051-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9051-122"><dt>Objidl.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9051-122"><dt>Objidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9051-123">Idl</span><span class="sxs-lookup"><span data-stu-id="c9051-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9051-124"><dt>Objidl.idl .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9051-124"><dt>Objidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9051-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9051-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9051-126">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="c9051-126">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





