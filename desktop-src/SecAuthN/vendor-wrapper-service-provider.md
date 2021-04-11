---
description: 廠商包裝函式的目的是要封裝並使用智慧卡製造商 (提供的低層級 COM 介面) 用於特定智慧卡。 這些介面不是由 Microsoft 提供。
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: 廠商包裝函式服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112789"
---
# <a name="vendor-wrapper-service-provider"></a>廠商包裝函式服務提供者

廠商包裝函式的目的是要封裝並使用智慧卡製造商 (提供的低層級 COM 介面) 用於特定智慧卡。 這些介面不是由 Microsoft 提供。

![廠商包裝函式](images/scspart1.png)

如 *ICCs 和個人電腦系統之互通性規格* 的第6部分所述 (請參閱) 的規格 [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ，此包裝函式所公開的功能比四個不同服務提供者的功能更容易使用。 包裝函式的功能可以分成四個主要區域：

-   智慧卡驗證服務，例如取得挑戰和卡片驗證。
-   智慧卡檔案存取或檔案系統服務，例如開啟、關閉、讀取及寫入。
-   智慧卡管理，例如附加和卸離。
-   智慧卡驗證服務，例如驗證及變更程式碼。

> [!Note]  
> 某些語言和國家或地區可能無法使用此規格。

 

這項功能僅適用于使用的卡片類型 (該卡片支援的功能、通訊協定等) ，而且每張卡片都有不同的功能。

Microsoft SCardCOM 範例包裝函式會使用 ATL COM 程式庫來執行簡單的包裝函式，並為其他包裝函式配置範本。 它會執行下列介面。



| 介面或物件                                     | Description                         |
|---------------------------------------------------------|-------------------------------------|
| [**ISCardAuth**](iscardauth.md)<br/>             | 驗證服務。<br/> |
| [**ISCardFileAccess**](iscardfileaccess.md)<br/> | 檔案系統服務。<br/>    |
| [**ISCardManage**](iscardmanage.md)<br/>         | 管理服務。<br/>     |
| [**ISCardVerify**](iscardverify.md)<br/>         | 驗證服務。<br/>   |



 

> [!Note]  
> SCardCOM 範例僅提供作為執行包裝函式介面的範例。 若要避免與其他廠商產生 DLL 名稱衝突，您不能使用 SCardCOM.dll 做為您所建立之任何 Dll 的名稱。

 

以下是廠商包裝函式的典型用法。 這個範例會使用 [**ISCardManage**](iscardmanage.md) 介面來建立將包裝到服務提供者的介面實例，以及用來驗證其作業的 [**ISCardVerify**](iscardverify.md) 介面。

**若要建立包裝函式服務提供者**

1.  建立 [**ISCardManage**](iscardmanage.md) 介面的實例。 您可以使用此介面來建立必要介面 (實例，例如 [**ISCardFileAccess**](iscardfileaccess.md) 或 [**ISCardVerify**](iscardverify.md)) 。 建立這些介面時，也會建立任何對應的低層級 COM 介面。
2.  透過適當的 [**ISCardManage**](iscardmanage.md) 方法來連接或連接到卡片。
3.  透過適當的 [**ISCardVerify**](iscardverify.md) 方法執行所需的作業 (這可能會呼叫多個低層級的 COM 介面和方法，以完成) 。
4.  針對其他作業重複執行。
5.  完成時釋放。

COM 介面名稱和介面識別碼 (GUID) 不應該從程式碼或範例包裝函式中所使用的識別碼變更。 不過，類別 GUID (也就是，介面的實際實作為所在的) 必須從使用的位置進行變更。 這在執行廠商包裝函式時特別重要。 其中一個範例是在特定電腦上使用多個廠商包裝函式。 這些包裝函式應該會執行相同的 COM 介面，但一律會使用不同的執行策略。 因此，需要不同的類別 (和類別識別碼) 。

 

 




