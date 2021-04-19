---
description: Windows 可攜式裝置支援下列其他屬性。
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: '其他屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982971"
---
# <a name="miscellaneous-properties"></a><span data-ttu-id="5a596-103">其他屬性</span><span class="sxs-lookup"><span data-stu-id="5a596-103">Miscellaneous Properties</span></span>

<span data-ttu-id="5a596-104">Windows 可攜式裝置支援下列其他屬性。</span><span class="sxs-lookup"><span data-stu-id="5a596-104">Windows Portable Devices supports the following miscellaneous properties.</span></span>



| <span data-ttu-id="5a596-105">屬性</span><span class="sxs-lookup"><span data-stu-id="5a596-105">Property</span></span>                                       | <span data-ttu-id="5a596-106">VarType</span><span class="sxs-lookup"><span data-stu-id="5a596-106">VarType</span></span>         | <span data-ttu-id="5a596-107">Description</span><span class="sxs-lookup"><span data-stu-id="5a596-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a596-108">**WPD \_ API \_ 選項 \_ 使用 \_ CLEAR \_ 資料流程 \_**</span><span class="sxs-lookup"><span data-stu-id="5a596-108">**WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM**</span></span> | <span data-ttu-id="5a596-109">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="5a596-109">**VT\_BOOL**</span></span>    | <span data-ttu-id="5a596-110">布林值，指定為數據傳輸建立的資料流程是否為明確的，也就是不包含 DRM。用戶端可以設定此選項，方法是將它加入至傳遞給 [**IPortableDeviceContent：： CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)的物件屬性。</span><span class="sxs-lookup"><span data-stu-id="5a596-110">A Boolean value that specifies whether the data stream created for data transfer will be clear, that is, DRM is not involved.Clients can set this option by adding it to the object properties passed to [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="5a596-111">**WPD \_ 服務 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="5a596-111">**WPD\_SERVICE\_VERSION**</span></span>                      | <span data-ttu-id="5a596-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5a596-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="5a596-113">字串，指定指定之裝置服務的執行版本。</span><span class="sxs-lookup"><span data-stu-id="5a596-113">A string that specifies the implementation version of a given device service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5a596-114">**\_允許 WPD 資料夾 \_ 內容 \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="5a596-114">**WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED**</span></span>       | <span data-ttu-id="5a596-115">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="5a596-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="5a596-116">值，指定可以是此資料夾之直接子系的物件類型。</span><span class="sxs-lookup"><span data-stu-id="5a596-116">A value that specifies the object types that can be direct children of this folder.</span></span> <span data-ttu-id="5a596-117">子資料夾可以有不同的功能。這個屬性是 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) ，其包含 \_ 指定允許物件類型的 VT CLSID 值。</span><span class="sxs-lookup"><span data-stu-id="5a596-117">Child folders can have different capabilities.This property is an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) holding VT\_CLSID values that specify permitted object types.</span></span><br/> <span data-ttu-id="5a596-118">如需 Windows 可攜式裝置所定義之物件類型的清單，請參閱 [物件的需求](requirements-for-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="5a596-118">For a list of object types defined by Windows Portable Devices, see [Requirements for Objects](requirements-for-objects.md).</span></span><br/>                                         |
| <span data-ttu-id="5a596-119">**WPD \_ 功能 \_ 物件 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="5a596-119">**WPD\_FUNCTIONAL\_OBJECT\_CATEGORY**</span></span>          | <span data-ttu-id="5a596-120">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="5a596-120">**VT\_CLSID**</span></span>   | <span data-ttu-id="5a596-121">值，指定物件的功能類別。</span><span class="sxs-lookup"><span data-stu-id="5a596-121">A value that specifies the object's functional category.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="5a596-122">**WPD \_ 轉譯 \_ 資訊 \_ 設定檔**</span><span class="sxs-lookup"><span data-stu-id="5a596-122">**WPD\_RENDERING\_INFORMATION\_PROFILES**</span></span>      | <span data-ttu-id="5a596-123">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="5a596-123">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="5a596-124">保存多個 [**IPortableDeviceValues**](iportabledevicevalues.md)介面的 [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) ，其中每個介面都包含物件所支援之設定檔的屬性設定。</span><span class="sxs-lookup"><span data-stu-id="5a596-124">An [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) that holds multiple [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces, each of which contains the property settings for a profile that the object supports.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="5a596-125">**WPD \_ 物件 \_ 提示 \_ 位置 \_ 顯示 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="5a596-125">**WPD\_OBJECT\_HINT\_LOCATION\_DISPLAY\_NAME**</span></span> | <span data-ttu-id="5a596-126">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="5a596-126">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="5a596-127">如果物件是提示位置，這個屬性會指出要對使用者顯示的提示特定名稱，而不是物件名稱。驅動程式可以指定各種物件類型的位置提示。</span><span class="sxs-lookup"><span data-stu-id="5a596-127">If an object is a hint location, this property indicates the hint-specific name to display to the user instead of the object name.Drivers can specify location hints for various object types.</span></span> <span data-ttu-id="5a596-128">這些是保留特定物件類型之資料夾的慣用儲存位置。</span><span class="sxs-lookup"><span data-stu-id="5a596-128">These are preferred storage locations for folders that hold a particular object type.</span></span> <span data-ttu-id="5a596-129">對等專案會是 Windows 中影像檔案的 [我的圖片] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="5a596-129">An equivalent would be the My Pictures folder for image files in Windows.</span></span> <span data-ttu-id="5a596-130">如果這個屬性不存在，通常會改用 [WPD \_ 物件 \_ 名稱](object-properties.md) 。</span><span class="sxs-lookup"><span data-stu-id="5a596-130">If this property does not exist, typically the [WPD\_OBJECT\_NAME](object-properties.md) is used instead.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a596-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a596-131">Requirements</span></span>



| <span data-ttu-id="5a596-132">需求</span><span class="sxs-lookup"><span data-stu-id="5a596-132">Requirement</span></span> | <span data-ttu-id="5a596-133">值</span><span class="sxs-lookup"><span data-stu-id="5a596-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a596-134">標頭</span><span class="sxs-lookup"><span data-stu-id="5a596-134">Header</span></span><br/> | <dl> <span data-ttu-id="5a596-135"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a596-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a596-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a596-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a596-137">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="5a596-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




