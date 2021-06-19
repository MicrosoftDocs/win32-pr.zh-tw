---
description: 在建立自訂 DirectShow 篩選器的篩選屬性頁的過程中，于篩選器中執行 ISpecifyPropertyPages 介面。
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: 步驟 2： 執行 ISpecifyPropertyPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe37a22c6ba9c14f8656ac41294360569316be1a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410051"
---
# <a name="step-2-implement-ispecifypropertypages"></a>步驟 2： 執行 ISpecifyPropertyPages

接下來，在篩選中執行 **ISpecifyPropertyPages** 介面。 這個介面具有單一方法 **GetPages**，它會針對篩選準則所支援的屬性頁傳回 clsid 的陣列。 在此範例中，篩選準則具有單一屬性頁。 從產生 CLSID 並在標頭檔中宣告它來開始：


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



現在，請執行 **GetPages** 方法：


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



使用 **CoTaskMemAlloc** 配置陣列的記憶體。 呼叫端會釋放記憶體。

下一 [步：步驟3。支援 QueryInterface](step-3--support-queryinterface.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立篩選屬性頁](creating-a-filter-property-page.md)
</dt> </dl>

 

 



