---
title: 設定 ADSI 開發的 Visual Basic 6。0
description: 本主題討論如何在 Visual Studio 中設定 Visual Basic，以開發 ADSI 應用程式。
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- 設定 adsi 開發 adsi 的 Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ed2e0f4cd0b56ee0167deda2e998314bb313d1a98cd0c43a9f06b495a4324f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838678"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>設定 ADSI 開發的 Visual Basic 6。0

**設定 Visual Basic 的 Microsoft Visual Studio 2010 開發環境**

1.  啟動 Visual Studio 2010。
2.  建立新的 Visual Basic 專案。
3.  將參考新增至 **ACTIVE DS 型別程式庫**。
    > [!Note]  
    > 如果您不需要早期的 COM 物件系結，請略過此步驟。

     

    1.  選取 **Project \| 加入參考**]。
    2.  選取 [ **COM** ] 索引標籤。
    3.  選取 [ **ACTIVE DS 類型程式庫**]。

4.  開始使用 ADSI 進行程式設計。

開始之前，請先登入 Windows 網域。 您必須擁有修改 Active Directory 資料庫的許可權。 依預設，系統管理員具有此許可權。

**範例 Visual Basic 6.0 應用程式：修改使用者的 FullName 和描述**

1.  遵循先前的步驟，建立標準可執行檔 Visual Basic 專案。
2.  按兩下表單。 在 [表單載入] 中 \_ ，輸入下列各項。 您必須以網域中容器中現有使用者的 ADsPath 取代 "LDAP：//CN = jeffsmith，CN = users，DC = fabrikam，DC = com" 字串。 建立可針對此用途修改的測試使用者帳戶。
    ```VB
    '------------------------------------------------------------
    ' This code example is used to set the FullName and Description
    '------------------------------------------------------------
    Dim usr As IADsUser

    ' Bind to a user object.
    Set usr = GetObject("LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com")

    usr.FullName = "Jeff Smith"
    usr.Description = "A user for fabrikam.com" 
    usr.SetInfo ' Commit the changes to the directory
    ```

    

3.  按下 **<F5>** 以執行程式。
4.  若要確認變更，請使用 Active Directory 消費者和電腦管理工具。 如需使用 ADSI 和 Visual Basic 的詳細資訊，請參閱[使用 Visual Basic 存取 Active Directory](accessing-active-directory-using-visual-basic.md)。

 

 




