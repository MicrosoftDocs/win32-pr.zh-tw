---
description: 指定服務的 PnP 硬體識別碼。
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: PnPXHardwareId 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996525"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="96406-103">PnPXHardwareId 元素</span><span class="sxs-lookup"><span data-stu-id="96406-103">PnPXHardwareId element</span></span>

<span data-ttu-id="96406-104">指定服務的 PnP 硬體識別碼。</span><span class="sxs-lookup"><span data-stu-id="96406-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="96406-105">PnP 符合此元素，並在裝置的 INF 檔案的 PnpxDevice 區段中提供硬體描述 (s) \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="96406-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="96406-106">根據此資訊，PnP 服務會選取並載入最適當的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="96406-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="96406-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="96406-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="96406-108">屬性</span><span class="sxs-lookup"><span data-stu-id="96406-108">Attributes</span></span>

<span data-ttu-id="96406-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="96406-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="96406-110">子元素</span><span class="sxs-lookup"><span data-stu-id="96406-110">Child elements</span></span>

<span data-ttu-id="96406-111">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="96406-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="96406-112">父元素</span><span class="sxs-lookup"><span data-stu-id="96406-112">Parent elements</span></span>



| <span data-ttu-id="96406-113">元素</span><span class="sxs-lookup"><span data-stu-id="96406-113">Element</span></span>                             | <span data-ttu-id="96406-114">描述</span><span class="sxs-lookup"><span data-stu-id="96406-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="96406-115">**託管**</span><span class="sxs-lookup"><span data-stu-id="96406-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="96406-116">定義服務主機所定義之服務的元素。</span><span class="sxs-lookup"><span data-stu-id="96406-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="96406-117">備註</span><span class="sxs-lookup"><span data-stu-id="96406-117">Remarks</span></span>

<span data-ttu-id="96406-118">若要指定一個以上的硬體識別碼，請以空白字元分隔識別碼，例如 "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3"。</span><span class="sxs-lookup"><span data-stu-id="96406-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="96406-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="96406-119">Element information</span></span>



| <span data-ttu-id="96406-120">標籤</span><span class="sxs-lookup"><span data-stu-id="96406-120">Label</span></span> | <span data-ttu-id="96406-121">值</span><span class="sxs-lookup"><span data-stu-id="96406-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="96406-122">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="96406-122">Minimum supported system</span></span><br/> | <span data-ttu-id="96406-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96406-123">Windows Vista</span></span> |
| <span data-ttu-id="96406-124">可以是空的</span><span class="sxs-lookup"><span data-stu-id="96406-124">Can be empty</span></span>                        | <span data-ttu-id="96406-125">是</span><span class="sxs-lookup"><span data-stu-id="96406-125">Yes</span></span>           |



 

 




