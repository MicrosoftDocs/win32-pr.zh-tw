---
title: 設定 ADSI 開發的 Visual C++ 6。0
description: 本主題說明如何在 Visual Studio 中設定 c + +，讓您可以開發 ADSI 應用程式。
ms.assetid: 6f1ab3eb-2e0b-4f3e-b93c-e24c8b3b1a27
ms.tgt_platform: multiple
keywords:
- 設定 ADSI 開發的 c + +
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7401977ea1980acb0f62e24d93c3aadf480cda8ef47a8e8d6e5c88ccbcb0fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082282"
---
# <a name="setting-up-visual-c-60-for-adsi-development"></a>設定 ADSI 開發的 Visual C++ 6。0

Microsoft Visual C++ 6.0 開發系統可以用來開發企業應用程式。 若要設定您的 Visual C++ 6.0 環境以開發 ADSI 應用程式，請執行下列步驟：

**設定 Microsoft Visual C++ 6.0 開發環境**

1.  指向 [包含] 和 [程式庫] 目錄。 選取 [ **工具 \| 選項**]。 按一下 [ **目錄** ] 索引標籤，並指定 ADSI 標頭檔的路徑。
2.  在您的專案中包含 Activeds .h 檔案。
3.  將 Activeds .lib 和 Adsiid .lib 檔案新增至專案的連結器輸入。
4.  開始使用 ADSI 進行程式設計。

登入 Windows 網域。 您也必須具有在 Active Directory 中修改資料的許可權。 依預設，系統管理員具有此許可權。 若要輸入此程式碼範例：

**範例 Visual C++ 應用程式：在網域中建立使用者**

1.  啟動 Visual C++ 6.0。
2.  建立獨立可執行檔專案。 它可以是 MFC、ATL 或主控台應用程式。
3.  遵循先前的步驟來設定您的專案。
4.  輸入下列程式碼範例。 以網域中容器的 ADsPath 取代 "LDAP：//CN = users，DC = fabrikam，DC = com" 字串。 您也應該使用網域中唯一的使用者名稱來取代使用者名稱 "jeffsmith"。

    ```C++
    #include "stdafx.h"
    #include "activeds.h"

    int main(int argc, char* argv[])
    {
        HRESULT hr;
        IADsContainer *pCont;
        IDispatch *pDisp=NULL;
        IADs *pUser;

         // Initialize COM before calling any ADSI functions or interfaces.
         CoInitialize(NULL);

        hr = ADsGetObject( L"LDAP://CN=users,DC=fabrikam,DC=com", 
                                   IID_IADsContainer, 
                                   (void**) &pCont );
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        //-----------------
        // Create a user
        //-----------------
        
        hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=jeffsmith"), &pDisp );
        
        // Release the container object.    
        pCont->Release();
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        hr = pDisp->QueryInterface( IID_IADs, (void**) &pUser );

        // Release the dispatch interface.
        pDisp->Release();

        if ( !SUCCEEDED(hr) )
        {    
            return 0;
        }

        // Commit the object data to the directory.
        pUser->SetInfo();

        // Release the object.
        pUser->Release();

        CoUninitialize();
    }
    ```

    

5.  建置並執行應用程式。 若要確認是否已建立使用者，請使用 Active Directory 消費者和電腦管理工具。

 

 




