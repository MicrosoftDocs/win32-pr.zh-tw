---
description: 針對 Windows 7，Windows 可攜式裝置支援裝置服務的下列方法屬性。 這些屬性是由 IPortableDeviceServiceCapabilities：： GetMethodAttributes 方法傳回。
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: '方法屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998774"
---
# <a name="method-attributes"></a><span data-ttu-id="e5381-104">方法屬性</span><span class="sxs-lookup"><span data-stu-id="e5381-104">Method Attributes</span></span>

<span data-ttu-id="e5381-105">針對 Windows 7，Windows 可攜式裝置支援裝置服務的下列方法屬性。</span><span class="sxs-lookup"><span data-stu-id="e5381-105">For Windows 7, Windows Portable Devices supports the following attributes for methods of a device service.</span></span> <span data-ttu-id="e5381-106">這些屬性是由 [**IPortableDeviceServiceCapabilities：： GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) 方法傳回。</span><span class="sxs-lookup"><span data-stu-id="e5381-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method.</span></span>




| <span data-ttu-id="e5381-107">屬性</span><span class="sxs-lookup"><span data-stu-id="e5381-107">Attribute</span></span>                                      | <span data-ttu-id="e5381-108">VarType</span><span class="sxs-lookup"><span data-stu-id="e5381-108">VarType</span></span>         | <span data-ttu-id="e5381-109">Description</span><span class="sxs-lookup"><span data-stu-id="e5381-109">Description</span></span>                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5381-110">**WPD \_ 方法 \_ 屬性 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="e5381-110">**WPD\_METHOD\_ATTRIBUTE\_ACCESS**</span></span>             | <span data-ttu-id="e5381-111">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="e5381-111">**VT\_CLSID**</span></span>   | <span data-ttu-id="e5381-112">需要的方法存取。</span><span class="sxs-lookup"><span data-stu-id="e5381-112">The required method access.</span></span>                                                                                               |
| <span data-ttu-id="e5381-113">**WPD \_ 方法 \_ 屬性 \_ 相關聯的 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="e5381-113">**WPD\_METHOD\_ATTRIBUTE\_ASSOCIATED\_FORMAT**</span></span> | <span data-ttu-id="e5381-114">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="e5381-114">**VT\_CLSID**</span></span>   | <span data-ttu-id="e5381-115">與方法相關聯的格式，如果沒有相關聯的格式，則為 **GUID \_ Null** 。</span><span class="sxs-lookup"><span data-stu-id="e5381-115">The format associated with the method, or **GUID\_NULL** if there is no associated format.</span></span>                                |
| <span data-ttu-id="e5381-116">**WPD \_ 方法 \_ 屬性 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="e5381-116">**WPD\_METHOD\_ATTRIBUTE\_NAME**</span></span>               | <span data-ttu-id="e5381-117">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="e5381-117">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="e5381-118">字串，指定方法的腳本易記名稱。</span><span class="sxs-lookup"><span data-stu-id="e5381-118">A string that specifies the script-friendly name of the method.</span></span> <span data-ttu-id="e5381-119">有效字元為英數位元 \[ a-zA-Z0-9 \] 和 ' \_ '。</span><span class="sxs-lookup"><span data-stu-id="e5381-119">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="e5381-120">**WPD \_ 方法 \_ 屬性 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="e5381-120">**WPD\_METHOD\_ATTRIBUTE\_PARAMETERS**</span></span>         | <span data-ttu-id="e5381-121">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="e5381-121">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="e5381-122">包含方法參數的 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="e5381-122">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that contains the method parameters.</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="e5381-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5381-123">Requirements</span></span>



| <span data-ttu-id="e5381-124">需求</span><span class="sxs-lookup"><span data-stu-id="e5381-124">Requirement</span></span> | <span data-ttu-id="e5381-125">值</span><span class="sxs-lookup"><span data-stu-id="e5381-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5381-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e5381-126">Header</span></span><br/> | <dl> <span data-ttu-id="e5381-127"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="e5381-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5381-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5381-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5381-129">**屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="e5381-129">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




