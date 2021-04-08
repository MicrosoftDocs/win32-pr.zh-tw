---
title: 執行 DSP 外掛程式的屬性頁
description: 執行 DSP 外掛程式的屬性頁
ms.assetid: 3dd3e547-fd06-4f01-8731-da1f8c958a32
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，音訊屬性
- DSP 外掛程式、音訊屬性
- 音訊 DSP 外掛程式，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec87318b77fec4e9218398c1cb43dd5954a49e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839683"
---
# <a name="implementing-the-property-page-for-a-dsp-plug-in"></a>執行 DSP 外掛程式的屬性頁

Windows Media Player 可以顯示每個 DSP 外掛程式的屬性頁，讓使用者設定變更外掛程式行為的值。 使用者可以從 [選項] 對話方塊的 [ **外掛程式** ] 索引標籤中 **，按一下要** 選取的 DSP 外掛程式名稱，然後按一下 [內容]，以存取此屬性頁。

Windows Media Player 外掛程式 Wizard 範例程式碼提供屬性頁的預設實作為，其中包含單一編輯方塊，可從使用者接收代表音訊音量比例因數的值。 當使用者按一下 [套用] 時，屬性頁面會將此值傳遞至外掛程式 **物件，讓** 外掛程式可以變更在處理期間用來調整磁片區的值。

## <a name="about-the-property-page-object"></a>關於屬性頁物件

屬性頁物件是可實 **IPropertyPage** 介面的 COM 物件。 外掛程式 wizard 所產生的範例程式碼會使用 **IPropertyPage** 的 ATL 執行，其記載于 MSDN 上的 Visual C++ 檔中。 您的程式碼至少應該提供 **IPropertyPage：： OnInitDialog** 的覆寫執行，它會處理在屬性頁開啟時所發生的事件，以及 **IPropertyPage：： Apply**（可處理 **使用者按一下 [** 套用] 時所發生的事件）。 外掛程式 wizard 會產生每個事件處理常式的範例程式碼。 **OnInitDialog** 的範例會從登錄抓取值，讓它可以顯示目前的縮放比例設定。 **Apply** 的範例執行會透過測試來驗證使用者輸入，以確保它落在指定的範圍內，然後將值保存到登錄中，然後將值傳遞 (如果 DSP 外掛程式屬性 put 方法的有效) （名為 **put \_ scale**）。

此外，您還需要新增程式碼來處理使用者變更您在屬性頁中提供的控制項值時所發生的事件。 例如，外掛程式 wizard 會執行名為 **OnChangeScale** 的函式，此函式只會在使用者變更屬性頁面上編輯方塊中的文字時，藉由呼叫 **SetDirty** 方法，並將引數值 **設為 TRUE**，就能 **啟用 [套用**] 按鈕。

## <a name="about-the-property-page-dialog-resource"></a>關於屬性頁對話方塊資源

屬性頁的使用者介面會儲存為對話方塊資源。 您可以藉由在 [專案工作區] 視窗中選取 [ **ResourceView** ] 索引標籤，然後開啟 **對話方塊** 資料夾，再按兩下屬性頁資源名稱，輕鬆地在 Visual Studio 中查看及編輯 [屬性頁] 對話方塊。 Visual Studio 中的對話方塊資源編輯器提供您所需的工具，以將控制項加入至 [屬性頁] 對話方塊，並建立對應至適當 Windows 訊息的事件處理常式。 如需有關如何在 Visual Studio 中使用資源編輯器的詳細資訊，請參閱 Visual Studio 說明。

## <a name="about-ispecifypropertypages"></a>關於 ISpecifyPropertyPages

如果 DSP 外掛程式提供屬性頁，外掛程式必須執行 **ISpecifyPropertyPages** 介面。 這個介面只包含一個方法： **ISpecifyPropertyPages：： GetPages**。 這是將屬性頁面與 DSP 外掛程式產生關聯的方法。 Windows Media Player 會在使用者叫用屬性頁時呼叫這個方法，傳遞 CAUUID 類型的參數，也就是 Guid 的計數陣列。 **GetPages** 的範例外掛程式會以單一 GUID （即外掛程式屬性頁物件的類別識別碼）填滿此結構。 Windows Media Player 接著會使用類別識別碼來建立屬性頁物件。

您可能會注意到， **GetPages** 的範例會使用 **COTASKMEMALLOC** 來配置 GUID 結構的記憶體。 呼叫者（在此案例中 Windows Media Player）的責任是使用 **CoTaskMemFree** 來釋放記憶體。 如需 CAUUID 結構的詳細資訊，請參閱 Platform SDK 檔。

## <a name="about-the-proxystub-dll"></a>關於 Proxy/Stub DLL

若要讓 DSP 外掛程式在 Windows Vista 上執行的 Windows Media Player 11 中運作，您必須為自訂介面提供 proxy/stub DLL，以用於將設定中的變更從 [屬性頁] 對話方塊傳達給外掛程式類別。 透過這類介面所進行的方法呼叫，必須在跨進程或單元界限進行呼叫時封送處理。 最新版的外掛程式 wizard 會建立範例 proxy/存根 DLL 專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行音訊 DSP 外掛程式**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




