---
description: WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ 要讀取的資料 \_ \_ 命令會傳送 MTP 命令區塊，後面接著資料階段。  (將資料從裝置傳送至主機。 ) 。
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: 'WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994790"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a><span data-ttu-id="ecc51-104">WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ \_ 要讀取的資料 \_ 命令</span><span class="sxs-lookup"><span data-stu-id="ecc51-104">WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ Command</span></span>

<span data-ttu-id="ecc51-105">**WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ \_ 要 \_ 讀取的資料** 命令會傳送 MTP 命令區塊，後面接著資料階段。</span><span class="sxs-lookup"><span data-stu-id="ecc51-105">The **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ** command sends an MTP command block, which will be followed by a data phase.</span></span> <span data-ttu-id="ecc51-106"> (將資料從裝置傳送至主機。 ) </span><span class="sxs-lookup"><span data-stu-id="ecc51-106">(The data is sent from the device to the host.)</span></span>

## <a name="command-category"></a><span data-ttu-id="ecc51-107">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="ecc51-107">Command category</span></span>

<span data-ttu-id="ecc51-108">**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="ecc51-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="ecc51-109">參數</span><span class="sxs-lookup"><span data-stu-id="ecc51-109">Parameters</span></span>

<span data-ttu-id="ecc51-110">驅動程式需要下列參數。</span><span class="sxs-lookup"><span data-stu-id="ecc51-110">The driver expects the following parameters.</span></span>



| <span data-ttu-id="ecc51-111">參數</span><span class="sxs-lookup"><span data-stu-id="ecc51-111">Parameter</span></span>                                      | <span data-ttu-id="ecc51-112">VarType</span><span class="sxs-lookup"><span data-stu-id="ecc51-112">VarType</span></span> | <span data-ttu-id="ecc51-113">Description</span><span class="sxs-lookup"><span data-stu-id="ecc51-113">Description</span></span>                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc51-114">**WPD \_ 屬性 \_ MTP \_ EXT \_ 操作 \_ 碼**</span><span class="sxs-lookup"><span data-stu-id="ecc51-114">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE**</span></span>   | <span data-ttu-id="ecc51-115">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ecc51-115">VT\_UI4</span></span> | <span data-ttu-id="ecc51-116">必要。</span><span class="sxs-lookup"><span data-stu-id="ecc51-116">Required.</span></span> <span data-ttu-id="ecc51-117">識別廠商延伸的 MTP 作業程式碼。</span><span class="sxs-lookup"><span data-stu-id="ecc51-117">Identifies a vendor-extended MTP operation code.</span></span>                                                                    |
| <span data-ttu-id="ecc51-118">**WPD \_ 屬性 \_ MTP \_ EXT \_ 操作 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="ecc51-118">**WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS**</span></span> | <span data-ttu-id="ecc51-119">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ecc51-119">VT\_UI4</span></span> | <span data-ttu-id="ecc51-120">必要。</span><span class="sxs-lookup"><span data-stu-id="ecc51-120">Required.</span></span> <span data-ttu-id="ecc51-121">**IPortableDevicePropVariantCollection**，識別廠商作業程式碼的必要參數。</span><span class="sxs-lookup"><span data-stu-id="ecc51-121">An **IPortableDevicePropVariantCollection**,which identifies the required parameters for the vendor operation code.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="ecc51-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecc51-122">Return Value</span></span>

<span data-ttu-id="ecc51-123">驅動程式會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="ecc51-123">The driver returns the following results.</span></span>



| <span data-ttu-id="ecc51-124">結果</span><span class="sxs-lookup"><span data-stu-id="ecc51-124">Result</span></span>                                                       | <span data-ttu-id="ecc51-125">VarType</span><span class="sxs-lookup"><span data-stu-id="ecc51-125">VarType</span></span>    | <span data-ttu-id="ecc51-126">Description</span><span class="sxs-lookup"><span data-stu-id="ecc51-126">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc51-127">**WPD \_ 屬性 \_ MTP \_ EXT \_ TRANSFER \_ TOTAL \_ DATA \_ SIZE**</span><span class="sxs-lookup"><span data-stu-id="ecc51-127">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_TOTAL\_DATA\_SIZE**</span></span>     | <span data-ttu-id="ecc51-128">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="ecc51-128">VT\_UI8</span></span>    | <span data-ttu-id="ecc51-129">必要。</span><span class="sxs-lookup"><span data-stu-id="ecc51-129">Required.</span></span> <span data-ttu-id="ecc51-130">傳回資料大小總計（以位元組為單位），不包括任何來自裝置的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="ecc51-130">Returns the total data size, in bytes, excluding any overhead coming from the device.</span></span> <span data-ttu-id="ecc51-131">如果裝置報告未知的 datasize (0xFFFFFFFF) ，驅動程式應該重複呼叫 **ReadData** ，直到收到短的區塊為止</span><span class="sxs-lookup"><span data-stu-id="ecc51-131">If the device reports unknown datasize (0xFFFFFFFF), the driver should call **ReadData** repeatedly until a short chunk is received</span></span> |
| <span data-ttu-id="ecc51-132">**WPD \_ 屬性 \_ MTP \_ EXT 最 \_ 理想的 \_ 傳輸 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="ecc51-132">**WPD\_PROPERTY\_MTP\_EXT\_OPTIMAL\_TRANSFER\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="ecc51-133">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="ecc51-133">VT\_UI4</span></span>    | <span data-ttu-id="ecc51-134">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ecc51-134">Optional.</span></span> <span data-ttu-id="ecc51-135">傳回傳輸緩衝區的最佳大小。</span><span class="sxs-lookup"><span data-stu-id="ecc51-135">Returns the optimal size of the transfer buffer.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="ecc51-136">**WPD \_ 屬性 \_ MTP \_ EXT EXT \_ 傳送 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="ecc51-136">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="ecc51-137">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ecc51-137">VT\_LPWSTR</span></span> | <span data-ttu-id="ecc51-138">必要。</span><span class="sxs-lookup"><span data-stu-id="ecc51-138">Required.</span></span> <span data-ttu-id="ecc51-139">指定後續資料傳輸的內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="ecc51-139">Specifies the context identifier for subsequent data transfers.</span></span>                                                                                                                                                           |



 

## <a name="calling-methods"></a><span data-ttu-id="ecc51-140">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="ecc51-140">Calling Methods</span></span>

<span data-ttu-id="ecc51-141">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="ecc51-141">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc51-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecc51-142">Requirements</span></span>



| <span data-ttu-id="ecc51-143">需求</span><span class="sxs-lookup"><span data-stu-id="ecc51-143">Requirement</span></span> | <span data-ttu-id="ecc51-144">值</span><span class="sxs-lookup"><span data-stu-id="ecc51-144">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc51-145">標頭</span><span class="sxs-lookup"><span data-stu-id="ecc51-145">Header</span></span><br/> | <dl> <span data-ttu-id="ecc51-146"><dt>WpdMtpExtensions。h</dt></span><span class="sxs-lookup"><span data-stu-id="ecc51-146"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecc51-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecc51-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc51-148">支援 MTP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="ecc51-148">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




