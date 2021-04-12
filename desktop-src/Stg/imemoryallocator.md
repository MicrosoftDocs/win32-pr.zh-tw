---
title: IMemoryAllocator 類別
description: 由 StgConvertPropertyToVariant 函式的記憶體配置器所執行。
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- IMemoryAllocator 類別結構化儲存體
- IMemoryAllocator 類別結構化儲存體，描述
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384765"
---
# <a name="imemoryallocator-class"></a><span data-ttu-id="a0aef-105">IMemoryAllocator 類別</span><span class="sxs-lookup"><span data-stu-id="a0aef-105">IMemoryAllocator class</span></span>

<span data-ttu-id="a0aef-106">**IMemoryAllocator** 類別是由 [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant)函數的記憶體配置器所執行。</span><span class="sxs-lookup"><span data-stu-id="a0aef-106">The **IMemoryAllocator** class is implemented by the memory allocator for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="methods"></a><span data-ttu-id="a0aef-107">方法</span><span class="sxs-lookup"><span data-stu-id="a0aef-107">Methods</span></span>



| <span data-ttu-id="a0aef-108">名稱</span><span class="sxs-lookup"><span data-stu-id="a0aef-108">Name</span></span>                                                     | <span data-ttu-id="a0aef-109">描述</span><span class="sxs-lookup"><span data-stu-id="a0aef-109">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0aef-110">**分配**</span><span class="sxs-lookup"><span data-stu-id="a0aef-110">**Allocate**</span></span>](imemoryallocator-allocate.md)<br/> | <span data-ttu-id="a0aef-111">當函數將 **SERIALIZEDPROPERTYVALUE** 資料類型轉換成 **PROPVARIANT** 資料類型時，為 [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant)函數配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="a0aef-111">Allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span><br/> |
| [<span data-ttu-id="a0aef-112">**免費**</span><span class="sxs-lookup"><span data-stu-id="a0aef-112">**Free**</span></span>](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | <span data-ttu-id="a0aef-113">釋放由 [**配置方法配置**](imemoryallocator-allocate.md) 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a0aef-113">Frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span><br/>                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="a0aef-114">備註</span><span class="sxs-lookup"><span data-stu-id="a0aef-114">Remarks</span></span>

<span data-ttu-id="a0aef-115">只有 [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) 函式會使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="a0aef-115">This class is only used by the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0aef-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0aef-116">Requirements</span></span>



| <span data-ttu-id="a0aef-117">需求</span><span class="sxs-lookup"><span data-stu-id="a0aef-117">Requirement</span></span> | <span data-ttu-id="a0aef-118">值</span><span class="sxs-lookup"><span data-stu-id="a0aef-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a0aef-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0aef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a0aef-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0aef-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a0aef-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0aef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a0aef-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0aef-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a0aef-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="a0aef-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0aef-124"><dt>Ole32.lib .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0aef-124"><dt>Ole32.lib</dt></span></span> </dl> |



 

