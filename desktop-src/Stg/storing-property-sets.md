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
# <a name="storing-property-sets"></a>儲存屬性集

應用程式可以公開某些檔的狀態資料，讓其他應用程式可以找到和讀取該資料。 其中一些範例是描述使用文字處理器建立之檔的作者、標題和關鍵字，或檔中使用的字型清單的屬性集。 這項功能不限於檔;它也可以用在内嵌物件上。 一般而言，屬性集的存取應透過 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面，但本節會描述先前建議的方法。

> [!Note]  
> 如果儲存應用程式內部的屬性集，您可能不會想要使用下列指導方針。 若要將屬性集公開給其他應用程式，請遵循這些指導方針。

 

**將屬性集儲存在複合檔案中**

1.  在儲存結構的相同層級中，建立 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 或 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 實例作為其資料流程。 遵循 **IStorage** 或 **IStream** 實例的名稱，並使用 " \\ 005"。 以0x05 開頭的資料流程和儲存名稱會保留給可在應用程式之間共用的通用屬性集。 此外，以該值開頭的資料流程會限制為 256 KB。 您可以從已發行的名稱和格式選取名稱，或指派屬性來設定 FMTID，並根據 [儲存物件命名慣例](storage-object-naming-conventions.md)中所述的慣例，從 FMTID 衍生名稱。
2.  屬性集可能會儲存在單一 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 實例或包含多個資料流程和儲存的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 實例中。 在 **IStorage** 實例的案例中，名為「內容」的內含資料流程是包含屬性值的主要資料流程，其中某些值可能是這個屬性集之儲存體內的其他資料流程或儲存實例的名稱。
3.  指定可顯示或提供以程式設計方式存取屬性值之物件類別的 CLSID。 如果沒有這類類別，則 CLSID 應設定為屬性集的格式識別碼。 若為使用 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 實例的屬性集，請將 **ISTORAGE** 實例的 CLSID 設定為與儲存在內容資料流程中的相同，或設定為 **clsid \_ Null**; 新建立的 **IStorage** 實例中的值。
4.  您可以選擇指定可顯示的名稱，以形成字典的內容。

有些應用程式只能讀取儲存為 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 實例的屬性集的實作為。 應用程式應該撰寫成預期屬性集可能會儲存在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 或 **IStream** 實例中，除非屬性集定義另外指出。 例如，摘要資訊屬性集定義指出只能儲存在命名的 **IStream** 實例中。 如果您要搜尋屬性集，但不知道它是儲存或資料流程，請先尋找具有您屬性集名稱的 **IStream** 實例。 如果失敗，請尋找 **IStorage** 實例。

若要更瞭解如何在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 的執行中儲存屬性集，假設有一個可編輯動物相關資訊的應用程式類別。 首先，系統 \_ 會為這組應用程式定義 clsid (clsid AnimalApp) ，以便他們瞭解包含動物資訊的屬性集 (**FMTID \_ AnimalInfo**) ，以及其他包含醫療資訊 (**FMTID \_ MedicalInfo**) 。

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

請注意， [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面的 clsid 和這兩個屬性集都是 **clsid \_ AnimalApp**。 這會識別可顯示及/或提供以程式設計方式存取這些屬性集的任何應用程式。 任何應用程式都可以讀取屬性集內的資料 () 的點，但只有以 CLSID AnimalApp 類別識別碼識別的應用程式 \_ 可以瞭解屬性集中資料的意義。

 

 




