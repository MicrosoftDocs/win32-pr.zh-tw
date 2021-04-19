---
description: Windows 可攜式裝置支援下列資源屬性。
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: '資源屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996259"
---
# <a name="resource-attributes"></a><span data-ttu-id="856b3-103">資源屬性</span><span class="sxs-lookup"><span data-stu-id="856b3-103">Resource Attributes</span></span>

<span data-ttu-id="856b3-104">Windows 可攜式裝置支援下列資源屬性。</span><span class="sxs-lookup"><span data-stu-id="856b3-104">Windows Portable Devices supports the following resource attributes.</span></span> <span data-ttu-id="856b3-105">下列方法會傳回這些屬性：</span><span class="sxs-lookup"><span data-stu-id="856b3-105">These attributes are returned by the following methods:</span></span>

-   [<span data-ttu-id="856b3-106">**IPortableDeviceResources::GetResourceAttributes**</span><span class="sxs-lookup"><span data-stu-id="856b3-106">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| <span data-ttu-id="856b3-107">屬性</span><span class="sxs-lookup"><span data-stu-id="856b3-107">Attribute</span></span>                                                  | <span data-ttu-id="856b3-108">VarType</span><span class="sxs-lookup"><span data-stu-id="856b3-108">VarType</span></span>      | <span data-ttu-id="856b3-109">Description</span><span class="sxs-lookup"><span data-stu-id="856b3-109">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="856b3-110">**WPD \_ 資源 \_ 屬性 \_ 可以 \_ 刪除**</span><span class="sxs-lookup"><span data-stu-id="856b3-110">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE**</span></span>                  | <span data-ttu-id="856b3-111">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="856b3-111">**VT\_BOOL**</span></span> | <span data-ttu-id="856b3-112">布林值，指定用戶端是否有權刪除資源。</span><span class="sxs-lookup"><span data-stu-id="856b3-112">A Boolean value that specifies whether a client has permission to delete the resource.</span></span> <span data-ttu-id="856b3-113">如果不存在，則會假設為 false。</span><span class="sxs-lookup"><span data-stu-id="856b3-113">If absent, it is assumed to be false.</span></span>                |
| <span data-ttu-id="856b3-114">**WPD \_ 資源 \_ 屬性 \_ 可以 \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="856b3-114">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ**</span></span>                    | <span data-ttu-id="856b3-115">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="856b3-115">**VT\_BOOL**</span></span> | <span data-ttu-id="856b3-116">布林值，指定用戶端是否有許可權開啟資源以進行讀取存取。</span><span class="sxs-lookup"><span data-stu-id="856b3-116">A Boolean value that specifies whether a client has permission to open the resource for Read access.</span></span> <span data-ttu-id="856b3-117">如果不存在，則會假設為 False。</span><span class="sxs-lookup"><span data-stu-id="856b3-117">If absent, it is assumed to be False.</span></span>  |
| <span data-ttu-id="856b3-118">**WPD \_ 資源 \_ 屬性 \_ 可以 \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="856b3-118">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE**</span></span>                   | <span data-ttu-id="856b3-119">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="856b3-119">**VT\_BOOL**</span></span> | <span data-ttu-id="856b3-120">布林值，指定用戶端是否有許可權開啟資源以進行寫入存取。</span><span class="sxs-lookup"><span data-stu-id="856b3-120">A Boolean value that specifies whether a client has permission to open the resource for Write access.</span></span> <span data-ttu-id="856b3-121">如果不存在，則會假設為 false。</span><span class="sxs-lookup"><span data-stu-id="856b3-121">If absent, it is assumed to be false.</span></span> |
| <span data-ttu-id="856b3-122">**WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 讀取 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="856b3-122">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE**</span></span>  | <span data-ttu-id="856b3-123">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="856b3-123">**VT\_UI4**</span></span>  | <span data-ttu-id="856b3-124">呼叫端應用於從資源緩衝讀取的建議緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="856b3-124">The recommended buffer size that a caller should use for buffered reads from the resource.</span></span>                                                  |
| <span data-ttu-id="856b3-125">**WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 寫入 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="856b3-125">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="856b3-126">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="856b3-126">**VT\_UI4**</span></span>  | <span data-ttu-id="856b3-127">呼叫端應該在資源上用於緩衝寫入的建議緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="856b3-127">The recommended buffer size that a caller should use for buffered writes on the resource.</span></span>                                                   |
| <span data-ttu-id="856b3-128">**WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="856b3-128">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>                  | <span data-ttu-id="856b3-129">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="856b3-129">**VT\_UI8**</span></span>  | <span data-ttu-id="856b3-130">資源資料的大小總計（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="856b3-130">The total size of the resource data, in bytes.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="856b3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="856b3-131">Requirements</span></span>



| <span data-ttu-id="856b3-132">需求</span><span class="sxs-lookup"><span data-stu-id="856b3-132">Requirement</span></span> | <span data-ttu-id="856b3-133">值</span><span class="sxs-lookup"><span data-stu-id="856b3-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="856b3-134">標頭</span><span class="sxs-lookup"><span data-stu-id="856b3-134">Header</span></span><br/> | <dl> <span data-ttu-id="856b3-135"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="856b3-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="856b3-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="856b3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="856b3-137">**屬性**</span><span class="sxs-lookup"><span data-stu-id="856b3-137">**Properties**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




