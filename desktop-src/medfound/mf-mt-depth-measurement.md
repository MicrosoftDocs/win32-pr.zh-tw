---
description: 值，定義影片畫面中深度值的測量系統。
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: 'MF_MT_DEPTH_MEASUREMENT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563918"
---
# <a name="mf_mt_depth_measurement-attribute"></a>MF \_ MT \_ 深度 \_ 度量屬性

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

值，定義影片畫面中深度值的測量系統。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個值是 [**\_ MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)列舉的成員

如果這個屬性不存在，則會假設為 **DistanceToFocalPlane**。 在 3D Euclidian 座標系統中，通常會更容易使用焦點平面的距離。

![distancetofocalplane 的圖例](images/distance-to-focal-plane.png)

與焦距中心格式的距離通常是來自感應器的原始資料，例如飛行攝影機的時間。

![distancetoopticalcenter 的圖例](images/distance-to-optical-center.png)

深度相機無法理解所有圖元的深度。 當圖元的信賴度很低時（因為材質、遮蔽或超出範圍等），該圖元的深度值可能會無效。

當深度圖元值為0時，圖元就會無效。

有些深度相機會附加每個圖元的位元遮罩中繼資料（除了 depth 值），以代表圖元深度不正確原因，因為材質、遮蔽或超出範圍等等。建議您避免將這類中繼資料附加為深度值的位，因為在圖元著色器中使用這類值時，通常會造成困難。 相反。 建議您使用具有相同解析度的個別8位映射緩衝區，並將其附加為 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)的屬性。 這類中繼資料會因每個相機廠商而異，且不會由平臺進行標準化。 我們建議使用完整的16個位來取得深度值，以便更輕鬆地處理下游，並使用固定值（例如0）進行失效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                      |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 




