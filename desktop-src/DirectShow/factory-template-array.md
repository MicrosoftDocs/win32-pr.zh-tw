---
description: Factory 範本陣列
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Factory 範本陣列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109900"
---
# <a name="factory-template-array"></a>Factory 範本陣列

Factory 範本包含下列公用成員變數：

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

這兩個函式指標（ [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) 和 [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md)）使用下列型別定義：

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

第一個是元件的具現化函數。 第二個是選擇性的初始化函數。 如果您提供初始化函式，它會從 DLL 進入點函數內部呼叫。 本文稍後將討論 DLL 進入點函數 (。 ) 

假設您要建立一個 DLL，其中包含名為 CMyComponent 的元件，而該元件繼承自 [**CUnknown**](cunknown.md)。 您必須在 DLL 中提供下列專案：

-   初始化函式，這個公用方法會傳回 CMyComponent 的新實例。
-   名為 *g \_ 範本* 的原廠範本的全域陣列。 此陣列包含 CMyComponent 的 factory 範本。
-   名為 *g \_ cTemplates* 的全域變數，可指定陣列的大小。

下列範例顯示如何宣告這些專案：


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



`CreateInstance`方法會呼叫類別的函式，並將指標傳回至新的類別實例。 參數 *pUnk* 是匯總 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)的指標。 您可以直接將此參數傳遞至類別的函式。 參數 *pHr* 是 HRESULT 值的指標。 類別的函式會將此值設定為適當的值，但如果此函式失敗，請將值設定為 E \_ OUTOFMEMORY。

[**NAME**](name.md)宏會在 debug 組建中產生字串，但會在零售組建中解析為 **Null** 。 在此範例中，會使用它來提供元件名稱，此名稱會出現在偵錯工具記錄檔中，但不會在最終版本中佔用記憶體。

`CreateInstance`方法可以有任何名稱，因為 class factory 參考 factory 範本中的函式指標。 但是， *g \_ 範本* 和 *g \_ cTemplates* 是 class factory 預期要尋找的全域變數，因此它們必須正好具有這些名稱。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)
</dt> </dl>

 

 
