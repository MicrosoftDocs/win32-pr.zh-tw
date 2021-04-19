---
description: Windows 可攜式裝置支援下列資源屬性內容。
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: '資源屬性屬性 (PortableDevice .h) '
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
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000952"
---
# <a name="resource-attribute-properties"></a><span data-ttu-id="f0f67-103">資源屬性屬性</span><span class="sxs-lookup"><span data-stu-id="f0f67-103">Resource Attribute Properties</span></span>

<span data-ttu-id="f0f67-104">Windows 可攜式裝置支援下列資源屬性內容。</span><span class="sxs-lookup"><span data-stu-id="f0f67-104">Windows Portable Devices supports the following resource attribute properties.</span></span>



| <span data-ttu-id="f0f67-105">屬性</span><span class="sxs-lookup"><span data-stu-id="f0f67-105">Property</span></span>                                    | <span data-ttu-id="f0f67-106">VarType</span><span class="sxs-lookup"><span data-stu-id="f0f67-106">VarType</span></span>         | <span data-ttu-id="f0f67-107">Description</span><span class="sxs-lookup"><span data-stu-id="f0f67-107">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0f67-108">**WPD \_ 資源 \_ 屬性 \_ 資源 \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="f0f67-108">**WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY**</span></span> | <span data-ttu-id="f0f67-109">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="f0f67-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="f0f67-110">這是包含單一值的 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) ，這是用來識別資源的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f0f67-110">This is an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value, which is the key identifying the resource.</span></span>                     |
| <span data-ttu-id="f0f67-111">**WPD \_ 資源 \_ 屬性 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="f0f67-111">**WPD\_RESOURCE\_ATTRIBUTE\_FORMAT**</span></span>        | <span data-ttu-id="f0f67-112">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="f0f67-112">**VT\_CLSID**</span></span>   | <span data-ttu-id="f0f67-113">指定資源格式的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="f0f67-113">A GUID value that specifies the format of the resource.</span></span> <span data-ttu-id="f0f67-114">如需 Windows 可攜式裝置所定義之格式的清單，請參閱 [物件格式](object-format-guids.md) 。</span><span class="sxs-lookup"><span data-stu-id="f0f67-114">See [Object Formats](object-format-guids.md) for a list of formats that are defined by Windows Portable Devices.</span></span> |
| <span data-ttu-id="f0f67-115">**WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="f0f67-115">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>   | <span data-ttu-id="f0f67-116">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="f0f67-116">**VT\_UI8**</span></span>     | <span data-ttu-id="f0f67-117">資源資料的大小總計（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f0f67-117">The total size of the resource data, in bytes.</span></span>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="f0f67-118">備註</span><span class="sxs-lookup"><span data-stu-id="f0f67-118">Remarks</span></span>

<span data-ttu-id="f0f67-119">這些屬性是由 [**IPortableDeviceResources：： GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) 方法傳回。</span><span class="sxs-lookup"><span data-stu-id="f0f67-119">These attributes are returned by the [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0f67-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0f67-120">Requirements</span></span>



| <span data-ttu-id="f0f67-121">需求</span><span class="sxs-lookup"><span data-stu-id="f0f67-121">Requirement</span></span> | <span data-ttu-id="f0f67-122">值</span><span class="sxs-lookup"><span data-stu-id="f0f67-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0f67-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f0f67-123">Header</span></span><br/> | <dl> <span data-ttu-id="f0f67-124"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0f67-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0f67-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0f67-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0f67-126">**IPortableDeviceResources::GetResourceAttributes**</span><span class="sxs-lookup"><span data-stu-id="f0f67-126">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[<span data-ttu-id="f0f67-127">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="f0f67-127">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




