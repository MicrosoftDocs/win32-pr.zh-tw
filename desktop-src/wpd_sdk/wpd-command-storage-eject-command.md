---
description: WPD \_ 命令 \_ 儲存體 \_ 退出命令會彈出可由電腦從遠端彈出的儲存媒體。
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: 'WPD_COMMAND_STORAGE_EJECT 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3eab2c6296b957b8edf1d65f21264cb93144aeb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978424"
---
# <a name="wpd_command_storage_eject-command"></a><span data-ttu-id="00371-103">WPD \_ 命令 \_ 儲存體 \_ 退出命令</span><span class="sxs-lookup"><span data-stu-id="00371-103">WPD\_COMMAND\_STORAGE\_EJECT Command</span></span>

<span data-ttu-id="00371-104">**WPD \_ 命令 \_ 儲存體 \_ 退出** 命令會彈出可由電腦從遠端彈出的儲存媒體。</span><span class="sxs-lookup"><span data-stu-id="00371-104">The **WPD\_COMMAND\_STORAGE\_EJECT** command ejects a storage medium that can be ejected remotely by the computer.</span></span>

## <a name="command-category"></a><span data-ttu-id="00371-105">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="00371-105">Command category</span></span>

<span data-ttu-id="00371-106">**WPD \_ 類別 \_ 儲存體**</span><span class="sxs-lookup"><span data-stu-id="00371-106">**WPD\_CATEGORY\_STORAGE**</span></span>

## <a name="parameters"></a><span data-ttu-id="00371-107">參數</span><span class="sxs-lookup"><span data-stu-id="00371-107">Parameters</span></span>

<span data-ttu-id="00371-108">驅動程式需要下列參數。</span><span class="sxs-lookup"><span data-stu-id="00371-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="00371-109">參數</span><span class="sxs-lookup"><span data-stu-id="00371-109">Parameter</span></span>                          | <span data-ttu-id="00371-110">VarType</span><span class="sxs-lookup"><span data-stu-id="00371-110">VarType</span></span>    | <span data-ttu-id="00371-111">Description</span><span class="sxs-lookup"><span data-stu-id="00371-111">Description</span></span>                                             |
|------------------------------------|------------|---------------------------------------------------------|
| <span data-ttu-id="00371-112">WPD \_ 屬性 \_ 儲存體 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="00371-112">WPD\_PROPERTY\_STORAGE\_OBJECT\_ID</span></span> | <span data-ttu-id="00371-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="00371-113">VT\_LPWSTR</span></span> | <span data-ttu-id="00371-114">必要。</span><span class="sxs-lookup"><span data-stu-id="00371-114">Required.</span></span> <span data-ttu-id="00371-115">要退出之儲存物件的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="00371-115">The object ID of the storage object to eject.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="00371-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="00371-116">Return Value</span></span>

<span data-ttu-id="00371-117">驅動程式應該會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="00371-117">The driver should return the following results.</span></span>



| <span data-ttu-id="00371-118">結果</span><span class="sxs-lookup"><span data-stu-id="00371-118">Result</span></span>                                         | <span data-ttu-id="00371-119">VarType</span><span class="sxs-lookup"><span data-stu-id="00371-119">VarType</span></span>   | <span data-ttu-id="00371-120">Description</span><span class="sxs-lookup"><span data-stu-id="00371-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00371-121">**WPD \_ 屬性 \_ 通用 \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00371-121">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="00371-122">VT \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="00371-122">VT\_ERROR</span></span> | <span data-ttu-id="00371-123">必要。</span><span class="sxs-lookup"><span data-stu-id="00371-123">Required.</span></span> <span data-ttu-id="00371-124">**HRESULT** ，表示執行命令的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="00371-124">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="00371-125">如果呼叫端提出不正確要求，驅動程式應該會傳回 **\_ \_ \_ 不 \_ 支援的 WIN32 (錯誤)** ，而且不需要傳回任何其他的結果值。</span><span class="sxs-lookup"><span data-stu-id="00371-125">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="00371-126">錯誤碼包括 [Windows 可攜式裝置錯誤代碼](error-constants.md) 或任何其他適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="00371-126">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="00371-127">**WPD \_ 屬性 \_ 常見的 \_ 驅動程式 \_ 錯誤碼 \_**</span><span class="sxs-lookup"><span data-stu-id="00371-127">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="00371-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="00371-128">VT\_UI4</span></span>   | <span data-ttu-id="00371-129">選擇性。</span><span class="sxs-lookup"><span data-stu-id="00371-129">Optional.</span></span> <span data-ttu-id="00371-130">驅動程式特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="00371-130">A driver-specific error code.</span></span> <span data-ttu-id="00371-131">這通常只會用於驅動程式測試，或者驅動程式、裝置和用戶端都是一起設計的。</span><span class="sxs-lookup"><span data-stu-id="00371-131">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="00371-132">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="00371-132">Calling Methods</span></span>

<span data-ttu-id="00371-133">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="00371-133">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="00371-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="00371-134">Requirements</span></span>



| <span data-ttu-id="00371-135">需求</span><span class="sxs-lookup"><span data-stu-id="00371-135">Requirement</span></span> | <span data-ttu-id="00371-136">值</span><span class="sxs-lookup"><span data-stu-id="00371-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="00371-137">標頭</span><span class="sxs-lookup"><span data-stu-id="00371-137">Header</span></span><br/> | <dl> <span data-ttu-id="00371-138"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="00371-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00371-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00371-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00371-140">**命令**</span><span class="sxs-lookup"><span data-stu-id="00371-140">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




