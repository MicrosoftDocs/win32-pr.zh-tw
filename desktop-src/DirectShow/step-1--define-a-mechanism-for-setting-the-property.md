---
description: 在建立自訂 DirectShow 篩選準則的篩選屬性頁時，定義用來設定屬性的機制。
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: 步驟 1： 定義用來設定屬性的機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410071"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a>步驟 1： 定義用來設定屬性的機制

篩選準則必須支援屬性頁面與其通訊的方式，讓屬性頁可以設定和抓取篩選的屬性。 可能的機制包括下列各項：

-   公開自訂 COM 介面。
-   透過 **IDispatch** 支援 Automation 屬性。
-   公開 **IPropertyBag** 介面，並定義一組命名屬性。

這個範例會使用名為 ISaturation 的自訂 COM 介面。 這不是實際的 DirectShow 介面;它只會在此範例中定義。 首先，在標頭檔中宣告介面，以及 (IID) 的介面識別碼：


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



您也可以使用 IDL 定義介面，並使用 MIDL 編譯器來建立標頭檔。 接下來，在篩選中執行自訂介面。 此範例會使用 "Get" 和 "Set" 方法做為篩選的飽和度值。 請注意，這兩種方法都可保護 m \_ lSaturation 成員的重要區段。


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



當然，您自己的實作為詳細資料將與此處所示的範例不同。

下一 [步：步驟2。執行 ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CCritSec 類別**](ccritsec.md)
</dt> <dt>

[建立篩選屬性頁](creating-a-filter-property-page.md)
</dt> </dl>

 

 



