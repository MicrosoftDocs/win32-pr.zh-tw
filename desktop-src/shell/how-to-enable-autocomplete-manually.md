---
description: 若要取得更詳細的自動完成行為控制，或加入自動完成字串的自訂來源，您必須自行管理自動完成物件。
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: 如何手動啟用自動完成
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973157"
---
# <a name="how-to-enable-autocomplete-manually"></a>如何手動啟用自動完成

若要取得更詳細的自動完成行為控制，或加入自動完成字串的自訂來源，您必須自行管理自動完成物件。 您可以透過下列方式手動啟用自動完成。

## <a name="instructions"></a>指示

### <a name="creating-a-simple-autocomplete-object"></a>建立簡單的自動完成物件

下列步驟說明如何建立和初始化簡單的自動完成物件。 簡單的自動完成物件會從單一來源完成字串。 在此範例中，已刻意省略錯誤檢查。

1.  建立自動完成物件。

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  建立自動完成來源。 您可以使用 [預先定義的自動完成來源](ac-ovw.md) ，也可以撰寫自己的自訂來源。

    下列程式碼會使用其中一個預先定義的自動完成來源。

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    下列程式碼會使用自訂的自動完成來源。 您可以藉由執行公開 [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) 介面的物件來撰寫自己的自動完成來源。 物件也可以選擇性地執行 [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) 和 [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) 介面。

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  設定自動完成來源 (選用) 的選項。

    如果來源公開 [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) 介面，您可以藉由設定自動完成來源的行為，藉此自訂。 使用預先定義的自動完成來源時，只有 CLSID \_ ACListISF 會匯出 **IACList2**。 如需選項及其值的完整清單，請參閱 [**IACList2：： >setoptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions)。

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  初始化自動完成物件。

    在此範例中， **hwndEdit** 是 [編輯] 控制項視窗的控制碼，可啟用自動完成。 如需最後兩個未使用參數的描述，請參閱 [**IAutoComplete：： Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) 。

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  將 [自動完成] 物件的選項設定 (選擇性) 。

    您可以藉由設定 [自動完成] 物件的選項來自訂其行為。 如需選項及其值的完整清單，請參閱 [**IACList2：： >setoptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions)的檔。

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  釋放物件。

    > [!Note]  
    > 即使在您發行之後，自動完成物件仍會附加至編輯控制項。 如果您未來需要存取這些物件-如果您想要在稍後變更自動完成選項（例如），則不需要在此時釋放。

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a>建立複合自動完成物件

複合自動完成物件會與多個來源的字串相符。 例如，Windows Internet Explorer 網址列會使用複合自動完成物件，因為使用者可能會開始輸入檔案或 URL 的名稱。 建立複合自動完成物件所涉及的大部分步驟，與「建立簡單的自動完成物件」中的步驟相同。 這些步驟會以這樣的方式表示。

1.  建立自動完成物件。 這與上述步驟1相同。

2.  建立自動完成複合來源物件管理員。

    自動完成複合來源物件可將多個自動完成來源合併成單一的自動完成來源。

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  建立並設定每個自動完成來源的選項。 針對每個來源重複上述步驟2和3。

4.  將每個自動完成來源附加至來源物件管理員。

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  初始化自動完成物件。

    這與上述步驟4相同，不同之處在于，您可以傳遞複合來源物件管理員，而不是將簡單的自動完成來源傳遞至 [**IAutoComplete：： Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init)。

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  設定自動完成物件的選項。 這與上述步驟5相同。

7.  釋放物件。

    在簡單的情況下，您可以在使用完畢後立即釋出物件，但是您也可以在稍後保留它們來變更選項。

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
