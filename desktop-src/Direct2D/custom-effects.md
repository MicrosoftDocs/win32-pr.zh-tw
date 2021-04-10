---
title: 自訂效果
description: 說明如何使用標準 HLSL 撰寫您自己的自訂效果。
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093252"
---
# <a name="custom-effects"></a>自訂效果

[Direct2D](./direct2d-portal.md) 隨附的效果程式庫會執行各種常見的映射作業。 如需效果的完整清單，請參閱 [內建效果](built-in-effects.md) 主題。 針對無法利用內建效果達成的功能，Direct2D 可讓您使用標準 [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)來撰寫自己的自訂效果。 您可以將這些自訂效果與 Direct2D 隨附的內建效果一起使用。

若要查看完整圖元、頂點和計算著色器效果的範例，請參閱 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)。

在本主題中，我們將說明您設計和建立功能完整的自訂效果所需的步驟和概念。

## <a name="introduction-what-is-inside-an-effect"></a>簡介：什麼是作用中？

![投影陰影效果圖。](images/custom-effects1.png)

從概念上來說， [Direct2D](./direct2d-portal.md) 效果會執行映射處理工作，例如變更亮度、對影像進行消除飽和，或如上所示，建立陰影。 應用程式很簡單。 他們可以接受零個以上的輸入影像、公開多個控制其作業的屬性，以及產生單一輸出影像。

有四個自訂效果的不同部分是由效果作者負責：

1.  效果介面：效果介面在概念上定義了應用程式如何與自訂效果互動 (例如效果所接受的輸入數目，以及) 可用的屬性。 效果介面會管理包含實際影像作業的轉換圖形。
2.  轉換圖形：每個效果都會建立由個別轉換所組成的內部轉換圖形。 每個轉換都代表單一映射作業。 效果會負責將這些轉換一起連結到圖形中，以執行預期的圖像效果。 效果可以加入、移除、修改及重新排序轉換，以回應效果的外部屬性變更。
3.  轉換：轉換代表單一映射作業。 其主要目的是要存放針對每個輸出圖元執行的著色器。 為了達到此目的，它會負責根據其著色器中的邏輯來計算其輸出影像的新大小。 它也必須計算其輸入影像的哪個區域，著色器需要從該區域讀取以轉譯要求的輸出區域。
4.  著色器：當應用程式建立 Direct3D 裝置) 時指定軟體轉譯時，會針對 GPU (或 CPU 上的轉換輸入執行著色器。 效果著色器會以高階網底語言撰寫 ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) ，並在效果的編譯期間編譯成位元組程式碼，然後在執行時間由效果載入。 本參考檔說明如何撰寫符合 [Direct2D](./direct2d-portal.md)規範的 HLSL。 Direct3D 檔包含基本的 HLSL 總覽。

## <a name="creating-an-effect-interface"></a>建立效果介面

效果介面會定義應用程式與自訂效果的互動方式。 若要建立效果介面，類別必須執行 ID2D1EffectImpl、定義描述效果 (的中繼資料，例如其名稱、輸入計數和屬性) ，以及建立註冊自訂效果以搭配 [Direct2D](./direct2d-portal.md)使用的方法。

一旦執行效果介面的所有元件之後，類別的標頭就會如下所示：


```C++
#include <d2d1_1.h>
#include <d2d1effectauthor.h>  
#include <d2d1effecthelpers.h>

// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);

class SampleEffect : public ID2D1EffectImpl
{
public:
    // 2.1 Declare ID2D1EffectImpl implementation methods.
    IFACEMETHODIMP Initialize(
        _In_ ID2D1EffectContext* pContextInternal,
        _In_ ID2D1TransformGraph* pTransformGraph
        );

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE changeType);
    IFACEMETHODIMP SetGraph(_In_ ID2D1TransformGraph* pGraph);

    // 2.2 Declare effect registration methods.
    static HRESULT Register(_In_ ID2D1Factory1* pFactory);
    static HRESULT CreateEffect(_Outptr_ IUnknown** ppEffectImpl);

    // 2.3 Declare IUnknown implementation methods.
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Outptr_ void** ppOutput);

private:
    // Constructor should be private since it should never be called externally.
    SampleEffect();

    LONG m_refCount; // Internal ref count used by AddRef() and Release() methods.
};
```



### <a name="implement-id2d1effectimpl"></a>執行 ID2D1EffectImpl

[**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)介面包含您必須執行的三個方法：

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a>Initialize (ID2D1EffectCoNtext \* pCoNtextInternal，ID2D1TransformGraph \* pTransformGraph) 

[Direct2D](./direct2d-portal.md)會在應用程式呼叫 [**ID2D1DeviceCoNtext：： CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)方法之後，呼叫 [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize)方法。 您可以使用這個方法來執行內部初始化或此效果所需的任何其他作業。 此外，您可以使用它來建立效果的初始轉換圖形。

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a>SetGraph (ID2D1TransformGraph \* pTransformGraph) 

當效果的輸入數目變更時， [Direct2D](./direct2d-portal.md)會呼叫 [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph)方法。 雖然大部分的效果都有固定數目的輸入，但其他像是 [複合效果](composite.md) 的輸入則支援可變的輸入數目。 此方法可讓這些效果更新其轉換圖形，以回應變更的輸入計數。 如果效果不支援變數輸入計數，則這個方法只會傳回 E \_ >notimpl。

### <a name="prepareforrender-d2d1_change_type-changetype"></a>PrepareForRender (D2D1 \_ 變更 \_ 類型 changeType) 

[**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender)方法可讓您有機會執行任何作業，以回應外部變更。 如果至少有一個條件成立， [Direct2D](./direct2d-portal.md)就會在呈現效果之前呼叫這個方法：

-   效果先前已初始化但尚未繪製。
-   效果屬性自上次繪製呼叫之後已經變更。
-   呼叫 [Direct2D](./direct2d-portal.md) 內容的狀態 (例如 DPI) 自上次繪製呼叫之後已經變更。

### <a name="implement-the-effect-registration-and-callback-methods"></a>實行效果註冊和回呼方法

應用程式必須先向 [Direct2D](./direct2d-portal.md) 註冊效果，才能將其具現化。 此註冊的範圍是 Direct2D factory 的實例，而且必須在每次執行應用程式時重複。 若要啟用此註冊，自訂效果會定義唯一的 GUID、註冊效果的公用方法，以及傳回效果實例的私用回呼方法。

### <a name="define-a-guid"></a>定義 GUID

您必須定義可唯一識別 [Direct2D](./direct2d-portal.md)註冊效果的 GUID。 應用程式在呼叫 [**ID2D1DeviceCoNtext：： CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)時，會使用相同的來識別效果。

這段程式碼示範如何定義效果的這類 GUID。 您必須使用 GUID 產生工具（例如 guidgen.exe）來建立自己的唯一 GUID。


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a>定義公用註冊方法

接下來，定義應用程式呼叫的公用方法，以使用 [Direct2D](./direct2d-portal.md)註冊效果。 因為效果註冊是 Direct2D factory 實例特有的，所以此方法會接受 [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) 介面作為參數。 方法接著會在 **ID2D1Factory1** 參數上呼叫 [**ID2D1Factory1：： RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API，以註冊效果。

此 API 接受 XML 字串來描述效果的中繼資料、輸入和屬性。 效果的中繼資料僅供資訊參考之用，並可透過 [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) 介面查詢應用程式。 另一方面，輸入和屬性資料是由 [Direct2D](./direct2d-portal.md) 使用，代表效果的功能。

以下顯示基本範例效果的 XML 字串。 將自訂屬性新增至效果區段中包含了 XML 的自訂屬性。


```XML
#define XML(X) TEXT(#X) // This macro creates a single string from multiple lines of text.

PCWSTR pszXml =
    XML(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description' type='string' value='This is a demo effect.'/>
            <Inputs>
                <Input name='SourceOne'/>
                <!-- <Input name='SourceTwo'/> -->
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
        </Effect>
        );
```



### <a name="define-an-effect-factory-callback-method"></a>定義效果 factory 回呼方法

效果也必須提供私用回呼方法，以透過單一 IUnknown 參數傳回效果的實例 \* \* 。 當透過 [**ID2D1Factory1：： RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API 透過 [**PD2D1 \_ 效果 \_ FACTORY**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory)參數註冊效果時，會提供此方法的指標給 [Direct2D](./direct2d-portal.md) \\ 。


```C++
HRESULT __stdcall SampleEffect::CreateEffect(_Outptr_ IUnknown** ppEffectImpl)
{
    // This code assumes that the effect class initializes its reference count to 1.
    *ppEffectImpl = static_cast<ID2D1EffectImpl*>(new SampleEffect());

    if (*ppEffectImpl == nullptr)
    {
        return E_OUTOFMEMORY;
    }

    return S_OK;
}
```



### <a name="implement-the-iunknown-interface"></a>執行 IUnknown 介面

最後，效果必須執行 IUnknown 介面，以與 COM 相容。

## <a name="creating-the-effects-transform-graph"></a>建立效果的轉換圖形

效果可以使用數種不同的轉換 (個別的影像作業) 來建立其所需的影像效果。 為了控制這些轉換套用至輸入影像的順序，效果會將它們排列成轉換圖形。 轉換圖可利用 [Direct2D](./direct2d-portal.md) 中包含的效果和轉換，以及效果作者所建立的自訂轉換。

### <a name="using-transforms-included-with-direct2d"></a>使用 Direct2D 隨附的轉換

這些是 [Direct2D](./direct2d-portal.md)所提供的最常使用轉換。

-   [**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform)：這項轉換會根據 blend 描述將任意數目的輸入混合在一起，請參閱 [**D2D1 \_ blend \_ 描述**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) 主題和混合範例的 [Direct2D 複合效果模式範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) 。 [**ID2D1EffectCoNtext：： CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform)方法會傳回這項轉換。
-   [**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform)：此轉換會根據指定的 [**D2D1 \_ 擴充 \_ 模式**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) 來展開影像的輸出大小。 [**ID2D1EffectCoNtext：： CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform)方法會傳回這項轉換。
-   [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform)：此轉換位移 (會將) 其輸入轉譯為任何整數的圖元數。 [**ID2D1EffectCoNtext：： CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform)方法會傳回這項轉換。
-   您可以使用 [**ID2D1EffectCoNtext：： CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) 方法，將任何現有的效果視為轉換圖形建立用途的轉換。

### <a name="creating-a-single-node-transform-graph"></a>建立單一節點的轉換圖形

建立轉換之後，效果的輸入必須連接到轉換的輸入，且轉換的輸出必須連接到效果的輸出。 如果效果只包含單一轉換，您可以使用 [**ID2D1TransformGraph：： SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) 方法輕鬆完成此動作。

您可以使用提供的 ID2D1TransformGraph 參數，在效果的 [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) 或 [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) 方法中建立或修改轉換。 如果效果需要在無法使用此參數的另一個方法中變更轉換圖形，效果可以將 [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) 參數儲存為類別的成員變數，並在其他位置存取它，例如 [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) 或自訂屬性回呼方法。

範例 [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) 方法如下所示。 這個方法會建立單一節點的轉換圖形，將每個軸中的影像位移100圖元。


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext,
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{
    HRESULT hr = pEffectContext->CreateOffsetTransform(
        D2D1::Point2L(100,100),  // Offsets the input by 100px in each axis.
        &m_pOffsetTransform
        );

    if (SUCCEEDED(hr))
    {
        // Connects the effect's input to the transform's input, and connects
        // the transform's output to the effect's output.
        hr = pTransformGraph->SetSingleTransformNode(m_pOffsetTransform);
    }

    return hr;
}
```



### <a name="creating-a-multi-node-transform-graph"></a>建立多節點轉換圖形

將多個轉換新增至效果的轉換圖，可讓您在內部執行多個映射作業，並以單一整合效果的形式呈現給應用程式。

如上所述，使用在效果的 [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize)方法中收到的 [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph)參數，可在任何效果方法中編輯效果的轉換圖形。 您可以使用該介面上的下列 Api 來建立或修改效果的轉換圖形：

### <a name="addnodeid2d1transformnode-pnode"></a>AddNode (ID2D1TransformNode \* pNode) 

實際上， [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) 方法會「註冊」具有效果的轉換，而且必須在轉換可以與任何其他轉換圖表方法搭配使用之前呼叫。

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a>ConnectToEffectInput (UINT32 toEffectInputIndex、ID2D1TransformNode \* pNode、UINT32 toNodeInputIndex) 

[**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput)方法會將效果的影像輸入連接至轉換的輸入。 相同的效果輸入可以連接到多個轉換。

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a>ConnectNode (ID2D1TransformNode \* pFromNode、ID2D1TransformNode \* PTONODE、UINT32 toNodeInputIndex) 

[**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode)方法會將轉換的輸出連接到另一個轉換的輸入。 轉換輸出可以連接到多個轉換。

### <a name="setoutputnodeid2d1transformnode-pnode"></a>SetOutputNode (ID2D1TransformNode \* pNode) 

[**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode)方法會將轉換的輸出連接到效果的輸出。 因為效果只會有一個輸出，所以只能將單一轉換指定為「輸出節點」。

此程式碼會使用兩個不同的轉換來建立統一效果。 在此情況下，效果是轉譯的陰影。


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext, 
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{   
    // Create the shadow effect.
    HRESULT hr = pEffectContext->CreateEffect(CLSID_D2D1Shadow, &m_pShadowEffect);

    // Create the shadow transform from the shadow effect.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateTransformNodeFromEffect(m_pShadowEffect, &m_pShadowTransform);
    }

    // Create the offset transform.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateOffsetTransform(
            D2D1::Point2L(0,0),
            &m_pOffsetTransform
            );
    }

    // Register both transforms with the effect graph.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pShadowTransform);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pOffsetTransform);
    }

    // Connect the custom effect's input to the shadow transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectToEffectInput(
            0,                  // Input index of the effect.
            m_pShadowTransform, // The receiving transform.
            0                   // Input index of the receiving transform.
            );
    }

    // Connect the shadow transform's output to the offset transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectNode(
            m_pShadowTransform, // 'From' node.
            m_pOffsetTransform, // 'To' node.
            0                   // Input index of the 'to' node. There is only one output for the 'From' node.
            );
    }

    // Connect the offset transform's output to the custom effect's output.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->SetOutputNode(
            m_pOffsetTransform
            );
    }

    return hr;
}
```



## <a name="adding-custom-properties-to-an-effect"></a>將自訂屬性新增至效果

效果可以定義自訂屬性，以允許應用程式在執行時間變更效果的行為。 定義自訂效果的屬性有三個步驟：

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a>將屬性中繼資料新增至效果的註冊資料

### <a name="add-property-to-registration-xml"></a>將屬性新增至註冊 XML

您必須在效果的初始註冊時，定義自訂效果的屬性（ [Direct2D](./direct2d-portal.md)）。 首先，您必須使用新的屬性，更新其公開註冊方法中的效果註冊 XML：


```C++
PCWSTR pszXml =
    TEXT(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description'
                type='string'
                value='Translates an image by a user-specifiable amount.'/>
            <Inputs>
                <Input name='Source'/>
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
            <Property name='Offset' type='vector2'>
                <Property name='DisplayName' type='string' value='Image Offset'/>
                <!— Optional sub-properties -->
                <Property name='Min' type='vector2' value='(-1000.0, -1000.0)' />
                <Property name='Max' type='vector2' value='(1000.0, 1000.0)' />
                <Property name='Default' type='vector2' value='(0.0, 0.0)' />
            </Property>
        </Effect>
        );
```



當您在 XML 中定義效果屬性時，它需要名稱、類型和顯示名稱。 屬性的顯示名稱，以及整體效果的類別、作者和描述值都可以當地語系化。

針對每個屬性，效果可以選擇性地指定預設值、最小值和最大值。 這些值僅供參考之用。 [Direct2D](./direct2d-portal.md)不會強制執行。 您必須自行在效果類別中執行任何指定的預設/最小/最大邏輯。

在 XML 中針對屬性所列的類型值，必須符合屬性的 getter 和 setter 方法所使用的對應資料類型。 下表顯示每個資料類型的對應 XML 值：



| 資料類型                                                                                                                              | 對應的 XML 值 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| PWSTR                                                                                                                                  | 字串                  |
| BOOL                                                                                                                                   | bool                    |
| UINT                                                                                                                                   | uint32                  |
| INT                                                                                                                                    | int32                   |
| FLOAT                                                                                                                                  | FLOAT                   |
| [**D2D \_ 向量 \_ 2f**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | vector2                 |
| [**D2D \_ 向量 \_ 3F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | vector3                 |
| [**D2D \_ 向量 \_ 4F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | vector4                 |
| [**D2D \_ 矩陣 \_ 3X2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool)) | matrix3x2               |
| [**D2D \_ 矩陣 \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | matrix4x3               |
| [**D2D \_ 矩陣 \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | matrix4x4               |
| [**D2D \_ 矩陣 \_ 5X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | matrix5x4               |
| 位元組\[\]                                                                                                                               | blob                    |
| IUnknown\*                                                                                                                             | iunknown                |
| [**ID2D1ColorCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*                                                                                       | colorcoNtext            |
| CLSID                                                                                                                                  | clsid                   |
| 列舉 ([**D2D1 \_ 插補 \_ 模式**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode)等 )                                                 | 列舉                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a>將新的屬性對應至 getter 和 setter 方法

接下來，效果必須將這個新的屬性對應至 getter 和 setter 方法。 這是透過傳遞至 [**ID2D1Factory1：： RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring)方法的 [**D2D1 \_ 屬性 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding)系結陣列來完成。

[**D2D1 \_ 屬性 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding)系結陣列看起來像這樣：


```C++
const D2D1_PROPERTY_BINDING bindings[] =
{
    D2D1_VALUE_TYPE_BINDING(
        L"Offset",      // The name of property. Must match name attribute in XML.
        &SetOffset,     // The setter method that is called on "SetValue".
        &GetOffset      // The getter method that is called on "GetValue".
        )
};
```



建立 XML 和系結陣列之後，請將其傳遞至 [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) 方法：


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



D2D1 VALUE 型別系結 \_ \_ \_ 宏需要效果類別在其他任何介面之前繼承自 [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) 。

效果的自訂屬性會依照在 XML 中宣告的順序來編制索引，而一旦建立之後，應用程式就可以使用 [**ID2D1Properties：： SetValue**](id2d1properties-setvalue-overload.md) 和 [**ID2D1Properties：： GetValue**](id2d1properties-getvalue-overload.md) 方法來存取這些屬性。 為了方便起見，您可以建立公用列舉，以列出效果標頭檔中的每個屬性：


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a>建立屬性的 getter 和 setter 方法

下一步是建立新屬性的 getter 和 setter 方法。 方法的名稱必須符合 [**D2D1 \_ 屬性 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) 系結陣列中所指定的名稱。 此外，在效果的 XML 中指定的屬性類型，必須符合 setter 方法參數的類型和 getter 方法的傳回值。


```C++
HRESULT SampleEffect::SetOffset(D2D_VECTOR_2F offset)
{
    // Method must manually clamp to values defined in XML.
    offset.x = min(offset.x, 1000.0f); 
    offset.x = max(offset.x, -1000.0f); 

    offset.y = min(offset.y, 1000.0f); 
    offset.y = max(offset.y, -1000.0f); 

    m_offset = offset;

    return S_OK;
}

D2D_VECTOR_2F SampleEffect::GetOffset() const
{
    return m_offset;
}
```



### <a name="update-effects-transforms-in-response-to-property-change"></a>更新效果的轉換，以回應屬性變更

若要實際更新效果的影像輸出以回應屬性變更，效果需要變更其基礎轉換。 這通常會在效果的 [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) 方法中完成，而 [Direct2D](./direct2d-portal.md) 會在其中一個效果的屬性變更時自動呼叫此方法。 不過，您可以在任何效果的方法中更新轉換：例如 Initialize 或效果的屬性 setter 方法。

例如，如果效果包含 [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) ，而且想要修改其位移值以回應變更的效果位移屬性，它會在 [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender)中新增下列程式碼：


```C++
IFACEMETHODIMP SampleEffect::PrepareForRender(D2D1_CHANGE_TYPE changeType)
{
    // All effect properties are DPI independent (specified in DIPs). In this offset
    // example, the offset value provided must be scaled from DIPs to pixels to ensure
    // a consistent appearance at different DPIs (excluding minor scaling artifacts).
    // A context's DPI can be retrieved using the ID2D1EffectContext::GetDPI API.
    
    D2D1_POINT_2L pixelOffset;
    pixelOffset.x = static_cast<LONG>(m_offset.x * (m_dpiX / 96.0f));
    pixelOffset.y = static_cast<LONG>(m_offset.y * (m_dpiY / 96.0f));
    
    // Update the effect's offset transform with the new offset value.
    m_pOffsetTransform->SetOffset(pixelOffset);

    return S_OK;
}
```



## <a name="creating-a-custom-transform"></a>建立自訂轉換

若要在 [Direct2D](./direct2d-portal.md)中所提供的映射作業以外的範圍執行，您必須執行自訂轉換。 自訂轉換可以使用自訂 HLSL 著色器，任意變更輸入影像。

轉換會根據所使用的著色器類型來執行兩個不同介面的其中一個。 使用圖元和/或頂點著色器的轉換必須執行 [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)，而使用計算著色器的轉換必須執行 [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform)。 這些介面都繼承自 [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)。 本節著重于如何執行兩者通用的功能。

[**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)介面有四個要執行的方法：

### <a name="getinputcount"></a>GetInputCount

這個方法會傳回整數，表示轉換的輸入計數。


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a>MapInputRectsToOutputRect

[Direct2D](./direct2d-portal.md) 會在每次轉譯轉換時呼叫 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) 方法。 Direct2D 會將代表每個輸入之界限的矩形傳遞至轉換。 接著，轉換會負責計算輸出影像的界限。 這個介面上所有方法的矩形大小 ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) 是以圖元為單位來定義，而不是 dip。

這個方法也會根據其著色器的邏輯和每個輸入的不透明區域，負責計算不透明的輸出區域。 影像的不透明區域的定義，就是將整個矩形的 Alpha 色板視為 ' 1 '。 如果不清楚轉換的輸出是否為不透明，則輸出不透明的矩形應該設定為 (0、0、0、0) 為安全值。 [Direct2D](./direct2d-portal.md) 會使用此資訊來執行具有「保證不透明」內容的轉譯優化。 如果這個值不正確，可能會導致轉譯不正確。

您可以修改轉換的轉譯行為 (如在此方法期間的第6到第8節) 所定義。 不過，您無法修改轉換圖形中的其他轉換，也無法在此修改圖形版面配置本身。


```C++
IFACEMETHODIMP SampleTransform::MapInputRectsToOutputRect(
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
    UINT32 inputRectCount,
    _Out_ D2D1_RECT_L* pOutputRect,
    _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
    )
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The output of the transform will be the same size as the input.
    *pOutputRect = pInputRects[0];
    // Indicate that the image's opacity has not changed.
    *pOutputOpaqueSubRect = pInputOpaqueSubRects[0];
    // The size of the input image can be saved here for subsequent operations.
    m_inputRect = pInputRects[0];

    return S_OK;
}
```



如需更複雜的範例，請考慮如何表示簡單的模糊運算：

如果模糊運算使用5圖元半徑，則輸出矩形的大小必須展開5圖元，如下所示。 修改矩形座標時，轉換必須確保其邏輯不會造成矩形座標中的任何 over/下溢。


```C++
// Expand output image by 5 pixels.

// Do not expand empty input rectangles.
if (pInputRects[0].right  > pInputRects[0].left &&
    pInputRects[0].bottom > pInputRects[0].top
    )
{
    pOutputRect->left   = ((pInputRects[0].left   - 5) < pInputRects[0].left  ) ? (pInputRects[0].left   - 5) : LONG_MIN;
    pOutputRect->top    = ((pInputRects[0].top    - 5) < pInputRects[0].top   ) ? (pInputRects[0].top    - 5) : LONG_MIN;
    pOutputRect->right  = ((pInputRects[0].right  + 5) > pInputRects[0].right ) ? (pInputRects[0].right  + 5) : LONG_MAX;
    pOutputRect->bottom = ((pInputRects[0].bottom + 5) > pInputRects[0].bottom) ? (pInputRects[0].bottom + 5) : LONG_MAX;
}
```



因為影像模糊，所以不透明的影像區域現在可能是部分透明的。 這是因為影像外面的區域預設為透明黑色，而此透明度將會混合到邊緣周圍的影像。 轉換必須反映其輸出不透明的矩形計算：


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



這些計算會在此視覺化：

![矩形計算圖例。](images/custom-effects2.png)

如需此方法的詳細資訊，請參閱 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) 參考頁面。

### <a name="mapoutputrecttoinputrects"></a>MapOutputRectToInputRects

[Direct2D](./direct2d-portal.md)會在 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)之後呼叫 [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects)方法。 轉換必須計算需要讀取的影像部分，才能正確轉譯要求的輸出區域。

如同之前，如果效果嚴格地對應圖元1-1，則可以將輸出矩形傳遞至輸入矩形：


```C++
IFACEMETHODIMP SampleTransform::MapOutputRectToInputRects(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
    UINT32 inputRectCount
    ) const
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The input needed for the transform is the same as the visible output.
    pInputRects[0] = *pOutputRect;
    return S_OK;
}
```



同樣地，如果轉換縮小或展開影像 (例如此處的模糊範例) ，圖元通常會使用周圍圖元來計算其值。 使用模糊時，圖元會以周圍的圖元為平均值，即使超出輸入影像的界限也是如此。 此行為會反映在計算中。 與之前相同，轉換會在展開矩形座標時檢查溢位。


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



此圖以視覺化方式呈現計算。 [Direct2D](./direct2d-portal.md) 會自動取樣不存在輸入影像的透明黑色圖元，讓模糊與螢幕上現有的內容逐漸混合。

![矩形外的效果取樣透明黑色圖元的圖例。](images/custom-effects3.png)

如果對應不是一般的，則這個方法應該將輸入矩形設定為最大區域，以保證結果正確。 若要這樣做，請將左邊和上邊緣設定為 INT \_ MIN，並將右和下邊緣設定為 int \_ MAX。

如需此方法的詳細資訊，請參閱 [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) 主題。

### <a name="mapinvalidrect"></a>MapInvalidRect

[Direct2D](./direct2d-portal.md) 也會呼叫 [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) 方法。 不過，不同于 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) 和 [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) 方法 Direct2D 不保證會在任何特定時間呼叫它。 這個方法在概念上會決定必須重新轉譯轉換輸出的哪個部分，以回應部分或其所有輸入變更。 有三種不同的案例可計算轉換的無效 rect。

### <a name="transforms-with-one-to-one-pixel-mapping"></a>使用一對一圖元對應的轉換

針對對應圖元1-1 的轉換，只要將不正確輸入矩形傳遞到不正確輸出矩形即可：


```C++
IFACEMETHODIMP SampleTransform::MapInvalidRect(
    UINT32 inputIndex,
    D2D1_RECT_L invalidInputRect,
    _Out_ D2D1_RECT_L* pInvalidOutputRect
    ) const
{
    // This transform is designed to only accept one input.
    if (inputIndex != 0)
    {
        return E_INVALIDARG;
    }

    // If part of the transform's input is invalid, mark the corresponding
    // output region as invalid. 
    *pInvalidOutputRect = invalidInputRect;

    return S_OK;
}
```



### <a name="transforms-with-many-to-many-pixel-mapping"></a>具有多對多圖元對應的轉換

當轉換的輸出圖元相依于其周圍區域時，不正確輸入矩形必須相對應展開。 這是為了反映出無效輸入矩形周圍的圖元也會受到影響，而且會變成無效。 例如，五個圖元模糊會使用下列計算：


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a>具有複雜圖元對應的轉換

針對輸入和輸出圖元沒有簡單對應的轉換，整個輸出可以標示為無效。 例如，如果轉換只是輸出輸入的平均色彩，則即使輸入的小部分變更，轉換的整個輸出也會變更。 在此情況下，不正確輸出矩形應該設定為邏輯上的無限矩形， (如下所示) 。 [Direct2D](./direct2d-portal.md) 會自動將此個到輸出的範圍。


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



如需此方法的詳細資訊，請參閱 [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) 主題。

完成這些方法之後，轉換的標頭就會包含下列各項：


```C++
class SampleTransform : public ID2D1Transform 
{
public:
    SampleTransform();

    // ID2D1TransformNode Methods:
    IFACEMETHODIMP_(UINT32) GetInputCount() const;
    
    // ID2D1Transform Methods:
    IFACEMETHODIMP MapInputRectsToOutputRect(
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
        UINT32 inputRectCount,
        _Out_ D2D1_RECT_L* pOutputRect,
        _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
        );    

    IFACEMETHODIMP MapOutputRectToInputRects(
        _In_ const D2D1_RECT_L* pOutputRect,
        _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
        UINT32 inputRectCount
        ) const;

    IFACEMETHODIMP MapInvalidRect(
        UINT32 inputIndex,
        D2D1_RECT_L invalidInputRect,
        _Out_ D2D1_RECT_L* pInvalidOutputRect 
        ) const;

    // IUnknown Methods:
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(REFIID riid, _Outptr_ void** ppOutput);

private:
    LONG m_cRef; // Internal ref count used by AddRef() and Release() methods.
    D2D1_RECT_L m_inputRect; // Stores the size of the input image.
};
```



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a>將圖元著色器新增至自訂轉換

一旦建立轉換，就必須提供會操作影像圖元的著色器。 本節涵蓋搭配自訂轉換使用圖元著色器的步驟。

### <a name="implementing-id2d1drawtransform"></a>執行 ID2D1DrawTransform

若要使用圖元著色器，轉換必須執行 [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) 介面，此介面繼承自第5節中所述的 [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) 介面。 此介面包含一個要執行的新方法：

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a>SetDrawInfo (ID2D1DrawInfo \* pDrawInfo) 

當第一次將轉換新增至效果的轉換圖形時， [Direct2D](./direct2d-portal.md)會呼叫 [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo)方法。 這個方法會提供 [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) 參數，以控制轉換的呈現方式。 請參閱此處提供之方法的 **ID2D1DrawInfo** 主題。

如果轉換選擇將此參數儲存為類別成員變數，則可以從其他方法（例如屬性 setter 或 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)）存取和變更 *drawInfo* 物件。 值得注意的是，它無法從 [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)的 [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects)或 [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect)方法中呼叫。

### <a name="creating-a-guid-for-the-pixel-shader"></a>建立圖元著色器的 GUID

接下來，轉換必須定義圖元著色器本身的唯一 GUID。 當 [Direct2D](./direct2d-portal.md) 將著色器載入記憶體時，以及當轉換選擇要用於執行的圖元著色器時，就會使用這種方式。 包含在 Visual Studio 中的工具（例如 guidgen.exe）可以用來產生隨機的 GUID。


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a>使用 Direct2D 載入圖元著色器

圖元著色器必須先載入至記憶體，才能供轉換使用。

若要將圖元著色器載入至記憶體，轉換應該從讀取已編譯的著色器位元組程式碼。Visual Studio (所產生的 CSO 檔案，請參閱 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 檔，以取得) 至位元組陣列的詳細資料。 這項技術在 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)中有詳細的示範。

將著色器資料載入位元組陣列之後，請在效果的 [**ID2D1EffectCoNtext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)物件上呼叫 [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)方法。 已載入具有相同 GUID 的著色器時， [Direct2D](./direct2d-portal.md)會忽略對 **LoadPixelShader** 的呼叫。

在圖元著色器載入至記憶體後，轉換必須將其 GUID 傳遞給 [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo)方法期間所提供之 [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo)參數上的 [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer)方法，以選取要執行的轉換。 在選取要執行之前，必須先將圖元著色器載入至記憶體。

### <a name="changing-shader-operation-with-constant-buffers"></a>使用常數緩衝區變更著色器作業

若要變更著色器的執行方式，轉換可以將常數緩衝區傳遞給圖元著色器。 若要這樣做，轉換會在類別標頭中定義包含所需變數的結構：


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



接著，轉換會在 [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo)方法中提供的 [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo)參數上呼叫 [**ID2D1DrawInfo：： SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer)方法，以將此緩衝區傳遞給著色器。

[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)也需要定義表示常數緩衝區的對應結構。 著色器結構中所包含的變數必須符合轉換結構中的變數。


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



一旦定義緩衝區後，就可以從圖元著色器內的任何位置讀取包含在內的值。

### <a name="writing-a-pixel-shader-for-direct2d"></a>為 Direct2D 撰寫圖元著色器

[Direct2D](./direct2d-portal.md) 轉換使用以標準 [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)撰寫的著色器。 不過，撰寫從轉換內容執行的圖元著色器有幾個重要概念。 如需完整功能的圖元著色器的完整範例，請參閱 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)。

[Direct2D](./direct2d-portal.md) 會自動將轉換的輸入對應至 HLSL 中的 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 和 [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) 物件。 第一個 **Texture2D** 位於登錄 t0，第一個 **SamplerState** 位於 register s0。 每個額外的輸入都位於下一個對應的暫存器 (t1 和 s1，例如) 。 您可以藉由呼叫 **Texture2D** 物件的範例，並傳入對應的 **SamplerState** 物件和材質座標，來取樣特定輸入的圖元資料。

每個呈現的圖元都會執行一次自訂圖元著色器。 每次執行著色器時， [Direct2D](./direct2d-portal.md) 會自動提供三個參數來識別其目前的執行位置：

-   場景-space 輸出：此參數代表整體目標介面的目前執行位置。 它是以圖元來定義，而其最小值/最大值會對應至 [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)所傳回之矩形的界限。
-   剪輯空間輸出：此參數是由 Direct3D 使用，且不能用於轉換的圖元著色器。
-   材質-space 輸入：這個參數代表特定輸入材質中的目前執行位置。 著色器不應該依賴此值的計算方式。 它應該只使用它來取樣圖元著色器的輸入，如下列程式碼所示：


```C++
Texture2D InputTexture : register(t0);
SamplerState InputSampler : register(s0);

float4 main(
    float4 clipSpaceOutput  : SV_POSITION,
    float4 sceneSpaceOutput : SCENE_POSITION,
    float4 texelSpaceInput0 : TEXCOORD0
    ) : SV_Target
{
    // Samples pixel from ten pixels above current position.

    float2 sampleLocation =
        texelSpaceInput0.xy    // Sample position for the current output pixel.
        + float2(0,-10)        // An offset from which to sample the input, specified in pixels.
        * texelSpaceInput0.zw; // Multiplier that converts pixel offset to sample position offset.

    float4 color = InputTexture.Sample(
        InputSampler,          // Sampler and Texture must match for a given input.
        sampleLocation
        );

    return color;
}
```



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a>將頂點著色器加入至自訂轉換

您可以使用頂點著色器來完成不同于圖元著色器的影像案例。 尤其是，頂點著色器可以藉由轉換構成影像的頂點來執行以幾何為基礎的影像效果。 頂點著色器可以與轉換指定的圖元著色器分開使用或搭配使用。 如果未指定頂點著色器， [Direct2D](./direct2d-portal.md) 會在預設的頂點著色器中替代，以搭配自訂圖元著色器使用。

將頂點著色器加入至自訂轉換的程式，與圖元著色器的程式類似–轉換會實 [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) 介面、建立 GUID，並 (選擇性地) 將常數緩衝區傳遞給著色器。 不過，有幾個重要的額外步驟，對頂點著色器而言是唯一的：

### <a name="creating-a-vertex-buffer"></a>建立頂點緩衝區

依定義的頂點著色器會在傳遞給它的頂點上執行，而不是個別圖元。 若要指定要在其上執行之著色器的頂點，轉換會建立要傳遞給著色器的頂點緩衝區。 頂點緩衝區的版面配置已超出本檔的範圍。 如需詳細資訊，請參閱 [Direct3D 參考](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ，或 [D2DCustomEffects SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) 以取得範例執行。

在記憶體中建立頂點緩衝區之後，轉換會在包含效果的 [**ID2D1EffectCoNtext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)物件上使用 [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer)方法，將該資料傳遞給 GPU。 同樣地，請參閱 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) 以取得範例執行。

如果轉換未指定任何頂點緩衝區， [Direct2D](./direct2d-portal.md) 會傳遞代表矩形影像位置的預設頂點緩衝區。

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a>變更 SetDrawInfo 以利用頂點著色器

如同使用圖元著色器，轉換必須載入並選取要執行的頂點著色器。 為了載入頂點著色器，它會在效果的 Initialize 方法中收到的 [**ID2D1EffectCoNtext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)方法上呼叫 [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader)方法。 若要選取要執行的頂點著色器，它會在轉換的 [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo)方法中收到的 [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo)參數上呼叫 [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) 。 這個方法會接受先前載入之頂點著色器的 GUID，以及 (選擇性地) 先前建立的頂點緩衝區，以供著色器執行。

### <a name="implementing-a-direct2d-vertex-shader"></a>執行 Direct2D 頂點著色器

繪圖轉換可以同時包含圖元著色器和頂點著色器。 如果轉換同時定義圖元著色器和端點著色器，則會直接將頂點著色器的輸出提供給圖元著色器：應用程式可以自訂頂點著色器的傳回簽章，或圖元著色器的參數，只要它們是一致的。

另一方面，如果轉換只包含頂點著色器，並且依賴 [Direct2D](./direct2d-portal.md)的預設傳遞圖元著色器，它必須傳回下列預設輸出：


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



頂點著色器會在著色器的場景空間輸出變數中儲存其頂點轉換的結果。 為了計算剪輯空間輸出和材質空間輸入變數， [Direct2D](./direct2d-portal.md) 會自動在常數緩衝區中提供轉換矩陣：


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};
```



您可以在下面找到範例頂點著色器程式碼，其使用轉換矩陣來計算 [Direct2D](./direct2d-portal.md)預期的正確剪輯和材質空間：


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};

// Default output structure. This can be customized if transform also contains pixel shader.
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};

// The parameter(s) passed to the vertex shader are defined by the vertex buffer's layout
// as specified by the transform. If no vertex buffer is specified, Direct2D passes two
// triangles representing the rectangular image with the following layout:
//
//    float4 outputScenePosition : OUTPUT_SCENE_POSITION;
//
//    The x and y coordinates of the outputScenePosition variable represent the image's
//    position on the screen. The z and w coordinates are used for perspective and
//    depth-buffering.

VSOut GeometryVS(float4 outputScenePosition : OUTPUT_SCENE_POSITION) 
{
    VSOut output;

    // Compute Scene-space output (vertex simply passed-through here). 
    output.sceneSpaceOutput.x = outputScenePosition.x;
    output.sceneSpaceOutput.y = outputScenePosition.y;
    output.sceneSpaceOutput.z = outputScenePosition.z;
    output.sceneSpaceOutput.w = outputScenePosition.w;

    // Generate standard Clip-space output coordinates.
    output.clipSpaceOutput.x = (output.sceneSpaceOutput.x * sceneToOutputX[0]) +
        output.sceneSpaceOutput.w * sceneToOutputX[1];

    output.clipSpaceOutput.y = (output.sceneSpaceOutput.y * sceneToOutputY[0]) + 
        output.sceneSpaceOutput.w * sceneToOutputY[1];

    output.clipSpaceOutput.z = output.sceneSpaceOutput.z;
    output.clipSpaceOutput.w = output.sceneSpaceOutput.w;

    // Generate standard Texel-space input coordinates.
    output.texelSpaceInput0.x = (outputScenePosition.x * sceneToInput0X[0]) + sceneToInput0X[1];
    output.texelSpaceInput0.y = (outputScenePosition.y * sceneToInput0Y[0]) + sceneToInput0Y[1];
    output.texelSpaceInput0.z = sceneToInput0X[0];
    output.texelSpaceInput0.w = sceneToInput0Y[0];

    return output;  
}
```



上述程式碼可以當做頂點著色器的起點使用。 它只會通過輸入影像，而不會執行任何轉換。 同樣地，請參閱 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) ，以取得完全實作為頂點著色器的轉換。

如果轉換未指定任何頂點緩衝區， [Direct2D](./direct2d-portal.md) 會在代表矩形影像位置的預設頂點緩衝區中替代。 頂點著色器的參數會變更為預設著色器輸出的參數：


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



頂點著色器可能不會修改其 *sceneSpaceOutput* 和 *clipSpaceOutput* 參數。 它必須原封不動地傳回。 不過，它可能會針對每個輸入影像修改 (s) 的 *texelSpaceInput* 參數。 如果轉換也包含自訂圖元著色器，則端點著色器仍能將額外的自訂參數直接傳遞給圖元著色器。 此外， *sceneSpace* 轉換會將自訂緩衝區 (B0) 不再提供。

## <a name="adding-a-compute-shader-to-a-custom-transform"></a>將計算著色器新增至自訂轉換

最後，自訂轉換可能會利用特定案例的計算著色器。 計算著色器可以用來執行需要對輸入和輸出影像緩衝區有任意存取權的複雜影像效果。 例如，基本的長條圖演算法因為記憶體存取限制，而無法使用圖元著色器來執行。

由於計算著色器的硬體功能層級需求高於圖元著色器，因此應該盡可能使用圖元著色器來執行指定的效果。 具體而言，計算著色器只會在大部分的 DirectX 10 層級卡片和更高版本上執行。 如果轉換選擇使用計算著色器，則在具現化期間，除了執行 [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) 介面之外，還必須檢查是否有適當的硬體支援。

### <a name="checking-for-compute-shader-support"></a>檢查計算著色器支援

如果效果使用計算著色器，則必須在建立時使用 [**ID2D1EffectCoNtext：： CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) 方法檢查計算著色器支援。 如果 GPU 不支援計算著色器，則效果必須傳回 [**D2DERR 的 \_ \_ 裝置 \_ 功能不足**](direct2d-error-codes.md)。

轉換可以使用的計算著色器有兩種不同的類型：著色器模型 4 (DirectX 10) 和著色器模型 5 (DirectX 11) 。 著色器模型4著色器有某些限制。 請參閱 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 檔以取得詳細資料。 轉換可以包含這兩種著色器，並可在需要時切換回著色器模型4：請參閱 [D2DCUSTOMEFFECTS SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) 以取得此的執行。

### <a name="implement-id2d1computetransform"></a>執行 ID2D1ComputeTransform

此介面包含兩個新的方法，可在 [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))中執行：

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a>SetComputeInfo (ID2D1ComputeInfo \* pComputeInfo) 

如同使用圖元和頂點著色器， [Direct2D](./direct2d-portal.md) 會在第一次將轉換新增至效果的轉換圖表時呼叫 [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) 方法。 這個方法會提供 [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) 參數，以控制轉換的呈現方式。 這包括透過 [**ID2D1ComputeInfo：： SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) 方法選擇要執行的計算著色器。 如果轉換選擇將此參數儲存為類別成員變數，則可以從任何轉換或效果方法存取和變更，但 [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) 和 [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) 方法除外。 如需其他可用的方法，請參閱 **ID2D1ComputeInfo** 主題。

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a>CalculateThreadgroups (ID2D1ComputeInfo \* pOutputRect、uint32 \* PDIMENSIONX、uint32 \* pDimensionY、uint32 \* pDimensionZ) 

雖然圖元著色器是以每個圖元為基礎執行，而且頂點著色器會以每個頂點為基礎執行，但是計算著色器會以每個 'threadgroup 的為基礎執行。 Threadgroup 代表在 GPU 上同時執行的執行緒數目。 計算著色器 HLSL 程式碼會決定每個 threadgroup 應執行多少執行緒。 效果會根據著色器的邏輯，調整 threadgroups 數目，讓著色器執行所需的次數。

[**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups)方法可讓轉換根據影像大小和轉換專屬的著色器知識，告知 [Direct2D](./direct2d-portal.md)需要多少執行緒群組。

計算著色器執行的次數是此處指定的 threadgroup 計數產品，以及計算著色器 [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)中的 ' numthreads ' 注釋。 例如，如果轉換將 threadgroup 維度設定為 (2，2，1) 著色器會為每個 threadgroup 指定 (3，3，1) 執行緒，然後執行 4 threadgroups，其中每個都有9個執行緒，總共36個執行緒實例。

常見的案例是針對計算著色器的每個實例處理一個輸出圖元。 若要計算此案例的執行緒群組數目，轉換會將影像的寬度和高度除以 [計算著色器] [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)中的 [numthreads] 注釋的個別 x 和 y 維度。

重要的是，如果執行此除法，則要求的執行緒群組數目必須一律無條件進位到最接近的整數，否則就不會執行「餘數」圖元。 如果著色器 (例如) 計算每個執行緒的單一圖元，則方法的程式碼會如下所示。


```C++
IFACEMETHODIMP SampleTransform::CalculateThreadgroups(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_ UINT32* pDimensionX,
    _Out_ UINT32* pDimensionY,
    _Out_ UINT32* pDimensionZ
    )
{    
    // The input image's dimensions are divided by the corresponding number of threads in each
    // threadgroup. This is specified in the HLSL, and in this example is 24 for both the x and y
    // dimensions. Dividing the image dimensions by these values calculates the number of
    // thread groups that need to be executed.

    *pDimensionX = static_cast<UINT32>(
         ceil((m_inputRect.right - m_inputRect.left) / 24.0f);

    *pDimensionY = static_cast<UINT32>(
         ceil((m_inputRect.bottom - m_inputRect.top) / 24.0f);

    // The z dimension is set to '1' in this example because the shader will
    // only be executed once for each pixel in the two-dimensional input image.
    // This value can be increased to perform additional executions for a given
    // input position.
    *pDimensionZ = 1;

    return S_OK;
}
```



[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)會使用下列程式碼來指定每個執行緒群組中的執行緒數目：


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



在執行期間，會將目前的 threadgroup 和目前的執行緒索引作為參數傳遞給著色器方法：


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in ID2D1ComputeTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
...
```



### <a name="reading-image-data"></a>讀取影像資料

計算著色器會以單一二維材質存取轉換的輸入影像：


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



不過，就像圖元著色器一樣，不保證影像的資料會在材質 (0、0) 開始。 相反地， [Direct2D](./direct2d-portal.md) 會提供可讓著色器彌補任何位移的系統常數：


```hlsl
// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the input rectangle to the shader in terms of pixels.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}
```



一旦定義上述常數緩衝區和 helper 方法之後，著色器就可以使用下列程式來取樣影像資料：


```hlsl
float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by input image offset.
            ),
        0
        );
```



### <a name="writing-image-data"></a>寫入影像資料

[Direct2D](./direct2d-portal.md) 預期著色器會定義要放置結果影像的輸出緩衝區。 在著色器模型 4 (DirectX 10) 中，由於功能條件約束，這必須是一維緩衝區：


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



輸出材質會先編制資料列索引，以允許儲存整個影像。


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



另一方面，著色器模型 5 (DirectX 11) 著色器可以使用二維輸出紋理：


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



在著色器模型5著色器中， [Direct2D](./direct2d-portal.md) 會在常數緩衝區中提供額外的 ' outputOffset ' 參數。 著色器的輸出應以此數量 offsetted：


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



完成的傳遞著色器模型5計算著色器如下所示。 在其中，每個計算著色器執行緒都會讀取並寫入輸入影像的單一圖元。


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

RWTexture2D<float4> OutputTexture : register(t1);

// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    int2 outputOffset;
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 5, z <= 64 and x*y*z <= 1024
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    uint imageWidth = resultRect.z - resultRect.x;
    uint imageHeight = resultRect.w - resultRect.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is
    // executed in chunks sized by the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups.
    // For this reason each shader should ensure the current dispatchThreadId is within the bounds of the input
    // image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



下列程式碼顯示對應的著色器模型4版本著色器。 請注意，著色器現在會轉譯成一維輸出緩衝區。


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

// Shader Model 4 does not support RWTexture2D, must use one-dimensional buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);

// These are default constants passed by D2D. See PixelShader and VertexShader
// projects for how to pass custom values into a shader.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y, groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint imageWidth = resultRect[2] - resultRect[0];
    uint imageHeight = resultRect[3] - resultRect[1];

    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is executed in chunks sized by
    // the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups. For this reason each shader should ensure the current
    // dispatchThreadId is within the bounds of the input image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[yIndex * imageWidth + xIndex] = color;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[D2DCustomEffects SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 