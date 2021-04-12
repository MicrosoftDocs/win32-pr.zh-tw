---
title: 取得會計屬性
description: Accounting 物件是要求處理常式集合中的其中一個物件。
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375873"
---
# <a name="obtaining-accounting-properties"></a><span data-ttu-id="5ce76-103">取得會計屬性</span><span class="sxs-lookup"><span data-stu-id="5ce76-103">Obtaining Accounting Properties</span></span>

> [!Note]  
> <span data-ttu-id="5ce76-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="5ce76-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="5ce76-105">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="5ce76-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="5ce76-106">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="5ce76-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="5ce76-107">Accounting 物件是要求處理常式集合中的其中一個物件。</span><span class="sxs-lookup"><span data-stu-id="5ce76-107">The accounting object is one of the objects in the Request Handlers collection.</span></span> <span data-ttu-id="5ce76-108">要求處理常式集合的列舉值為 **屬性 \_ IAS \_ REQUESTHANDLERS \_ 集合**。</span><span class="sxs-lookup"><span data-stu-id="5ce76-108">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="5ce76-109">會計物件的處理常式名稱是「Microsoft 帳戶處理」。</span><span class="sxs-lookup"><span data-stu-id="5ce76-109">The name of the handler for the accounting object is "Microsoft Accounting".</span></span>

<span data-ttu-id="5ce76-110">下列 Visual Basic 程式碼會從會計物件處理常式存取可用的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ce76-110">The following Visual Basic code accesses the properties available from the accounting object handler.</span></span>


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



<span data-ttu-id="5ce76-111">若要使用 c + + 存取帳戶處理屬性，請先取得要求處理常式集合。</span><span class="sxs-lookup"><span data-stu-id="5ce76-111">To access the accounting properties using C++, first obtain the request handlers collection.</span></span> <span data-ttu-id="5ce76-112">抓取 [集合](/windows/desktop/Nps/sdo-retrieving-a-collection) 包含的 c + + 程式碼會示範如何取得集合。</span><span class="sxs-lookup"><span data-stu-id="5ce76-112">The [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection) contains C++ code that demonstrates how to obtain a collection.</span></span> <span data-ttu-id="5ce76-113">要求處理常式集合的列舉值為 **屬性 \_ IAS \_ REQUESTHANDLERS \_ 集合**。</span><span class="sxs-lookup"><span data-stu-id="5ce76-113">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="5ce76-114"> (對應至各種 NPS 集合的值會以 [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) 列舉型別列舉。 ) </span><span class="sxs-lookup"><span data-stu-id="5ce76-114">(The values corresponding to the various NPS collections are enumerated by the [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type.)</span></span>

<span data-ttu-id="5ce76-115">要求處理常式集合包含名為「Microsoft 帳戶處理」的物件。</span><span class="sxs-lookup"><span data-stu-id="5ce76-115">The request handlers collection contains an object named "Microsoft Accounting".</span></span> <span data-ttu-id="5ce76-116">從集合中取出這個物件。</span><span class="sxs-lookup"><span data-stu-id="5ce76-116">Retrieve this object from the collection.</span></span> <span data-ttu-id="5ce76-117">[從集合中抓取物件](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)的區段包含 c + + 程式碼，該程式碼會示範如何從集合取得物件。</span><span class="sxs-lookup"><span data-stu-id="5ce76-117">The section [Retrieving an Object from a Collection](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contains C++ code that demonstrates how to obtain an object from a collection.</span></span>

<span data-ttu-id="5ce76-118">當您擁有 Microsoft Accounting 物件之後，請使用 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))取得物件的 [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)介面。</span><span class="sxs-lookup"><span data-stu-id="5ce76-118">Once you have the Microsoft Accounting object, obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object using [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="5ce76-119">抓取 [使用者 SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) 的區段包含 c + + 程式碼，該程式碼會示範如何取得物件的 **ISdo** 介面。</span><span class="sxs-lookup"><span data-stu-id="5ce76-119">The section [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains C++ code that demonstrates how obtain an **ISdo** interface for an object.</span></span> <span data-ttu-id="5ce76-120">然後，您可以使用 [**ISdo：： GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) 方法來取得 Microsoft Accounting 物件的屬性值。</span><span class="sxs-lookup"><span data-stu-id="5ce76-120">You can then use the [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) method to obtain property values for the Microsoft Accounting object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ce76-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ce76-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ce76-122">正在抓取集合</span><span class="sxs-lookup"><span data-stu-id="5ce76-122">Retrieving a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[<span data-ttu-id="5ce76-123">從集合中取出物件</span><span class="sxs-lookup"><span data-stu-id="5ce76-123">Retrieving an Object from a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[<span data-ttu-id="5ce76-124">正在抓取使用者 SDO</span><span class="sxs-lookup"><span data-stu-id="5ce76-124">Retrieving a User SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[<span data-ttu-id="5ce76-125">**ISdo**</span><span class="sxs-lookup"><span data-stu-id="5ce76-125">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

<span data-ttu-id="5ce76-126">[**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="5ce76-126">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> <dt>

[<span data-ttu-id="5ce76-127">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="5ce76-127">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 