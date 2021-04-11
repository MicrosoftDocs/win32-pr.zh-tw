---
description: CMediaControl 類別提供雙重介面 IMediaControl 之 IDispatch 方法的基類處理。 它會將 IMediaControl 介面的屬性和方法保留為純虛擬。
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: CMediaControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853479"
---
# <a name="cmediacontrol-class"></a><span data-ttu-id="33623-104">CMediaControl 類別</span><span class="sxs-lookup"><span data-stu-id="33623-104">CMediaControl class</span></span>

![cmediacontrol 類別階層](images/cutil02.png)

<span data-ttu-id="33623-106">`CMediaControl`類別提供雙重介面 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)之 [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)方法的基類處理。</span><span class="sxs-lookup"><span data-stu-id="33623-106">The `CMediaControl` class provides base class handling of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods of the dual-interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol).</span></span> <span data-ttu-id="33623-107">它會將 **IMediaControl** 介面的屬性和方法保留為純虛擬。</span><span class="sxs-lookup"><span data-stu-id="33623-107">It leaves as pure virtual the properties and methods of the **IMediaControl** interface.</span></span>

<span data-ttu-id="33623-108">篩選圖形管理員通常是唯一會執行 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="33623-108">Typically, the filter graph manager is the only object that implements the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span> <span data-ttu-id="33623-109"> (篩選準則會執行由 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)繼承的 [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)介面，以從篩選圖形管理員接收控制命令 ) 。因此，此類別庫的限制僅供篩選開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="33623-109">(filters implement the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface, inherited by [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), to receive control commands from the filter graph manager.) Therefore, this class library is of limited use to filter developers.</span></span>

<span data-ttu-id="33623-110">[**CMediaControl：： GetIDsOfNames**](cmediacontrol-getidsofnames.md)、 [**CMediaControl：： GetTypeInfo**](cmediacontrol-gettypeinfo.md)、 [**CMediaControl：： GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)和 [**CMediaControl：： Invoke**](cmediacontrol-invoke.md)成員函式是使用 [**CBaseDispatch**](cbasedispatch.md)類別 (的 [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)方法的標準實，而類型程式庫) 來剖析命令並傳遞給 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)介面的純虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="33623-110">The [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl::GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md), and [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member functions are standard implementations of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span>

<span data-ttu-id="33623-111">Odl 中定義的 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 方法會保留為純虛擬。</span><span class="sxs-lookup"><span data-stu-id="33623-111">The [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods, defined in control.odl, are left as pure virtual.</span></span>



| <span data-ttu-id="33623-112">成員函數</span><span class="sxs-lookup"><span data-stu-id="33623-112">Member Functions</span></span>                                           | <span data-ttu-id="33623-113">Description</span><span class="sxs-lookup"><span data-stu-id="33623-113">Description</span></span>                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33623-114">**CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="33623-114">**CMediaControl**</span></span>](cmediacontrol-cmediacontrol.md)       | <span data-ttu-id="33623-115">結構 **CMediaControl** 物件。</span><span class="sxs-lookup"><span data-stu-id="33623-115">Constructs a **CMediaControl** object.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="33623-116">IDispatch 方法</span><span class="sxs-lookup"><span data-stu-id="33623-116">IDispatch Methods</span></span>                                          | <span data-ttu-id="33623-117">Description</span><span class="sxs-lookup"><span data-stu-id="33623-117">Description</span></span>                                                                                                                                                                                                                             |
| [<span data-ttu-id="33623-118">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="33623-118">**GetIDsOfNames**</span></span>](cmediacontrol-getidsofnames.md)       | <span data-ttu-id="33623-119">將單一成員和一組選擇性的參數對應至一組對應的整數分派識別碼 (Dispid) ，可在後續呼叫 [**CMediaControl：： Invoke**](cmediacontrol-invoke.md) 方法期間使用。</span><span class="sxs-lookup"><span data-stu-id="33623-119">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used during subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) method.</span></span> |
| [<span data-ttu-id="33623-120">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="33623-120">**GetTypeInfo**</span></span>](cmediacontrol-gettypeinfo.md)           | <span data-ttu-id="33623-121">抓取類型資訊物件，此物件可以取得介面的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="33623-121">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>                                                                                                                                          |
| [<span data-ttu-id="33623-122">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="33623-122">**GetTypeInfoCount**</span></span>](cmediacontrol-gettypeinfocount.md) | <span data-ttu-id="33623-123">抓取物件所提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="33623-123">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="33623-124">**調用**</span><span class="sxs-lookup"><span data-stu-id="33623-124">**Invoke**</span></span>](cmediacontrol-invoke.md)                     | <span data-ttu-id="33623-125">提供物件所公開的屬性和方法的存取權。</span><span class="sxs-lookup"><span data-stu-id="33623-125">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                                                                         |



 

 

 
