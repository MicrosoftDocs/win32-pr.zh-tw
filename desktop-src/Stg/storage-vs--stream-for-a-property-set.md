---
title: 屬性集的儲存和資料流程物件
description: 程式設計人員指定在建立屬性集時，屬性集是否儲存在儲存體或資料流程中。
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4ebd5d03c3b17e02aa47a7a859576b4cc04607a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104024249"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a><span data-ttu-id="00d28-103">屬性集的儲存和資料流程物件</span><span class="sxs-lookup"><span data-stu-id="00d28-103">Storage and Stream Objects for a Property Set</span></span>

<span data-ttu-id="00d28-104">程式設計人員指定在建立屬性集時，屬性集是否儲存在儲存體或資料流程中。</span><span class="sxs-lookup"><span data-stu-id="00d28-104">The programmer specifies whether a property set is stored in a storage or a stream when the property set is created.</span></span> <span data-ttu-id="00d28-105">PROPSETFLAG \_ 簡單列舉值（以 *grfFlags* 參數傳遞給 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 方法）指出這一點。</span><span class="sxs-lookup"><span data-stu-id="00d28-105">The PROPSETFLAG\_NONSIMPLE enumeration value, passed in the *grfFlags* parameter to the [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) method, indicates this.</span></span> <span data-ttu-id="00d28-106">設定屬性集儲存位置會提供適當的應用程式控制，以透過 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面與 COM 屬性集完全互通。</span><span class="sxs-lookup"><span data-stu-id="00d28-106">Setting where the property set is stored provides proper application controls to fully interoperate through the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface with the COM property set.</span></span>

<span data-ttu-id="00d28-107">如果設定了 PROPSETFLAG \_ 簡單旗標，則會將屬性集儲存在儲存物件中，並將簡單屬性值寫入其中。</span><span class="sxs-lookup"><span data-stu-id="00d28-107">If the PROPSETFLAG\_NONSIMPLE flag is set, the property set is stored in a storage object, and nonsimple property values can be written to it.</span></span> <span data-ttu-id="00d28-108">簡單值包括具有 VT  \_ 儲存體、VT \_ 資料流程、VT \_ 儲存 \_ 物件或 VT \_ 資料流程 \_ 物件之 VARTYPE 的值。</span><span class="sxs-lookup"><span data-stu-id="00d28-108">Nonsimple values include values with a **VARTYPE** of VT\_STORAGE, VT\_STREAM, VT\_STORED\_OBJECT, or VT\_STREAMED\_OBJECT.</span></span> <span data-ttu-id="00d28-109">如需 **VARTYPE** 值和其使用方式的詳細資訊，請參閱 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構。</span><span class="sxs-lookup"><span data-stu-id="00d28-109">For more information about **VARTYPE** values and how to use them, see the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="00d28-110">如果 \_ 未設定 PROPSETFLAG 簡單旗標，則只可將簡單的值寫入屬性集。</span><span class="sxs-lookup"><span data-stu-id="00d28-110">If the PROPSETFLAG\_NONSIMPLE flag is not set, only simple values can be written to the property set.</span></span>

<span data-ttu-id="00d28-111">在簡單屬性集的儲存物件中，會建立名為「內容」的資料流程。</span><span class="sxs-lookup"><span data-stu-id="00d28-111">In the storage object of a nonsimple property set, a stream is created named Contents.</span></span> <span data-ttu-id="00d28-112">這是屬性集的主要資料流程，並保留所有簡單的屬性值。</span><span class="sxs-lookup"><span data-stu-id="00d28-112">This is the primary stream of the property set, and holds all simple property values.</span></span> <span data-ttu-id="00d28-113">簡單屬性值 (資料流程和儲存) 會儲存在屬性設定為子串流和儲存體的主要儲存物件下。</span><span class="sxs-lookup"><span data-stu-id="00d28-113">Nonsimple property values (streams and storages) are stored under the main storage object of the property set as substreams and storages.</span></span> <span data-ttu-id="00d28-114">也就是說，這些簡單值會儲存為內容資料流程的同級。</span><span class="sxs-lookup"><span data-stu-id="00d28-114">That is, these nonsimple values are stored as siblings to the Contents stream.</span></span> <span data-ttu-id="00d28-115">同輩資料流程和儲存的名稱是由實作為來決定，並儲存在內容資料流程中，類似于儲存簡單字串屬性的方式。</span><span class="sxs-lookup"><span data-stu-id="00d28-115">The name of the sibling streams and storages is determined by the implementation, and stored in the Contents stream similar to the way a simple string property is stored.</span></span>

 

 