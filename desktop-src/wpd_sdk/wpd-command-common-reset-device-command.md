---
description: WPD \_ 命令 \_ 一般 \_ 重設 \_ 裝置命令會重設裝置。 這並不表示重新格式化;這相當於關閉和開啟裝置。
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: 'WPD_COMMAND_COMMON_RESET_DEVICE 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984476"
---
# <a name="wpd_command_common_reset_device-command"></a><span data-ttu-id="c9dcc-104">WPD \_ 命令 \_ 一般 \_ 重設 \_ 裝置命令</span><span class="sxs-lookup"><span data-stu-id="c9dcc-104">WPD\_COMMAND\_COMMON\_RESET\_DEVICE Command</span></span>

<span data-ttu-id="c9dcc-105">**WPD \_ 命令 \_ 一般 \_ 重設 \_ 裝置** 命令會重設裝置。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-105">The **WPD\_COMMAND\_COMMON\_RESET\_DEVICE** command resets the device.</span></span> <span data-ttu-id="c9dcc-106">這並不表示重新格式化;這相當於關閉和開啟裝置。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-106">This does not mean reformatting; it is equivalent to turning the device off and on again.</span></span>

## <a name="command-category"></a><span data-ttu-id="c9dcc-107">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="c9dcc-107">Command category</span></span>

<span data-ttu-id="c9dcc-108">**WPD \_ 類別 \_ 通用**</span><span class="sxs-lookup"><span data-stu-id="c9dcc-108">**WPD\_CATEGORY\_COMMON**</span></span>

## <a name="parameters"></a><span data-ttu-id="c9dcc-109">參數</span><span class="sxs-lookup"><span data-stu-id="c9dcc-109">Parameters</span></span>

<span data-ttu-id="c9dcc-110">此命令沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9dcc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9dcc-111">Return Value</span></span>

<span data-ttu-id="c9dcc-112">驅動程式應該會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-112">The driver should return the following results.</span></span>



| <span data-ttu-id="c9dcc-113">結果</span><span class="sxs-lookup"><span data-stu-id="c9dcc-113">Result</span></span>                                         | <span data-ttu-id="c9dcc-114">VarType</span><span class="sxs-lookup"><span data-stu-id="c9dcc-114">VarType</span></span>   | <span data-ttu-id="c9dcc-115">Description</span><span class="sxs-lookup"><span data-stu-id="c9dcc-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9dcc-116">**WPD \_ 屬性 \_ 通用 \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c9dcc-116">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="c9dcc-117">VT \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="c9dcc-117">VT\_ERROR</span></span> | <span data-ttu-id="c9dcc-118">必要。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-118">Required.</span></span> <span data-ttu-id="c9dcc-119">**HRESULT** ，表示執行命令的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-119">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="c9dcc-120">如果呼叫端提出不正確要求，驅動程式應該會傳回 **\_ \_ \_ 不 \_ 支援的 WIN32 (錯誤)** ，而且不需要傳回任何其他的結果值。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-120">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="c9dcc-121">錯誤碼包括 [Windows 可攜式裝置錯誤代碼](error-constants.md) 或任何其他適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-121">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="c9dcc-122">**WPD \_ 屬性 \_ 常見的 \_ 驅動程式 \_ 錯誤碼 \_**</span><span class="sxs-lookup"><span data-stu-id="c9dcc-122">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="c9dcc-123">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="c9dcc-123">VT\_UI4</span></span>   | <span data-ttu-id="c9dcc-124">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-124">Optional.</span></span> <span data-ttu-id="c9dcc-125">驅動程式特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-125">A driver-specific error code.</span></span> <span data-ttu-id="c9dcc-126">這通常只會用於驅動程式測試，或者驅動程式、裝置和用戶端都是一起設計的。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-126">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="c9dcc-127">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="c9dcc-127">Calling Methods</span></span>

<span data-ttu-id="c9dcc-128">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="c9dcc-128">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9dcc-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9dcc-129">Requirements</span></span>



| <span data-ttu-id="c9dcc-130">需求</span><span class="sxs-lookup"><span data-stu-id="c9dcc-130">Requirement</span></span> | <span data-ttu-id="c9dcc-131">值</span><span class="sxs-lookup"><span data-stu-id="c9dcc-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9dcc-132">標頭</span><span class="sxs-lookup"><span data-stu-id="c9dcc-132">Header</span></span><br/> | <dl> <span data-ttu-id="c9dcc-133"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9dcc-133"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9dcc-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9dcc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9dcc-135">**命令**</span><span class="sxs-lookup"><span data-stu-id="c9dcc-135">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




