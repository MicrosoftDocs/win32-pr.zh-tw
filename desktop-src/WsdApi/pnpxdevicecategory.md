---
description: 指定裝置所屬的 PnP X 分類。 您可以指定一個以上的類別。
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: PnPXDeviceCategory 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08084d780c26d2f7fab902156939fd14a3e60c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996585"
---
# <a name="pnpxdevicecategory-element"></a><span data-ttu-id="86438-104">PnPXDeviceCategory 元素</span><span class="sxs-lookup"><span data-stu-id="86438-104">PnPXDeviceCategory element</span></span>

<span data-ttu-id="86438-105">指定裝置所屬的 PnP X 分類。</span><span class="sxs-lookup"><span data-stu-id="86438-105">Specifies the PnP-X category to which the device belongs.</span></span> <span data-ttu-id="86438-106">您可以指定一個以上的類別。</span><span class="sxs-lookup"><span data-stu-id="86438-106">More than one category can be specified.</span></span>

## <a name="usage"></a><span data-ttu-id="86438-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="86438-107">Usage</span></span>

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a><span data-ttu-id="86438-108">屬性</span><span class="sxs-lookup"><span data-stu-id="86438-108">Attributes</span></span>

<span data-ttu-id="86438-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="86438-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="86438-110">子元素</span><span class="sxs-lookup"><span data-stu-id="86438-110">Child elements</span></span>

<span data-ttu-id="86438-111">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="86438-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="86438-112">父元素</span><span class="sxs-lookup"><span data-stu-id="86438-112">Parent elements</span></span>



| <span data-ttu-id="86438-113">元素</span><span class="sxs-lookup"><span data-stu-id="86438-113">Element</span></span>                                                   | <span data-ttu-id="86438-114">描述</span><span class="sxs-lookup"><span data-stu-id="86438-114">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86438-115">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="86438-115">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="86438-116">定義要執行之裝置的製造商和型號中繼資料。</span><span class="sxs-lookup"><span data-stu-id="86438-116">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="86438-117">備註</span><span class="sxs-lookup"><span data-stu-id="86438-117">Remarks</span></span>

<span data-ttu-id="86438-118">裝置也可以指定裝置子類別，以取得更具描述性的裝置類別。</span><span class="sxs-lookup"><span data-stu-id="86438-118">Devices can also specify a device subcategory for a more descriptive device category.</span></span> <span data-ttu-id="86438-119">例如，「Microsoft.windowsmobile.forms 攝影機. DigitalStillCamera MediaDevices. MusicPlayer」識別的裝置是具有相機和音樂播放機的 Microsoft Windows Mobile 裝置。</span><span class="sxs-lookup"><span data-stu-id="86438-119">For example, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifies a device that is a Microsoft Windows Mobile  device with a camera and music player.</span></span> <span data-ttu-id="86438-120">此裝置的主要裝置類別會是「電話」。</span><span class="sxs-lookup"><span data-stu-id="86438-120">The primary device category for this device would be "Phones".</span></span>

<span data-ttu-id="86438-121">若要指定一個以上的裝置類別，請以空格分隔類別。</span><span class="sxs-lookup"><span data-stu-id="86438-121">To specify more than one device category, separate the categories with a space.</span></span> <span data-ttu-id="86438-122">例如，「印表機存放裝置」會識別主要類別為「印表機」和「儲存體」次要類別的裝置。</span><span class="sxs-lookup"><span data-stu-id="86438-122">For example, "Printers Storage" identifies a device with a primary category of "Printers" and a secondary category of "Storage".</span></span>

<span data-ttu-id="86438-123">如果有 **PnPXDeviceCategory** 元素，則 [**至少一個裝載**](hosted.md) 的元素應該同時包含 [**PnPXHardwareId**](pnpxhardwareid.md) 和 [**PnPXCompatibleId**](pnpxcompatibleid.md) 專案。</span><span class="sxs-lookup"><span data-stu-id="86438-123">If a **PnPXDeviceCategory** element is present, then at least one [**hosted**](hosted.md) element should contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="86438-124">同樣地，如果 **PnPXHardwareId** 和 **PnPXCompatibleId** 元素 **存在於裝載的元素中**，則 [**ThisModelMetadata**](thismodelmetadata.md)元素內至少應該有一個 **PnPXDeviceCategory** 元素。</span><span class="sxs-lookup"><span data-stu-id="86438-124">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, at least one **PnPXDeviceCategory** element should be present inside the [**thisModelMetadata**](thismodelmetadata.md) element.</span></span>

## <a name="element-information"></a><span data-ttu-id="86438-125">項目資訊</span><span class="sxs-lookup"><span data-stu-id="86438-125">Element information</span></span>



| <span data-ttu-id="86438-126">標籤</span><span class="sxs-lookup"><span data-stu-id="86438-126">Label</span></span> | <span data-ttu-id="86438-127">值</span><span class="sxs-lookup"><span data-stu-id="86438-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="86438-128">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="86438-128">Minimum supported system</span></span><br/> | <span data-ttu-id="86438-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86438-129">Windows Vista</span></span> |
| <span data-ttu-id="86438-130">可以是空的</span><span class="sxs-lookup"><span data-stu-id="86438-130">Can be empty</span></span>                        | <span data-ttu-id="86438-131">是</span><span class="sxs-lookup"><span data-stu-id="86438-131">Yes</span></span>           |



 

 




