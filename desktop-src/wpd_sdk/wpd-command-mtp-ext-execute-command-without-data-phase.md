---
description: '\_ \_ \_ 沒有資料階段命令的 WPD 命令 MTP EXT \_ EXECUTE \_ 命令 \_ 會傳送 \_ \_ MTP 命令區塊。 沒有與此命令相關聯的後續資料階段。'
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: 'WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58648547c33206e1de19c14aea48427bc9db0be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998653"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a><span data-ttu-id="e03c0-104">\_ \_ \_ \_ \_ \_ 未包含 \_ 資料 \_ 階段命令的 WPD 命令 MTP EXT EXECUTE 命令</span><span class="sxs-lookup"><span data-stu-id="e03c0-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE Command</span></span>

<span data-ttu-id="e03c0-105">**\_ \_ \_ \_ \_ \_ 沒有 \_ 資料 \_ 階段命令的 WPD 命令 MTP EXT EXECUTE 命令會** 傳送 MTP 命令區塊。</span><span class="sxs-lookup"><span data-stu-id="e03c0-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE** command sends an MTP command block.</span></span> <span data-ttu-id="e03c0-106">沒有與此命令相關聯的後續資料階段。</span><span class="sxs-lookup"><span data-stu-id="e03c0-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="e03c0-107">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="e03c0-107">Command category</span></span>

<span data-ttu-id="e03c0-108">**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="e03c0-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="e03c0-109">參數</span><span class="sxs-lookup"><span data-stu-id="e03c0-109">Parameters</span></span>

<span data-ttu-id="e03c0-110">驅動程式需要下列參數。</span><span class="sxs-lookup"><span data-stu-id="e03c0-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="e03c0-111">參數</span><span class="sxs-lookup"><span data-stu-id="e03c0-111">Parameter</span></span>                                      | <span data-ttu-id="e03c0-112">VarType</span><span class="sxs-lookup"><span data-stu-id="e03c0-112">VarType</span></span> | <span data-ttu-id="e03c0-113">Description</span><span class="sxs-lookup"><span data-stu-id="e03c0-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e03c0-114">**WPD \_ 屬性 \_ MTP \_ EXT \_ 操作 \_ 碼**</span><span class="sxs-lookup"><span data-stu-id="e03c0-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="e03c0-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e03c0-115">VT\_UI4</span></span> | <span data-ttu-id="e03c0-116">必要。</span><span class="sxs-lookup"><span data-stu-id="e03c0-116">Required.</span></span> <span data-ttu-id="e03c0-117">識別廠商延伸的 MTP 作業程式碼。</span><span class="sxs-lookup"><span data-stu-id="e03c0-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="e03c0-118">**WPD \_ 屬性 \_ MTP \_ EXT \_ 操作 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="e03c0-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="e03c0-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e03c0-119">VT\_UI4</span></span> | <span data-ttu-id="e03c0-120">必要。</span><span class="sxs-lookup"><span data-stu-id="e03c0-120">Required.</span></span> <span data-ttu-id="e03c0-121">**IPortableDevicePropVariantCollection**，識別廠商作業程式碼的必要參數。</span><span class="sxs-lookup"><span data-stu-id="e03c0-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="e03c0-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="e03c0-122">Return Value</span></span>

<span data-ttu-id="e03c0-123">驅動程式會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="e03c0-123">The driver returns the following results.</span></span>



| <span data-ttu-id="e03c0-124">結果</span><span class="sxs-lookup"><span data-stu-id="e03c0-124">Result</span></span>                                        | <span data-ttu-id="e03c0-125">VarType</span><span class="sxs-lookup"><span data-stu-id="e03c0-125">VarType</span></span> | <span data-ttu-id="e03c0-126">Description</span><span class="sxs-lookup"><span data-stu-id="e03c0-126">Description</span></span>                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e03c0-127">**WPD \_ 屬性 \_ MTP \_ EXT \_ 回應 \_ 碼**</span><span class="sxs-lookup"><span data-stu-id="e03c0-127">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="e03c0-128">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e03c0-128">VT\_UI4</span></span> | <span data-ttu-id="e03c0-129">必要。</span><span class="sxs-lookup"><span data-stu-id="e03c0-129">Required.</span></span> <span data-ttu-id="e03c0-130">廠商作業程式碼的回應碼。</span><span class="sxs-lookup"><span data-stu-id="e03c0-130">The response code to the vendor operation code.</span></span>                                                                      |
| <span data-ttu-id="e03c0-131">**WPD \_ 屬性 \_ MTP \_ EXT \_ \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="e03c0-131">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="e03c0-132">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e03c0-132">VT\_UI4</span></span> | <span data-ttu-id="e03c0-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="e03c0-133">Optional.</span></span> <span data-ttu-id="e03c0-134">識別任何回應參數的 **IPortableDevicePropVariantCollection** 。</span><span class="sxs-lookup"><span data-stu-id="e03c0-134">An **IPortableDevicePropVariantCollection** that identifies any response parameters.</span></span> <span data-ttu-id="e03c0-135">此集合可能是空的。</span><span class="sxs-lookup"><span data-stu-id="e03c0-135">This collection might be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="e03c0-136">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="e03c0-136">Calling Methods</span></span>

<span data-ttu-id="e03c0-137">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="e03c0-137">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="e03c0-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="e03c0-138">Requirements</span></span>



| <span data-ttu-id="e03c0-139">需求</span><span class="sxs-lookup"><span data-stu-id="e03c0-139">Requirement</span></span> | <span data-ttu-id="e03c0-140">值</span><span class="sxs-lookup"><span data-stu-id="e03c0-140">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e03c0-141">標頭</span><span class="sxs-lookup"><span data-stu-id="e03c0-141">Header</span></span><br/> | <dl> <span data-ttu-id="e03c0-142"><dt>WpdMtpExtensions。h</dt></span><span class="sxs-lookup"><span data-stu-id="e03c0-142"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e03c0-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e03c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e03c0-144">支援 MTP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="e03c0-144">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




