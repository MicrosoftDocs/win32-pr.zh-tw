---
title: 使用 SID 系結至物件
description: 在 Windows Server 2003 中，可以使用物件安全識別碼 (SID) 以及 GUID 來系結至物件。 物件 SID 會儲存在 objectSID 屬性中。 系結至 SID 無法在 Windows 2000 上運作。
ms.assetid: 18b4613c-eb93-4204-96f2-0f91d7900587
ms.tgt_platform: multiple
keywords:
- 使用 SID AD 系結至物件
- Active Directory、使用、系結、使用 SID 系結至物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11508d82ddc415e304503a7fee67296b8d2fc966262cf054437fe8a4bd5523a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118023760"
---
# <a name="binding-to-an-object-using-a-sid"></a>使用 SID 系結至物件

在 Windows Server 2003 中，可以使用物件安全識別碼 (SID) 以及 GUID 來系結至物件。 物件 SID 會儲存在 **objectSID** 屬性中。 系結至 SID 無法在 Windows 2000 上運作。

Active Directory Domain Services 的 LDAP 提供者會提供方法，以使用物件 SID 系結至物件。 系結字串格式為：


```C++
LDAP://servername/<SID=XXXXX>
```



在此範例中，"servername" 是目錄伺服器的名稱，而 "XXXXX" 是 SID 之十六進位值的字串表示。 "Servername" 是選擇性的。 SID 字串是以表單指定，字串中的每個字元都是 SID 的每個位元組的十六進位標記法。 例如，如果陣列為：


```C++
0xAB 0x14 0xE2
```



SID 系結字串會是 " &lt; SID = AB14E2 &gt; "。 [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata)函式不能用來將 SID 陣列轉換成字串，因為它在每個位元組字元前面加上反斜線，這不是有效的系結字串格式。

SID 字串也可以採用 " &lt; SID = S-x-x-xx-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-xxx &gt; " 格式，其中 "S-X-x-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-xxx" 部分與 [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) 函數所傳回的字串相同。

使用物件 SID 進行系結時，不支援某些 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 和 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 方法和屬性。 使用物件 SID 系結所取得的物件不支援下列 **IADs** 屬性：

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**名稱**](/windows/desktop/ADSI/iads-property-methods)
-   [**父代**](/windows/desktop/ADSI/iads-property-methods)

使用物件 SID 系結所取得的物件不支援下列 **IADsContainer** 方法：

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**建立**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**刪除**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

若要在使用物件 SID 系結至物件之後使用這些方法和屬性，請使用 [**IADs 取得**](/windows/desktop/api/iads/nf-iads-iads-get) 物件辨別名稱，然後使用辨別名稱再次系結至物件。

下列程式碼範例示範如何將 **objectSid** 轉換為可系結字串。


```C++
HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes);

/********

    GetSIDBindStringFromVariant()

    Converts a SID in VARIANT form, such as an objectSid value, and 
    converts it into a bindable string in the form:

    LDAP://<SID=xxxxxxx...>

    The returned string is allocated with AllocADsMem and must be 
    freed by the caller with FreeADsMem.

*********/

LPWSTR GetSIDBindStringFromVariant(VARIANT vSID)
{
    LPWSTR pwszReturn = NULL;

    if(VT_ARRAY & vSID.vt) 
    {
        HRESULT hr;
        LPBYTE pByte;
        DWORD dwBytes = 0;

        hr = VariantArrayToBytes(vSID, &pByte, &dwBytes);
        if(S_OK == hr)
        {
            // Convert the BYTE array into a string of hex 
            // characters.
            CComBSTR sbstrTemp = "LDAP://<SID=";

            for(DWORD i = 0; i < dwBytes; i++)
            {
                WCHAR wszByte[3];

                swprintf_s(wszByte, L"%02x", pByte[i]);
                sbstrTemp += wszByte;
            }

            sbstrTemp += ">";
            pwszReturn = 
               (LPWSTR)AllocADsMem((sbstrTemp.Length() + 1) * 
                sizeof(WCHAR));
            if(pwszReturn)
            {
                wcscpy_s(pwszReturn, sbstrTemp.m_str);
            }

            FreeADsMem(pByte);
        }
    }

    return pwszReturn;
}

/*********

    VariantArrayToBytes()

    This function converts a VARIANT array into an array of BYTES. 
    This function allocates the buffer using AllocADsMem. The 
    caller must free this memory with FreeADsMem when it is no 
    longer required.

**********/

HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes)
{
    if(!(Variant.vt & VT_ARRAY) ||
        !Variant.parray ||
        !ppBytes ||
        !pdwBytes)
    {
        return E_INVALIDARG;
    }

    *ppBytes = NULL;
    *pdwBytes = 0;

    HRESULT hr = E_FAIL;
    SAFEARRAY *pArrayVal = NULL;
    CHAR HUGEP *pArray = NULL;
    
    // Retrieve the safe array.
    pArrayVal = Variant.parray;
    DWORD dwBytes = pArrayVal->rgsabound[0].cElements;
    *ppBytes = (LPBYTE)AllocADsMem(dwBytes);
    if(NULL == *ppBytes) 
    {
        return E_OUTOFMEMORY;
    }

    hr = SafeArrayAccessData(pArrayVal, (void HUGEP * FAR *) &pArray);
    if(SUCCEEDED(hr))
    {
        // Copy the bytes to the safe array.
        CopyMemory(*ppBytes, pArray, dwBytes);
        SafeArrayUnaccessData( pArrayVal );
        *pdwBytes = dwBytes;
    }
    
    return hr;
}
```



 

 