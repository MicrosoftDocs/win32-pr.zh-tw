---
description: 針對 Windows 7，Windows 可攜式裝置支援裝置服務的方法和事件的下列參數屬性。
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: '參數屬性 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982259"
---
# <a name="parameter-attributes"></a><span data-ttu-id="35968-103">參數屬性</span><span class="sxs-lookup"><span data-stu-id="35968-103">Parameter Attributes</span></span>

<span data-ttu-id="35968-104">針對 Windows 7，Windows 可攜式裝置支援裝置服務的方法和事件的下列參數屬性。</span><span class="sxs-lookup"><span data-stu-id="35968-104">For Windows 7, Windows Portable Devices supports the following parameter attributes for methods and events of a device service.</span></span> <span data-ttu-id="35968-105">這些方法會傳回這些屬性：</span><span class="sxs-lookup"><span data-stu-id="35968-105">These attributes are returned by the these methods:</span></span>

-   [<span data-ttu-id="35968-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span><span class="sxs-lookup"><span data-stu-id="35968-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [<span data-ttu-id="35968-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span><span class="sxs-lookup"><span data-stu-id="35968-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| <span data-ttu-id="35968-108">屬性</span><span class="sxs-lookup"><span data-stu-id="35968-108">Attribute</span></span>                                            | <span data-ttu-id="35968-109">VarType</span><span class="sxs-lookup"><span data-stu-id="35968-109">VarType</span></span>         | <span data-ttu-id="35968-110">Description</span><span class="sxs-lookup"><span data-stu-id="35968-110">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35968-111">**WPD \_ 參數 \_ 屬性 \_ 預設 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="35968-111">**WPD\_PARAMETER\_ATTRIBUTE\_DEFAULT\_VALUE**</span></span>        | <span data-ttu-id="35968-112">VT \_ *XXXX*</span><span class="sxs-lookup"><span data-stu-id="35968-112">VT\_*XXXX*</span></span>      | <span data-ttu-id="35968-113">參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="35968-113">The default value of the parameter.</span></span>                                                                                                                                                         |
| <span data-ttu-id="35968-114">**WPD \_ 參數 \_ 屬性 \_ 列舉 \_ 元素**</span><span class="sxs-lookup"><span data-stu-id="35968-114">**WPD\_PARAMETER\_ATTRIBUTE\_ENUMERATION\_ELEMENTS**</span></span> | <span data-ttu-id="35968-115">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="35968-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="35968-116">[**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)介面，其中包含參數的列舉值。</span><span class="sxs-lookup"><span data-stu-id="35968-116">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface that contains the enumeration values for the parameter.</span></span>                                   |
| <span data-ttu-id="35968-117">**WPD \_ 參數 \_ 屬性 \_ 表單**</span><span class="sxs-lookup"><span data-stu-id="35968-117">**WPD\_PARAMETER\_ATTRIBUTE\_FORM**</span></span>                  | <span data-ttu-id="35968-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="35968-118">**VT\_UI4**</span></span>     | <span data-ttu-id="35968-119">允許的有效參數值形式。</span><span class="sxs-lookup"><span data-stu-id="35968-119">The form of valid parameter values allowed.</span></span>                                                                                                                                                 |
| <span data-ttu-id="35968-120">**WPD \_ 參數 \_ 屬性 \_ \_ 大小上限**</span><span class="sxs-lookup"><span data-stu-id="35968-120">**WPD\_PARAMETER\_ATTRIBUTE\_MAX\_SIZE**</span></span>             | <span data-ttu-id="35968-121">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="35968-121">**VT\_UI8**</span></span>     | <span data-ttu-id="35968-122">參數的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="35968-122">The maximum size of the parameter, in bytes .</span></span>                                                                                                                                               |
| <span data-ttu-id="35968-123">**WPD \_ 參數 \_ 屬性 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="35968-123">**WPD\_PARAMETER\_ATTRIBUTE\_NAME**</span></span>                  | <span data-ttu-id="35968-124">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="35968-124">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="35968-125">字串，指定事件或方法參數的腳本易記名稱。</span><span class="sxs-lookup"><span data-stu-id="35968-125">A string that specifies the script-friendly name of an event or method parameter.</span></span> <span data-ttu-id="35968-126">有效字元為英數位元 \[ a-zA-Z0-9 \] 和 ' \_ '。</span><span class="sxs-lookup"><span data-stu-id="35968-126">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span>                                                 |
| <span data-ttu-id="35968-127">**WPD \_ 參數 \_ 屬性 \_ 順序**</span><span class="sxs-lookup"><span data-stu-id="35968-127">**WPD\_PARAMETER\_ATTRIBUTE\_ORDER**</span></span>                 | <span data-ttu-id="35968-128">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="35968-128">**VT\_UI4**</span></span>     | <span data-ttu-id="35968-129">以零為基底的參數順序索引，讓順序值0對應至第一個參數。</span><span class="sxs-lookup"><span data-stu-id="35968-129">The zero-based parameter-order index, so that an order value of 0 corresponds to the first parameter.</span></span>                                                                                       |
| <span data-ttu-id="35968-130">**WPD \_ 參數 \_ 屬性 \_ 範圍 \_ 最小值**</span><span class="sxs-lookup"><span data-stu-id="35968-130">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MIN**</span></span>            | <span data-ttu-id="35968-131">VT \_ *XXXX*</span><span class="sxs-lookup"><span data-stu-id="35968-131">VT\_*XXXX*</span></span>      | <span data-ttu-id="35968-132">表單 WPD \_ 參數 \_ 屬性 \_ 表單範圍之參數的最大值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="35968-132">The maximum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="35968-133">**WPD \_ 參數 \_ 屬性 \_ 範圍 \_ 最大值**</span><span class="sxs-lookup"><span data-stu-id="35968-133">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MAX**</span></span>            | <span data-ttu-id="35968-134">VT \_ *XXXX*</span><span class="sxs-lookup"><span data-stu-id="35968-134">VT\_*XXXX*</span></span>      | <span data-ttu-id="35968-135">表單 WPD \_ 參數 \_ 屬性 \_ 表單範圍之參數的最小值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="35968-135">The minimum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="35968-136">**WPD \_ 參數 \_ 屬性 \_ 範圍 \_ 步驟**</span><span class="sxs-lookup"><span data-stu-id="35968-136">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_STEP**</span></span>           | <span data-ttu-id="35968-137">VT \_ *XXXX*</span><span class="sxs-lookup"><span data-stu-id="35968-137">VT\_*XXXX*</span></span>      | <span data-ttu-id="35968-138">表單 WPD \_ 參數 \_ 屬性 \_ 表單範圍的參數步驟值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="35968-138">The step value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                          |
| <span data-ttu-id="35968-139">**WPD \_ 參數 \_ 屬性 \_ 正則 \_ 運算式**</span><span class="sxs-lookup"><span data-stu-id="35968-139">**WPD\_PARAMETER\_ATTRIBUTE\_REGULAR\_EXPRESSION**</span></span>   | <span data-ttu-id="35968-140">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="35968-140">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="35968-141">正則運算式，為表單 WPD \_ 參數 \_ 屬性 \_ 表單 \_ 正則 \_ 運算式的參數指定可接受的值。</span><span class="sxs-lookup"><span data-stu-id="35968-141">A regular expression that specifies acceptable values for parameters of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION.</span></span>                                                      |
| <span data-ttu-id="35968-142">**WPD \_ 參數 \_ 屬性 \_ 使用 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="35968-142">**WPD\_PARAMETER\_ATTRIBUTE\_USAGE\_TYPE**</span></span>           | <span data-ttu-id="35968-143">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="35968-143">**VT\_UI4**</span></span>     | <span data-ttu-id="35968-144">整數，指定方法參數的使用方式，例如 in/out。有效的值為 [**WPD \_ 參數 \_ 使用 \_ 類型**](wpd-parameter-usage-types.md) 列舉類型。</span><span class="sxs-lookup"><span data-stu-id="35968-144">An integer that specifies the usage of a method parameter, for example, in/out. Valid values are of the [**WPD\_PARAMETER\_USAGE\_TYPES**](wpd-parameter-usage-types.md) enumeration type.</span></span> |
| <span data-ttu-id="35968-145">**WPD \_ 參數 \_ 屬性 \_ VARTYPE**</span><span class="sxs-lookup"><span data-stu-id="35968-145">**WPD\_PARAMETER\_ATTRIBUTE\_VARTYPE**</span></span>               | <span data-ttu-id="35968-146">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="35968-146">**VT\_UI4**</span></span>     | <span data-ttu-id="35968-147">參數 VarType。</span><span class="sxs-lookup"><span data-stu-id="35968-147">The parameter VarType.</span></span>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="35968-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="35968-148">Requirements</span></span>



| <span data-ttu-id="35968-149">需求</span><span class="sxs-lookup"><span data-stu-id="35968-149">Requirement</span></span> | <span data-ttu-id="35968-150">值</span><span class="sxs-lookup"><span data-stu-id="35968-150">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="35968-151">標頭</span><span class="sxs-lookup"><span data-stu-id="35968-151">Header</span></span><br/> | <dl> <span data-ttu-id="35968-152"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="35968-152"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35968-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35968-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35968-154">**屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="35968-154">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




