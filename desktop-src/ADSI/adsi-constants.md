---
title: ADSI 常數
description: 下表列出 Active Directory 服務介面中定義和使用的常數 (ADSI) 。
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671191"
---
# <a name="adsi-constants"></a><span data-ttu-id="ec39c-109">ADSI 常數</span><span class="sxs-lookup"><span data-stu-id="ec39c-109">ADSI Constants</span></span>

<span data-ttu-id="ec39c-110">下表列出 Active Directory 服務介面中定義和使用的常數 (ADSI) 。</span><span class="sxs-lookup"><span data-stu-id="ec39c-110">The following table lists constants defined and used in Active Directory Service Interfaces (ADSI).</span></span>



| <span data-ttu-id="ec39c-111">ADSI 常數</span><span class="sxs-lookup"><span data-stu-id="ec39c-111">ADSI constant</span></span>                      | <span data-ttu-id="ec39c-112">值</span><span class="sxs-lookup"><span data-stu-id="ec39c-112">Value</span></span>                                   | <span data-ttu-id="ec39c-113">描述</span><span class="sxs-lookup"><span data-stu-id="ec39c-113">Description</span></span>                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec39c-114">**ADS \_ EXT \_ INITCREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="ec39c-114">**ADS\_EXT\_INITCREDENTIALS**</span></span>      | <span data-ttu-id="ec39c-115">1</span><span class="sxs-lookup"><span data-stu-id="ec39c-115">1</span></span>                                       | <span data-ttu-id="ec39c-116">代表提供給 [**IADsExtension：：操作**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) 方法的自訂資料包含使用者認證的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="ec39c-116">A control code that indicates that the custom data supplied to the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method contains user credentials.</span></span>                                                     |
| <span data-ttu-id="ec39c-117">**ADS \_ EXT \_ INITIALIZE \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="ec39c-117">**ADS\_EXT\_INITIALIZE\_COMPLETE**</span></span> | <span data-ttu-id="ec39c-118">2</span><span class="sxs-lookup"><span data-stu-id="ec39c-118">2</span></span>                                       | <span data-ttu-id="ec39c-119">搭配 [**IADsExtension：：操作**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) 所使用的控制項程式碼，指出延伸模組可以執行任何必要的初始化，端視父物件所支援的功能而定。</span><span class="sxs-lookup"><span data-stu-id="ec39c-119">A control code used with [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) to indicate that extensions can perform any necessary initialization, depending on the features supported by the parent object.</span></span> |
| <span data-ttu-id="ec39c-120">**ADS \_ EXT \_ MAXEXTDISPID**</span><span class="sxs-lookup"><span data-stu-id="ec39c-120">**ADS\_EXT\_MAXEXTDISPID**</span></span>         | <span data-ttu-id="ec39c-121">16777215</span><span class="sxs-lookup"><span data-stu-id="ec39c-121">16777215</span></span>                                | <span data-ttu-id="ec39c-122">擴充物件可用於其方法和屬性的 DISPID 最高。</span><span class="sxs-lookup"><span data-stu-id="ec39c-122">The highest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                   |
| <span data-ttu-id="ec39c-123">**ADS \_ EXT \_ MINEXTDISPID**</span><span class="sxs-lookup"><span data-stu-id="ec39c-123">**ADS\_EXT\_MINEXTDISPID**</span></span>         | <span data-ttu-id="ec39c-124">1</span><span class="sxs-lookup"><span data-stu-id="ec39c-124">1</span></span>                                       | <span data-ttu-id="ec39c-125">擴充物件可用於其方法和屬性的最小 DISPID。</span><span class="sxs-lookup"><span data-stu-id="ec39c-125">The lowest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                    |
| <span data-ttu-id="ec39c-126">**ADS \_ VLV \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="ec39c-126">**ADS\_VLV\_RESPONSE**</span></span>             | <span data-ttu-id="ec39c-127">L "fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span><span class="sxs-lookup"><span data-stu-id="ec39c-127">L"fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span></span> | <span data-ttu-id="ec39c-128">搭配 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) 方法使用，以取得 VLV 搜尋中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ec39c-128">Used with the [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) method to retrieve VLV search metadata.</span></span> <span data-ttu-id="ec39c-129">如需詳細資訊，請參閱 [如何使用 VLV 搜尋](how-to-search-using-vlv.md)。</span><span class="sxs-lookup"><span data-stu-id="ec39c-129">For more information, see [How to Search Using VLV](how-to-search-using-vlv.md).</span></span>        |
| <span data-ttu-id="ec39c-130">**DBPROPFLAGS \_ ADSISEARCH**</span><span class="sxs-lookup"><span data-stu-id="ec39c-130">**DBPROPFLAGS\_ADSISEARCH**</span></span>        | <span data-ttu-id="ec39c-131">0x0000C000</span><span class="sxs-lookup"><span data-stu-id="ec39c-131">0x0000C000</span></span>                              | <span data-ttu-id="ec39c-132">用來處理 OLE DB 提供者。</span><span class="sxs-lookup"><span data-stu-id="ec39c-132">Used to work with the OLE DB provider.</span></span>                                                                                                                                                                           |



 

 

 




