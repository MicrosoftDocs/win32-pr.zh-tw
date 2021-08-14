---
title: 程式碼詳細資料
description: 本節會列出 ADSI 範例提供者元件的執行原始程式碼。 本檔中的所有原始程式碼參考都有可能變更，並可在 ADSI SDK 所包含的範例程式碼目錄中取得。
ms.assetid: 207912e5-ac17-48c7-9536-981a8e92e8cf
ms.tgt_platform: multiple
keywords:
- 程式碼詳細資料 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f03e7c7ed7d61d56f338a8bb44d51b1890d4bd24cd7dc1e6050f1900f6ff61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692284"
---
# <a name="code-details"></a>程式碼詳細資料

本節會列出 ADSI 範例提供者元件的執行原始程式碼。 本檔中的所有原始程式碼參考都有可能變更，並可在 ADSI SDK 所包含的範例程式碼目錄中取得。

> [!Note]  
> [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)方法 **GetEx** 和 **PutEx** 不會在 ADSI 範例提供者元件中執行。 也就是說，執行繼承自 **IADs** 的 Active Directory 物件的程式碼沒有 **GetEx** 和 **PutEx** 方法。 這包括支援 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)的架構類別物件、支援 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)的屬性物件、支援 **IADs** 的泛型 Active Directory 物件，以及任何支援 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)的容器物件。 此外，語法物件不會出現在範例提供者元件中。 不過，ADSI 架構需要將語法物件包含在架構容器物件中，就像架構類別和屬性物件一樣。

 

下表列出 Active Directory 服務介面 SDK 中提供者範例目錄中所包含的原始程式碼檔。



| 原始程式碼檔                 | 描述                                                                                                                                                       |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cclsobj .cpp](cclsobj-cpp.md)   | 架構類別物件常式。                                                                                                                                     |
| [cdispmgr .cpp](cdispmgr-cpp.md) | 分派管理員執行。                                                                                                                                  |
| [cenumns .cpp](cenumns-cpp.md)   | 命名空間列舉常式。                                                                                                                                   |
| [cenumsch .cpp](cenumsch-cpp.md) | 架構列舉常式。                                                                                                                                      |
| [cenumobj .cpp](cenumobj-cpp.md) | 泛型物件列舉常式。                                                                                                                              |
| [cenumvar .cpp](cenumvar-cpp.md) | XxxEnumVariant 衍生類別的基底實作為基底。                                                                                                           |
| [cgenobj .cpp](cgenobj-cpp.md)   | 泛型物件常式。                                                                                                                                          |
| [cnamcf .cpp](cnamcf-cpp.md)     | 命名空間 class factory 常式。                                                                                                                                 |
| [cnamesp .cpp](cnamesp-cpp.md)   | 命名空間物件常式。                                                                                                                                        |
| [一般 .cpp](common-cpp.md)     | 所有提供者物件的通用程式碼。                                                                                                                              |
| [core .cpp](core-cpp.md)         | 所有 Active Directory 物件所共用的 ' core ' 屬性的實作為。                                                                                     |
| [cprops .cpp](cprops-cpp.md)     | 屬性快取功能。                                                                                                                                          |
| [cprov .cpp](cprov-cpp.md)       | 最上層提供者物件常式。                                                                                                                               |
| [cprovcf .cpp](cprovcf-cpp.md)   | 最上層提供者物件類別 factory 常式。                                                                                                                 |
| [cprpobj .cpp](cprpobj-cpp.md)   | 屬性物件常式。                                                                                                                                         |
| [cschobj .cpp](cschobj-cpp.md)   | 架構物件常式。                                                                                                                                           |
| [getobj .cpp](getobj-cpp.md)     | GetObject 功能。                                                                                                                                                |
| [globals](globals-cpp.md)   | ADSI 範例提供者元件 globals。                                                                                                                          |
| [guid .cpp](guid-cpp.md)         | 範例提供者元件 Clsid 和 LIBIDs。                                                                                                                     |
| [libmain .cpp](libmain-cpp.md)   | adssmp.dll 的 Libmain。                                                                                                                                           |
| [memory .cpp](memory-cpp.md)     | 範例提供者元件記憶體管理常式。                                                                                                            |
| [pack .cpp](pack-cpp.md)         | 範例提供者元件套件/解除封裝變數中的資料。                                                                                                          |
| [剖析 .cpp](parse-cpp.md)       | 範例提供者元件命名空間的路徑剖析。                                                                                                            |
| [屬性 .cpp](property-cpp.md) | 依名稱取得和放置屬性。                                                                                                                                   |
| [物件 .cpp](object-cpp.md)     | 用於篩選的範例提供者元件物件類型清單程式碼。                                                                                                   |
| [regdsapi .cpp](regdsapi-cpp.md) | 範例提供者元件登錄目錄服務 Api。                                                                                                       |
| smpoper .cpp                      | 資料轉換常式。                                                                                                                                         |
| [stdfact .cpp](stdfact-cpp.md)   | 標準 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 實行。                                                                                                  |
| adssmp .inf                       | 範例目錄資料存放區登錄資料。 如需詳細資訊，請參閱 [安裝範例提供者元件](installing-the-example-provider-component.md)。 |



 

 

 