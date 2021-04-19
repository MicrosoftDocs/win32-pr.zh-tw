---
description: 指定服務的 PnP 硬體識別碼。
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: PnPXHardwareId 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977258"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="4e0e9-103">PnPXHardwareId 元素</span><span class="sxs-lookup"><span data-stu-id="4e0e9-103">PnPXHardwareId element</span></span>

<span data-ttu-id="4e0e9-104">指定服務的 PnP 硬體識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e0e9-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="4e0e9-105">PnP 符合此元素，並在裝置的 INF 檔案的 PnpxDevice 區段中提供硬體描述 (s) \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="4e0e9-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="4e0e9-106">根據此資訊，PnP 服務會選取並載入最適當的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4e0e9-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="4e0e9-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="4e0e9-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="4e0e9-108">屬性</span><span class="sxs-lookup"><span data-stu-id="4e0e9-108">Attributes</span></span>

<span data-ttu-id="4e0e9-109">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="4e0e9-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4e0e9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4e0e9-110">Child elements</span></span>

<span data-ttu-id="4e0e9-111">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="4e0e9-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="4e0e9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4e0e9-112">Parent elements</span></span>



| <span data-ttu-id="4e0e9-113">元素</span><span class="sxs-lookup"><span data-stu-id="4e0e9-113">Element</span></span>                             | <span data-ttu-id="4e0e9-114">描述</span><span class="sxs-lookup"><span data-stu-id="4e0e9-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e0e9-115">**託管**</span><span class="sxs-lookup"><span data-stu-id="4e0e9-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="4e0e9-116">定義服務主機所定義之服務的元素。</span><span class="sxs-lookup"><span data-stu-id="4e0e9-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4e0e9-117">備註</span><span class="sxs-lookup"><span data-stu-id="4e0e9-117">Remarks</span></span>

<span data-ttu-id="4e0e9-118">若要指定一個以上的硬體識別碼，請以空白字元分隔識別碼，例如 "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3"。</span><span class="sxs-lookup"><span data-stu-id="4e0e9-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="4e0e9-119">項目資訊</span><span class="sxs-lookup"><span data-stu-id="4e0e9-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4e0e9-120">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="4e0e9-120">Minimum supported system</span></span><br/> | <span data-ttu-id="4e0e9-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e0e9-121">Windows Vista</span></span> |
| <span data-ttu-id="4e0e9-122">可以是空的</span><span class="sxs-lookup"><span data-stu-id="4e0e9-122">Can be empty</span></span>                        | <span data-ttu-id="4e0e9-123">是</span><span class="sxs-lookup"><span data-stu-id="4e0e9-123">Yes</span></span>           |



 

 




