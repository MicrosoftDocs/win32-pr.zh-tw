---
description: 本主題說明在 DirectShow capture 篩選器上執行輸出 pin 的需求。
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: 捕獲篩選準則的 Pin 需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e72c74f06970bf6124d0e5dffea458bb41bcd0a19db44acc71a51615aa2fee8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316108"
---
# <a name="pin-requirements-for-capture-filters"></a>捕獲篩選準則的 Pin 需求

本主題說明在 DirectShow capture 篩選器上執行輸出 pin 的需求。

## <a name="pin-name"></a>接腳名稱

您可以為 pin 提供任何名稱。 如果 pin 名稱以波狀符號 (~) 字元開頭，則當應用程式呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)時，篩選 Graph 管理員不會自動呈現該 pin。 例如，如果篩選具有 capture pin 和預覽 pin，您可以分別將它們命名為 "~ Capture" 和 "Preview"。 如果應用程式在圖形中轉譯該篩選，預覽 pin 將會連接到其預設轉譯器，而不會連接到捕捉釘選，這是合理的預設行為。 這也適用于傳遞不打算轉譯之資訊資料的 pin，或需要設定自訂屬性的釘選。 請注意，應用程式仍然可以手動連接具有波狀符號 (~) 前置詞的釘選。

## <a name="pin-category"></a>釘選類別

捕捉篩選準則一律具有 capture pin，而且可能有預覽 pin。 某些 capture 篩選器可能會有其他輸出圖釘，以提供其他類型的資料，例如控制資訊。 每個輸出圖釘都必須公開 [**IKsPropertySet**](ikspropertyset.md) 介面。 應用程式會使用此介面來判斷釘選類別。 Pin 通常會傳回 PIN \_ 類別 \_ 捕獲或 pin \_ 類別 \_ 預覽。 如需詳細資訊，請參閱 [釘選屬性集](pin-property-set.md)。

下列範例顯示如何執行 [**IKsPropertySet**](ikspropertyset.md) ，以傳回捕捉釘選上的釘選類別：


```C++
// Set: Cannot set any properties.
HRESULT CMyCapturePin::Set(REFGUID guidPropSet, DWORD dwID,
    void *pInstanceData, DWORD cbInstanceData, void *pPropData, 
    DWORD cbPropData)
{
    return E_NOTIMPL;
}

// Get: Return the pin category (our only property). 
HRESULT CMyCapturePin::Get(
    REFGUID guidPropSet,   // Which property set.
    DWORD dwPropID,        // Which property in that set.
    void *pInstanceData,   // Instance data (ignore).
    DWORD cbInstanceData,  // Size of the instance data (ignore).
    void *pPropData,       // Buffer to receive the property data.
    DWORD cbPropData,      // Size of the buffer.
    DWORD *pcbReturned     // Return the size of the property.
)
{
    if (guidPropSet != AMPROPSETID_Pin) 
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pPropData == NULL && pcbReturned == NULL)
        return E_POINTER;
    if (pcbReturned)
        *pcbReturned = sizeof(GUID);
    if (pPropData == NULL)  // Caller just wants to know the size.
        return S_OK;
    if (cbPropData < sizeof(GUID)) // The buffer is too small.
        return E_UNEXPECTED;
    *(GUID *)pPropData = PIN_CATEGORY_CAPTURE;
    return S_OK;
}

// QuerySupported: Query whether the pin supports the specified property.
HRESULT CMyCapturePin::QuerySupported(REFGUID guidPropSet, DWORD dwPropID,
    DWORD *pTypeSupport)
{
    if (guidPropSet != AMPROPSETID_Pin)
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pTypeSupport)
        // We support getting this property, but not setting it.
        *pTypeSupport = KSPROPERTY_SUPPORT_GET; 
    return S_OK;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[寫入捕獲篩選器](writing-capture-filters.md)
</dt> </dl>

 

 



