---
description: Windows可攜式裝置支援下列影像屬性。
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: '影像屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 0d2ebe552a66dadf6b9bec6a0a741d85e1c7f1f018ef108e36ec1bb3cb4b6165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430757"
---
# <a name="image-properties"></a>影像屬性

Windows可攜式裝置支援下列影像屬性。



| 屬性                                                                                                                                       | VarType     | 描述                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 影像 \_ BITDEPTH**                                                                                                                       | **VT \_ UI4** | 影像的位深度。                                                                                                                                                                                                                                                                                                                     |
| <span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**WPD \_ 影像 \_ 色彩已 \_ 更正 \_ 狀態** | **VT \_ UI4** | [**WPD \_ 色彩更正 \_ 的 \_ 狀態值 \_**](wpd-color-corrected-status-values.md)列舉，指定檔案是否已進行色彩更正。這可防止多個裝置在進行後置處理時自動對影像進行色彩校正。<br/>                                                                       |
| **WPD \_ 影像 \_ 裁剪 \_ 狀態**                                                                                                                | **VT \_ UI4** | [**WPD \_ 裁剪的 \_ 狀態值 \_**](wpd-cropped-status-values.md)列舉，這個值會指定檔案是否已裁剪。這可防止多個裝置在後續處理期間自動裁剪影像。<br/>                                                                                                        |
| **WPD \_ 影像 \_ 曝光 \_ 索引**                                                                                                                | **VT \_ UI4** | 值，這個值會識別在捕獲此映射時的電影速度設定。這些設定會對應至 ASA/等的 ISO 指派。<br/> 通常，裝置支援離散列舉值，但可能會持續控制範圍。<br/> 0xFFFFFFFF 的值對應到自動 ISO 設定。<br/> |
| **WPD \_ 影像 \_ 曝光 \_ 時間**                                                                                                                 | **VT \_ UI4** | 識別在捕獲此映射時裝置的快門速度。單位以秒為單位，以10000來調整。<br/>                                                                                                                                                                                                                        |
| **WPD \_ 影像 \_ FNUMBER**                                                                                                                        | **VT \_ UI4** | 識別在捕獲此影像時的鏡頭光圈設定。單位等於以100調整的 f 數位。<br/>                                                                                                                                                                                                              |
| **WPD \_ 影像 \_ 水準 \_ 解析度**                                                                                                         | **VT \_ R8**  | 指出影像的水準解析度，以每英寸的點為單位， (DPI) 。                                                                                                                                                                                                                                                                       |
| **WPD \_ 影像 \_ 垂直 \_ 解析度**                                                                                                           | **VT \_ R8**  | 指出影像的垂直解析度（以每英寸的點為單位）， (DPI) 。                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




