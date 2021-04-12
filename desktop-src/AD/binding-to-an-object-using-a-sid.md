---
title: 使用 SID 系結至物件
description: 在 Windows Server 2003 中，可以使用物件安全識別碼 (SID) 和 GUID 來系結至物件。 物件 SID 會儲存在 objectSID 屬性中。 系結至 SID 無法在 Windows 2000 上運作。
ms.assetid: 18b4613c-eb93-4204-96f2-0f91d7900587
ms.tgt_platform: multiple
keywords:
- 使用 SID AD 系結至物件
- Active Directory、使用、系結、使用 SID 系結至物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad4ecf2d6faa385ab8085730e4f1cb0689e403
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462932"
---
# <a name="binding-to-an-object-using-a-sid"></a><span data-ttu-id="62c71-107">使用 SID 系結至物件</span><span class="sxs-lookup"><span data-stu-id="62c71-107">Binding to an Object Using a SID</span></span>

<span data-ttu-id="62c71-108">在 Windows Server 2003 中，可以使用物件安全識別碼 (SID) 和 GUID 來系結至物件。</span><span class="sxs-lookup"><span data-stu-id="62c71-108">In Windows Server 2003, it is possible to bind to an object using the object Security Identifier (SID) as well as a GUID.</span></span> <span data-ttu-id="62c71-109">物件 SID 會儲存在 **objectSID** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="62c71-109">The object SID is stored in the **objectSID** attribute.</span></span> <span data-ttu-id="62c71-110">系結至 SID 無法在 Windows 2000 上運作。</span><span class="sxs-lookup"><span data-stu-id="62c71-110">Binding to an SID does not work on Windows 2000.</span></span>

<span data-ttu-id="62c71-111">Active Directory Domain Services 的 LDAP 提供者會提供方法，以使用物件 SID 系結至物件。</span><span class="sxs-lookup"><span data-stu-id="62c71-111">The LDAP provider for Active Directory Domain Services provides a method to bind to an object using the object SID.</span></span> <span data-ttu-id="62c71-112">系結字串格式為：</span><span class="sxs-lookup"><span data-stu-id="62c71-112">The binding string format is:</span></span>


```C++
LDAP://servername/<SID=XXXXX>
```



<span data-ttu-id="62c71-113">在此範例中，"servername" 是目錄伺服器的名稱，而 "XXXXX" 是 SID 之十六進位值的字串表示。</span><span class="sxs-lookup"><span data-stu-id="62c71-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the SID.</span></span> <span data-ttu-id="62c71-114">"Servername" 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="62c71-114">The "servername" is optional.</span></span> <span data-ttu-id="62c71-115">SID 字串是以表單指定，字串中的每個字元都是 SID 的每個位元組的十六進位標記法。</span><span class="sxs-lookup"><span data-stu-id="62c71-115">The SID string is specified in a form where each character in the string is the hexadecimal representation of each byte of the SID.</span></span> <span data-ttu-id="62c71-116">例如，如果陣列為：</span><span class="sxs-lookup"><span data-stu-id="62c71-116">For example, if the array is:</span></span>


```C++
0xAB 0x14 0xE2
```



<span data-ttu-id="62c71-117">SID 系結字串會是 " &lt; SID = AB14E2 &gt; "。</span><span class="sxs-lookup"><span data-stu-id="62c71-117">the SID binding string would be "&lt;SID=AB14E2&gt;".</span></span> <span data-ttu-id="62c71-118">[**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata)函式不能用來將 SID 陣列轉換成字串，因為它在每個位元組字元前面加上反斜線，這不是有效的系結字串格式。</span><span class="sxs-lookup"><span data-stu-id="62c71-118">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function should not be used to convert the SID array into a string because it precedes each byte character with a backslash, which is not a valid bind string format.</span></span>

<span data-ttu-id="62c71-119">SID 字串也可以採用 " &lt; SID = S-x-x-xx-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-xxx &gt; " 格式，其中 "S-X-x-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-xxx" 部分與 [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) 函數所傳回的字串相同。</span><span class="sxs-lookup"><span data-stu-id="62c71-119">The SID string can also take the form "&lt;SID=S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX&gt;", where the "S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX" portion is the same as the string returned by the [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) function.</span></span>

<span data-ttu-id="62c71-120">使用物件 SID 進行系結時，不支援某些 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 和 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="62c71-120">When binding using the object SID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="62c71-121">使用物件 SID 系結所取得的物件不支援下列 **IADs** 屬性：</span><span class="sxs-lookup"><span data-stu-id="62c71-121">The following **IADs** properties are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="62c71-122">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="62c71-122">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="62c71-123">**Name**</span><span class="sxs-lookup"><span data-stu-id="62c71-123">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="62c71-124">**父代**</span><span class="sxs-lookup"><span data-stu-id="62c71-124">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="62c71-125">使用物件 SID 系結所取得的物件不支援下列 **IADsContainer** 方法：</span><span class="sxs-lookup"><span data-stu-id="62c71-125">The following **IADsContainer** methods are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="62c71-126">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="62c71-126">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="62c71-127">**建立**</span><span class="sxs-lookup"><span data-stu-id="62c71-127">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="62c71-128">**刪除**</span><span class="sxs-lookup"><span data-stu-id="62c71-128">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="62c71-129">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="62c71-129">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="62c71-130">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="62c71-130">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="62c71-131">若要在使用物件 SID 系結至物件之後使用這些方法和屬性，請使用 [**IADs 取得**](/windows/desktop/api/iads/nf-iads-iads-get) 物件辨別名稱，然後使用辨別名稱再次系結至物件。</span><span class="sxs-lookup"><span data-stu-id="62c71-131">To use these methods and properties after binding to an object using the object SID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="62c71-132">下列程式碼範例示範如何將 **objectSid** 轉換為可系結字串。</span><span class="sxs-lookup"><span data-stu-id="62c71-132">The following code example shows how to convert an **objectSid** into a bindable string.</span></span>


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



 

 