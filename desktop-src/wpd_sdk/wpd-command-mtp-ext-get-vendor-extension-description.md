---
description: WPD \_ 命令 \_ MTP \_ EXT \_ 的取得 \_ 廠商 \_ 擴充 \_ 功能 description 命令會抓取廠商延伸的描述字串。 這個字串是由 DeviceInfo 資料集所定義。
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: 'WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997721"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a><span data-ttu-id="a1649-104">WPD \_ 命令 \_ MTP \_ EXT \_ GET \_ 廠商 \_ EXTENSION \_ DESCRIPTION 命令</span><span class="sxs-lookup"><span data-stu-id="a1649-104">WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION Command</span></span>

<span data-ttu-id="a1649-105">**WPD \_ 命令 \_ MTP EXT 的 \_ \_ 取得 \_ 廠商 \_ 擴充功能 \_ description** 命令會抓取廠商延伸的描述字串。</span><span class="sxs-lookup"><span data-stu-id="a1649-105">The **WPD\_COMMAND\_MTP\_EXT\_GET\_VENDOR\_EXTENSION\_DESCRIPTION** command retrieves the vendor-extension description string.</span></span> <span data-ttu-id="a1649-106">這個字串是由 **DeviceInfo** 資料集所定義。</span><span class="sxs-lookup"><span data-stu-id="a1649-106">This string is defined by a **DeviceInfo** dataset.</span></span>

## <a name="command-category"></a><span data-ttu-id="a1649-107">命令類別目錄</span><span class="sxs-lookup"><span data-stu-id="a1649-107">Command category</span></span>

<span data-ttu-id="a1649-108">**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="a1649-108">**WPD\_CATEGORY\_MTP\_EXT\_VENDOR\_OPERATIONS**</span></span>

## <a name="parameters"></a><span data-ttu-id="a1649-109">參數</span><span class="sxs-lookup"><span data-stu-id="a1649-109">Parameters</span></span>

<span data-ttu-id="a1649-110">此命令沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a1649-110">This command has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1649-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1649-111">Return Value</span></span>

<span data-ttu-id="a1649-112">驅動程式會傳回下列結果。</span><span class="sxs-lookup"><span data-stu-id="a1649-112">The driver returns the following results.</span></span>



| <span data-ttu-id="a1649-113">結果</span><span class="sxs-lookup"><span data-stu-id="a1649-113">Result</span></span>                                                      | <span data-ttu-id="a1649-114">VarType</span><span class="sxs-lookup"><span data-stu-id="a1649-114">VarType</span></span>    | <span data-ttu-id="a1649-115">Description</span><span class="sxs-lookup"><span data-stu-id="a1649-115">Description</span></span>                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| <span data-ttu-id="a1649-116">**WPD \_ 屬性 \_ MTP \_ EXT \_ \* \_ 延伸模組 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="a1649-116">**WPD\_PROPERTY\_MTP\_EXT\_VENDOR\_EXTENSION\_DESCRIPTION**</span></span> | <span data-ttu-id="a1649-117">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a1649-117">VT\_LPWSTR</span></span> | <span data-ttu-id="a1649-118">必要。</span><span class="sxs-lookup"><span data-stu-id="a1649-118">Required.</span></span> <span data-ttu-id="a1649-119">指定廠商延伸的描述字串。</span><span class="sxs-lookup"><span data-stu-id="a1649-119">Specifies the vendor-extension description string.</span></span> |



 

## <a name="calling-methods"></a><span data-ttu-id="a1649-120">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="a1649-120">Calling Methods</span></span>

<span data-ttu-id="a1649-121">只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="a1649-121">Can only be called directly by using [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1649-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1649-122">Requirements</span></span>



| <span data-ttu-id="a1649-123">需求</span><span class="sxs-lookup"><span data-stu-id="a1649-123">Requirement</span></span> | <span data-ttu-id="a1649-124">值</span><span class="sxs-lookup"><span data-stu-id="a1649-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1649-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a1649-125">Header</span></span><br/> | <dl> <span data-ttu-id="a1649-126"><dt>WpdMtpExtensions。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1649-126"><dt>WpdMtpExtensions.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1649-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1649-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1649-128">支援 MTP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="a1649-128">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 




