---
description: WPD \_ 命令 \_ sms SEND 命令會透過 \_ sms 功能物件，起始傳送短訊息服務 (sms) 訊息。
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: 'WPD_COMMAND_SMS_SEND 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982956"
---
# <a name="wpd_command_sms_send-command"></a><span data-ttu-id="5a128-103">WPD \_ 命令 \_ SMS \_ SEND 命令</span><span class="sxs-lookup"><span data-stu-id="5a128-103">WPD\_COMMAND\_SMS\_SEND Command</span></span>

<span data-ttu-id="5a128-104">**WPD \_ 命令 \_ sms \_ SEND** 命令會透過 sms 功能物件，起始傳送短訊息服務 (sms) 訊息。</span><span class="sxs-lookup"><span data-stu-id="5a128-104">The **WPD\_COMMAND\_SMS\_SEND** command initiates the sending of a short message service (SMS) message by an SMS functional object.</span></span>

## <a name="command-category"></a><span data-ttu-id="5a128-105">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="5a128-105">Command category</span></span>

<span data-ttu-id="5a128-106">**WPD \_ 類別 \_ SMS**</span><span class="sxs-lookup"><span data-stu-id="5a128-106">**WPD\_CATEGORY\_SMS**</span></span>

## <a name="parameters"></a><span data-ttu-id="5a128-107">參數</span><span class="sxs-lookup"><span data-stu-id="5a128-107">Parameters</span></span>

<span data-ttu-id="5a128-108">驅動程式需要下列參數。</span><span class="sxs-lookup"><span data-stu-id="5a128-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="5a128-109">參數</span><span class="sxs-lookup"><span data-stu-id="5a128-109">Parameter</span></span>                              | <span data-ttu-id="5a128-110">VarType</span><span class="sxs-lookup"><span data-stu-id="5a128-110">VarType</span></span>             | <span data-ttu-id="5a128-111">Description</span><span class="sxs-lookup"><span data-stu-id="5a128-111">Description</span></span>                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a128-112">WPD \_ 屬性 \_ 通用 \_ 命令 \_ 目標</span><span class="sxs-lookup"><span data-stu-id="5a128-112">WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET</span></span> | <span data-ttu-id="5a128-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5a128-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="5a128-114">必要。</span><span class="sxs-lookup"><span data-stu-id="5a128-114">Required.</span></span> <span data-ttu-id="5a128-115">應傳送訊息之 SMS 功能物件的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a128-115">The object ID of the SMS functional object that should send the message.</span></span> <span data-ttu-id="5a128-116">不同的 SMS 功能物件可以有不同的設定。</span><span class="sxs-lookup"><span data-stu-id="5a128-116">Different SMS functional objects can have different settings.</span></span>                                                                                     |
| <span data-ttu-id="5a128-117">WPD \_ 屬性 \_ SMS \_ 收件者</span><span class="sxs-lookup"><span data-stu-id="5a128-117">WPD\_PROPERTY\_SMS\_RECIPIENT</span></span>          | <span data-ttu-id="5a128-118">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5a128-118">VT\_LPWSTR</span></span>          | <span data-ttu-id="5a128-119">必要。</span><span class="sxs-lookup"><span data-stu-id="5a128-119">Required.</span></span> <span data-ttu-id="5a128-120">收件者的 URI。</span><span class="sxs-lookup"><span data-stu-id="5a128-120">The URI of the recipient.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="5a128-121">WPD \_ 屬性 \_ SMS \_ 訊息 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="5a128-121">WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE</span></span>      | <span data-ttu-id="5a128-122">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="5a128-122">VT\_UI4</span></span>             | <span data-ttu-id="5a128-123">必要。</span><span class="sxs-lookup"><span data-stu-id="5a128-123">Required.</span></span> <span data-ttu-id="5a128-124">指出訊息類型 (文字或二進位) 的 [**SMS \_ 訊息 \_ 類型**](sms-message-types.md) 列舉值。</span><span class="sxs-lookup"><span data-stu-id="5a128-124">An [**SMS\_MESSAGE\_TYPES**](sms-message-types.md) enumerator that indicates the type of message (text or binary).</span></span>                                                                                                        |
| <span data-ttu-id="5a128-125">WPD \_ 屬性 \_ SMS \_ 文字 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="5a128-125">WPD\_PROPERTY\_SMS\_TEXT\_MESSAGE</span></span>      | <span data-ttu-id="5a128-126">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5a128-126">VT\_LPWSTR</span></span>          | <span data-ttu-id="5a128-127">選擇性。</span><span class="sxs-lookup"><span data-stu-id="5a128-127">Optional.</span></span> <span data-ttu-id="5a128-128">如果 **WPD \_ 屬性 \_ SMS \_ 訊息 \_ 類型** 指出文字訊息，這就是訊息字串; 否則，就不會包含此參數。</span><span class="sxs-lookup"><span data-stu-id="5a128-128">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a text message, this is the message string; otherwise, this parameter is not included.</span></span>                                                                                  |
| <span data-ttu-id="5a128-129">WPD \_ 屬性 \_ SMS \_ 二進位 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="5a128-129">WPD\_PROPERTY\_SMS\_BINARY\_MESSAGE</span></span>    | <span data-ttu-id="5a128-130">VT \_ 向量 \| vt \_ UI1</span><span class="sxs-lookup"><span data-stu-id="5a128-130">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="5a128-131">選擇性。</span><span class="sxs-lookup"><span data-stu-id="5a128-131">Optional.</span></span> <span data-ttu-id="5a128-132">如果 **WPD \_ 屬性 \_ SMS \_ 訊息 \_ 類型** 指出二進位訊息，這就是位元組陣列的指標; 否則不會包含此參數。</span><span class="sxs-lookup"><span data-stu-id="5a128-132">If **WPD\_PROPERTY\_SMS\_MESSAGE\_TYPE** indicates a binary message, this is a pointer to an array of bytes; otherwise, this parameter is not included.</span></span> <span data-ttu-id="5a128-133">值的第一個 DWORD 是陣列的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5a128-133">The first DWORD of the value is the length of the array, in bytes.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="5a128-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a128-134">Return Value</span></span>

<span data-ttu-id="5a128-135">驅動程式應該會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="5a128-135">The driver should return the following results.</span></span>



| <span data-ttu-id="5a128-136">結果</span><span class="sxs-lookup"><span data-stu-id="5a128-136">Result</span></span>                                         | <span data-ttu-id="5a128-137">VarType</span><span class="sxs-lookup"><span data-stu-id="5a128-137">VarType</span></span>   | <span data-ttu-id="5a128-138">Description</span><span class="sxs-lookup"><span data-stu-id="5a128-138">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a128-139">**WPD \_ 屬性 \_ 通用 \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5a128-139">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>             | <span data-ttu-id="5a128-140">VT \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="5a128-140">VT\_ERROR</span></span> | <span data-ttu-id="5a128-141">必要。</span><span class="sxs-lookup"><span data-stu-id="5a128-141">Required.</span></span> <span data-ttu-id="5a128-142">**HRESULT** ，表示執行命令的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="5a128-142">An **HRESULT** that indicates success or failure to carry out the command.</span></span> <span data-ttu-id="5a128-143">如果呼叫端提出不正確要求，驅動程式應該會傳回 **\_ \_ \_ 不 \_ 支援的 WIN32 (錯誤)** ，而且不需要傳回任何其他的結果值。</span><span class="sxs-lookup"><span data-stu-id="5a128-143">If the caller is making an invalid request, the driver should return **HRESULT\_FROM\_WIN32(ERROR\_NOT\_SUPPORTED)** and is not required to return any other result values.</span></span> <span data-ttu-id="5a128-144">錯誤碼包括 [Windows 可攜式裝置錯誤代碼](error-constants.md) 或任何其他適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5a128-144">Error codes include [Windows Portable Devices error codes](error-constants.md) or any other appropriate error codes.</span></span> |
| <span data-ttu-id="5a128-145">**WPD \_ 屬性 \_ 常見的 \_ 驅動程式 \_ 錯誤碼 \_**</span><span class="sxs-lookup"><span data-stu-id="5a128-145">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span> | <span data-ttu-id="5a128-146">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="5a128-146">VT\_UI4</span></span>   | <span data-ttu-id="5a128-147">選擇性。</span><span class="sxs-lookup"><span data-stu-id="5a128-147">Optional.</span></span> <span data-ttu-id="5a128-148">驅動程式特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5a128-148">A driver-specific error code.</span></span> <span data-ttu-id="5a128-149">這通常只會用於驅動程式測試，或者驅動程式、裝置和用戶端都是一起設計的。</span><span class="sxs-lookup"><span data-stu-id="5a128-149">This is typically only used for driver testing, or if the driver, device, and client are all designed together.</span></span>                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a><span data-ttu-id="5a128-150">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="5a128-150">Calling Methods</span></span>

<span data-ttu-id="5a128-151">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="5a128-151">Can only be called directly using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a128-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a128-152">Requirements</span></span>



| <span data-ttu-id="5a128-153">需求</span><span class="sxs-lookup"><span data-stu-id="5a128-153">Requirement</span></span> | <span data-ttu-id="5a128-154">值</span><span class="sxs-lookup"><span data-stu-id="5a128-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a128-155">標頭</span><span class="sxs-lookup"><span data-stu-id="5a128-155">Header</span></span><br/> | <dl> <span data-ttu-id="5a128-156"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a128-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a128-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a128-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a128-158">**命令**</span><span class="sxs-lookup"><span data-stu-id="5a128-158">**Commands**</span></span>](commands.md)
</dt> </dl>

 

 




