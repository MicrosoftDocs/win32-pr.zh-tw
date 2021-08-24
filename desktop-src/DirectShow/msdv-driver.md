---
description: MSDV 驅動程式
ms.assetid: 146ca753-fe41-49d3-8b1c-077e10a28192
title: MSDV 驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5377471f61944c60f57720df6bc64482681d64515f54c853d78cfa405842ff15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748614"
---
# <a name="msdv-driver"></a>MSDV 驅動程式

MSDV 是適用于 DV 攝影機的 Microsoft Windows Driver Model (WDM) 驅動程式。 當裝置插入電源時，驅動程式會顯示為 DirectShow 的篩選準則。 它是以兩個篩選準則分類來列舉：

-   CLSID \_ VideoInputDeviceCategory ( 「影片捕獲來源」 ) 
-   \_KSCATEGORY 轉譯 \_ ( 「WDM 串流轉譯裝置」 ) 

篩選的易記名稱是 `Microsoft DV Camera and VCR` 或當地語系化的對等專案。 在某些裝置中， **description** 屬性包含特定模型的描述，可用來取代一般的易記名稱。 如需詳細資訊，請參閱 [選取擷取裝置](selecting-a-capture-device.md)。

MSDV 有兩個輸出圖釘。 一個 pin 會提供包含交錯音訊和影片資料的 DV 框架。 另一個 pin 提供僅限影片的框架，沒有音訊。 MSDV 無法同時從這兩個 pin 進行串流，所以一次只能連接一個輸出圖釘。 如需從 DV 裝置捕獲影片的詳細資訊，請參閱 [將 dv 帶到](capture-dv-to-file.md)檔案。

![從裝置捕獲 dv 資料](images/dv-filters4.png)

大部分的 DV 攝影機都有影片磁帶錄製器 (VTR) 的次級，可將資料從磁帶傳輸到電腦。 針對應用程式，從磁帶進行捕捉的運作方式與捕捉即時影片相同。 唯一的差別在於應用程式必須控制外部磁帶傳輸—啟動和停止磁帶、倒轉等等。 基於這個目的，MSDV 會公開 [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)、 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)和 [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) 介面。 如需控制 VTR 的詳細資訊，請參閱 [控制 DV 攝像機](controlling-a-dv-camcorder.md)。

您也可以從電腦傳輸 DV 到攝像機。 然後可以在攝像機的上架畫面中查看影片，或記錄到磁帶上。 為了支援此功能，MSDV 具有可接收交錯 DV 串流的輸入 pin。 當輸入連接連接時，MSDV 會作為轉譯器篩選器，而不是「捕捉」篩選。 MSDV 不支援在此模式中進行搜尋。 如需將 DV 傳送至裝置的詳細資訊，請參閱 [從檔案傳輸 dv 至磁帶](transmit-dv-from-file-to-tape.md)。

![將 dv 資料傳輸至裝置](images/dv-filters5.png)

請注意，輸入和輸出 pin 無法同時連線，因為裝置無法同時以雙向方式進行串流。

在許多攝影機中，在 VTR 模式和攝影機模式之間切換，會導致裝置關閉。 因此，當使用者切換模式時，DirectShow 可能會遺失裝置。 如需裝置移除事件的詳細資訊，請參閱 [裝置移除通知](device-removal-notification.md)。

## <a name="remarks"></a>備註

如需 MSDV 驅動程式所支援之 DV 格式的相關資訊，請參閱 [**DV 影片子類型**](dv-video-subtypes.md)。

使用 MSDV 建立篩選圖形的一些秘訣：

-   您無法使用 [**IGraphBuilder：： render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 在 MSDV 上轉譯輸出圖釘。  (篩選 Graph 管理員嘗試將輸出連接連接至 MSDV 的輸入 pin 失敗。 ) 改為使用 [**IGraphBuilder：：連線**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)或 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)。
-   當篩選圖形包含 MSDV 時，MSDV 應該提供圖形的參考時鐘。 從 DirectX 8.0，篩選 Graph 管理員會自動選擇 MSDV 做為參考時鐘。 使用較舊的版本時，您應該在篩選 Graph 管理員上呼叫 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)方法。 如需有關時鐘的詳細資訊，請參閱[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。
-   視裝置而定， **IAMExtDevice**、 **IAMExtTransport** 和 **IAMTimeCodeReader** 中的某些方法可能會傳回 Windows 錯誤碼，而不是 **HRESULT** 值。 可能的錯誤代碼包括下列各項。

    | 錯誤碼              | 描述                                                                                      |
    |-------------------------|--------------------------------------------------------------------------------------------------|
    | 錯誤 \_ 超時          | 外部裝置命令已超時。                                                        |
    | 錯誤 \_ 需求 \_ 未 \_ ACCEP  | 裝置未接受此外部裝置命令。                                          |
    | \_不 \_ 支援的錯誤   | 裝置不支援此外部裝置命令。                                        |
    | 錯誤 \_ 要求已 \_ 中止 | 外部裝置命令已中止。 可能是裝置已移除或發生匯流排重設。 |

    

     

### <a name="device-information"></a>裝置資訊

在 Windows Millennium Edition 和 Windows XP 中，DV 篩選器的裝置標記除了 **FriendlyName** 屬性之外，還支援 **Description** 屬性。 這個屬性會傳回從 INF 檔案取得之裝置的描述，其中通常包含裝置的品牌名稱。 但是，並非所有裝置型號都支援此屬性。

如需裝置名字標記的詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。

### <a name="clock-times"></a>時鐘時間

MSDV 驅動程式會使用1394資料封包中包含的1394匯流排時鐘來衍生時鐘。 它會使用這些值，以時間戳記 DV 媒體範例。 由於此來源時鐘不是電腦系統時鐘，因此時間最後會與電腦系統時鐘漂移。 不過，如先前所述，根據預設，篩選 Graph 管理員會將 MSDV 選取為圖形參考時鐘。

[**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)介面會報告驅動程式目前的已卸載框架量值;在指定的時間內，此值可能不會與實際的已捨棄框架數目完全同步處理。 如果已卸載框架，表示系統未平衡 (資料生產量超過) 的資料耗用量。 例如，使用者的硬碟可能不夠快，無法支援 DV 捕捉率。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> </dl>

 

 



