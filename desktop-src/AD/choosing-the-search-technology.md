---
title: 選擇搜尋技術
description: 本主題包含用來搜尋 Active Directory 的技術清單。
ms.assetid: c9e887e3-7de4-4461-bc32-03db71c3e272
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory 中的搜尋技術
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6edba5c87ed438bc0047e0381d7e366cd6cc865
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462920"
---
# <a name="choosing-the-search-technology"></a>選擇搜尋技術

下表所列的技術可以用來搜尋 Active Directory Domain Services。



| 技術                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1)<br/> | [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1)類別是由[DirectoryServices](/dotnet/api/system.directoryservices?view=dotnet-plat-ext-3.1)命名空間提供，以允許在 Active Directory Domain Services 內搜尋 .NET Framework。 如需詳細資訊，請參閱 [搜尋目錄](/previous-versions/ms180879(v=vs.90))。<br/>                                                                                                                                  |
| [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)<br/>                       | ADSI 提供 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 介面，以使用 LDAP 查詢 Active Directory 伺服器以及其他目錄服務（例如 NDS）。 **>idirectorysearch** 是傳回豐富型別資料的 COM 介面，例如整數、八進位字串、字串、安全描述項、UTC 時間、大整數或布林值。 如需如何使用 **>idirectorysearch** 的詳細資訊，請參閱 [使用 >idirectorysearch 介面來搜尋](/windows/desktop/ADSI/searching-with-idirectorysearch)。<br/> |
| OLE DB<br/>                                                              | OLE DB 是一組 COM 介面，可讓應用程式在不同的資料來源中統一存取儲存的資料，而不論位置或類型。 ADSI 也提供 ADSI 的 OLE DB 提供者，可讓應用程式使用 OLE DB 來存取 Active Directory Domain Services。 ADSI OLE DB 提供者會使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 介面來提交查詢，以 Active Directory Domain Services 並收集結果。<br/>                                     |
| ADO 和其他以 OLE DB 為基礎的資料存取技術<br/>                 | ADSI OLE DB 提供者可根據 OLE DB （例如 ADO），在 Active Directory Domain Services 內搜尋任何資料存取技術。<br/>                                                                                                                                                                                                                                                                                                                                                                |
| LDAP API<br/>                                                            | Windows 2000 網域控制站是與 LDAP 第3版相容的目錄伺服器。 LDAP API 是 C 樣式的函式程式庫。 應用程式可以使用 LDAP API 在 Active Directory Domain Services 內搜尋。<br/>                                                                                                                                                                                                                                                                              |



 

選擇技術時，請考慮下列事項：

-   針對 Microsoft Visual Basic 和 Visual Basic Scripting Edition (VBScript) ，建議使用 ADO。
-   針對 C/c + +，您可以選擇任何一種技術。
-   如果您的應用程式廣泛使用 ADSI，使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)可能比較簡單。 如果您使用 [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) 來管理 Active Directory Domain Services 中的物件，請使用 **>idirectorysearch** 來處理從搜尋中傳回的屬性更容易進行。 **>idirectorysearch** 使用與 **IDirectoryObject** 相同的 [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue)結構來表示屬性。 此外，幾乎所有的 ADSI COM 物件都會公開 **>idirectorysearch** 。 如果您有 ADSI COM 物件的指標，您可以呼叫 **QueryInterface** 來取得 **>idirectorysearch** 指標，您可以使用此指標從 ADSI COM 物件所代表的目錄物件開始執行搜尋。
-   如果您的應用程式已經使用 OLE DB、ADO 或 LDAP API，您可以繼續使用這些技術在 Active Directory Domain Services 內進行搜尋。
-   如果您的應用程式必須聯結 Active Directory 網域服務和 SQL Server 7 資料庫的資料，請使用 OLE DB。 藉由使用 OLE DB，您的應用程式可以執行從一或多個 Microsoft SQL Server 7 資料庫參考 Active Directory Domain Services 和資料表和資料列集的分散式查詢。

 

