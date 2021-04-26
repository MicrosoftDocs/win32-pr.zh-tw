---
description: 定義服務主機所定義之服務的 ServiceID、類型、PnPXHardwareId 和 PnPXCompatibleId 元素。
ms.assetid: f901a88f-7e01-4e7f-a0f2-59f2a01b03cd
title: hosted 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d281b5e058f8716c12c655ebcdb9a17bdfa4fb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994885"
---
# <a name="hosted-element"></a><span data-ttu-id="6decf-103">hosted 元素</span><span class="sxs-lookup"><span data-stu-id="6decf-103">hosted element</span></span>

<span data-ttu-id="6decf-104">定義服務主機所定義之服務的 [**ServiceID**](serviceid.md)、 [**類型**](types.md)、[**PnPXHardwareId**](pnpxhardwareid.md)和 [**PnPXCompatibleId**](pnpxcompatibleid.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="6decf-104">Defines the [**ServiceID**](serviceid.md), [**Types**](types.md),[**PnPXHardwareId**](pnpxhardwareid.md), and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements for the services defined by the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="6decf-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="6decf-105">Usage</span></span>

``` syntax
<hosted>
  child elements
</hosted>
```

## <a name="attributes"></a><span data-ttu-id="6decf-106">屬性</span><span class="sxs-lookup"><span data-stu-id="6decf-106">Attributes</span></span>

<span data-ttu-id="6decf-107">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="6decf-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6decf-108">子元素</span><span class="sxs-lookup"><span data-stu-id="6decf-108">Child elements</span></span>



| <span data-ttu-id="6decf-109">元素</span><span class="sxs-lookup"><span data-stu-id="6decf-109">Element</span></span>                                                 | <span data-ttu-id="6decf-110">描述</span><span class="sxs-lookup"><span data-stu-id="6decf-110">Description</span></span>                                                                      |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="6decf-111">**PnPXCompatibleId**</span><span class="sxs-lookup"><span data-stu-id="6decf-111">**PnPXCompatibleId**</span></span>](pnpxcompatibleid.md)<br/> | <span data-ttu-id="6decf-112">指定服務的 PnP 相容識別碼。</span><span class="sxs-lookup"><span data-stu-id="6decf-112">Specifies the PnP-X Compatible Identifier of the service.</span></span><br/> <br/> |
| [<span data-ttu-id="6decf-113">**PnPXHardwareId**</span><span class="sxs-lookup"><span data-stu-id="6decf-113">**PnPXHardwareId**</span></span>](pnpxhardwareid.md)<br/>     | <span data-ttu-id="6decf-114">指定服務的 PnP 硬體識別碼。</span><span class="sxs-lookup"><span data-stu-id="6decf-114">Specifies the PnP-X Hardware Identifier of the service.</span></span><br/> <br/>   |
| [<span data-ttu-id="6decf-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="6decf-115">**ServiceID**</span></span>](serviceid.md)<br/>               | <span data-ttu-id="6decf-116">定義服務主機的服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="6decf-116">Defines a service identifier for the service host.</span></span><br/> <br/>        |
| [<span data-ttu-id="6decf-117">**類型**</span><span class="sxs-lookup"><span data-stu-id="6decf-117">**Types**</span></span>](types.md)<br/>                       | <span data-ttu-id="6decf-118">定義 XSD 限定名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="6decf-118">Defines a list of XSD qualified names.</span></span><br/> <br/>                    |



### <a name="child-element-sequence"></a><span data-ttu-id="6decf-119">子項目順序</span><span class="sxs-lookup"><span data-stu-id="6decf-119">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types, 
  PnPXHardwareId?, 
  PnPXCompatibleId?
)
```

## <a name="parent-elements"></a><span data-ttu-id="6decf-120">父元素</span><span class="sxs-lookup"><span data-stu-id="6decf-120">Parent elements</span></span>



| <span data-ttu-id="6decf-121">元素</span><span class="sxs-lookup"><span data-stu-id="6decf-121">Element</span></span>                                         | <span data-ttu-id="6decf-122">描述</span><span class="sxs-lookup"><span data-stu-id="6decf-122">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="6decf-123">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="6decf-123">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="6decf-124">要執行之裝置的裝載中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6decf-124">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6decf-125">備註</span><span class="sxs-lookup"><span data-stu-id="6decf-125">Remarks</span></span>

<span data-ttu-id="6decf-126">服務主機提供的每個服務都應該有自己的 **託管** 元素資訊，以確保服務在對中繼資料要求的回應中已正確發佈。</span><span class="sxs-lookup"><span data-stu-id="6decf-126">Each service provided by a service host should have its own **hosted** element information to ensure that the service is published properly in responses to metadata requests.</span></span>

<span data-ttu-id="6decf-127">[**PnPXHardwareId**](pnpxhardwareid.md)和 [**PnPXCompatibleId**](pnpxcompatibleid.md)元素是選擇性的，但在使用時，必須一起使用。</span><span class="sxs-lookup"><span data-stu-id="6decf-127">The [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements are optional, but when used, they must be used together.</span></span> <span data-ttu-id="6decf-128">如果有的話，也必須有另一個。</span><span class="sxs-lookup"><span data-stu-id="6decf-128">If one is present, the other must be present as well.</span></span>

<span data-ttu-id="6decf-129">如果有 [**PnPXDeviceCategory**](pnpxdevicecategory.md) 元素，則 **至少一個裝載** 的元素必須同時包含 [**PnPXHardwareId**](pnpxhardwareid.md) 和 [**PnPXCompatibleId**](pnpxcompatibleid.md) 專案。</span><span class="sxs-lookup"><span data-stu-id="6decf-129">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one **hosted** element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="6decf-130">同樣地，如果 **PnPXHardwareId** 和 **PnPXCompatibleId** 元素 **存在於裝載的元素中**，則 [**ThisModelMetadata**](thismodelmetadata.md)元素內至少必須有一個 **PnPXDeviceCategory** 元素。</span><span class="sxs-lookup"><span data-stu-id="6decf-130">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element must be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="6decf-131">項目資訊</span><span class="sxs-lookup"><span data-stu-id="6decf-131">Element information</span></span>



| <span data-ttu-id="6decf-132">標籤</span><span class="sxs-lookup"><span data-stu-id="6decf-132">Label</span></span> | <span data-ttu-id="6decf-133">值</span><span class="sxs-lookup"><span data-stu-id="6decf-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6decf-134">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="6decf-134">Minimum supported system</span></span><br/> | <span data-ttu-id="6decf-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6decf-135">Windows Vista</span></span> |
| <span data-ttu-id="6decf-136">可以是空的</span><span class="sxs-lookup"><span data-stu-id="6decf-136">Can be empty</span></span>                        | <span data-ttu-id="6decf-137">否</span><span class="sxs-lookup"><span data-stu-id="6decf-137">No</span></span>            |



 

 




