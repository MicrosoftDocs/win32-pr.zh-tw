---
title: 早期繫結支援
description: 下列程式碼範例會提供具有早期系結支援的案例。
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- 擴充功能 ADSI，早期繫結支援
- binding AD，早期繫結支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093299"
---
# <a name="early-binding-support"></a>早期繫結支援

下列程式碼範例會提供具有早期系結支援的案例。


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



在此程式碼範例中，兩個擴充元件會擴充 **使用者** 物件。 每個擴充功能都會發行自己的介面。 每個擴充功能都無法辨識其他擴充介面;只有 ADSI 能夠辨識這兩個擴充功能的存在。 每個擴充功能都會將其 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 委派給 ADSI。 ADSI 可做為這兩種擴充功能的匯總工具，以及任何其他未來的延伸模組。 從任何延伸模組或 ADSI 查詢介面，會產生相同的一致結果。

下列程式描述如何建立擴充功能。

## <a name="step-1-add-aggregation-to-your-component"></a>步驟1：將匯總加入至您的元件

遵循 COM 規格，將匯總加入至您的元件。 總而言之，您必須在 **CreateInstance** 期間接受對元件的 *pUnknown* 要求，並在元件已匯總時，將 *pUnknown* 委派給匯總工具的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 。

## <a name="step-2-register-your-extension"></a>步驟2：註冊您的延伸模組

現在您必須決定要擴充的目錄類別。 您無法使用相同的介面來完成這項工作，以便用於 ADSI 介面，例如 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)、 [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)。 目錄物件會保存在目錄中，而您的延伸模組和 ADSI 正在用戶端電腦上執行。 目錄物件範例包括 **使用者**、 **電腦**、 **列印** 路徑、 **serviceConnectionPoint** 和 **nTDSService**。 您可以在 Active Directory 中加入新的類別，也可以為這個新類別建立新的擴充功能。

您可以使用登錄機碼，將目錄類別名稱與 ADSI 擴充元件產生關聯。 下圖表示現有的登錄配置，以及新的金鑰。

-   新的索引鍵（稱為 **延伸** 模組）包含索引鍵清單，其中每個索引鍵都代表目錄中的類別。 每個類別（例如， **使用者**、 **列印佇列** 或 **電腦**）都會維護子機碼清單。
-   每個子機碼都包含 ADSI 擴充元件的 CLSID。
-   每個 CLSID 子機碼都包含一個允許多個值的字串專案。 您應該只列出參與匯總的介面。

> [!Note]  
> 仍然需要擴充物件來註冊標準 COM 金鑰。

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a>範例

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

來自 Extension1 的介面清單可能與延伸模組2的介面不同。 使用中時，物件支援匯總工具 (ADSI) 的介面，以及匯總的 Extension1 和延伸模組2所提供的所有介面。 解析衝突的介面 (匯總工具和匯總或多個匯總所支援的相同介面，) 由擴充功能的優先順序決定。

您也可以將您的 CLSID 延伸模組與多個物件類別名稱產生關聯。 例如，您的延伸模組可以擴充 **使用者** 和 **連絡人** 物件。

> [!Note]  
> 擴充行為會加入至每個物件的類別，而不是針對每個物件的實例。

 

最佳做法是使用 **DllRegisterSvr** 函式的呼叫來註冊您的延伸模組，就像任何其他 COM 元件一樣。 也提供使用 **DllUnregisterServer** 函式取消註冊擴充功能的功能。

下列程式碼範例示範如何註冊擴充功能。


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 