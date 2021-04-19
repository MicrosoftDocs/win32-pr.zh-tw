---
description: 調整影片資料流程的大小。
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: " (Wmcodecdsp 的影片尺寸調整) "
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971688"
---
# <a name="video-resizer-dsp"></a>影片尺寸調整 DSP

調整影片資料流程的大小。

## <a name="clsid"></a>CLSID

CLSID \_ CResizerDMO

## <a name="interfaces"></a>介面

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResizerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a>格式

影片調整器 DSP 在作為 DirectX 媒體物件時，支援下列輸入/輸出媒體子類型 (的) 。

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ AYUV
-   MEDIASUBTYPE \_ V216
-   MEDIASUBTYPE \_ YV12

影片調整器 DSP 支援下列輸入/輸出媒體子類型作為媒體基礎轉換 (MFT) 。

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ AYUV
-   MFVideoFormat \_ V216
-   MFVideoFormat \_ YV12

## <a name="properties"></a>屬性

-   [MFPKEY \_ 調整 \_ SRC \_ 左方](mfpkey-resize-src-left.md)
-   [MFPKEY \_ 調整 \_ SRC \_ TOP](mfpkey-resize-src-top.md)
-   [MFPKEY \_ 調整 \_ SRC \_ 寬度](mfpkey-resize-src-width.md)
-   [MFPKEY \_ 調整 \_ SRC \_ 高度大小](mfpkey-resize-src-height.md)
-   [MFPKEY \_ 將 \_ DST \_ 左大小調整](mfpkey-resize-dst-left.md)
-   [MFPKEY \_ 調整 \_ DST \_ 頂端](mfpkey-resize-dst-top.md)
-   [MFPKEY \_ 調整 \_ DST \_ 寬度](mfpkey-resize-dst-width.md)
-   [MFPKEY \_ 調整 \_ DST \_ 高度](mfpkey-resize-dst-height.md)
-   [MFPKEY \_ 調整 \_ 品質](mfpkey-resize-quality.md)
-   [MFPKEY 重 \_ 設大小 \_ 交錯](mfpkey-resize-interlace.md)
-   [MFPKEY 重 \_ 設大小 \_ GEOMAPX](mfpkey-resize-geomapx.md)
-   [MFPKEY 重 \_ 設大小 \_ GEOMAPY](mfpkey-resize-geomapy.md)
-   [MFPKEY 重 \_ 設大小 \_ GEOMAPWIDTH](mfpkey-resize-geomapwidth.md)
-   [MFPKEY 重 \_ 設大小 \_ GEOMAPHEIGHT](mfpkey-resize-geomapheight.md)
-   [MFPKEY 重 \_ 設大小 \_ MINAPX](mfpkey-resize-minapx.md)
-   [MFPKEY 重 \_ 設大小 \_ MINAPY](mfpkey-resize-minapy.md)
-   [MFPKEY 重 \_ 設大小 \_ MINAPWIDTH](mfpkey-resize-minapwidth.md)
-   [MFPKEY 重 \_ 設大小 \_ MINAPHEIGHT](mfpkey-resize-minapheight.md)
-   [MFPKEY 重 \_ 設大小 \_ PANSCANAPX](mfpkey-resize-panscanapx.md)
-   [MFPKEY 重 \_ 設大小 \_ PANSCANAPY](mfpkey-resize-panscanapy.md)
-   [MFPKEY 重 \_ 設大小 \_ PANSCANAPWIDTH](mfpkey-resize-panscanapwidth.md)
-   [MFPKEY 重 \_ 設大小 \_ PANSCANAPHEIGHT](mfpkey-resize-panscanapheight.md)
-   [MFPKEY \_ PIXELASPECTRATIO](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a>備註

影片調整器 DSP 會實作為可做為 www.contoso.com 或 MFT 的 COM 物件。 此物件具有單一類別識別碼 (CLSID) ，不論它是否可作為一或一個 MFT。 如需有關 DSP 作為一或是 MFT 之時機的詳細資訊，請參閱 [數位訊號處理器](windowsmediadigitalsignalprocessors.md)。

針對 RGB 媒體子類型 (Guid) 的全域唯一識別碼，會根據 DSP 是以 SQL-DMO 或 MFT 的方式而有所不同。 非 RGB 媒體子類型的 Guid 是相同的，不論 DSP 是以 SQL-DMO 或 MFT 作為的。 如需表示媒體子類型之 Guid 的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。

這個 DSP 可以在影片影像上執行裁剪和縮放。 輸出類型的格式必須符合輸入類型的格式。 DSP 不會執行色彩空間轉換。

設定輸出類型之前，您可以使用下表所列的屬性來定義下列任何區域。



| 區域                   | 屬性                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 來源矩形         | MFPKEY \_ 調整 \_ SRC \_ 左方<br/> MFPKEY \_ 調整 \_ SRC \_ TOP<br/> MFPKEY \_ 調整 \_ SRC \_ 寬度<br/> MFPKEY \_ 調整 \_ SRC \_ 高度大小<br/>            |
| 目的地矩形    | MFPKEY \_ 將 \_ DST \_ 左大小調整<br/> MFPKEY \_ 調整 \_ DST \_ 頂端<br/> MFPKEY \_ 調整 \_ DST \_ 寬度<br/> MFPKEY \_ 調整 \_ DST \_ 高度<br/>            |
| 幾何光圈       | MFPKEY 重 \_ 設大小 \_ GEOMAPX<br/> MFPKEY 重 \_ 設大小 \_ GEOMAPY<br/> MFPKEY 重 \_ 設大小 \_ GEOMAPWIDTH<br/> MFPKEY 重 \_ 設大小 \_ GEOMAPHEIGHT<br/>             |
| 最小顯示光圈 | MFPKEY 重 \_ 設大小 \_ MINAPX<br/> MFPKEY 重 \_ 設大小 \_ MINAPY<br/> MFPKEY 重 \_ 設大小 \_ MINAPWIDTH<br/> MFPKEY 重 \_ 設大小 \_ MINAPHEIGHT<br/>                 |
| Pan/掃描區域          | MFPKEY 重 \_ 設大小 \_ PANSCANAPX<br/> MFPKEY 重 \_ 設大小 \_ PANSCANAPY<br/> MFPKEY 重 \_ 設大小 \_ PANSCANAPWIDTH<br/> MFPKEY 重 \_ 設大小 \_ PANSCANAPHEIGHT<br/> |



 

在每個案例中，您必須設定所有相關聯的屬性，設定才會生效。

DSP 會複製來源矩形所定義之來源影像的部分，並將它伸展或壓縮到輸出緩衝區上的目的地矩形。 來源和目的地矩形不需要相同的大小。 輸出媒體類型中的框架大小必須夠大，才能容納目的地矩形。

幾何光圈、最小顯示光圈和平移/掃描區域不會影響 DSP 調整影片的大小。 不過，它們可能會影響下游元件解讀影片框架的方式。 尤其是，增強型影片轉譯器 (EVR) 在計算圖片外觀比例和顯示區域時，會使用這些值。

如果您使用媒體基礎媒體類型，則可以直接在輸出媒體類型中設定幾何光圈、最小顯示光圈和平移/掃描區域。 否則，如果您使用的是 SQL-DMO 媒體類型，請使用屬性進行設定。

如需詳細資訊，請參閱下列主題：

-   [**MF \_ MT \_ 幾何 \_ 光圈**](mf-mt-geometric-aperture-attribute.md)
-   [**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md)
-   [**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vidreszr.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數位訊號處理器](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
