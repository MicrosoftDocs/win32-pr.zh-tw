---
description: WPD \_ 命令 \_ mtp \_ ext \_ WRITE \_ DATA 命令會在執行 WPD \_ 命令 \_ mtp \_ ext ext \_ EXECUTE \_ 命令並執行 \_ \_ 資料 \_ \_ 寫入命令之後，將資料傳送至裝置。
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: 'WPD_COMMAND_MTP_EXT_WRITE_DATA 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993565"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a><span data-ttu-id="f5968-103">WPD \_ 命令 \_ MTP \_ EXT \_ WRITE \_ DATA 命令</span><span class="sxs-lookup"><span data-stu-id="f5968-103">WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA Command</span></span>

<span data-ttu-id="f5968-104">**WPD \_ 命令 \_ mtp \_ ext \_ WRITE \_ DATA** 命令會在執行 **WPD \_ 命令 \_ mtp \_ ext ext \_ EXECUTE \_ 命令並執行 \_ \_ 資料 \_ \_ 寫入** 命令之後，將資料傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="f5968-104">The **WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA** command sends data to the device after the **WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE** command is run.</span></span>

## <a name="command-category"></a><span data-ttu-id="f5968-105">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="f5968-105">Command category</span></span>

<span data-ttu-id="f5968-106">**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="f5968-106">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="f5968-107">參數</span><span class="sxs-lookup"><span data-stu-id="f5968-107">Parameters</span></span>

<span data-ttu-id="f5968-108">驅動程式需要下列參數。</span><span class="sxs-lookup"><span data-stu-id="f5968-108">The driver expects the following parameters.</span></span>



| <span data-ttu-id="f5968-109">參數</span><span class="sxs-lookup"><span data-stu-id="f5968-109">Parameter</span></span>                                                    | <span data-ttu-id="f5968-110">VarType</span><span class="sxs-lookup"><span data-stu-id="f5968-110">VarType</span></span>             | <span data-ttu-id="f5968-111">Description</span><span class="sxs-lookup"><span data-stu-id="f5968-111">Description</span></span>                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5968-112">**WPD \_ 屬性 \_ MTP \_ EXT EXT \_ 傳送 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="f5968-112">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_CONTEXT**</span></span>               | <span data-ttu-id="f5968-113">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="f5968-113">VT\_LPWSTR</span></span>          | <span data-ttu-id="f5968-114">必要。</span><span class="sxs-lookup"><span data-stu-id="f5968-114">Required.</span></span> <span data-ttu-id="f5968-115">識別先前對裝置所做的呼叫所傳回的內容。</span><span class="sxs-lookup"><span data-stu-id="f5968-115">Identifies the context that was returned by the previous call to the device.</span></span> |
| <span data-ttu-id="f5968-116">**WPD \_ 屬性 \_ MTP \_ EXT \_ TRANSFER \_ \_ BYTES \_ TO \_ WRITE**</span><span class="sxs-lookup"><span data-stu-id="f5968-116">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_TO\_WRITE**</span></span> | <span data-ttu-id="f5968-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="f5968-117">VT\_UI4</span></span>             | <span data-ttu-id="f5968-118">必要。</span><span class="sxs-lookup"><span data-stu-id="f5968-118">Required.</span></span> <span data-ttu-id="f5968-119">指定要寫入的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f5968-119">Specifies the number of bytes to write.</span></span>                                      |
| <span data-ttu-id="f5968-120">**WPD \_ 屬性 \_ MTP \_ EXT \_ 轉送 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="f5968-120">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_DATA**</span></span>                  | <span data-ttu-id="f5968-121">VT \_ 向量 \| vt \_ UI1</span><span class="sxs-lookup"><span data-stu-id="f5968-121">VT\_VECTOR\|VT\_UI1</span></span> | <span data-ttu-id="f5968-122">必要。</span><span class="sxs-lookup"><span data-stu-id="f5968-122">Required.</span></span> <span data-ttu-id="f5968-123">識別要將裝置資料複製到其中的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f5968-123">Identifies the buffer into which the device data is copied.</span></span>                  |



 

## <a name="return-value"></a><span data-ttu-id="f5968-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5968-124">Return Value</span></span>

<span data-ttu-id="f5968-125">驅動程式會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="f5968-125">The driver returns the following results.</span></span>



| <span data-ttu-id="f5968-126">結果</span><span class="sxs-lookup"><span data-stu-id="f5968-126">Result</span></span>                                                     | <span data-ttu-id="f5968-127">VarType</span><span class="sxs-lookup"><span data-stu-id="f5968-127">VarType</span></span> | <span data-ttu-id="f5968-128">Description</span><span class="sxs-lookup"><span data-stu-id="f5968-128">Description</span></span>                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| <span data-ttu-id="f5968-129">**WPD \_ 屬性 \_ MTP \_ EXT \_ EXT \_ \_ BYTES 寫入位元組數 \_**</span><span class="sxs-lookup"><span data-stu-id="f5968-129">**WPD\_PROPERTY\_MTP\_EXT\_TRANSFER\_NUM\_BYTES\_WRITTEN**</span></span> | <span data-ttu-id="f5968-130">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="f5968-130">VT\_UI4</span></span> | <span data-ttu-id="f5968-131">必要。</span><span class="sxs-lookup"><span data-stu-id="f5968-131">Required.</span></span> <span data-ttu-id="f5968-132">指定傳送至裝置的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f5968-132">Specifies the number of bytes sent to the device..</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="f5968-133">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="f5968-133">Calling Methods</span></span>

<span data-ttu-id="f5968-134">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="f5968-134">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5968-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5968-135">Requirements</span></span>



| <span data-ttu-id="f5968-136">需求</span><span class="sxs-lookup"><span data-stu-id="f5968-136">Requirement</span></span> | <span data-ttu-id="f5968-137">值</span><span class="sxs-lookup"><span data-stu-id="f5968-137">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5968-138">標頭</span><span class="sxs-lookup"><span data-stu-id="f5968-138">Header</span></span><br/> | <dl> <span data-ttu-id="f5968-139"><dt>WpdMtpExtensions。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5968-139"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5968-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5968-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5968-141">支援 MTP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="f5968-141">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




