---
title: 儲存屬性集
description: 應用程式可以公開某些檔的狀態資料，讓其他應用程式可以找到和讀取該資料。
ms.assetid: 2e0b5f6c-da1d-47f2-a50d-1ac7f2f0c45d
keywords:
- 儲存屬性集的結構化儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60710b84b52fcc709f8ba3ad1e930d6f5a50a4cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839480"
---
# <a name="storing-property-sets"></a><span data-ttu-id="59f41-104">儲存屬性集</span><span class="sxs-lookup"><span data-stu-id="59f41-104">Storing Property Sets</span></span>

<span data-ttu-id="59f41-105">應用程式可以公開某些檔的狀態資料，讓其他應用程式可以找到和讀取該資料。</span><span class="sxs-lookup"><span data-stu-id="59f41-105">Applications can expose some of the state data of their documents so that other applications can locate and read that data.</span></span> <span data-ttu-id="59f41-106">其中一些範例是描述使用文字處理器建立之檔的作者、標題和關鍵字，或檔中使用的字型清單的屬性集。</span><span class="sxs-lookup"><span data-stu-id="59f41-106">Some examples are a property set describing the author, title, and keywords of a document created with a word processor, or the list of fonts used in a document.</span></span> <span data-ttu-id="59f41-107">這項功能不限於檔;它也可以用在内嵌物件上。</span><span class="sxs-lookup"><span data-stu-id="59f41-107">This facility is not restricted to documents; it can also be used on embedded objects.</span></span> <span data-ttu-id="59f41-108">一般而言，屬性集的存取應透過 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面，但本節會描述先前建議的方法。</span><span class="sxs-lookup"><span data-stu-id="59f41-108">Generally, access to property sets should be through the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interfaces, but this section describes the previously recommended way.</span></span>

> [!Note]  
> <span data-ttu-id="59f41-109">如果儲存應用程式內部的屬性集，您可能不會想要使用下列指導方針。</span><span class="sxs-lookup"><span data-stu-id="59f41-109">If storing a property set that is internal to your application, you may not want to use the following guidelines.</span></span> <span data-ttu-id="59f41-110">若要將屬性集公開給其他應用程式，請遵循這些指導方針。</span><span class="sxs-lookup"><span data-stu-id="59f41-110">To expose your property set to other applications, follow these guidelines.</span></span>

 

<span data-ttu-id="59f41-111">**將屬性集儲存在複合檔案中**</span><span class="sxs-lookup"><span data-stu-id="59f41-111">**To store a property set in a compound file**</span></span>

1.  <span data-ttu-id="59f41-112">在儲存結構的相同層級中，建立 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 或 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 實例作為其資料流程。</span><span class="sxs-lookup"><span data-stu-id="59f41-112">Create an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) instance in the same level of the storage structure as its data streams.</span></span> <span data-ttu-id="59f41-113">遵循 **IStorage** 或 **IStream** 實例的名稱，並使用 " \\ 005"。</span><span class="sxs-lookup"><span data-stu-id="59f41-113">Follow the name of your **IStorage** or **IStream** instance with "\\005."</span></span> <span data-ttu-id="59f41-114">以0x05 開頭的資料流程和儲存名稱會保留給可在應用程式之間共用的通用屬性集。</span><span class="sxs-lookup"><span data-stu-id="59f41-114">Stream and storage names that begin with 0x05 are reserved for common property sets that can be shared among applications.</span></span> <span data-ttu-id="59f41-115">此外，以該值開頭的資料流程會限制為 256 KB。</span><span class="sxs-lookup"><span data-stu-id="59f41-115">Also, streams beginning with that value are limited to 256 KB.</span></span> <span data-ttu-id="59f41-116">您可以從已發行的名稱和格式選取名稱，或指派屬性來設定 FMTID，並根據 [儲存物件命名慣例](storage-object-naming-conventions.md)中所述的慣例，從 FMTID 衍生名稱。</span><span class="sxs-lookup"><span data-stu-id="59f41-116">The names can be selected from either published names and formats, or by assigning the property set a FMTID and deriving the name from the FMTID according to the conventions described in [Storage Object Naming Conventions](storage-object-naming-conventions.md).</span></span>
2.  <span data-ttu-id="59f41-117">屬性集可能會儲存在單一 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 實例或包含多個資料流程和儲存的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 實例中。</span><span class="sxs-lookup"><span data-stu-id="59f41-117">A property set may be stored in a single [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) instance or in an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instance containing multiple streams and storages.</span></span> <span data-ttu-id="59f41-118">在 **IStorage** 實例的案例中，名為「內容」的內含資料流程是包含屬性值的主要資料流程，其中某些值可能是這個屬性集之儲存體內的其他資料流程或儲存實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="59f41-118">In the case of an **IStorage** instance, the contained stream named Contents is the primary stream containing property values, where some values may be names of other streams or storage instances within the storage for this property set.</span></span>
3.  <span data-ttu-id="59f41-119">指定可顯示或提供以程式設計方式存取屬性值之物件類別的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="59f41-119">Specify the CLSID of the object class that can display or provide programmatic access to the property values.</span></span> <span data-ttu-id="59f41-120">如果沒有這類類別，則 CLSID 應設定為屬性集的格式識別碼。</span><span class="sxs-lookup"><span data-stu-id="59f41-120">If there is no such class, the CLSID should be set to the format identifier of the property set.</span></span> <span data-ttu-id="59f41-121">若為使用 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 實例的屬性集，請將 **ISTORAGE** 實例的 CLSID 設定為與儲存在內容資料流程中的相同，或設定為 **clsid \_ Null**; 新建立的 **IStorage** 實例中的值。</span><span class="sxs-lookup"><span data-stu-id="59f41-121">For a property set that uses an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instance, either set the CLSID of the **IStorage** instance to be the same as that stored in the Contents stream or to **CLSID\_NULL**; the value in a newly created **IStorage** instance.</span></span>
4.  <span data-ttu-id="59f41-122">您可以選擇指定可顯示的名稱，以形成字典的內容。</span><span class="sxs-lookup"><span data-stu-id="59f41-122">You have the option of specifying displayable names that form the contents of the dictionary.</span></span>

<span data-ttu-id="59f41-123">有些應用程式只能讀取儲存為 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 實例的屬性集的實作為。</span><span class="sxs-lookup"><span data-stu-id="59f41-123">Some applications can read only implementations of property sets stored as [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) instances.</span></span> <span data-ttu-id="59f41-124">應用程式應該撰寫成預期屬性集可能會儲存在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 或 **IStream** 實例中，除非屬性集定義另外指出。</span><span class="sxs-lookup"><span data-stu-id="59f41-124">Applications should be written to expect that a property set may be stored in either an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or **IStream** instance, unless the property set definition indicates otherwise.</span></span> <span data-ttu-id="59f41-125">例如，摘要資訊屬性集定義指出只能儲存在命名的 **IStream** 實例中。</span><span class="sxs-lookup"><span data-stu-id="59f41-125">For example, the Summary Information property set definition states that it can only be stored in a named **IStream** instance.</span></span> <span data-ttu-id="59f41-126">如果您要搜尋屬性集，但不知道它是儲存或資料流程，請先尋找具有您屬性集名稱的 **IStream** 實例。</span><span class="sxs-lookup"><span data-stu-id="59f41-126">In cases where you are searching for a property set and do not know whether it is a storage or stream, look for an **IStream** instance with your property set name first.</span></span> <span data-ttu-id="59f41-127">如果失敗，請尋找 **IStorage** 實例。</span><span class="sxs-lookup"><span data-stu-id="59f41-127">If that fails, look for an **IStorage** instance.</span></span>

<span data-ttu-id="59f41-128">若要更瞭解如何在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 的執行中儲存屬性集，假設有一個可編輯動物相關資訊的應用程式類別。</span><span class="sxs-lookup"><span data-stu-id="59f41-128">To better understand storing property sets in an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) implementation, suppose there is a class of applications that edit information about animals.</span></span> <span data-ttu-id="59f41-129">首先，系統 \_ 會為這組應用程式定義 clsid (clsid AnimalApp) ，以便他們瞭解包含動物資訊的屬性集 (**FMTID \_ AnimalInfo**) ，以及其他包含醫療資訊 (**FMTID \_ MedicalInfo**) 。</span><span class="sxs-lookup"><span data-stu-id="59f41-129">First, a CLSID (CLSID\_AnimalApp) is defined for this set of applications, so they can indicate that they understand property sets that contain animal information (**FMTID\_AnimalInfo**), and others that contain medical information (**FMTID\_MedicalInfo**).</span></span>

``` syntax
IStorage (File): "C:\OLE\REVO.DOC" 
  IStorage: "\005AnimalInfo", CLSID = CLSID_AnimalApp 
    IStream: "Contents" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = FMTID_AnimalInfo 
      Property: Type = PID_ANIMALTYPE, Type = VT_LPWSTR, 
              Value = L"Dog" 
      Property: Type = PID_ANIMALNAME, Type = VT_LPWSTR, 
              Value = L"Revo" 
      Property: Type = PID_MEDICALHISTORY, Type = VT_STREAMED_OBJECT, 
              Value = "MedicalInfo" 
      ... 
    IStream: "MedicalInfo" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = CLSID_MedicalInfo 
      Property: Type = PID_VETNAME, Type = VT_LPWSTR, 
              Value = L"Dr. Woof" 
      Property: Type = PID_LASTEXAM, Type = VT_DATE, Value = ...
```

<span data-ttu-id="59f41-130">請注意， [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面的 clsid 和這兩個屬性集都是 **clsid \_ AnimalApp**。</span><span class="sxs-lookup"><span data-stu-id="59f41-130">Be aware that the CLSID of the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and both property sets is **CLSID\_AnimalApp**.</span></span> <span data-ttu-id="59f41-131">這會識別可顯示及/或提供以程式設計方式存取這些屬性集的任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="59f41-131">This identifies any application that can display and/or provide programmatic access to these property sets.</span></span> <span data-ttu-id="59f41-132">任何應用程式都可以讀取屬性集內的資料 () 的點，但只有以 CLSID AnimalApp 類別識別碼識別的應用程式 \_ 可以瞭解屬性集中資料的意義。</span><span class="sxs-lookup"><span data-stu-id="59f41-132">Any application can read the data within the property sets (the point behind property sets), but only applications identified with the class identifier of CLSID\_AnimalApp can understand the meaning of the data in the property sets.</span></span>

 

 




