---
description: 在填充碼資料庫中包含專案和其標記資訊的索引。
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936161"
---
# <a name="tagid"></a><span data-ttu-id="cff6a-103">TAGID</span><span class="sxs-lookup"><span data-stu-id="cff6a-103">TAGID</span></span>

<span data-ttu-id="cff6a-104">在填充碼資料庫中包含專案和其標記資訊的索引。</span><span class="sxs-lookup"><span data-stu-id="cff6a-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a><span data-ttu-id="cff6a-105">備註</span><span class="sxs-lookup"><span data-stu-id="cff6a-105">Remarks</span></span>

<span data-ttu-id="cff6a-106">**TAGID** 是資料庫特有的。</span><span class="sxs-lookup"><span data-stu-id="cff6a-106">A **TAGID** is specific to a database.</span></span> <span data-ttu-id="cff6a-107">它可以是代表索引的整數值，也可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="cff6a-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="cff6a-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ Null (0) </span><span class="sxs-lookup"><span data-stu-id="cff6a-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="cff6a-109">**TAGID** 不存在。</span><span class="sxs-lookup"><span data-stu-id="cff6a-109">The **TAGID** does not exist.</span></span> <span data-ttu-id="cff6a-110">當函數無法傳回有效的 **TAGID** 時，就會從該函式傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="cff6a-110">This value is returned from a function when it cannot return a valid **TAGID**.</span></span>

</dd> <dt>

<span data-ttu-id="cff6a-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID \_ ROOT (0) </span><span class="sxs-lookup"><span data-stu-id="cff6a-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="cff6a-112">表示根清單標記，可用來做為取得子 **TAGID** 的父系。</span><span class="sxs-lookup"><span data-stu-id="cff6a-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cff6a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cff6a-113">Requirements</span></span>



| <span data-ttu-id="cff6a-114">需求</span><span class="sxs-lookup"><span data-stu-id="cff6a-114">Requirement</span></span> | <span data-ttu-id="cff6a-115">值</span><span class="sxs-lookup"><span data-stu-id="cff6a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cff6a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cff6a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cff6a-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cff6a-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cff6a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cff6a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cff6a-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cff6a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cff6a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cff6a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff6a-121">**標記**</span><span class="sxs-lookup"><span data-stu-id="cff6a-121">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="cff6a-122">標記類型</span><span class="sxs-lookup"><span data-stu-id="cff6a-122">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="cff6a-123">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="cff6a-123">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




