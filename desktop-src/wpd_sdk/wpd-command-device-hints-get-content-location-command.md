---
description: WPD \_ 命令 \_ 裝置 \_ 提示 \_ 取得 \_ 內容 \_ 位置命令會抓取可保存指定類型物件之資料夾的物件識別碼。
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: 'WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985975"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a><span data-ttu-id="79c95-103">WPD \_ 命令 \_ 裝置 \_ 提示 \_ 取得 \_ 內容 \_ 位置命令</span><span class="sxs-lookup"><span data-stu-id="79c95-103">WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION Command</span></span>

<span data-ttu-id="79c95-104">**WPD \_ 命令 \_ 裝置 \_ 提示 \_ 取得 \_ 內容 \_ 位置** 命令會抓取可保存指定類型物件之資料夾的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="79c95-104">The **WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION** command retrieves the object IDs of folders that can hold an object of a specified type.</span></span> <span data-ttu-id="79c95-105">此命令會以更快的方式提供，讓用戶端探索裝置儲存特定物件的位置，而不是暴力物件列舉。</span><span class="sxs-lookup"><span data-stu-id="79c95-105">This command is provided as a faster way for a client to discover where a device stores specific objects than by brute object enumeration.</span></span>

## <a name="command-category"></a><span data-ttu-id="79c95-106">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="79c95-106">Command category</span></span>

<span data-ttu-id="79c95-107">**WPD \_ 類別 \_ 裝置 \_ 提示**</span><span class="sxs-lookup"><span data-stu-id="79c95-107">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>

## <a name="parameters"></a><span data-ttu-id="79c95-108">參數</span><span class="sxs-lookup"><span data-stu-id="79c95-108">Parameters</span></span>

<span data-ttu-id="79c95-109">驅動程式需要下列參數。</span><span class="sxs-lookup"><span data-stu-id="79c95-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="79c95-110">參數</span><span class="sxs-lookup"><span data-stu-id="79c95-110">Parameter</span></span>                                   | <span data-ttu-id="79c95-111">VarType</span><span class="sxs-lookup"><span data-stu-id="79c95-111">VarType</span></span>   | <span data-ttu-id="79c95-112">Description</span><span class="sxs-lookup"><span data-stu-id="79c95-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c95-113">WPD \_ 屬性 \_ 裝置 \_ 提示 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="79c95-113">WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_TYPE</span></span> | <span data-ttu-id="79c95-114">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="79c95-114">VT\_CLSID</span></span> | <span data-ttu-id="79c95-115">必要。</span><span class="sxs-lookup"><span data-stu-id="79c95-115">Required.</span></span> <span data-ttu-id="79c95-116">呼叫端希望尋找容器的物件類型。</span><span class="sxs-lookup"><span data-stu-id="79c95-116">The object type that the caller wishes to find the container for.</span></span> <span data-ttu-id="79c95-117">例如，若要尋找用來在數位相機上保存影像的最上層資料夾，呼叫者會提交 WPD \_ 內容 \_ 類型 \_ 影像。</span><span class="sxs-lookup"><span data-stu-id="79c95-117">For example, to find the top-level folders used to hold images on a digital camera, the caller would submit WPD\_CONTENT\_TYPE\_IMAGE.</span></span> <span data-ttu-id="79c95-118">如需瞭解 Windows 可攜式裝置所定義的物件類型清單，請參閱 [物件的需求](requirements-for-objects.md) 。</span><span class="sxs-lookup"><span data-stu-id="79c95-118">See [Requirements for Objects](requirements-for-objects.md) for a list of object types defined by Windows Portable Devices.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="79c95-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="79c95-119">Return Value</span></span>

<span data-ttu-id="79c95-120">驅動程式應該會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="79c95-120">The driver should return the following results.</span></span>



| <span data-ttu-id="79c95-121">結果</span><span class="sxs-lookup"><span data-stu-id="79c95-121">Result</span></span>                                               | <span data-ttu-id="79c95-122">VarType</span><span class="sxs-lookup"><span data-stu-id="79c95-122">VarType</span></span>     | <span data-ttu-id="79c95-123">Description</span><span class="sxs-lookup"><span data-stu-id="79c95-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c95-124">**WPD \_ 屬性 \_ 裝置 \_ 提示 \_ 內容 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="79c95-124">**WPD\_PROPERTY\_DEVICE\_HINTS\_CONTENT\_LOCATIONS**</span></span> | <span data-ttu-id="79c95-125">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="79c95-125">VT\_UNKNOWN</span></span> | <span data-ttu-id="79c95-126">必要。</span><span class="sxs-lookup"><span data-stu-id="79c95-126">Required.</span></span> <span data-ttu-id="79c95-127">VT LPWSTR 數值型別的 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) \_ ，指定包含由呼叫參數表示之類型物件的資料夾物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="79c95-127">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) of type VT\_LPWSTR values that specify the object IDs of folders containing objects of the type indicated by the calling parameter.</span></span> <span data-ttu-id="79c95-128">如果找不到資料夾，這應該是空的清單。結果所指出的資料夾可能包含或可能不包含其他內容類型的物件。</span><span class="sxs-lookup"><span data-stu-id="79c95-128">If no folders are found, this should be an empty list.The folders indicated by the result may or may not contain objects of other content types.</span></span> <span data-ttu-id="79c95-129">如需資料夾限制的詳細資訊，請參閱 [WPD \_ 資料夾 \_ 內容 \_ 類型的 \_ 允許](miscellaneous-properties.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="79c95-129">See the [WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED](miscellaneous-properties.md) property for information on folder restrictions.</span></span><br/> |
| <span data-ttu-id="79c95-130">**WPD \_ 屬性 \_ 通用 \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="79c95-130">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                   | <span data-ttu-id="79c95-131">VT \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="79c95-131">VT\_ERROR</span></span>   | <span data-ttu-id="79c95-132">必要。</span><span class="sxs-lookup"><span data-stu-id="79c95-132">Required.</span></span> <span data-ttu-id="79c95-133">**HRESULT** ，指出處理命令的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="79c95-133">An **HRESULT** that indicates success or failure of handling the command.</span></span> <span data-ttu-id="79c95-134">如果呼叫端提出不正確要求，驅動程式應該會傳回 **\_ \_ \_ 不 \_ 支援的 WIN32 (錯誤)** ，而且不需要傳回任何其他的結果值。</span><span class="sxs-lookup"><span data-stu-id="79c95-134">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="79c95-135">錯誤碼包括 [Windows 可攜式裝置錯誤代碼](error-constants.md) 或任何其他適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="79c95-135">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="79c95-136">**WPD \_ 屬性 \_ 常見的 \_ 驅動程式 \_ 錯誤碼 \_**</span><span class="sxs-lookup"><span data-stu-id="79c95-136">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>       | <span data-ttu-id="79c95-137">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="79c95-137">VT\_UI4</span></span>     | <span data-ttu-id="79c95-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="79c95-138">Optional.</span></span> <span data-ttu-id="79c95-139">驅動程式特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="79c95-139">A driver-specific error code.</span></span> <span data-ttu-id="79c95-140">這通常只會用於驅動程式測試，或者驅動程式、裝置和用戶端都是一起設計的。</span><span class="sxs-lookup"><span data-stu-id="79c95-140">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a><span data-ttu-id="79c95-141">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="79c95-141">Calling Methods</span></span>

<span data-ttu-id="79c95-142">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="79c95-142">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="79c95-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="79c95-143">Requirements</span></span>



| <span data-ttu-id="79c95-144">需求</span><span class="sxs-lookup"><span data-stu-id="79c95-144">Requirement</span></span> | <span data-ttu-id="79c95-145">值</span><span class="sxs-lookup"><span data-stu-id="79c95-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c95-146">標頭</span><span class="sxs-lookup"><span data-stu-id="79c95-146">Header</span></span><br/> | <dl> <span data-ttu-id="79c95-147"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="79c95-147"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




