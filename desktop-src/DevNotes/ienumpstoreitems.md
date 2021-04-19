---
description: 提供 IPStore 介面的 COM 標準列舉方法。
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: 'IEnumPStoreItems 介面 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998391"
---
# <a name="ienumpstoreitems-interface"></a><span data-ttu-id="37ee3-103">IEnumPStoreItems 介面</span><span class="sxs-lookup"><span data-stu-id="37ee3-103">IEnumPStoreItems interface</span></span>

<span data-ttu-id="37ee3-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="37ee3-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="37ee3-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="37ee3-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="37ee3-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="37ee3-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="37ee3-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="37ee3-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="37ee3-108">提供 [**IPStore**](ipstore.md) 介面的 COM 標準列舉方法。</span><span class="sxs-lookup"><span data-stu-id="37ee3-108">Provides the COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="37ee3-109">成員</span><span class="sxs-lookup"><span data-stu-id="37ee3-109">Members</span></span>

<span data-ttu-id="37ee3-110">**IEnumPStoreItems** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="37ee3-110">The **IEnumPStoreItems** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="37ee3-111">**IEnumPStoreItems** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="37ee3-111">**IEnumPStoreItems** also has these types of members:</span></span>

-   [<span data-ttu-id="37ee3-112">方法</span><span class="sxs-lookup"><span data-stu-id="37ee3-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="37ee3-113">方法</span><span class="sxs-lookup"><span data-stu-id="37ee3-113">Methods</span></span>

<span data-ttu-id="37ee3-114">**IEnumPStoreItems** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="37ee3-114">The **IEnumPStoreItems** interface has these methods.</span></span>



| <span data-ttu-id="37ee3-115">方法</span><span class="sxs-lookup"><span data-stu-id="37ee3-115">Method</span></span>                                  | <span data-ttu-id="37ee3-116">描述</span><span class="sxs-lookup"><span data-stu-id="37ee3-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37ee3-117">**克隆**</span><span class="sxs-lookup"><span data-stu-id="37ee3-117">**Clone**</span></span>](ienumpstoreitems-clone.md) | <span data-ttu-id="37ee3-118">建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。</span><span class="sxs-lookup"><span data-stu-id="37ee3-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="37ee3-119">**下一步**</span><span class="sxs-lookup"><span data-stu-id="37ee3-119">**Next**</span></span>](ienumpstoreitems-next.md)   | <span data-ttu-id="37ee3-120">取得列舉順序中的下一個指定資料項目。</span><span class="sxs-lookup"><span data-stu-id="37ee3-120">Gets the next specified data item in the enumeration sequence.</span></span><br/>                          |
| [<span data-ttu-id="37ee3-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="37ee3-121">**Reset**</span></span>](ienumpstoreitems-reset.md) | <span data-ttu-id="37ee3-122">重設為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="37ee3-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="37ee3-123">**跳過**</span><span class="sxs-lookup"><span data-stu-id="37ee3-123">**Skip**</span></span>](ienumpstoreitems-skip.md)   | <span data-ttu-id="37ee3-124">略過列舉序列中指定的資料項目。</span><span class="sxs-lookup"><span data-stu-id="37ee3-124">Skips the specified data item in the enumeration sequence.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="37ee3-125">備註</span><span class="sxs-lookup"><span data-stu-id="37ee3-125">Remarks</span></span>

<span data-ttu-id="37ee3-126">列舉之後，必須釋放每個專案。</span><span class="sxs-lookup"><span data-stu-id="37ee3-126">It is necessary to free each item after enumerating it.</span></span> <span data-ttu-id="37ee3-127">當您不再使用列舉值物件時，也必須釋放它。</span><span class="sxs-lookup"><span data-stu-id="37ee3-127">The enumerator object must also be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="37ee3-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="37ee3-128">Requirements</span></span>



| <span data-ttu-id="37ee3-129">需求</span><span class="sxs-lookup"><span data-stu-id="37ee3-129">Requirement</span></span> | <span data-ttu-id="37ee3-130">值</span><span class="sxs-lookup"><span data-stu-id="37ee3-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37ee3-131">標頭</span><span class="sxs-lookup"><span data-stu-id="37ee3-131">Header</span></span><br/> | <dl> <span data-ttu-id="37ee3-132"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="37ee3-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="37ee3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="37ee3-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="37ee3-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37ee3-134"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
