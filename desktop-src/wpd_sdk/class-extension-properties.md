---
description: Windows 可攜式裝置支援下列類別延伸模組屬性。
ms.assetid: 9b8983ba-5824-495d-868f-fd22b98e1954
title: '類別擴充屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Class
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c7e961b80ae990653e6c354640b35c28f8bcf8b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999158"
---
# <a name="class-extension-properties"></a><span data-ttu-id="3e7f4-103">類別延伸模組屬性</span><span class="sxs-lookup"><span data-stu-id="3e7f4-103">Class Extension Properties</span></span>

<span data-ttu-id="3e7f4-104">Windows 可攜式裝置支援下列類別延伸模組屬性。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-104">Windows Portable Devices supports the following class extension properties.</span></span>



| <span data-ttu-id="3e7f4-105">屬性</span><span class="sxs-lookup"><span data-stu-id="3e7f4-105">Property</span></span>                                                                      | <span data-ttu-id="3e7f4-106">VarType</span><span class="sxs-lookup"><span data-stu-id="3e7f4-106">VarType</span></span>         | <span data-ttu-id="3e7f4-107">Description</span><span class="sxs-lookup"><span data-stu-id="3e7f4-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7f4-108">**WPD \_ 類別 \_ 延伸模組 \_ 選項 \_ 支援的 \_ 內容 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-108">**WPD\_CLASS\_EXTENSION\_OPTIONS\_SUPPORTED\_CONTENT\_TYPES**</span></span>                 | <span data-ttu-id="3e7f4-109">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="3e7f4-110">值，指定驅動程式所支援之內容類型的 (超集合) 清單 (類似于呼叫 WPD \_ 命令功能，可 \_ \_ \_ \_ \_ 在 **WPD \_ 功能 \_ 類別目錄 \_ 所有**) 上取得支援的內容類型。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-110">A value that specifies the (superset) list of content types supported by the driver (similar to calling WPD\_COMMAND\_CAPABILITIES\_GET\_SUPPORTED\_CONTENT\_TYPES on **WPD\_FUNCTIONAL\_CATEGORY\_ALL**).</span></span>                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3e7f4-111">**WPD \_ 類別 \_ 延伸模組選項不會 \_ \_ \_ 註冊 \_ WPD \_ 裝置 \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-111">**WPD\_CLASS\_EXTENSION\_OPTIONS\_DONT\_REGISTER\_WPD\_DEVICE\_INTERFACE**</span></span>    | <span data-ttu-id="3e7f4-112">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-112">**VT\_BOOL**</span></span>    | <span data-ttu-id="3e7f4-113">值，指定呼叫端是否想要 WPD 類別擴充程式庫來註冊 WPD 裝置類別介面。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-113">A value that specifies whether the caller wants the WPD class extension library to register the WPD Device Class interface.</span></span> <span data-ttu-id="3e7f4-114">如果這個值為 true，呼叫端會負責註冊。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-114">If this value is true, the caller takes responsibility for registration.</span></span><br/> <span data-ttu-id="3e7f4-115">如果這個值為 false，則表示呼叫端需要類別延伸模組程式庫來執行註冊。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-115">If this value is false, it indicates that the caller expects the class extension library to perform the registration.</span></span><br/><span data-ttu-id="3e7f4-116">大部分的驅動程式都應該允許類別延伸模組程式庫執行註冊，但類別延伸程式庫註冊 WPD 裝置類別介面的情況可能會造成不良的影響。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-116">Most drivers should allow the class extension library to perform the registration, except where registering the WPD Device Class interface by the class extension library might cause adverse effects.</span></span> |
| <span data-ttu-id="3e7f4-117">**WPD \_ 類別 \_ 延伸模組 \_ 選項 \_ 註冊 \_ WPD 私用 \_ \_ 裝置 \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-117">**WPD\_CLASS\_EXTENSION\_OPTIONS\_REGISTER\_WPD\_PRIVATE\_DEVICE\_INTERFACE**</span></span> | <span data-ttu-id="3e7f4-118">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-118">**VT\_BOOL**</span></span>    | <span data-ttu-id="3e7f4-119">指出呼叫端想要 WPD 類別擴充程式庫註冊私用 WPD 裝置類別介面。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-119">Indicates that the caller wants the WPD class extension library to register the private WPD Device Class interface.</span></span> <span data-ttu-id="3e7f4-120">這不建議用於大部分的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-120">This is not recommended for most drivers.</span></span> <span data-ttu-id="3e7f4-121">只有當類別延伸程式庫註冊 WPD 裝置類別介面時，才應該使用它，將會造成不良的影響。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-121">It should only be used in cases where the registering of the WPD Device Class interface by the class extension library will cause adverse effects.</span></span> <span data-ttu-id="3e7f4-122">此選項通常會與 WPD 類別延伸模組選項搭配使用，而不會將 **\_ \_ \_ \_ \_ \_ WPD \_ 裝置 \_ 介面** 設為 **TRUE**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-122">This option is typically used in conjunction with **WPD\_CLASS\_EXTENSION\_OPTIONS\_DONT\_REGISTER\_WPD\_DEVICE\_INTERFACE** set to **TRUE**</span></span>                                                                                          |
| <span data-ttu-id="3e7f4-123">**WPD \_ 類別 \_ 延伸模組 \_ 選項 \_ 裝置 \_ 識別 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-123">**WPD\_CLASS\_EXTENSION\_OPTIONS\_DEVICE\_IDENTIFICATION\_VALUES**</span></span>            | <span data-ttu-id="3e7f4-124">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-124">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="3e7f4-125">這是包含裝置識別碼值的 [IPortableDeviceValues](iportabledevicevalues.md) ， (**WPD \_ 裝置 \_ 製造商**、 **WPD \_ 裝置 \_ 型號**、 **WPD \_ 裝置 \_ 固件 \_ 版本** ，以及 **WPD \_ 裝置 \_ 功能 \_ 唯一 \_ 識別碼**) 。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-125">This is an [IPortableDeviceValues](iportabledevicevalues.md) which contains the device identification values (**WPD\_DEVICE\_MANUFACTURER**, **WPD\_DEVICE\_MODEL**, **WPD\_DEVICE\_FIRMWARE\_VERSION** and **WPD\_DEVICE\_FUNCTIONAL\_UNIQUE\_ID**).</span></span> <span data-ttu-id="3e7f4-126">在初始化時將此包含在其他類別延伸模組選項中</span><span class="sxs-lookup"><span data-stu-id="3e7f4-126">Include this with other Class Extension options when initializing</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3e7f4-127">**WPD \_ 類別 \_ 擴充功能 \_ 選項 \_ 傳輸 \_ 頻寬**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-127">**WPD\_CLASS\_EXTENSION\_OPTIONS\_TRANSPORT\_BANDWIDTH**</span></span>                      | <span data-ttu-id="3e7f4-128">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-128">**VT\_UI4**</span></span>     | <span data-ttu-id="3e7f4-129">指出傳輸的理論最大頻寬（以每秒千位）</span><span class="sxs-lookup"><span data-stu-id="3e7f4-129">Indicates the theoretical maximum bandwidth of the transport in kilobits per second</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3e7f4-130">**WPD \_ 類別 \_ 延伸模組 \_ 選項 \_ 裝置 \_ 識別 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-130">**WPD\_CLASS\_EXTENSION\_OPTIONS\_DEVICE\_IDENTIFICATION\_VALUES**</span></span>            | <span data-ttu-id="3e7f4-131">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-131">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="3e7f4-132">這是包含裝置識別碼值的 [IPortableDeviceValues](iportabledevicevalues.md) ， (**WPD \_ 裝置 \_ 製造商**、 **WPD \_ 裝置 \_ 型號**、 **WPD \_ 裝置 \_ 固件 \_ 版本** ，以及 **WPD \_ 裝置 \_ 功能 \_ 唯一 \_ 識別碼**) 。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-132">This is an [IPortableDeviceValues](iportabledevicevalues.md) which contains the device identification values (**WPD\_DEVICE\_MANUFACTURER**, **WPD\_DEVICE\_MODEL**, **WPD\_DEVICE\_FIRMWARE\_VERSION** and **WPD\_DEVICE\_FUNCTIONAL\_UNIQUE\_ID**).</span></span> <span data-ttu-id="3e7f4-133">在初始化時將此包含在其他類別延伸模組選項中。</span><span class="sxs-lookup"><span data-stu-id="3e7f4-133">Include this with other Class Extension options when initializing.</span></span>                                                                                                                                                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="3e7f4-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e7f4-134">Requirements</span></span>



| <span data-ttu-id="3e7f4-135">需求</span><span class="sxs-lookup"><span data-stu-id="3e7f4-135">Requirement</span></span> | <span data-ttu-id="3e7f4-136">值</span><span class="sxs-lookup"><span data-stu-id="3e7f4-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7f4-137">標頭</span><span class="sxs-lookup"><span data-stu-id="3e7f4-137">Header</span></span><br/> | <dl> <span data-ttu-id="3e7f4-138"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e7f4-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e7f4-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e7f4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e7f4-140">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="3e7f4-140">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




