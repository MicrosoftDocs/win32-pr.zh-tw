---
description: Windows 可攜式裝置支援下列 SMS 屬性。
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: 'SMS 屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978656"
---
# <a name="sms-properties"></a><span data-ttu-id="83a72-103">SMS 屬性</span><span class="sxs-lookup"><span data-stu-id="83a72-103">SMS Properties</span></span>

<span data-ttu-id="83a72-104">Windows 可攜式裝置支援下列 SMS 屬性。</span><span class="sxs-lookup"><span data-stu-id="83a72-104">Windows Portable Devices supports the following SMS properties.</span></span>



| <span data-ttu-id="83a72-105">屬性</span><span class="sxs-lookup"><span data-stu-id="83a72-105">Property</span></span>                   | <span data-ttu-id="83a72-106">VarType</span><span class="sxs-lookup"><span data-stu-id="83a72-106">VarType</span></span>        | <span data-ttu-id="83a72-107">Description</span><span class="sxs-lookup"><span data-stu-id="83a72-107">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83a72-108">**WPD \_ SMS \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="83a72-108">**WPD\_SMS\_ENCODING**</span></span>     | <span data-ttu-id="83a72-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="83a72-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="83a72-110">值，指定驅動程式將如何編碼用戶端傳送的文字訊息。</span><span class="sxs-lookup"><span data-stu-id="83a72-110">A value that specifies how the driver will encode the text message sent by the client.</span></span> <span data-ttu-id="83a72-111">這是唯讀屬性;用戶端無法指定裝置用來傳送訊息的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="83a72-111">This is a read-only property; the client cannot specify what encoding type a device uses to send messages.</span></span> <span data-ttu-id="83a72-112">這些值會複製 [**WPD \_ SMS \_ 編碼 \_ 類型**](wpd-sms-encoding-types.md) 的列舉值。</span><span class="sxs-lookup"><span data-stu-id="83a72-112">These values duplicate the [**WPD\_SMS\_ENCODING\_TYPES**](wpd-sms-encoding-types.md) enumerated values.</span></span> |
| <span data-ttu-id="83a72-113">**WPD \_ SMS \_ 最大承載 \_**</span><span class="sxs-lookup"><span data-stu-id="83a72-113">**WPD\_SMS\_MAX\_PAYLOAD**</span></span> | <span data-ttu-id="83a72-114">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="83a72-114">**VT\_UI4**</span></span>    | <span data-ttu-id="83a72-115">訊息中可包含的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="83a72-115">The maximum number of bytes that can be contained in a message.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="83a72-116">**WPD \_ SMS \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="83a72-116">**WPD\_SMS\_PROVIDER**</span></span>     | <span data-ttu-id="83a72-117">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="83a72-117">**VT\_LPWSTR**</span></span> | <span data-ttu-id="83a72-118">服務提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="83a72-118">The service provider's name.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="83a72-119">**WPD \_ SMS \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="83a72-119">**WPD\_SMS\_TIMEOUT**</span></span>      | <span data-ttu-id="83a72-120">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="83a72-120">**VT\_UI4**</span></span>    | <span data-ttu-id="83a72-121">傳回 timeout 之前的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="83a72-121">The number of milliseconds until a timeout is returned.</span></span>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="83a72-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="83a72-122">Requirements</span></span>



| <span data-ttu-id="83a72-123">需求</span><span class="sxs-lookup"><span data-stu-id="83a72-123">Requirement</span></span> | <span data-ttu-id="83a72-124">值</span><span class="sxs-lookup"><span data-stu-id="83a72-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="83a72-125">標頭</span><span class="sxs-lookup"><span data-stu-id="83a72-125">Header</span></span><br/> | <dl> <span data-ttu-id="83a72-126"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="83a72-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83a72-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83a72-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a72-128">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="83a72-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




