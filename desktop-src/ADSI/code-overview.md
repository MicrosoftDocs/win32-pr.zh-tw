---
title: 程式碼總覽
description: 下圖是執行 ADSI 範例提供者元件所需之程式碼區塊的概念表示。
ms.assetid: b353c2d9-ef86-4e4c-ac00-4756fc9ec57d
ms.tgt_platform: multiple
keywords:
- 程式碼總覽廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99a4974ac97488fc051ea80dbde7a8a83fa329e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024096"
---
# <a name="code-overview"></a>程式碼總覽

下圖是執行 ADSI 範例提供者元件所需之程式碼區塊的概念表示。 下圖將說明每個區段。 有經驗的 COM 程式設計人員可能會發現這是範例提供者元件的理想總覽。 如需詳細資訊，請參閱程式 [代碼詳細資料](code-details.md)。

![範例提供者執行](images/dssmco.png)

下列編號專案對應到圖中的區塊元素。

1.  載入 DLL (Libmain .cpp、Guid.empty) 。 DLL 的進入點。 這兩個提供者物件的 Class factory 靜態物件定義： Guid.empty 包含各種範例提供者元件物件之執行的 CLSID 定義。
2.  Provider 物件 class factory 和建立程式碼 (Cprovcf .cpp、Cprov .cpp、Stdfact .cpp) 。 提供者物件是支援在標記系結作業期間 [**IParseDisplayName**](/windows/win32/api/oleidl/nn-oleidl-iparsedisplayname) 的物件，如在範例提供者元件中尋找和系結所述。
3.  系結至 (Getobj .cpp) 的物件。 此程式碼會呼叫剖析器來檢查指定的 ADsPath 語法是否正確，然後針對要建立為 Active Directory 物件的專案，執行任何必要的從 ADsPath 對應到原生目錄服務路徑。 它會查閱此類型物件的架構定義，並填入必要的屬性。 建立 Active Directory 物件之後，會針對呼叫端抓取 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 的介面指標。
4.  提供者命名空間的剖析器 (剖析 .cpp) 。 這是專案3叫用的程式碼。 剖析器會驗證傳入的 ADsPath 字串在語法上是否正確。
5.  Namespace 物件的 Class factory、建立和列舉 (Cnamcf .cpp、Cnamesp .cpp、Cenumns .cpp) 。 命名空間物件是可列舉的容器物件，可尋找此命名空間的所有根節點物件。
6.  泛型 Active Directory 物件的 class factory 和建立程式碼、class factory、泛型 ADs 容器物件的建立和列舉程式碼 (Cgenobj .cpp、Cenumobj .cpp、Common .cpp、Core .cpp) 。 這段程式碼會在建立 Active Directory 物件時執行。
7.  篩選和列舉變數 (Cenumvar .cpp、物件 .cpp) 。 當單一類型的 VARIANT 元素集合在 ADSI 內進行管理時，會使用此程式碼。
8.  全域 (全域 .cpp) 。 命名空間關鍵字、從原生資料格式到 ADs Automation VARIANT 類型的語法對應結構，全都定義于此處。
9.  封送處理/封送處理資料 (套件 .cpp、屬性 .cpp、Smpoper .cpp) 。 當物件的屬性載入至屬性快取時，就會發生從原生資料格式轉換成支援的 Automation VARIANT 類型集合。 當具有指標的結構在記憶體中複製、刪除或移動時，必須執行資料的其他特殊處理。
10. 屬性快取 (Cprops .cpp) 。 快取屬性是 ADSI 環境的一項功能。 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)、 [**IADs：： GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)和 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)方法會針對屬性快取採取動作。
11. 記憶體管理 (Memory .cpp) 。 使用一組記憶體函式來配置和釋放記憶體，可讓範例提供者元件追蹤記憶體使用並停止記憶體流失。
12. 架構物件和管理 (Cschobj .cpp、Cprpobj .cpp、Cclsobj .cpp、Cenumsch .cpp) 。 這包括用來建立、管理和列舉架構物件的常式。 這包括架構類別物件、屬性物件和語法物件，除了能夠列舉架構類別容器物件之外。
13. 作業系統特定的呼叫 (RegDSAPI .cpp) 。 這包括參考原生作業系統的所有呼叫。 在其他函式中，它們包含開啟、關閉、讀取和修改物件的功能，以及存取架構和屬性資料的函式。 範例提供者元件在使用登錄模擬目錄階層時發生。 只有對提供者寫入器而言，函式名稱應該很感興趣。
14. [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (Cdispmgr .cpp) 。 這段程式碼會存取類型程式庫資料，以允許以自動化相容的方式叫用介面方法。

 

 