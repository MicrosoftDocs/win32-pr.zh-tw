---
description: 針對 Windows 7，Windows 可攜式裝置在裝置服務上支援下列格式的屬性。 這些屬性是由 IPortableDeviceServiceCapabilities：： GetFormatAttributes 方法傳回。
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: '格式屬性 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990657"
---
# <a name="format-attributes"></a><span data-ttu-id="c2d06-104">格式屬性</span><span class="sxs-lookup"><span data-stu-id="c2d06-104">Format Attributes</span></span>

<span data-ttu-id="c2d06-105">針對 Windows 7，Windows 可攜式裝置在裝置服務上支援下列格式的屬性。</span><span class="sxs-lookup"><span data-stu-id="c2d06-105">For Windows 7, Windows Portable Devices supports the following attributes for formats on a device service.</span></span> <span data-ttu-id="c2d06-106">這些屬性是由 [**IPortableDeviceServiceCapabilities：： GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) 方法傳回。</span><span class="sxs-lookup"><span data-stu-id="c2d06-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method.</span></span>




| <span data-ttu-id="c2d06-107">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c2d06-107">**Attribute**</span></span>                        | <span data-ttu-id="c2d06-108">**VarType**</span><span class="sxs-lookup"><span data-stu-id="c2d06-108">**VarType**</span></span>    | <span data-ttu-id="c2d06-109">**說明**</span><span class="sxs-lookup"><span data-stu-id="c2d06-109">**Description**</span></span>                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d06-110">**WPD \_ 格式 \_ 屬性 \_ MIMETYPE**</span><span class="sxs-lookup"><span data-stu-id="c2d06-110">**WPD\_FORMAT\_ATTRIBUTE\_MIMETYPE**</span></span> | <span data-ttu-id="c2d06-111">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c2d06-111">**VT\_LPWSTR**</span></span> | <span data-ttu-id="c2d06-112">MIME 類型的格式。</span><span class="sxs-lookup"><span data-stu-id="c2d06-112">The format MIME type.</span></span>                                                                                                     |
| <span data-ttu-id="c2d06-113">**WPD \_ 格式 \_ 屬性 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="c2d06-113">**WPD\_FORMAT\_ATTRIBUTE\_NAME**</span></span>     | <span data-ttu-id="c2d06-114">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c2d06-114">**VT\_LPWSTR**</span></span> | <span data-ttu-id="c2d06-115">字串，指定格式的腳本易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c2d06-115">A string that specifies the script-friendly name of the format.</span></span> <span data-ttu-id="c2d06-116">有效字元為英數位元 \[ a-zA-Z0-9 \] 和 ' \_ '。</span><span class="sxs-lookup"><span data-stu-id="c2d06-116">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c2d06-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2d06-117">Requirements</span></span>



| <span data-ttu-id="c2d06-118">需求</span><span class="sxs-lookup"><span data-stu-id="c2d06-118">Requirement</span></span> | <span data-ttu-id="c2d06-119">值</span><span class="sxs-lookup"><span data-stu-id="c2d06-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d06-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c2d06-120">Header</span></span><br/> | <dl> <span data-ttu-id="c2d06-121"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2d06-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2d06-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2d06-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d06-123">**屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="c2d06-123">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




