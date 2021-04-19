---
description: WPD \_ 命令 \_ MTP EXT \_ - \_ 取得 \_ 支援的 \_ 廠商 opcode \_ 碼命令傳送 MTP 命令區塊。 沒有與此命令相關聯的後續資料階段。
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: 'WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984779"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a><span data-ttu-id="65ae1-104">WPD \_ 命令 \_ MTP \_ EXT \_ GET \_ 支援的 \_ 廠商 opcode \_ 碼命令</span><span class="sxs-lookup"><span data-stu-id="65ae1-104">WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES Command</span></span>

<span data-ttu-id="65ae1-105">**WPD \_ 命令 \_ MTP EXT- \_ \_ 取得 \_ 支援的廠商 opcode \_ \_ 碼** 命令傳送 MTP 命令區塊。</span><span class="sxs-lookup"><span data-stu-id="65ae1-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_SUPPORTED\_VENDOR\_OPCODES** command sends an MTP command block.</span></span> <span data-ttu-id="65ae1-106">沒有與此命令相關聯的後續資料階段。</span><span class="sxs-lookup"><span data-stu-id="65ae1-106">There is no subsequent data phase associated with this command.</span></span>

## <a name="command-category"></a><span data-ttu-id="65ae1-107">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="65ae1-107">Command category</span></span>

<span data-ttu-id="65ae1-108">**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="65ae1-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="65ae1-109">參數</span><span class="sxs-lookup"><span data-stu-id="65ae1-109">Parameters</span></span>

<span data-ttu-id="65ae1-110">此命令沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="65ae1-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65ae1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="65ae1-111">Return Value</span></span>

<span data-ttu-id="65ae1-112">驅動程式會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="65ae1-112">The driver returns the following results.</span></span>



| <span data-ttu-id="65ae1-113">結果</span><span class="sxs-lookup"><span data-stu-id="65ae1-113">Result</span></span>                                                | <span data-ttu-id="65ae1-114">VarType</span><span class="sxs-lookup"><span data-stu-id="65ae1-114">VarType</span></span> | <span data-ttu-id="65ae1-115">Description</span><span class="sxs-lookup"><span data-stu-id="65ae1-115">Description</span></span>                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ae1-116">**WPD \_ 屬性 \_ MTP \_ EXT \_ \* \_ 操作 \_ 代碼**</span><span class="sxs-lookup"><span data-stu-id="65ae1-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_OPERATION\_CODES**</span></span> | <span data-ttu-id="65ae1-117">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="65ae1-117">VT\_UI4</span></span> | <span data-ttu-id="65ae1-118">必要。</span><span class="sxs-lookup"><span data-stu-id="65ae1-118">Required.</span></span> <span data-ttu-id="65ae1-119">**IPortableDevicePropVariantCollection** ，其中包含所有廠商擴充的作業代碼。</span><span class="sxs-lookup"><span data-stu-id="65ae1-119">An **IPortableDevicePropVariantCollection** that contains all vendor-extended operation codes.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="65ae1-120">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="65ae1-120">Calling Methods</span></span>

<span data-ttu-id="65ae1-121">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="65ae1-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="65ae1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="65ae1-122">Requirements</span></span>



| <span data-ttu-id="65ae1-123">需求</span><span class="sxs-lookup"><span data-stu-id="65ae1-123">Requirement</span></span> | <span data-ttu-id="65ae1-124">值</span><span class="sxs-lookup"><span data-stu-id="65ae1-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ae1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="65ae1-125">Header</span></span><br/> | <dl> <span data-ttu-id="65ae1-126"><dt>WpdMtpExtensions。h</dt></span><span class="sxs-lookup"><span data-stu-id="65ae1-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ae1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65ae1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ae1-128">支援 MTP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="65ae1-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




