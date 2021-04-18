---
description: 步驟 10：
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: 步驟 10： 支援 COM 註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fead7e3448d8f02fd477141699e1107ca288afd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971477"
---
# <a name="step-10-support-com-registration"></a>步驟 10： 支援 COM 註冊

最後一項工作是支援 COM 註冊，讓屬性框架可以建立您屬性頁的新實例。 將另一個 [**CFactoryTemplate**](cfactorytemplate.md) 專案加入至全域 *g \_ 範本* 陣列，用來註冊 DLL 中的所有 COM 物件。 請勿包含屬性頁的任何篩選設定資訊。


```C++
const AMOVIESETUP_FILTER FilterSetupData = 
{ 
    /* Not shown ... */
};

CFactoryTemplate g_Templates[] =
{   
    // This entry is for the filter.
    {
        wszName,
        &CLSID_GrayFilter,
        CGrayFilter::CreateInstance,
        NULL,
        &FilterSetupData 
    },
    // This entry is for the property page.
    { 
        L"Saturation Props",
        &CLSID_SaturationProp,
        CGrayProp::CreateInstance, 
        NULL, NULL
    }
};
```



如果您如下列程式碼所示宣告 *g \_ cTemplates* ，則它會根據陣列大小自動具有正確的值：


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



此外，將靜態 `CreateInstance` 方法加入至屬性頁類別。 您可以為方法命名任何您偏好的名稱，但簽章必須符合下列範例所示的內容：


```C++
static CUnknown * WINAPI CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CGrayProp *pNewObject = new CGrayProp(pUnk);
    if (pNewObject == NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 
```



若要測試屬性頁，請註冊 DLL，然後在 GraphEdit 中載入篩選。 以滑鼠右鍵按一下篩選器，然後選取 [ **篩選屬性**]。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立篩選屬性頁](creating-a-filter-property-page.md)
</dt> <dt>

[如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)
</dt> </dl>

 

 



