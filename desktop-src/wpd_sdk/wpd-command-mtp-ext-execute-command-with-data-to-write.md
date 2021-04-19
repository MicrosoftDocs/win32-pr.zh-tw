---
description: WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ 要寫入的資料 \_ \_ 命令會傳送 MTP 命令區塊，後面接著資料階段。 資料會從主機傳送到裝置。
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: 'WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999430"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a><span data-ttu-id="90dc3-104">WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ \_ 要寫入的資料 \_ 命令</span><span class="sxs-lookup"><span data-stu-id="90dc3-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE Command</span></span>

<span data-ttu-id="90dc3-105">**WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ \_ 要 \_ 寫入的資料** 命令會傳送 MTP 命令區塊，後面接著資料階段。</span><span class="sxs-lookup"><span data-stu-id="90dc3-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command sends an MTP command block, which is followed by a data phase.</span></span> <span data-ttu-id="90dc3-106">資料會從主機傳送到裝置。</span><span class="sxs-lookup"><span data-stu-id="90dc3-106">The data is sent from the host to the device.</span></span>

## <a name="command-category"></a><span data-ttu-id="90dc3-107">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="90dc3-107">Command category</span></span>

<span data-ttu-id="90dc3-108">**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="90dc3-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="90dc3-109">參數</span><span class="sxs-lookup"><span data-stu-id="90dc3-109">Parameters</span></span>

<span data-ttu-id="90dc3-110">驅動程式需要下列參數。</span><span class="sxs-lookup"><span data-stu-id="90dc3-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="90dc3-111">參數</span><span class="sxs-lookup"><span data-stu-id="90dc3-111">Parameter</span></span>                                                | <span data-ttu-id="90dc3-112">VarType</span><span class="sxs-lookup"><span data-stu-id="90dc3-112">VarType</span></span> | <span data-ttu-id="90dc3-113">Description</span><span class="sxs-lookup"><span data-stu-id="90dc3-113">Description</span></span>                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90dc3-114">**WPD \_ 屬性 \_ MTP \_ EXT \_ 操作 \_ 碼**</span><span class="sxs-lookup"><span data-stu-id="90dc3-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>             | <span data-ttu-id="90dc3-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="90dc3-115">VT\_UI4</span></span> | <span data-ttu-id="90dc3-116">必要。</span><span class="sxs-lookup"><span data-stu-id="90dc3-116">Required.</span></span> <span data-ttu-id="90dc3-117">識別廠商延伸的 MTP 作業程式碼。</span><span class="sxs-lookup"><span data-stu-id="90dc3-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                              |
| <span data-ttu-id="90dc3-118">**WPD \_ 屬性 \_ MTP \_ EXT \_ 操作 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="90dc3-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span>           | <span data-ttu-id="90dc3-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="90dc3-119">VT\_UI4</span></span> | <span data-ttu-id="90dc3-120">必要。</span><span class="sxs-lookup"><span data-stu-id="90dc3-120">Required.</span></span> <span data-ttu-id="90dc3-121">**IPortableDevicePropVariantCollection** 集合，識別廠商作業程式碼的必要參數。</span><span class="sxs-lookup"><span data-stu-id="90dc3-121">An **IPortableDevicePropVariantCollection** collection that identifies the required parameters for the vendor operation code.</span></span> |
| <span data-ttu-id="90dc3-122">**WPD \_ 屬性 \_ MTP \_ EXT \_ TRANSFER \_ TOTAL \_ DATA \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="90dc3-122">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span> | <span data-ttu-id="90dc3-123">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="90dc3-123">VT\_UI8</span></span> | <span data-ttu-id="90dc3-124">必要項。指定要傳送至裝置的資料大小總計（以位元組為單位），不包括任何額外負荷。</span><span class="sxs-lookup"><span data-stu-id="90dc3-124">Required.Specifies the total data size, in bytes, excluding any overhead, to be sent to device.</span></span>                                         |



 

## <a name="return-value"></a><span data-ttu-id="90dc3-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="90dc3-125">Return Value</span></span>

<span data-ttu-id="90dc3-126">驅動程式會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="90dc3-126">The driver returns the following results.</span></span>



| <span data-ttu-id="90dc3-127">結果</span><span class="sxs-lookup"><span data-stu-id="90dc3-127">Result</span></span>                                                       | <span data-ttu-id="90dc3-128">VarType</span><span class="sxs-lookup"><span data-stu-id="90dc3-128">VarType</span></span>    | <span data-ttu-id="90dc3-129">Description</span><span class="sxs-lookup"><span data-stu-id="90dc3-129">Description</span></span>                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90dc3-130">**WPD \_ 屬性 \_ MTP \_ EXT 最 \_ 理想的 \_ 傳輸 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="90dc3-130">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="90dc3-131">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="90dc3-131">VT\_UI4</span></span>    | <span data-ttu-id="90dc3-132">必要。</span><span class="sxs-lookup"><span data-stu-id="90dc3-132">Required.</span></span> <span data-ttu-id="90dc3-133">指定傳輸緩衝區的最佳大小。</span><span class="sxs-lookup"><span data-stu-id="90dc3-133">Specifies the optimal size of the transfer buffer.</span></span>                       |
| <span data-ttu-id="90dc3-134">**WPD \_ 屬性 \_ MTP \_ EXT EXT \_ 傳送 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="90dc3-134">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="90dc3-135">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="90dc3-135">VT\_LPWSTR</span></span> | <span data-ttu-id="90dc3-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="90dc3-136">Optional.</span></span> <span data-ttu-id="90dc3-137">驅動程式用來進行後續資料傳輸的內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="90dc3-137">A context identifier that the driver uses for subsequent data transfers.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="90dc3-138">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="90dc3-138">Calling Methods</span></span>

<span data-ttu-id="90dc3-139">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="90dc3-139">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="90dc3-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="90dc3-140">Requirements</span></span>



| <span data-ttu-id="90dc3-141">需求</span><span class="sxs-lookup"><span data-stu-id="90dc3-141">Requirement</span></span> | <span data-ttu-id="90dc3-142">值</span><span class="sxs-lookup"><span data-stu-id="90dc3-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="90dc3-143">標頭</span><span class="sxs-lookup"><span data-stu-id="90dc3-143">Header</span></span><br/> | <dl> <span data-ttu-id="90dc3-144"><dt>WpdMtpExtensions。h</dt></span><span class="sxs-lookup"><span data-stu-id="90dc3-144"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90dc3-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90dc3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90dc3-146">支援 MTP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="90dc3-146">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




