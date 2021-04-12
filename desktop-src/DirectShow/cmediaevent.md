---
description: CMediaEvent 類別提供雙重介面 IMediaEvent 之 IDispatch 方法的基類實作為基底類別。 它會將 IMediaEvent 介面的屬性和方法保留為純虛擬。
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: CMediaEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195768"
---
# <a name="cmediaevent-class"></a><span data-ttu-id="81122-104">CMediaEvent 類別</span><span class="sxs-lookup"><span data-stu-id="81122-104">CMediaEvent class</span></span>

![cmediaevent 類別階層](images/cutil03.png)

<span data-ttu-id="81122-106">`CMediaEvent`類別提供雙重介面 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)之 **IDispatch** 方法的基類實作為基底類別。</span><span class="sxs-lookup"><span data-stu-id="81122-106">The `CMediaEvent` class provides base class implementation of the **IDispatch** methods of the dual-interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span> <span data-ttu-id="81122-107">它會將 **IMediaEvent** 介面的屬性和方法保留為純虛擬。</span><span class="sxs-lookup"><span data-stu-id="81122-107">It leaves as pure virtual the properties and methods of the **IMediaEvent** interface.</span></span>

<span data-ttu-id="81122-108">`CMediaEvent`類別也提供衍生自 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)之 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)介面的基類實作為基底類別。</span><span class="sxs-lookup"><span data-stu-id="81122-108">The `CMediaEvent` class also provides base class implementation of the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface which derives from [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span>

<span data-ttu-id="81122-109">[**CMediaEvent：： GetIDsOfNames**](cmediaevent-getidsofnames.md)、 [**CMediaEvent：： GetTypeInfo**](cmediaevent-gettypeinfo.md)、 [**CMediaEvent：： GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)和 [**CMediaEvent：： Invoke**](cmediaevent-invoke.md)成員函式是 **IDispatch** 介面的標準，使用 [**CBaseDispatch**](cbasedispatch.md)類別 (和類型程式庫) 來剖析命令，並將其傳遞給 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)介面的純虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="81122-109">The [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent::GetTypeInfoCount**](cmediaevent-gettypeinfocount.md), and [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member functions are standard implementations of the **IDispatch** interface using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>



| <span data-ttu-id="81122-110">成員函數</span><span class="sxs-lookup"><span data-stu-id="81122-110">Member Functions</span></span>                                         | <span data-ttu-id="81122-111">Description</span><span class="sxs-lookup"><span data-stu-id="81122-111">Description</span></span>                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81122-112">**CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="81122-112">**CMediaEvent**</span></span>](cmediaevent-cmediaevent.md)           | <span data-ttu-id="81122-113">結構 **CMediaEvent** 物件。</span><span class="sxs-lookup"><span data-stu-id="81122-113">Constructs a **CMediaEvent** object.</span></span>                                                                                                                                                          |
| <span data-ttu-id="81122-114">IDispatch 方法</span><span class="sxs-lookup"><span data-stu-id="81122-114">IDispatch Methods</span></span>                                        | <span data-ttu-id="81122-115">Description</span><span class="sxs-lookup"><span data-stu-id="81122-115">Description</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="81122-116">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="81122-116">**GetIDsOfNames**</span></span>](cmediaevent-getidsofnames.md)       | <span data-ttu-id="81122-117">將單一成員和一組選擇性的參數對應至一組對應的整數分派識別碼，可在後續呼叫 **IDispatch：： Invoke** 方法時使用。</span><span class="sxs-lookup"><span data-stu-id="81122-117">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used during subsequent calls to the **IDispatch::Invoke** method.</span></span> |
| [<span data-ttu-id="81122-118">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="81122-118">**GetTypeInfo**</span></span>](cmediaevent-gettypeinfo.md)           | <span data-ttu-id="81122-119">抓取類型資訊物件，此物件會捕獲介面的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="81122-119">Retrieves a type-information object, which retrieves the type information for an interface.</span></span>                                                                                                   |
| [<span data-ttu-id="81122-120">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="81122-120">**GetTypeInfoCount**</span></span>](cmediaevent-gettypeinfocount.md) | <span data-ttu-id="81122-121">抓取物件所提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="81122-121">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                    |
| [<span data-ttu-id="81122-122">**調用**</span><span class="sxs-lookup"><span data-stu-id="81122-122">**Invoke**</span></span>](cmediaevent-invoke.md)                     | <span data-ttu-id="81122-123">提供物件所公開的屬性和方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="81122-123">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                               |



 

 

 



