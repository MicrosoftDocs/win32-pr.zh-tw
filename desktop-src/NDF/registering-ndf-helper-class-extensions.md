---
title: 註冊 NDF Helper 類別延伸模組
description: 每個 helper 類別延伸都有許多與其相關聯的登錄機碼。 COM 需要一些金鑰，而 NDF 需要一些金鑰。
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6457e144abdeb1dbed1e33bb10e21302f918da8cdc5a6fd2090f3665e83f0316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798495"
---
# <a name="registering-ndf-helper-class-extensions"></a>註冊 NDF Helper 類別延伸模組

每個 helper 類別延伸都有許多與其相關聯的登錄機碼。 COM 需要一些金鑰，而 NDF 需要一些金鑰。

## <a name="com-registry-keys"></a>COM 登錄機碼

Helper 類別延伸模組必須實作為 COM 伺服器。 必須針對每個 helper 類別延伸模組完成 COM 註冊。 物件的 CLSID、 [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) 介面和 [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) 介面必須註冊。 註冊會為 NDF 協助程式類別延伸建立許多與 COM 相關的登錄機碼。

## <a name="ndf-registry-keys"></a>NDF 登錄機碼

協助程式類別延伸必須先註冊，才能與網路診斷架構和其他相關的 helper 類別互動。 這可透過擴展登錄來完成。

下列程式示範如何將 helper 類別延伸新增至登錄。

1.  藉由在底下建立 DLL 的索引鍵，以發佈由 DLL 和其相依性所執行之 helper 類別的名稱

    **HKLM \\System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper class DLL* \\ **HelperClasses** \\ *helper class Name*

    以使用者定義的值取代 *VendorName*、 *helper 類別 DLL* 和 *Helper 類別名稱* ，如下所述。

    | 值               | 類型    | 意義                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | *VendorName*        | REG \_ SZ | 廠商的名稱。                                                      |
    | *Helper 類別 DLL*  | REG \_ SZ | DLL 的名稱，不含副檔名。                                          |
    | *Helper 類別名稱* | REG \_ SZ | 目前 helper 類別相依的 helper 類別名稱。 |

    

     

2.  在每個協助程式 *類別名稱* 索引鍵下，發佈下列資訊。

    

    | 值         | 類型       | 意義                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **CLSID**     | REG \_ SZ    | 包含 helper 類別之 COM 類別識別碼的字串。                                                                                                            |
    | **版本**   | REG \_ SZ    | 字串，其中包含格式的 helper 類別的主要和次要版本 <major> <minor> 。                                                        |
    | **已發行** | REG \_ DWORD | 值為1表示應該直接從診斷用戶端叫用此 helper 類別。 0表示只能從另一個 helper 類別呼叫它。 |
    | **父系**    | REG \_ SZ    | 字串，這個字串會為擴充的 Microsoft 可延伸 helper 類別命名。                                                                                       |

    

     

3.  針對每個協助程式類別，在底下建立索引鍵以發佈相符屬性的清單

    **HKLM \\System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper class DLL* \\ **HelperClasses** \\ *Helper class Name* \\ **MatchAttributes**

    這些索引鍵必須包含一或多個值 (下列類型的每個屬性) 一個以上。

    | 值             | 類型                             | 意義                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | **AttributeName** | REG \_ SZ \| REG \_ DWORD \| REG \_ 二進位檔 | 值，這個值會完成特定屬性的名稱和值組。 |

    

     

 

 




