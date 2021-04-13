---
description: 在填充碼資料庫中包含專案和其標記資訊的索引。
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8631811f101850b68bdbad1097c19b9a41737bd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510449"
---
# <a name="tagref"></a><span data-ttu-id="da93f-103">TAGREF</span><span class="sxs-lookup"><span data-stu-id="da93f-103">TAGREF</span></span>

<span data-ttu-id="da93f-104">在填充碼資料庫中包含專案和其標記資訊的索引。</span><span class="sxs-lookup"><span data-stu-id="da93f-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="da93f-105">備註</span><span class="sxs-lookup"><span data-stu-id="da93f-105">Remarks</span></span>

<span data-ttu-id="da93f-106">**TAGREF** 適用于填充碼資料庫，且在多個資料庫中都是有效的。</span><span class="sxs-lookup"><span data-stu-id="da93f-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="da93f-107">它可以是代表索引的整數值，也可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="da93f-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="da93f-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ Null (0) </span><span class="sxs-lookup"><span data-stu-id="da93f-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="da93f-109">**TAGREF** 不存在。</span><span class="sxs-lookup"><span data-stu-id="da93f-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="da93f-110">當函數無法傳回有效的 **TAGREF** 時，就會從該函式傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="da93f-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="da93f-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF \_ ROOT (0) </span><span class="sxs-lookup"><span data-stu-id="da93f-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="da93f-112">表示根清單標記，可用來做為取得子 **TAGREF** 的父系。</span><span class="sxs-lookup"><span data-stu-id="da93f-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da93f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="da93f-113">Requirements</span></span>



| <span data-ttu-id="da93f-114">需求</span><span class="sxs-lookup"><span data-stu-id="da93f-114">Requirement</span></span> | <span data-ttu-id="da93f-115">值</span><span class="sxs-lookup"><span data-stu-id="da93f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da93f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da93f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="da93f-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da93f-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da93f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da93f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="da93f-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da93f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da93f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da93f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da93f-121">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="da93f-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="da93f-122">**標記**</span><span class="sxs-lookup"><span data-stu-id="da93f-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="da93f-123">標記類型</span><span class="sxs-lookup"><span data-stu-id="da93f-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="da93f-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="da93f-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




