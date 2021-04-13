---
description: 定義方法，此方法會決定是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。
title: IStorageProviderCopyHook 介面
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384402"
---
# <a name="istorageprovidercopyhook-interface"></a><span data-ttu-id="2837a-103">IStorageProviderCopyHook 介面</span><span class="sxs-lookup"><span data-stu-id="2837a-103">IStorageProviderCopyHook interface</span></span>

<span data-ttu-id="2837a-104">公開方法，這個方法會判斷是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="2837a-104">Exposes a method that determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="members"></a><span data-ttu-id="2837a-105">成員</span><span class="sxs-lookup"><span data-stu-id="2837a-105">Members</span></span>

<span data-ttu-id="2837a-106">**IStorageProviderCopyHook** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="2837a-106">The **IStorageProviderCopyHook** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2837a-107">**IStorageProviderCopyHook** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2837a-107">**IStorageProviderCopyHook** also has these types of members:</span></span>

- [<span data-ttu-id="2837a-108">方法</span><span class="sxs-lookup"><span data-stu-id="2837a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2837a-109">方法</span><span class="sxs-lookup"><span data-stu-id="2837a-109">Methods</span></span>

<span data-ttu-id="2837a-110">**IStorageProviderCopyHook** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2837a-110">The **IStorageProviderCopyHook** interface has these methods.</span></span>



| <span data-ttu-id="2837a-111">方法</span><span class="sxs-lookup"><span data-stu-id="2837a-111">Method</span></span>                                           | <span data-ttu-id="2837a-112">描述</span><span class="sxs-lookup"><span data-stu-id="2837a-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2837a-113">**CopyCallback**</span><span class="sxs-lookup"><span data-stu-id="2837a-113">**CopyCallback**</span></span>](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  <span data-ttu-id="2837a-114">決定是否允許 Shell 移動、複製、刪除或重新命名雲端提供者的同步根中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="2837a-114">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>                                                           |


## <a name="requirements"></a><span data-ttu-id="2837a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2837a-115">Requirements</span></span>

| <span data-ttu-id="2837a-116">需求</span><span class="sxs-lookup"><span data-stu-id="2837a-116">Requirement</span></span> | <span data-ttu-id="2837a-117">值</span><span class="sxs-lookup"><span data-stu-id="2837a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2837a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2837a-118">Minimum supported client</span></span> | <span data-ttu-id="2837a-119">Windows 10 Insider Preview 組建19624</span><span class="sxs-lookup"><span data-stu-id="2837a-119">Windows 10 Insider Preview Build 19624</span></span>                                                |
| <span data-ttu-id="2837a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2837a-120">Header</span></span><br/>                   | <span data-ttu-id="2837a-121">shobjidl.h。h</span><span class="sxs-lookup"><span data-stu-id="2837a-121">shobjidl.h</span></span>   |
