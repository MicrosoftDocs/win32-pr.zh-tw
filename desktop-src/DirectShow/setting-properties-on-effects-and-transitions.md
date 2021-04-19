---
description: 設定效果和轉換的屬性
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: 設定效果和轉換的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972915"
---
# <a name="setting-properties-on-effects-and-transitions"></a>設定效果和轉換的屬性

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

許多 [DirectShow 編輯服務](directshow-editing-services.md) 效果和轉換都支援控制其行為的屬性。 應用程式可以使用 [**IPropertySetter**](ipropertysetter.md) 介面來設定屬性的值。 基礎效果或轉換物件必須支援 **IDispatch** 來設定屬性。 使用影片效果和轉換，應用程式可以設定一段時間後會變更的值範圍。  (例如，您可以設定抹除轉換，以在整個框架中來回移動。 ) 有音訊效果時，屬性的值為靜態，且不會隨著時間而變更。 唯一的例外是 [音量信封](volume-envelope-effect.md) 效果，其支援磁片區層級的動態屬性。

若要設定屬性，請執行下列步驟。

1.  建立屬性 setter (CLSID PropertySetter) 的實例 \_ 。
2.  以屬性資料填入 [**DEXTER \_ PARAM**](dexter-param.md) 和 [**DEXTER \_ 值**](dexter-value.md) 結構。 以下將討論這些結構。
3.  將 [**DEXTER \_ PARAM**](dexter-param.md) 和 [**DEXTER \_ 值**](dexter-value.md) 結構傳遞至 [**IPropertySetter：： AddProp**](ipropertysetter-addprop.md) 方法。
4.  針對您要設定的每個屬性重複步驟2和3。
5.  將 [**IPropertySetter**](ipropertysetter.md) 介面指標傳遞至 [**IAMTimelineObj：： SetPropertySetter**](iamtimelineobj-setpropertysetter.md) 方法。

[**DEXTER \_ PARAM**](dexter-param.md)結構會指定所要設定的屬性。 它包含下列成員。

-   **名稱**：屬性的名稱
-   **dispID**： Reserved，必須為零
-   值 **：值** 數目

DEXTER \_ 值結構會指定屬性在指定時間的值。 它包含下列成員。

-   **v**：為屬性指定新值的 VARIANT 類型。 這個變異的 **vt** 成員定義了屬性的資料型別。 如需 **VARIANT** 型別的詳細資訊，請參閱 Windows SDK。
-   **rt**：屬性會假設此值（相對於效果或轉換的開始時間）的參考時間。 效果或轉換的開始時間相對於其父物件的開始時間。
-   **dwInterp**：指定屬性如何從先前值變更為新值的旗標。 使用 DEXTERF \_ 跳躍旗標，屬性會在指定的時間立即跳到新值。 使用 DEXTERF \_ 插補旗標，屬性會以線性方式從先前的值插入。

如果您將 **vt** 成員設定為 vt \_ BSTR，屬性 setter 會進行任何必要的轉換。 若為浮點值，請在小數點之前加上前置零。 例如，0.3，而不是. 3。

> [!Note]  
> 應用程式應該避免依賴從 **BSTR** 轉換成數值。 如果屬性具有數值，則可以使用適當的數值 **VARIANT** 類型。

 

屬性的值可能會隨著時間而變更，因此 [**IPropertySetter：： AddProp**](ipropertysetter-addprop.md) 方法會採用單一 [**DEXTER \_ 參數**](dexter-param.md) 結構和 [**DEXTER \_ 值**](dexter-value.md) 結構陣列的指標。 陣列會為屬性定義一組以時間為基礎的值。 陣列的成員必須是遞增的時間順序，而且 DEXTER PARAM 結構 **的次序成員** \_ 必須等於陣列的長度。

下列程式碼範例會建立適用于 [SMPTE](smpte-wipe-transition.md) 抹除轉換的屬性資料。 它會將抹除碼設定為120，以建立 oval 抹除。 它會將參考時間設定為零，表示轉換開始。


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



**動態變更屬性**

轉譯影片編輯專案之後，就可以在圖形執行時修改效果或轉換物件的屬性。 不過，只有當您在應用程式呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md)之前設定該物件的屬性時，才有可能這樣做。 若是如此，您可以在效果或轉換上呼叫 [**IAMTimelineObj：： GetPropertySetter**](iamtimelineobj-getpropertysetter.md) 、清除或修改屬性，變更將會在圖形執行時動態發生。 發生變更時可能會有視覺異常，因此建議僅供預覽。 當您將專案寫入檔案時，請勿變更屬性。

如果您在呼叫 **ConnectFrontEnd** 之前未在效果或轉換物件上設定任何屬性，您就無法在圖形執行時將屬性加入其中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用效果和轉換](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



