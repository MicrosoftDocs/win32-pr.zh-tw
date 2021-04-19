---
description: 提供 IPStore 介面的 COM 標準列舉方法。
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: 'IEnumPStoreTypes 介面 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 748f6e21701fdd27c2a88d1959b0b29cf56929f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000951"
---
# <a name="ienumpstoretypes-interface"></a><span data-ttu-id="46515-103">IEnumPStoreTypes 介面</span><span class="sxs-lookup"><span data-stu-id="46515-103">IEnumPStoreTypes interface</span></span>

<span data-ttu-id="46515-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="46515-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="46515-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="46515-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="46515-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="46515-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="46515-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="46515-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="46515-108">提供 [**IPStore**](ipstore.md) 介面的 COM 標準列舉方法。</span><span class="sxs-lookup"><span data-stu-id="46515-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="46515-109">成員</span><span class="sxs-lookup"><span data-stu-id="46515-109">Members</span></span>

<span data-ttu-id="46515-110">**IEnumPStoreTypes** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="46515-110">The **IEnumPStoreTypes** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="46515-111">**IEnumPStoreTypes** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="46515-111">**IEnumPStoreTypes** also has these types of members:</span></span>

-   [<span data-ttu-id="46515-112">方法</span><span class="sxs-lookup"><span data-stu-id="46515-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="46515-113">方法</span><span class="sxs-lookup"><span data-stu-id="46515-113">Methods</span></span>

<span data-ttu-id="46515-114">**IEnumPStoreTypes** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="46515-114">The **IEnumPStoreTypes** interface has these methods.</span></span>



| <span data-ttu-id="46515-115">方法</span><span class="sxs-lookup"><span data-stu-id="46515-115">Method</span></span>                                  | <span data-ttu-id="46515-116">描述</span><span class="sxs-lookup"><span data-stu-id="46515-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46515-117">**克隆**</span><span class="sxs-lookup"><span data-stu-id="46515-117">**Clone**</span></span>](ienumpstoretypes-clone.md) | <span data-ttu-id="46515-118">建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。</span><span class="sxs-lookup"><span data-stu-id="46515-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="46515-119">**下一步**</span><span class="sxs-lookup"><span data-stu-id="46515-119">**Next**</span></span>](ienumpstoretypes-next.md)   | <span data-ttu-id="46515-120">取得列舉順序中的下一個指定提供者類型。</span><span class="sxs-lookup"><span data-stu-id="46515-120">Gets the next specified provider type in the enumeration sequence.</span></span><br/>                      |
| [<span data-ttu-id="46515-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="46515-121">**Reset**</span></span>](ienumpstoretypes-reset.md) | <span data-ttu-id="46515-122">重設為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="46515-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="46515-123">**跳過**</span><span class="sxs-lookup"><span data-stu-id="46515-123">**Skip**</span></span>](ienumpstoretypes-skip.md)   | <span data-ttu-id="46515-124">略過列舉序列中指定的提供者類型。</span><span class="sxs-lookup"><span data-stu-id="46515-124">Skips the specified provider type in the enumeration sequence.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="46515-125">備註</span><span class="sxs-lookup"><span data-stu-id="46515-125">Remarks</span></span>

<span data-ttu-id="46515-126">當列舉值物件不再使用時，必須釋放它。</span><span class="sxs-lookup"><span data-stu-id="46515-126">The enumerator object must be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="46515-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="46515-127">Requirements</span></span>



| <span data-ttu-id="46515-128">需求</span><span class="sxs-lookup"><span data-stu-id="46515-128">Requirement</span></span> | <span data-ttu-id="46515-129">值</span><span class="sxs-lookup"><span data-stu-id="46515-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46515-130">標頭</span><span class="sxs-lookup"><span data-stu-id="46515-130">Header</span></span><br/> | <dl> <span data-ttu-id="46515-131"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="46515-131"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="46515-132">DLL</span><span class="sxs-lookup"><span data-stu-id="46515-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="46515-133"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46515-133"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
