---
title: 使用 ADsOpenObject 和 IADsOpenDSObject Objdso.opendsobject 系結
description: 當您必須指定替代認證以及需要資料加密時，ADsOpenObject 函式和 IADsOpenDSObject Objdso.opendsobject 方法會用來系結至目錄服務物件。
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- 使用 ADsOpenObject 和 IADsOpenDSObject Objdso.opendsobject ADSI
- ADSI ADSI、using、ADsOpenObject 和 IADsOpenDSObject Objdso.opendsobject 的系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41ffe1e9ad0b8a78d1a8c563de250851a894012938682c4cfd0d0fd713f99bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082772"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a>使用 ADsOpenObject 和 IADsOpenDSObject：： Objdso.opendsobject 系結

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)函式和 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)方法是在必須指定替代認證以及需要資料加密時，用來系結至目錄服務物件。

可能的話，應該使用呼叫執行緒的認證。 但是，如果必須使用替代認證，則必須使用 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 函數或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 方法。 如果使用替代認證，請務必不要快取密碼。 您可以指定第一個系結作業的使用者名稱和密碼，然後只在後續的系結中指定使用者名稱，來執行多個系結作業。 只要符合下列條件，系統就會在第一次呼叫時設定會話，並在後續的系結呼叫上使用相同的會話：

-   每個系結作業中都有相同的使用者名稱。
-   在每個系結作業中執行無伺服器系結或系結至相同的伺服器。
-   從其中一個系結作業中保存物件參考，以維護開啟的會話。 釋放最後一個物件參考時，就會關閉會話。

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)和 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)使用 Windows NT 的 [安全性支援提供者介面 (SSPI)](/windows/desktop/SecAuthN/sspi)以允許驗證選項的彈性。 使用這些介面的主要優點是為 Active Directory 用戶端提供不同類型的驗證，以及加密會話。 目前，ADSI 不允許傳入憑證。 因此，您可以使用 SSL 進行加密，然後使用 Kerberos、NTLM 或簡單驗證，視旗標在 *>dwreserved* 參數上的設定方式而定。

雖然您一律會取得最高的喜好設定通訊協定，但是您無法在 ADSI 中要求特定的 SSPI 提供者。 如果 Windows 用戶端系結至執行 Windows 的電腦，則此通訊協定為 Kerberos。 在網頁的案例中，不允許驗證憑證是可接受的，因為在執行網頁之前會先進行驗證。

雖然開啟作業可讓您指定使用者和密碼，但您不應該這麼做。 相反地，請不要指定任何認證，並隱含地使用呼叫端安全性內容的認證。 若要使用呼叫端的認證搭配 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)系結至目錄物件，請指定 **Null** 做為使用者名稱和密碼。

最後，若要系結無驗證，請使用 **ADS \_ 無 \_ 驗證** 旗標。 無驗證表示 ADSI 會嘗試系結為目標物件的匿名使用者，且不會執行任何驗證。 這相當於在 LDAP 中要求匿名系結，並指出所有使用者都包含在安全性內容中。

如果驗證旗標設定為零，ADSI 會執行簡單的系結，以純文字形式傳送。

> [!Caution]  
> 如果指定使用者名稱和密碼但未指定驗證旗標，則會透過網路以純文字傳輸使用者名稱和密碼，這會造成安全性風險。 請勿指定使用者名稱和密碼，而不指定驗證旗標。

 

## <a name="examples"></a>範例

下列 Visual Basic 程式碼範例顯示如何使用 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)方法。


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



下列 c + + 程式碼範例示範如何使用 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 函數。


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



[**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)介面也可以在 c + + 中使用，但它會複製 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)函數。

下列 c + + 程式碼範例示範如何使用 [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) 介面執行與上述程式碼範例中相同的系結作業。


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 