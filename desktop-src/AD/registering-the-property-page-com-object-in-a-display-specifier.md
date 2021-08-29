---
title: 在顯示規範中註冊屬性頁 COM 物件
description: 本主題說明如何使用 Windows 登錄和 Active Directory 註冊包含 Active Directory 屬性工作表的擴充 DLL。
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- 在顯示規範中註冊屬性頁 COM 物件 Active Directory
- 屬性頁 COM 物件 Active Directory，在顯示規範中註冊
- 顯示指定名稱 Active Directory，在中註冊屬性頁 COM 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6685e406cb1bfdc16f73dd2fddd94a195fe74a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881237"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a>在顯示規範中註冊屬性頁 COM 物件

當您使用 COM 建立 Active Directory Domain Services 的內容工作表延伸 DLL 時，您也必須向 Windows 登錄和 Active Directory Domain Services 註冊擴充功能。 註冊擴充功能可讓 Active Directory 的系統管理 MMC 嵌入式管理單元和 Windows shell 辨識延伸模組。

## <a name="registering-in-the-windows-registry"></a>在 Windows 登錄中註冊

和所有 COM 伺服器一樣，必須在 Windows 登錄中註冊屬性工作表延伸模組。 此擴充功能會在下列機碼下註冊。

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*&lt; Clsid &gt;* 是 [**STRINGFROMCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)函數所產生之 clsid 的字串表示。 在 *&lt; &gt; clsid* 機碼下，有一個 **InProcServer32** 機碼會將物件識別為32位的內部進程伺服器。 在 **InProcServer32** 索引鍵下，DLL 的位置會指定為預設值，而執行緒模型則是在 **>threadingmodel** 值中指定。 所有屬性工作表延伸模組都必須使用「單元」執行緒模型。

## <a name="registering-with-active-directory-domain-services"></a>向 Active Directory Domain Services 註冊

屬性工作表延伸註冊是一種地區設定特有的。 如果屬性工作表延伸適用于所有地區設定，則必須在 [顯示規範] 容器中所有地區設定子容器的物件類別 [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) 物件中註冊。 如果屬性工作表延伸針對特定地區設定進行當地語系化，請在該地區設定 subcontainer 的 **displaySpecifier** 物件中註冊它。 如需顯示規範容器和地區設定的詳細資訊，請參閱 [顯示](display-specifiers.md) 規範和 [DisplaySpecifiers 容器](displayspecifiers-container.md)。

有三個顯示指定名稱屬性可以在其中註冊屬性工作表延伸模組。 這些都是 [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages)、 [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)和 [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages)。

[**AdminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages)屬性會識別要在 Active Directory 系統管理嵌入式管理單元中顯示的系統管理屬性頁。當使用者在其中一個 Active Directory 系統管理 MMC 嵌入式管理單元中，流覽適當類別之物件的屬性時，就會出現屬性頁。

[**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)屬性會識別要在 Windows shell 中顯示的終端使用者屬性頁。 當使用者在 Windows 檔案總管中流覽適當類別的物件屬性時，就會出現屬性頁。 從 Windows Server 2003 作業系統開始，Windows shell 不會再顯示 Active Directory Domain Services 中的物件。

[**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages)僅適用于 Windows Server 2003 作業系統。 當使用者在其中一個 Active Directory 系統管理 MMC 嵌入式管理單元中，針對適當類別的一個以上物件來查看屬性時，就會出現屬性頁。

所有這些屬性都是多重值。

[**AdminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages)和 [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)屬性的值需要下列格式。


```C++
<order number>,<clsid>,<optional data>
```



[**AdminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages)屬性的值需要下列格式。


```C++
<order number>,<clsid>
```



「 &lt; 訂單編號」 &gt; 是一種不帶正負號的數位，表示工作表中的頁面位置。 顯示內容表時，系統會使用每個值的「訂單編號」比較來排序這些值 &lt; &gt; 。 如果有一個以上的值具有相同的「 &lt; 訂單編號」 &gt; ，則這些屬性頁 COM 物件會以從 Active Directory 伺服器讀取的順序載入。 可能的話，您應該使用非現有的「 &lt; 訂單編號」 &gt; ; 也就是，屬性中的其他值不會使用一個。 沒有指定的開始位置，而且「訂單編號」序列中允許有間距 &lt; &gt; 。

" &lt; Clsid &gt; " 是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函式所產生之 clsid 的字串表示。

「 &lt; 選擇性資料」 &gt; 是不需要的字串值。 您可以使用傳遞至 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)方法的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)指標，由屬性頁 COM 物件來抓取此值。 屬性頁 COM 物件會藉由呼叫 [**IDataObject：：**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) [**CFSTR \_ DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) 剪貼簿格式來取得此資料。 這會提供包含 [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo)結構的 **HGLOBAL** 。 **DSPROPERTYPAGEINFO** 結構包含包含「選擇性資料」的 Unicode 字串 &lt; &gt; 。 &lt; &gt; [**AdminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages)屬性不能有「選擇性資料」。 下列 C/c + + 程式碼範例顯示如何取出「 &lt; 選擇性資料」 &gt; 。


```C++
fe.cfFormat = RegisterClipboardFormat(CFSTR_DSPROPERTYPAGEINFO);
fe.ptd = NULL;
fe.dwAspect = DVASPECT_CONTENT;
fe.lindex = -1;
fe.tymed = TYMED_HGLOBAL;
hr = pDataObj->GetData(&fe, &stm);
if(SUCCEEDED(hr))
{
    DSPROPERTYPAGEINFO *pPageInfo;
    
    pPageInfo = (DSPROPERTYPAGEINFO*)GlobalLock(stm.hGlobal);
    if(pPageInfo)
    {
        LPWSTR  pwszData;

        pwszData = (LPWSTR)((LPBYTE)pPageInfo + pPageInfo->offsetString);
        pwszData = NULL;
        
        GlobalUnlock(stm.hGlobal);
    }

    ReleaseStgMedium(&stm);
}
```



屬性工作表延伸可以執行多個屬性頁;「選擇性資料」的其中一個可能用途 &lt; &gt; 是為要顯示的頁面命名。 這可讓您彈性地選擇要執行多個 COM 物件（每個頁面各一個），或使用單一 COM 物件來處理多個頁面。

下列程式碼範例是可用於 [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages)、 [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)或 [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) 屬性的範例值。


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> 針對 Windows shell，會在使用者登入時抓取顯示規範資料，並為使用者會話快取。 針對系統管理嵌入式管理單元，當載入嵌入式管理單元時，會抓取顯示規範資料，並且在進程的存留期間快取。 針對 Windows shell，這表示在使用者登出之後，顯示規範的變更會生效，然後再次登入。 若為系統管理嵌入式管理單元，則在載入嵌入式管理單元或主控台檔案時，變更將會生效。

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a>將值加入至屬性工作表擴充屬性

下列程式描述如何在其中一個屬性工作表延伸屬性下註冊屬性工作表延伸模組。

**在其中一個屬性工作表延伸屬性下註冊屬性工作表延伸模組**

1.  請確定屬性值中還沒有延伸模組存在。
2.  在屬性頁順序清單的結尾處加入新值。 這會將 &lt; 屬性值的 "order number &gt; " 部分設定為最高現有訂單編號之後的下一個值。
3.  [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex)方法是用來將新的值加入至屬性。 *LnControlCode* 參數必須設定為 **ADS \_ 屬性 \_ 附加**，以便將新值附加至現有的值，因此不會覆寫現有的值。 您必須在之後呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 方法，才能認可目錄的變更。

請注意，您可以為一個以上的物件類別註冊相同的屬性工作表延伸模組。

[**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex)方法是用來將新的值加入至屬性。 *LnControlCode* 參數必須設定為 **ADS \_ 屬性 \_ 附加**，如此一來，新的值就會附加至現有的值，因此不會覆寫現有的值。 必須先呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 方法，才能認可目錄的變更。

下列程式碼範例會在電腦的預設地區設定中，將屬性工作表延伸加入至群組類別。 請注意， **AddPropertyPageToDisplaySpecifier** 函式會驗證現有值中的屬性工作表延伸 CLSID，取得最高的順序數位，並使用 [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) 搭配 **ADS \_ 屬性 \_ 附加** 控制項程式碼來新增屬性頁面的值。


```C++
//  Add msvcrt.dll to the project.
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include "atlbase.h"

HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of the class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         );

HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                 );

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject);

//  Entry point for the application.
void wmain(int argc, wchar_t *argv[ ])
{

    wprintf(L"This program adds a sample property page to the display specifier for group class in the local computer's default locale.\n");

    // Initialize COM.
    CoInitialize(NULL);
    HRESULT hr = S_OK;

    //  Class ID for the sample property page.
    LPOLESTR szCLSID = L"{D9FCE809-8A10-11d2-A7E7-00C04F79DC0F}";
    LPOLESTR szClass = L"group";
    CLSID clsid;
    //  Convert to GUID.
    hr = CLSIDFromString(
        szCLSID,  //  Pointer to the string representation of the CLSID.
        &clsid    //  Pointer to the CLSID.
        );

    hr = AddPropertyPageToDisplaySpecifier(szClass, //  ldapDisplayName of the class.
                                           &clsid //  CLSID of property page COM object.
                                          );
    if (S_OK == hr)
        wprintf(L"Property page registered successfully\n");
    else if (S_FALSE == hr)
        wprintf(L"Property page was not added because it was already registered.\n");
    else
        wprintf(L"Property page was not added. HR: %x.\n");

    //  Uninitialize COM.
    CoUninitialize();
    return;
}

//  Adds a property page to Active Directory admin snap-ins.
HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         )
{
    HRESULT hr = E_FAIL;
    IADsContainer *pContainer = NULL;
    LPOLESTR szDispSpec = new OLECHAR[MAX_PATH];
    IADs *pObject = NULL;
    VARIANT var;
    CComBSTR sbstrProperty = L"adminPropertyPages";
    LCID locale = NULL;
    //  Get the display specifier container using default system locale.
    //  When adding a property page COM object, specify the locale
    //  because the registration is locale-specific.
    //  This means if you created a property page
    //  for German, explicitly add it to the 407 container,
    //  so that it will be used when a computer is running with locale
    //  set to German and not the locale set on the
    //  computer where this application is running.
    hr = BindToDisplaySpecifiersContainerByLocale(&locale,
                                                  &pContainer
                                                 );
    //  Handle fail case where dispspec object
    //  is not found and give option to create one.

    if (SUCCEEDED(hr))
    {
        //  Bind to display specifier object for the specified class.
        //  Build the display specifier name.
#ifdef _MBCS
        wcscpy_s(szDispSpec, szClassName);
        wcscat_s(szDispSpec, L"-Display");
        hr = GetDisplaySpecifier(pContainer, szDispSpec, &pObject);
#endif _MBCS#endif _MBCS
        if (SUCCEEDED(hr))
        {
            //  Convert GUID to string.
            LPOLESTR szDSGUID = new WCHAR [39];
            ::StringFromGUID2(*pPropPageCLSID, szDSGUID, 39); 

            //  Get the adminPropertyPages property.
            hr = pObject->GetEx(sbstrProperty, &var);
            if (SUCCEEDED(hr))
            {
                LONG lstart, lend;
                SAFEARRAY *sa = V_ARRAY(&var);
                VARIANT varItem;
                //  Get the lower and upper bound.
                hr = SafeArrayGetLBound(sa, 1, &lstart);
                if (SUCCEEDED(hr))
                {
                    hr = SafeArrayGetUBound(sa, 1, &lend);
                }
                if (SUCCEEDED(hr))
                {
                    //  Iterate the values to verify if the prop page CLSID
                    //  is already registered.
                    VariantInit(&varItem);
                    BOOL bExists = FALSE;
                    UINT uiLastItem = 0;
                    UINT uiTemp = 0;
                    INT iOffset = 0;
                    LPOLESTR szMainStr = new OLECHAR[MAX_PATH];
                    LPOLESTR szItem = new OLECHAR[MAX_PATH];
                    LPOLESTR szStr = NULL;
                    for (long idx=lstart; idx <= lend; idx++)
                    {
                        hr = SafeArrayGetElement(sa, &idx, &varItem);
                        if (SUCCEEDED(hr))
                        {
#ifdef _MBCS
                            //  Verify that the specified CLSID is already registered.
                            wcscpy_s(szMainStr,varItem.bstrVal);
                            if (wcsstr(szMainStr,szDSGUID))
                                bExists = TRUE;
                            //  Get the index which is the number before the first comma.
                            szStr = wcschr(szMainStr, ',');
                            iOffset = (int)(szStr - szMainStr);
                            wcsncpy_s(szItem, szMainStr, iOffset);
                            szItem[iOffset]=0L;
                            uiTemp = _wtoi(szItem);
                            if (uiTemp > uiLastItem)
                                uiLastItem = uiTemp;
                            VariantClear(&varItem);
#endif _MBCS
                        }
                    }
                    //  If the CLSID is not registered, add it.
                    if (!bExists)
                    {
                        //  Build the value to add.
                        LPOLESTR szValue = new OLECHAR[MAX_PATH];
                        //  Next index to add at end of list.
#ifdef _MBCS
                        uiLastItem++;
                        _itow_s(uiLastItem, szValue, 10);   
                        wcscat_s(szValue,L",");
                        //  Add the class ID for the property page.
                        wcscat_s(szValue,szDSGUID);
                        wprintf(L"Value to add: %s\n", szValue);
#endif _MBCS

                        VARIANT varAdd;
                        //  Only one value to add
                        LPOLESTR pszAddStr[1];
                        pszAddStr[0]=szValue;
                        ADsBuildVarArrayStr(pszAddStr, 1, &varAdd);

                        hr = pObject->PutEx(ADS_PROPERTY_APPEND, sbstrProperty, varAdd);
                        if (SUCCEEDED(hr))
                        {
                            //  Commit the change.
                            hr = pObject->SetInfo();
                        }
                    }
                    else
                        hr = S_FALSE;
                }
            }
            VariantClear(&var);
        }
        if (pObject)
            pObject->Release();
    }

    return hr;
}

//  This function returns a pointer to the display specifier container 
//  for the specified locale.
//  If locale is NULL, use the default system locale and then return the locale in the locale param.
HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                )
{
    HRESULT hr = E_FAIL;

    if ((!ppDispSpecCont)||(!locale))
        return E_POINTER;

    //  If no locale is specified, use the default system locale.
    if (!(*locale))
    {
        *locale = GetSystemDefaultLCID();
        if (!(*locale))
            return E_FAIL;
    }

    //  Verify that it is a valid locale.
    if (!IsValidLocale(*locale, LCID_SUPPORTED))
        return E_INVALIDARG;

    LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
    IADs *pObj = NULL;
    VARIANT var;

    hr = ADsOpenObject(L"LDAP://rootDSE",
                       NULL,
                       NULL,
                       ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                       IID_IADs,
                       (void**)&pObj);

    if (SUCCEEDED(hr))
    {
        //  Get the DN to the config container.
        hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
        if (SUCCEEDED(hr))
        {
#ifdef _MBCS
            //  Build the string to bind to the DisplaySpecifiers container.
            swprintf_s(szPath,L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", *locale, var.bstrVal);
            //  Bind to the DisplaySpecifiers container.
            *ppDispSpecCont = NULL;
            hr = ADsOpenObject(szPath,
                               NULL,
                               NULL,
                               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                               IID_IADsContainer,
                               (void**)ppDispSpecCont);
#endif _MBCS

            if(FAILED(hr))
            {
                if (*ppDispSpecCont)
                {
                    (*ppDispSpecCont)->Release();
                    (*ppDispSpecCont) = NULL;
                }
            }
        }
    }
    //   Cleanup.
    VariantClear(&var);
    if (pObj)
        pObj->Release();

    return hr;
}

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject)
{
    HRESULT hr = E_FAIL;
    CComBSTR sbstrDSPath;
    IDispatch *pDisp = NULL;

    if (!pContainer)
    {
        hr = E_POINTER;
        return hr;
    }

    //  Verify other pointers.
    //  Initialize the output pointer.
    (*ppObject) = NULL;

    //  Build relative path to the display specifier object.
    sbstrDSPath = "CN=";
    sbstrDSPath += szDispSpec;

    //  Use child object binding with IADsContainer::GetObject.
    hr = pContainer->GetObject(CComBSTR("displaySpecifier"),
        sbstrDSPath,
        &pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(IID_IADs, (void**)ppObject);
        if (FAILED(hr))
        {
            //  Clean up.
            if (*ppObject)
                (*ppObject)->Release();
        }
    }

    if (pDisp)
        pDisp->Release();

    return hr;

}
```



 

 
