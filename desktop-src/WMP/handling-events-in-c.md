---
title: 在 c + + 中處理事件
description: 在 c + + 中處理事件
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player，c + +
- Windows Media Player 物件模型，c + +
- 物件模型，c + +
- Windows Media Player Mobile，c + +
- Windows Media Player 的 ActiveX 控制項，c + +
- Windows Media Player 的行動 ActiveX 控制項，c + +
- ActiveX 控制項，c + +
- C + + 程式內嵌
- 內嵌，c + + 程式
- Windows Media Player 的 ActiveX 控制項，事件處理
- Windows Media Player 的行動 ActiveX 控制項、事件處理
- ActiveX 控制項，事件處理
- 事件，c + +
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092285"
---
# <a name="handling-events-in-c"></a>在 c + + 中處理事件

您可以透過兩種方式接收來自 Windows Media Player 的事件。

-   透過 **IDispatch** ，使用 **\_ WMPOCXEvents** 介面。 這是在大部分內嵌案例中使用的介面。
-   透過 **IWMPEvents** 介面。 當您的程式碼連接至完整模式播放程式時（例如，在遠端處理 Windows Media Player 控制項或 UI 外掛程式時），就可以使用此介面。

在每個案例中，您可以使用 COM 連接點開始接聽事件。

下列範例程式碼會使用三個成員變數：


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



若要取出連接點，您必須先使用連接點容器的 **QueryInterface** 。


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



接著，要求您要使用之事件介面的連接點。 下列範例程式碼會先嘗試使用 **IWMPEvents**。 如果該介面無法使用，則會使用 **\_ WMPOCXEvents**。


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



最後，呼叫 **IConnectionPoint：： Advise** 來要求事件。


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



在上述範例中，第一個參數會假設呼叫的類別會同時執行 **IWMPEvents** 和 **\_ WMPOCXEvents**。 第二個參數是用來停止接聽事件的傳回值，例如當程式結束時，使用類似下列的程式碼：


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



執行 **IWMPEvents** 和 **\_ WMPOCXEvents** 的事件處理常式會有所不同。 針對 **IWMPEvents**，您必須執行函式來處理介面所定義的每個事件，即使您不打算使用事件也一樣。


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



若要執行 **\_ WMPOCXEvents** 處理常式，您必須使用 **idispatch：： Invoke**，此為 **idispatch** 介面上發生之所有事件的單一事件處理常式執行。 這表示您可以選擇只處理特定事件並忽略其他事件。 下列範例程式碼示範使用 **Invoke** 的 **\_ WMPOCXEvents** 處理常式，它只會處理 **OpenStateChange** 和 **PlayStateChange** 事件：


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



在上述的範例程式碼中，每個案例只會呼叫對應事件的 **IWMPEvents** 處理常式。 如果您的程式碼只會處理 **\_ WMPOCXEvents**，您可以直接呼叫自訂函式，或處理 **case** 語句之後的內嵌事件。

## <a name="receiving-events-from-windows-media-player-10-mobile"></a>從 Windows Media Player 10 行動裝置接收事件

Windows Media Player 10 行動裝置控制項僅支援透過 **\_ WMPOCXEvents** 和 **IWMPEvents** 接收特定事件。 如需詳細資訊，請參閱 **IWMPEvents** 的檔。

## <a name="samples"></a>範例

Windows Media Player 安裝套件會安裝示範事件處理的範例。 如需詳細資訊，請參閱 WMPHost 範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**範例**](samples.md)
</dt> <dt>

[**在 c + + 程式中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




