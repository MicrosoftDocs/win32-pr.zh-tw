---
description: 註冊 SQL-DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: 註冊 SQL-DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973538"
---
# <a name="registering-a-dmo"></a>註冊 SQL-DMO

為了讓用戶端使用您的，必須在使用者的系統上註冊 CLSID。 這是透過 DLL 的 **DllRegisterServer** 函式來完成。 如果您使用 Active Template Library (ATL) ，則 ATL wizard 會自動產生此函數。

您也可以在一或多個標準的 SQL-DMO 類別下註冊您的。 這可讓用戶端使用 [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) 函數探索您的。 類別目錄是由 GUID 所定義，而且會列在第一節的 [guid](dmo-guids.md)中。

在類別目錄下註冊的是選擇性的。 若要這樣做，請呼叫 [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) 函式，並指定該名稱、CLSID 和分類的易記名稱。 （選擇性）您也可以註冊 DMOs 支援的一組媒體類型。 如需詳細資訊，請參閱 [Sql-dmo 媒體類型](dmo-media-types.md)。

下列範例顯示如何註冊支援 PCM 音訊輸入和輸出的音訊效果。 在此情況下，輸入類型和輸出類型都相同。


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



此範例假設使用 ATL 建立專案;函式的最後一行會呼叫標準 ATL 方法來註冊 COM 伺服器。 如果您不是使用 ATL，則您的函式看起來會不同。

**取消註冊**

**DllUnregisterServer** 函數必須移除 **DllRegisterServer** 函數所建立的任何登錄專案。 如果您在註冊時呼叫 **DMORegister** ，則必須在取消註冊時使用相同的類別 [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) 。

下列範例會移除在上述範例中建立的登錄專案：


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**DirectShow 業績值**

基於建立篩選圖形的目的，DirectShow 會將預設的業績值指派給 DMOs。 您可以藉由將登錄專案新增至 HKEY \_ 類別根目錄 CLSID 中的 sql-dmo 登錄機碼來覆寫此值 \_ \\ 。 包含名為的 **DWORD** 值 `Merit` ，其值會指定其值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 SQL-DMO](writing-a-dmo.md)
</dt> </dl>

 

 



