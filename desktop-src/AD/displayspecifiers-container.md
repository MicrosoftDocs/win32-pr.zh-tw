---
title: DisplaySpecifiers 容器
description: 顯示規範會依地區設定儲存在設定容器的 DisplaySpecifiers 容器中。 由於設定容器會複寫到整個樹系中，因此顯示規範會傳播到樹系中的所有網域。
ms.assetid: d7647c50-f95c-41ef-8d67-dc72542cae5a
ms.tgt_platform: multiple
keywords:
- DisplaySpecifiers 容器
- 容器，顯示規範
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406258a6c9983581491420a49621e3d10df4601e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462880"
---
# <a name="displayspecifiers-container"></a>DisplaySpecifiers 容器

顯示規範會依地區設定儲存在設定容器的 DisplaySpecifiers 容器中。 由於設定容器會複寫到整個樹系中，因此顯示規範會傳播到樹系中的所有網域。

設定容器會儲存 DisplaySpecifiers 容器，然後儲存對應于每個地區設定的容器。 這些地區設定容器的命名方式是使用地區設定識別碼的十六進位標記法。 例如，美國/英文地區設定容器的名稱是409，德文地區設定的容器名為407，而日文地區設定的容器名為411。 如需詳細資訊和可能的語言識別項清單，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。

每個地區設定容器都會儲存 [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) 類別的物件。

若要列出地區設定的所有顯示指定名稱，請列舉 DisplaySpecifiers 容器內指定之地區設定容器中的所有 [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) 物件。

下列程式碼範例包含一個函式，該函式會系結至指定地區設定的顯示規範容器：


```C++
/**********
This function returns a pointer to the display specifier container 
for the specified locale.

If locale is NULL, use default system locale and then return the 
locale in the locale parameter.
***********/
HRESULT BindToDisplaySpecifiersContainerByLocale(
    LCID *locale,
    IADs **ppDispSpecCont)
{
HRESULT hr = E_FAIL;
 
if ((!ppDispSpecCont)||(!locale))
    return E_POINTER;
 
// If no locale is specified, use the default system locale.
if (!(*locale))
{
    *locale = GetSystemDefaultLCID();
    if (!(*locale))
        return E_FAIL;
}
 
// Be sure that the locale is valid.
if (!IsValidLocale(*locale, LCID_SUPPORTED))
    return E_INVALIDARG;
 
LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
IADs *pObj = NULL;
VARIANT var;
 
hr = ADsOpenObject(L"LDAP://rootDSE",
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)&pObj);
 
if (SUCCEEDED(hr))
{
    // Get the DN to the configuration container.
    hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
    if (SUCCEEDED(hr))
    {
        // Build the string to bind to the container for the
        // specified locale in the DisplaySpecifiers container.
        swprintf_s(
            szPath, 
            L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", 
            *locale, 
            var.bstrVal);

        // Bind to the container.
        *ppDispSpecCont = NULL;
        hr = ADsOpenObject(szPath,
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)ppDispSpecCont);
 
        if(FAILED(hr))
        {
            if ((*ppDispSpecCont))
            {
                (*ppDispSpecCont)->Release();
                (*ppDispSpecCont) = NULL;
            }
        }
    }
}
 
// Cleanup.
VariantClear(&var);
if (pObj)
    pObj->Release();
 
return hr;
}
```



 

 