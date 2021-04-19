---
description: 抓取物件所支援的屬性。
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: 'WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984333"
---
# <a name="wpd_command_object_properties_get_supported-command"></a><span data-ttu-id="22d3a-103">WPD \_ 命令 \_ 物件 \_ 屬性 \_ 取得 \_ 支援的命令</span><span class="sxs-lookup"><span data-stu-id="22d3a-103">WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED Command</span></span>

<span data-ttu-id="22d3a-104">**WPD \_ 命令 \_ 物件 \_ 屬性 \_ GET \_ 支援** 的命令會抓取物件所支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="22d3a-104">The **WPD\_COMMAND\_OBJECT\_PROPERTIES\_GET\_SUPPORTED** command retrieves the properties supported by an object.</span></span>

## <a name="command-category"></a><span data-ttu-id="22d3a-105">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="22d3a-105">Command Category</span></span>

<span data-ttu-id="22d3a-106">**WPD \_ 類別 \_ 物件 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="22d3a-106">**WPD\_CATEGORY\_OBJECT\_PROPERTIES**</span></span>

## <a name="parameters"></a><span data-ttu-id="22d3a-107">參數</span><span class="sxs-lookup"><span data-stu-id="22d3a-107">Parameters</span></span>

<span data-ttu-id="22d3a-108">驅動程式需要下列參數。</span><span class="sxs-lookup"><span data-stu-id="22d3a-108">The driver expects the following parameter.</span></span>



| <span data-ttu-id="22d3a-109">參數</span><span class="sxs-lookup"><span data-stu-id="22d3a-109">Parameter</span></span>                                         | <span data-ttu-id="22d3a-110">VarType</span><span class="sxs-lookup"><span data-stu-id="22d3a-110">VarType</span></span>        | <span data-ttu-id="22d3a-111">Description</span><span class="sxs-lookup"><span data-stu-id="22d3a-111">Description</span></span>                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="22d3a-112">**WPD \_ 屬性 \_ 物件 \_ 屬性 \_ 物件 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="22d3a-112">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_OBJECT\_ID**</span></span> | <span data-ttu-id="22d3a-113">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="22d3a-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="22d3a-114">必要。</span><span class="sxs-lookup"><span data-stu-id="22d3a-114">Required.</span></span> <span data-ttu-id="22d3a-115">包含所要求之屬性的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="22d3a-115">The ID of the object that contains the requested properties.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="22d3a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="22d3a-116">Return Value</span></span>

<span data-ttu-id="22d3a-117">驅動程式應該會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="22d3a-117">The driver should return the following results.</span></span>



| <span data-ttu-id="22d3a-118">結果</span><span class="sxs-lookup"><span data-stu-id="22d3a-118">Result</span></span>                                                | <span data-ttu-id="22d3a-119">VarType</span><span class="sxs-lookup"><span data-stu-id="22d3a-119">VarType</span></span>         | <span data-ttu-id="22d3a-120">Description</span><span class="sxs-lookup"><span data-stu-id="22d3a-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d3a-121">**WPD \_ 屬性 \_ 物件 \_ 屬性 \_ 索引 \_ 鍵**</span><span class="sxs-lookup"><span data-stu-id="22d3a-121">**WPD\_PROPERTY\_OBJECT\_PROPERTIES\_PROPERTY\_KEYS**</span></span> | <span data-ttu-id="22d3a-122">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="22d3a-122">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="22d3a-123">必要。</span><span class="sxs-lookup"><span data-stu-id="22d3a-123">Required.</span></span> <span data-ttu-id="22d3a-124">[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)介面，指定所有支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="22d3a-124">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that specifies all of the supported properties.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="22d3a-125">**WPD \_ 屬性 \_ 通用 \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="22d3a-125">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                    | <span data-ttu-id="22d3a-126">**VT \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="22d3a-126">**VT\_ERROR**</span></span>   | <span data-ttu-id="22d3a-127">必要。</span><span class="sxs-lookup"><span data-stu-id="22d3a-127">Required.</span></span> <span data-ttu-id="22d3a-128">表示整體成功或失敗的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="22d3a-128">An **HRESULT** value that indicates overall success or failure.</span></span> <span data-ttu-id="22d3a-129">可能的結果值包括 [Windows 可攜式裝置錯誤碼](error-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="22d3a-129">Possible result values include [Windows Portable Devices error codes](error-constants.md).</span></span> <span data-ttu-id="22d3a-130">如果呼叫端提出不正確要求，驅動程式應該 **\_ 從 WIN32 傳回 HRESULT \_ (\_ 不支援的錯誤 \_)** 但不需要傳回任何其他結果值。</span><span class="sxs-lookup"><span data-stu-id="22d3a-130">If the caller makes an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** but is otherwise not required to return any other result value.</span></span> |
| <span data-ttu-id="22d3a-131">**WPD \_ 屬性 \_ 常見的 \_ 驅動程式 \_ 錯誤碼 \_**</span><span class="sxs-lookup"><span data-stu-id="22d3a-131">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>        | <span data-ttu-id="22d3a-132">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="22d3a-132">**VT\_UI4**</span></span>     | <span data-ttu-id="22d3a-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="22d3a-133">Optional.</span></span> <span data-ttu-id="22d3a-134">驅動程式特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="22d3a-134">A driver-specific error code.</span></span> <span data-ttu-id="22d3a-135">這通常只用于驅動程式測試，或者驅動程式、裝置和用戶端都是一起設計的。</span><span class="sxs-lookup"><span data-stu-id="22d3a-135">This is typically used only for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="22d3a-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="22d3a-136">Requirements</span></span>



| <span data-ttu-id="22d3a-137">需求</span><span class="sxs-lookup"><span data-stu-id="22d3a-137">Requirement</span></span> | <span data-ttu-id="22d3a-138">值</span><span class="sxs-lookup"><span data-stu-id="22d3a-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d3a-139">標頭</span><span class="sxs-lookup"><span data-stu-id="22d3a-139">Header</span></span><br/> | <dl> <span data-ttu-id="22d3a-140"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="22d3a-140"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d3a-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22d3a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d3a-142">**命令**</span><span class="sxs-lookup"><span data-stu-id="22d3a-142">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




