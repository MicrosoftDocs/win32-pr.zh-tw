---
description: IEnumPStoreProviders 介面-提供 IPStore 介面的 COM 標準列舉方法。
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: 'IEnumPStoreProviders 介面 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089346"
---
# <a name="ienumpstoreproviders-interface"></a><span data-ttu-id="339cf-103">IEnumPStoreProviders 介面</span><span class="sxs-lookup"><span data-stu-id="339cf-103">IEnumPStoreProviders interface</span></span>

<span data-ttu-id="339cf-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="339cf-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="339cf-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="339cf-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="339cf-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="339cf-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="339cf-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="339cf-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="339cf-108">提供 [**IPStore**](ipstore.md) 介面的 COM 標準列舉方法。</span><span class="sxs-lookup"><span data-stu-id="339cf-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="339cf-109">成員</span><span class="sxs-lookup"><span data-stu-id="339cf-109">Members</span></span>

<span data-ttu-id="339cf-110">**IEnumPStoreProviders** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="339cf-110">The **IEnumPStoreProviders** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="339cf-111">**IEnumPStoreProviders** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="339cf-111">**IEnumPStoreProviders** also has these types of members:</span></span>

-   [<span data-ttu-id="339cf-112">方法</span><span class="sxs-lookup"><span data-stu-id="339cf-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="339cf-113">方法</span><span class="sxs-lookup"><span data-stu-id="339cf-113">Methods</span></span>

<span data-ttu-id="339cf-114">**IEnumPStoreProviders** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="339cf-114">The **IEnumPStoreProviders** interface has these methods.</span></span>



| <span data-ttu-id="339cf-115">方法</span><span class="sxs-lookup"><span data-stu-id="339cf-115">Method</span></span>                                      | <span data-ttu-id="339cf-116">描述</span><span class="sxs-lookup"><span data-stu-id="339cf-116">Description</span></span>                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="339cf-117">**克隆**</span><span class="sxs-lookup"><span data-stu-id="339cf-117">**Clone**</span></span>](ienumpstoreproviders-clone.md) | <span data-ttu-id="339cf-118">建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。</span><span class="sxs-lookup"><span data-stu-id="339cf-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="339cf-119">**下一步**</span><span class="sxs-lookup"><span data-stu-id="339cf-119">**Next**</span></span>](ienumpstoreproviders-next.md)   | <span data-ttu-id="339cf-120">取得列舉順序中的下一個指定提供者。</span><span class="sxs-lookup"><span data-stu-id="339cf-120">Gets the next specified provider in the enumeration sequence.</span></span><br/>                           |
| [<span data-ttu-id="339cf-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="339cf-121">**Reset**</span></span>](ienumpstoreproviders-reset.md) | <span data-ttu-id="339cf-122">重設為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="339cf-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="339cf-123">**跳過**</span><span class="sxs-lookup"><span data-stu-id="339cf-123">**Skip**</span></span>](ienumpstoreproviders-skip.md)   | <span data-ttu-id="339cf-124">略過列舉序列中指定的提供者。</span><span class="sxs-lookup"><span data-stu-id="339cf-124">Skips the specified provider in the enumeration sequence.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="339cf-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="339cf-125">Requirements</span></span>



| <span data-ttu-id="339cf-126">需求</span><span class="sxs-lookup"><span data-stu-id="339cf-126">Requirement</span></span> | <span data-ttu-id="339cf-127">值</span><span class="sxs-lookup"><span data-stu-id="339cf-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="339cf-128">標頭</span><span class="sxs-lookup"><span data-stu-id="339cf-128">Header</span></span><br/> | <dl> <span data-ttu-id="339cf-129"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="339cf-129"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="339cf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="339cf-130">DLL</span></span><br/>    | <dl> <span data-ttu-id="339cf-131"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="339cf-131"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
