---
description: WPD \_ 命令 \_ 仍為 \_ image CAPTURE 啟始命令啟始仍 \_ \_ 有影像功能物件的靜止影像捕捉。 如果由於拍攝圖片而建立新的物件，驅動程式應該傳送 WPD \_ 事件 \_ 物件 \_ 新增事件。
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: 'WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976278"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a><span data-ttu-id="4af7f-104">WPD \_ 命令 \_ 仍為 \_ 影像 \_ 捕捉 \_ 起始命令</span><span class="sxs-lookup"><span data-stu-id="4af7f-104">WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE Command</span></span>

<span data-ttu-id="4af7f-105">**WPD \_ 命令仍 \_ 為 \_ image \_ CAPTURE \_** 啟始命令啟始仍有影像功能物件的靜止影像捕捉。</span><span class="sxs-lookup"><span data-stu-id="4af7f-105">The **WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE** command initiates a still image capture by a still image functional object.</span></span> <span data-ttu-id="4af7f-106">如果由於拍攝圖片而建立新的物件，驅動程式應該傳送 **WPD \_ 事件 \_ 物件 \_ 新增** 事件。</span><span class="sxs-lookup"><span data-stu-id="4af7f-106">If a new object is created as a result of taking a picture, the driver should send the **WPD\_EVENT\_OBJECT\_ADDED** event.</span></span>

## <a name="command-category"></a><span data-ttu-id="4af7f-107">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="4af7f-107">Command category</span></span>

<span data-ttu-id="4af7f-108">**WPD \_ 類別 \_ 仍為 \_ 影像 \_ 捕捉**</span><span class="sxs-lookup"><span data-stu-id="4af7f-108">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span>

## <a name="parameters"></a><span data-ttu-id="4af7f-109">參數</span><span class="sxs-lookup"><span data-stu-id="4af7f-109">Parameters</span></span>

<span data-ttu-id="4af7f-110">驅動程式需要下列參數。</span><span class="sxs-lookup"><span data-stu-id="4af7f-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="4af7f-111">參數</span><span class="sxs-lookup"><span data-stu-id="4af7f-111">Parameter</span></span>                              | <span data-ttu-id="4af7f-112">VarType</span><span class="sxs-lookup"><span data-stu-id="4af7f-112">VarType</span></span>    | <span data-ttu-id="4af7f-113">Description</span><span class="sxs-lookup"><span data-stu-id="4af7f-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4af7f-114">WPD \_ 屬性 \_ 通用 \_ 命令 \_ 目標</span><span class="sxs-lookup"><span data-stu-id="4af7f-114">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="4af7f-115">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4af7f-115">VT\_LPWSTR</span></span> | <span data-ttu-id="4af7f-116">必要。</span><span class="sxs-lookup"><span data-stu-id="4af7f-116">Required.</span></span> <span data-ttu-id="4af7f-117">裝置上的靜止影像捕捉功能物件的物件識別碼，該物件應該拍攝圖片。每個仍為「影像捕捉」功能的物件可以有不同的設定，而且可能會參考裝置上的不同硬體 (例如，電話的前或後置相機) ，而此參數會指出要使用哪一個。</span><span class="sxs-lookup"><span data-stu-id="4af7f-117">The object ID of the still image capture functional object on the device that should take the picture.Each still image capture functional object can have different settings, and may refer to different hardware on a device (for example, a front or back camera of a phone), and this parameter indicates which one to use.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4af7f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="4af7f-118">Return Value</span></span>

<span data-ttu-id="4af7f-119">驅動程式應該會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="4af7f-119">The driver should return the following results.</span></span>



| <span data-ttu-id="4af7f-120">結果</span><span class="sxs-lookup"><span data-stu-id="4af7f-120">Result</span></span>                                         | <span data-ttu-id="4af7f-121">VarType</span><span class="sxs-lookup"><span data-stu-id="4af7f-121">VarType</span></span>   | <span data-ttu-id="4af7f-122">Description</span><span class="sxs-lookup"><span data-stu-id="4af7f-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4af7f-123">**WPD \_ 屬性 \_ 通用 \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4af7f-123">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="4af7f-124">VT \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="4af7f-124">VT\_ERROR</span></span> | <span data-ttu-id="4af7f-125">必要。</span><span class="sxs-lookup"><span data-stu-id="4af7f-125">Required.</span></span> <span data-ttu-id="4af7f-126">**HRESULT** ，表示執行命令的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="4af7f-126">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="4af7f-127">如果呼叫端提出不正確要求，驅動程式應該會傳回 **\_ \_ \_ 不 \_ 支援的 WIN32 (錯誤)** ，而且不需要傳回任何其他的結果值。</span><span class="sxs-lookup"><span data-stu-id="4af7f-127">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="4af7f-128">錯誤碼包括 [Windows 可攜式裝置錯誤代碼](error-constants.md) 或任何其他適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4af7f-128">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="4af7f-129">**WPD \_ 屬性 \_ 常見的 \_ 驅動程式 \_ 錯誤碼 \_**</span><span class="sxs-lookup"><span data-stu-id="4af7f-129">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="4af7f-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="4af7f-130">VT\_UI4</span></span>   | <span data-ttu-id="4af7f-131">選擇性。</span><span class="sxs-lookup"><span data-stu-id="4af7f-131">Optional.</span></span> <span data-ttu-id="4af7f-132">驅動程式特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4af7f-132">A driver-specific error code.</span></span> <span data-ttu-id="4af7f-133">裝置廠商通常會使用此值，在使用其應用程式時改善裝置錯誤診斷。</span><span class="sxs-lookup"><span data-stu-id="4af7f-133">This value is typically used by device vendors to improve diagnosis of device errors while using their applications.</span></span> <span data-ttu-id="4af7f-134">一般用途的應用程式會忽略它，而只依賴 WPD \_ 屬性 \_ 通用的 \_ HRESULT。</span><span class="sxs-lookup"><span data-stu-id="4af7f-134">General purpose applications would ignore it and rely solely on WPD\_PROPERTY\_COMMON\_HRESULT instead.</span></span>                                                                                                                   |



 

## <a name="calling-methods"></a><span data-ttu-id="4af7f-135">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="4af7f-135">Calling Methods</span></span>

<span data-ttu-id="4af7f-136">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="4af7f-136">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="4af7f-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="4af7f-137">Requirements</span></span>



| <span data-ttu-id="4af7f-138">需求</span><span class="sxs-lookup"><span data-stu-id="4af7f-138">Requirement</span></span> | <span data-ttu-id="4af7f-139">值</span><span class="sxs-lookup"><span data-stu-id="4af7f-139">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4af7f-140">標頭</span><span class="sxs-lookup"><span data-stu-id="4af7f-140">Header</span></span><br/> | <dl> <span data-ttu-id="4af7f-141"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="4af7f-141"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4af7f-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4af7f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4af7f-143">**命令**</span><span class="sxs-lookup"><span data-stu-id="4af7f-143">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




