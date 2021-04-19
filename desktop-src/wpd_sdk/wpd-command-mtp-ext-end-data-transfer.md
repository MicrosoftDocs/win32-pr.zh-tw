---
description: WPD \_ 命令 \_ MTP \_ EXT \_ END \_ DATA \_ transfer 命令會完成來自裝置的資料傳輸和讀取回應。
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: 'WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001152"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a><span data-ttu-id="9de82-103">WPD \_ 命令 \_ MTP \_ EXT \_ END \_ DATA \_ TRANSFER 命令</span><span class="sxs-lookup"><span data-stu-id="9de82-103">WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER Command</span></span>

<span data-ttu-id="9de82-104">**WPD \_ 命令 \_ MTP \_ EXT \_ END \_ DATA \_ transfer** 命令會完成來自裝置的資料傳輸和讀取回應。</span><span class="sxs-lookup"><span data-stu-id="9de82-104">The **WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER** command completes a data transfer and read response from the device.</span></span> <span data-ttu-id="9de82-105">此傳輸是由 [**WPD \_ 命令 \_ mtp \_ ext \_ execute \_ 命令 \_ 與 \_ data \_ to \_ READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) 命令或 [**WPD \_ 命令 \_ mtp \_ ext \_ execute \_ 命令 \_ 與 \_ data \_ to \_ WRITE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) 命令起始。</span><span class="sxs-lookup"><span data-stu-id="9de82-105">The transfer is initiated by either the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) command or the [**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) command.</span></span>

## <a name="command-category"></a><span data-ttu-id="9de82-106">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="9de82-106">Command category</span></span>

<span data-ttu-id="9de82-107">**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="9de82-107">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="9de82-108">參數</span><span class="sxs-lookup"><span data-stu-id="9de82-108">Parameters</span></span>

<span data-ttu-id="9de82-109">驅動程式需要下列參數。</span><span class="sxs-lookup"><span data-stu-id="9de82-109">The driver expects the following parameters.</span></span>



| <span data-ttu-id="9de82-110">參數</span><span class="sxs-lookup"><span data-stu-id="9de82-110">Parameter</span></span>                                      | <span data-ttu-id="9de82-111">VarType</span><span class="sxs-lookup"><span data-stu-id="9de82-111">VarType</span></span>    | <span data-ttu-id="9de82-112">Description</span><span class="sxs-lookup"><span data-stu-id="9de82-112">Description</span></span>                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9de82-113">**WPD \_ 屬性 \_ MTP \_ EXT EXT \_ 傳送 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="9de82-113">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span> | <span data-ttu-id="9de82-114">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="9de82-114">VT\_LPWSTR</span></span> | <span data-ttu-id="9de82-115">必要。</span><span class="sxs-lookup"><span data-stu-id="9de82-115">Required.</span></span> <span data-ttu-id="9de82-116">識別先前的方法呼叫所傳回的內容。</span><span class="sxs-lookup"><span data-stu-id="9de82-116">Identifies the context that is returned by an earlier method call.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="9de82-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="9de82-117">Return Value</span></span>

<span data-ttu-id="9de82-118">驅動程式會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="9de82-118">The driver returns the following results.</span></span>



| <span data-ttu-id="9de82-119">結果</span><span class="sxs-lookup"><span data-stu-id="9de82-119">Result</span></span>                                        | <span data-ttu-id="9de82-120">VarType</span><span class="sxs-lookup"><span data-stu-id="9de82-120">VarType</span></span> | <span data-ttu-id="9de82-121">Description</span><span class="sxs-lookup"><span data-stu-id="9de82-121">Description</span></span>                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9de82-122">**WPD \_ 屬性 \_ MTP \_ EXT \_ 回應 \_ 碼**</span><span class="sxs-lookup"><span data-stu-id="9de82-122">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**</span></span>   | <span data-ttu-id="9de82-123">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="9de82-123">VT\_UI4</span></span> | <span data-ttu-id="9de82-124">必要的。回應碼為廠商作業程式碼。</span><span class="sxs-lookup"><span data-stu-id="9de82-124">Required.The response code to the vendor operation code.</span></span>                                                                                |
| <span data-ttu-id="9de82-125">**WPD \_ 屬性 \_ MTP \_ EXT \_ \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="9de82-125">**WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS**</span></span> | <span data-ttu-id="9de82-126">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="9de82-126">VT\_UI4</span></span> | <span data-ttu-id="9de82-127">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9de82-127">Optional.</span></span> <span data-ttu-id="9de82-128">識別任何回應參數的 **IPortableDevicePropVariantCollection** 集合。</span><span class="sxs-lookup"><span data-stu-id="9de82-128">An **IPortableDevicePropVariantCollection** collection that identifies any response parameters.</span></span> <span data-ttu-id="9de82-129">此集合可以是空的。</span><span class="sxs-lookup"><span data-stu-id="9de82-129">This collection can be empty.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="9de82-130">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="9de82-130">Calling Methods</span></span>

<span data-ttu-id="9de82-131">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="9de82-131">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="9de82-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="9de82-132">Requirements</span></span>



| <span data-ttu-id="9de82-133">需求</span><span class="sxs-lookup"><span data-stu-id="9de82-133">Requirement</span></span> | <span data-ttu-id="9de82-134">值</span><span class="sxs-lookup"><span data-stu-id="9de82-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9de82-135">標頭</span><span class="sxs-lookup"><span data-stu-id="9de82-135">Header</span></span><br/> | <dl> <span data-ttu-id="9de82-136"><dt>WpdMtpExtensions。h</dt></span><span class="sxs-lookup"><span data-stu-id="9de82-136"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de82-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9de82-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de82-138">支援 MTP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="9de82-138">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

