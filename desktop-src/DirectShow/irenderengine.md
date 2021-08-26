---
description: IRenderEngine 介面會從時間軸建立篩選圖形，以轉譯 DirectShow 編輯服務 (DES) 專案。DES 提供兩個可執行此介面的元件：基本轉譯引擎會建立未壓縮的輸出。
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: 'IRenderEngine 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a13d51eb41a917dc4790c75a8a1f8a881dbcb8489364722ff8805bdf26fc77f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051308"
---
# <a name="irenderengine-interface"></a>IRenderEngine 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IRenderEngine`介面會從時間軸建立篩選圖形，以轉譯[DirectShow 編輯服務](directshow-editing-services.md) (DES) 專案。

DES 提供兩個可執行此介面的元件：

-   *基本轉譯引擎* 會建立未壓縮的輸出。 您可以使用預覽的輸出，或透過壓縮篩選將其傳送至檔案，並將其寫入檔案。
-   *智慧型轉譯引擎* 會使用 *智慧型 recompression* 來建立壓縮的輸出。 使用智慧型 recompression 時，只有當原始程式檔的格式與輸出格式不同時，才會 recompressed 原始程式檔。 具有相符格式的來源會直接寫入輸出檔。 根據案例而定，智慧型 recompression 可以大幅改善轉譯時間。

智慧型轉譯引擎也支援 [**ISmartRenderEngine**](ismartrenderengine.md) 介面。

雖然應用程式可以建立篩選圖形並將它傳遞至轉譯引擎，但一般案例是讓轉譯引擎建立篩選圖形。 建立圖形是兩階段的流程。 首先，藉由呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 方法來建立前端。 然後將前端的輸出接點連接到所需的轉譯篩選準則：

-   適用于預覽的影片和音訊轉譯器，或
-   壓縮機、multiplexers 和 file 寫入器，以產生最終輸出。

## <a name="members"></a>成員

**IRenderEngine** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IRenderEngine** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IRenderEngine** 介面具有這些方法。



| 方法                                                                             | 描述                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**提交**](irenderengine-commit.md)                                             | 未實作。<br/>                                                           |
| [**ConnectFrontEnd**](irenderengine-connectfrontend.md)                           | 從目前的時間軸建立篩選圖形的前端。<br/>        |
| [**取消認可**](irenderengine-decommit.md)                                         | 未實作。<br/>                                                           |
| [**DoSmartRecompression**](irenderengine-dosmartrecompression.md)                 | 不支援。<br/>                                                             |
| [**GetCaps**](irenderengine-getcaps.md)                                           | 未實作。<br/>                                                           |
| [**GetFilterGraph**](irenderengine-getfiltergraph.md)                             | 抓取轉譯引擎已建立的篩選圖形（如果有的話）。<br/> |
| [**GetGroupOutputPin**](irenderengine-getgroupoutputpin.md)                       | 抓取指定群組的輸出圖釘。<br/>                          |
| [**GetTimelineObject**](irenderengine-gettimelineobject.md)                       | 抓取轉譯引擎目前使用的時間軸。<br/>          |
| [**GetVendorString**](irenderengine-getvendorstring.md)                           | 捕獲廠商字串。<br/>                                               |
| [**RenderOutputPins**](irenderengine-renderoutputpins.md)                         | 建立篩選圖形的預覽部分。<br/>                        |
| [**ScrapIt**](irenderengine-scrapit.md)                                           | 捨棄轉譯引擎的篩選圖形以及所有相關聯的物件。<br/>      |
| [**SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)         | 設定轉譯期間的動態重新連接層級。<br/>                   |
| [**SetFilterGraph**](irenderengine-setfiltergraph.md)                             | 指定要用於轉譯引擎的篩選圖形。<br/>                     |
| [**SetInterestRange**](irenderengine-setinterestrange.md)                         | 不支援。<br/>                                                             |
| [**SetInterestRange2**](irenderengine-setinterestrange2.md)                       | 不支援。<br/>                                                             |
| [**SetRenderRange**](irenderengine-setrenderrange.md)                             | 設定要轉譯的時間範圍。<br/>                                     |
| [**SetRenderRange2**](irenderengine-setrenderrange2.md)                           | 設定要轉譯的時間範圍，以 **雙精度浮點數**。<br/>                    |
| [**SetSourceConnectCallback**](irenderengine-setsourceconnectcallback.md)         | 不支援。<br/>                                                             |
| [**SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)           | 指定轉譯引擎如何驗證檔案名。<br/>                      |
| [**SetTimelineObject**](irenderengine-settimelineobject.md)                       | 設定要使用之轉譯引擎的時間軸。<br/>                            |
| [**UseInSmartRecompressionGraph**](irenderengine-useinsmartrecompressiongraph.md) | 不支援。<br/>                                                             |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[轉譯 Project](rendering-a-project.md)
</dt> </dl>

 

 
