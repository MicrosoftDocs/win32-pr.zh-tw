---
description: 擴充 ITablet 介面。
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: ITablet2 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980619"
---
# <a name="itablet2-interface"></a><span data-ttu-id="95601-103">ITablet2 介面</span><span class="sxs-lookup"><span data-stu-id="95601-103">ITablet2 interface</span></span>

<span data-ttu-id="95601-104">擴充 [**ITablet 介面**](itablet.md)。</span><span class="sxs-lookup"><span data-stu-id="95601-104">Extends the [**ITablet Interface**](itablet.md).</span></span>

## <a name="members"></a><span data-ttu-id="95601-105">成員</span><span class="sxs-lookup"><span data-stu-id="95601-105">Members</span></span>

<span data-ttu-id="95601-106">**ITablet2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="95601-106">The **ITablet2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="95601-107">**ITablet2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="95601-107">**ITablet2** also has these types of members:</span></span>

-   [<span data-ttu-id="95601-108">方法</span><span class="sxs-lookup"><span data-stu-id="95601-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="95601-109">方法</span><span class="sxs-lookup"><span data-stu-id="95601-109">Methods</span></span>

<span data-ttu-id="95601-110">**ITablet2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="95601-110">The **ITablet2** interface has these methods.</span></span>



| <span data-ttu-id="95601-111">方法</span><span class="sxs-lookup"><span data-stu-id="95601-111">Method</span></span>                                          | <span data-ttu-id="95601-112">描述</span><span class="sxs-lookup"><span data-stu-id="95601-112">Description</span></span>                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95601-113">**GetDeviceKind**</span><span class="sxs-lookup"><span data-stu-id="95601-113">**GetDeviceKind**</span></span>](itablet2-getdevicekind.md) | <span data-ttu-id="95601-114">傳回 tablet 物件所代表的硬體裝置類型，例如滑鼠、畫筆或觸控。</span><span class="sxs-lookup"><span data-stu-id="95601-114">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95601-115">備註</span><span class="sxs-lookup"><span data-stu-id="95601-115">Remarks</span></span>

<span data-ttu-id="95601-116">此介面是在 Windows Vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="95601-116">This interface was introduced in Windows Vista.</span></span>

<span data-ttu-id="95601-117">開發人員不應使用此介面。</span><span class="sxs-lookup"><span data-stu-id="95601-117">Developers should not use this interface.</span></span>

<span data-ttu-id="95601-118">下列程式碼說明如何定義 **ITablet2** 介面。</span><span class="sxs-lookup"><span data-stu-id="95601-118">The following code describes how the **ITablet2** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a><span data-ttu-id="95601-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="95601-119">Requirements</span></span>



| <span data-ttu-id="95601-120">需求</span><span class="sxs-lookup"><span data-stu-id="95601-120">Requirement</span></span> | <span data-ttu-id="95601-121">值</span><span class="sxs-lookup"><span data-stu-id="95601-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95601-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95601-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95601-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95601-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="95601-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95601-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95601-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="95601-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="95601-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="95601-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="95601-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95601-127"><dt>Wisptis.exe</dt></span></span> </dl> |



 

