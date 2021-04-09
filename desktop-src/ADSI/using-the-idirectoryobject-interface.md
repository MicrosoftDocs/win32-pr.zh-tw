---
title: 使用 IDirectoryObject 介面
description: 當您在 C 或 c + + 中建立使用早期繫結的 ADSI 用戶端時，如果您的用戶端呼叫 IDirectoryObject 介面，而不是 IADs 介面，您將會有更多的 ADSI 資料類型可供使用。
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- 使用 IDirectoryObject ADSI
- ADSI ADSI，使用 IDirectoryObject 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671104"
---
# <a name="using-the-idirectoryobject-interface"></a><span data-ttu-id="2ee51-105">使用 IDirectoryObject 介面</span><span class="sxs-lookup"><span data-stu-id="2ee51-105">Using the IDirectoryObject Interface</span></span>

<span data-ttu-id="2ee51-106">當您在 C 或 c + + 中建立使用早期繫結的 ADSI 用戶端時，如果您的用戶端呼叫 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面，而不是 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面，您將會有更多的 adsi 資料類型可供使用。</span><span class="sxs-lookup"><span data-stu-id="2ee51-106">When you create an ADSI client in C or C++ that uses early binding, you will have a wider variety of ADSI data types available to use for your client if it calls the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface instead of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="2ee51-107">**IDirectoryObject** 介面提供的方法可支援物件的維護屬性子集，以及存取其屬性。</span><span class="sxs-lookup"><span data-stu-id="2ee51-107">The **IDirectoryObject** interface provides methods to support a subset of an object's maintenance properties and to access its attributes.</span></span> <span data-ttu-id="2ee51-108">下圖顯示資料結構之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="2ee51-108">The following figure shows the relationships among the data structures.</span></span>

![idirectoryobject 介面資料結構](images/ds2dso.png)

<span data-ttu-id="2ee51-110">在上圖中，structure [**ADS \_ 物件 \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_object_info) 定義的屬性會依分辨名稱、相對分辨名稱、容器 (p n) 、依物件類型 (ClassDN) ，以及架構定義 (SchemaDN) 來識別物件。</span><span class="sxs-lookup"><span data-stu-id="2ee51-110">In the preceding figure, the structure [**ADS\_OBJECT\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_object_info) defines properties that identify the object by distinguished name, relative distinguished name, by container (ParentDN), by object type (ClassDN), and by schema definition (SchemaDN).</span></span> <span data-ttu-id="2ee51-111">屬性描述項 [**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)包含名稱、資料類型、 [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)中所顯示的資料值陣列，以及指示基礎目錄服務對 [ADS \_ ATTR \_ \*](adsi-constants.md)屬性中詳細說明的屬性執行特定作業的旗標。</span><span class="sxs-lookup"><span data-stu-id="2ee51-111">The attribute descriptor [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) consists of a name, data type, an array of data values shown in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue), and a flag that directs the underlying directory service to perform certain operations on the attributes detailed in [ADS\_ATTR\_\* constants](adsi-constants.md).</span></span> <span data-ttu-id="2ee51-112">這些屬性的資料類型包括 ADSI 擴充語法類型，如 [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)中所述。</span><span class="sxs-lookup"><span data-stu-id="2ee51-112">The data types for these attributes include the ADSI extended syntax types, detailed in [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).</span></span>

 

 




