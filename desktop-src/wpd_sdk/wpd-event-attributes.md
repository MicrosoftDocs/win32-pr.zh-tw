---
description: 針對 Windows 7，Windows 可攜式裝置支援裝置服務事件的下列屬性。 這些屬性是由 IPortableDeviceServiceCapabilities：： GetEventAttributes 方法傳回。
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: '事件屬性 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999077"
---
# <a name="event-attributes-portabledeviceh"></a><span data-ttu-id="0d958-104">事件屬性 (PortableDevice) </span><span class="sxs-lookup"><span data-stu-id="0d958-104">Event Attributes (PortableDevice.h)</span></span>

<span data-ttu-id="0d958-105">針對 Windows 7，Windows 可攜式裝置支援裝置服務事件的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="0d958-105">For Windows 7, Windows Portable Devices supports the following attributes for events of a device service.</span></span> <span data-ttu-id="0d958-106">這些屬性是由 [**IPortableDeviceServiceCapabilities：： GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) 方法傳回。</span><span class="sxs-lookup"><span data-stu-id="0d958-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method.</span></span>




| <span data-ttu-id="0d958-107">屬性</span><span class="sxs-lookup"><span data-stu-id="0d958-107">Attribute</span></span>                             | <span data-ttu-id="0d958-108">VarType</span><span class="sxs-lookup"><span data-stu-id="0d958-108">VarType</span></span>         | <span data-ttu-id="0d958-109">Description</span><span class="sxs-lookup"><span data-stu-id="0d958-109">Description</span></span>                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d958-110">**WPD \_ 事件 \_ 屬性 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="0d958-110">**WPD\_EVENT\_ATTRIBUTE\_NAME**</span></span>       | <span data-ttu-id="0d958-111">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="0d958-111">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="0d958-112">字串，指定事件的腳本易記名稱。</span><span class="sxs-lookup"><span data-stu-id="0d958-112">A string that specifies the script-friendly name of the event.</span></span> <span data-ttu-id="0d958-113">有效字元為英數位元 \[ a-zA-Z0-9 \] 和 ' \_ '。</span><span class="sxs-lookup"><span data-stu-id="0d958-113">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="0d958-114">**WPD \_ 事件 \_ 屬性 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="0d958-114">**WPD\_EVENT\_ATTRIBUTE\_OPTIONS**</span></span>    | <span data-ttu-id="0d958-115">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="0d958-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="0d958-116">包含事件選項的 [**IPortableDeviceValues**](iportabledevicevalues.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d958-116">An [**IPortableDeviceValues**](iportabledevicevalues.md) that contains the event options.</span></span>                               |
| <span data-ttu-id="0d958-117">**WPD \_ 事件 \_ 屬性 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="0d958-117">**WPD\_EVENT\_ATTRIBUTE\_PARAMETERS**</span></span> | <span data-ttu-id="0d958-118">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="0d958-118">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="0d958-119">包含事件參數的 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d958-119">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) that contains the event parameters.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="0d958-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d958-120">Requirements</span></span>



| <span data-ttu-id="0d958-121">需求</span><span class="sxs-lookup"><span data-stu-id="0d958-121">Requirement</span></span> | <span data-ttu-id="0d958-122">值</span><span class="sxs-lookup"><span data-stu-id="0d958-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d958-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0d958-123">Header</span></span><br/> | <dl> <span data-ttu-id="0d958-124"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d958-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d958-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d958-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d958-126">**屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="0d958-126">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




