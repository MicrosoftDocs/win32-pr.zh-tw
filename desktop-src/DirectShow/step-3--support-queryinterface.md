---
description: 步驟 3：
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: 步驟 3： 支援 QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e3d44b67971e165b8586aa3a02cc65ab3ab05f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971574"
---
# <a name="step-3-support-queryinterface"></a>步驟 3： 支援 QueryInterface

若要向用戶端公開篩選的新介面，請執行下列動作：

-   在篩選準則的公用宣告區段中包含 [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) 宏：
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   覆寫 [**CUnknown：： NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) ，以檢查兩個介面的 iid：
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

下一 [步：步驟4。建立屬性頁](step-4--create-the-property-page.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立篩選屬性頁](creating-a-filter-property-page.md)
</dt> <dt>

[如何執行 IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



