---
title: IDWriteFont2 介面
description: 代表字型集合中的實體字型。
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- IDWriteFont2 介面直接寫入
- IDWriteFont2 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a47e56915747b0e118a6f63484b9dd3dcdbd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317312"
---
# <a name="idwritefont2-interface"></a><span data-ttu-id="353e8-105">IDWriteFont2 介面</span><span class="sxs-lookup"><span data-stu-id="353e8-105">IDWriteFont2 interface</span></span>

<span data-ttu-id="353e8-106">代表字型集合中的實體字型。</span><span class="sxs-lookup"><span data-stu-id="353e8-106">Represents a physical font in a font collection.</span></span>

<span data-ttu-id="353e8-107">這個介面會新增檢查色彩轉譯路徑是否可能需要的功能。</span><span class="sxs-lookup"><span data-stu-id="353e8-107">This interface adds the ability to check if a color rendering path is potentially necessary.</span></span>

## <a name="members"></a><span data-ttu-id="353e8-108">成員</span><span class="sxs-lookup"><span data-stu-id="353e8-108">Members</span></span>

<span data-ttu-id="353e8-109">**IDWriteFont2** 介面繼承自 [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)。</span><span class="sxs-lookup"><span data-stu-id="353e8-109">The **IDWriteFont2** interface inherits from [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1).</span></span> <span data-ttu-id="353e8-110">**IDWriteFont2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="353e8-110">**IDWriteFont2** also has these types of members:</span></span>

-   [<span data-ttu-id="353e8-111">方法</span><span class="sxs-lookup"><span data-stu-id="353e8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="353e8-112">方法</span><span class="sxs-lookup"><span data-stu-id="353e8-112">Methods</span></span>

<span data-ttu-id="353e8-113">**IDWriteFont2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="353e8-113">The **IDWriteFont2** interface has these methods.</span></span>



| <span data-ttu-id="353e8-114">方法</span><span class="sxs-lookup"><span data-stu-id="353e8-114">Method</span></span>                                          | <span data-ttu-id="353e8-115">描述</span><span class="sxs-lookup"><span data-stu-id="353e8-115">Description</span></span>                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="353e8-116">**IsColorFont**</span><span class="sxs-lookup"><span data-stu-id="353e8-116">**IsColorFont**</span></span>](idwritefont2-iscolorfont.md) | <span data-ttu-id="353e8-117">可判斷是否有可能需要色彩轉譯路徑。</span><span class="sxs-lookup"><span data-stu-id="353e8-117">Enables determining if a color rendering path is potentially necessary.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="353e8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="353e8-118">Requirements</span></span>



| <span data-ttu-id="353e8-119">需求</span><span class="sxs-lookup"><span data-stu-id="353e8-119">Requirement</span></span> | <span data-ttu-id="353e8-120">值</span><span class="sxs-lookup"><span data-stu-id="353e8-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="353e8-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="353e8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="353e8-122">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="353e8-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="353e8-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="353e8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="353e8-124">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="353e8-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="353e8-125">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="353e8-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="353e8-126">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="353e8-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="353e8-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="353e8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="353e8-128"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="353e8-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="353e8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="353e8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="353e8-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="353e8-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="353e8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="353e8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="353e8-132">**IDWriteFont1**</span><span class="sxs-lookup"><span data-stu-id="353e8-132">**IDWriteFont1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

