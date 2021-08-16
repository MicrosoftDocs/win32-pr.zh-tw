---
description: 強制編碼器將下一個畫面格編碼為主要畫面格。
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: 'CODECAPI_AVEncVideoForceKeyFrame 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e28738dcd7398ce04abe7f71778e94d7d5d4f49393365e92c43bbb347d98c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880704"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>CODECAPI \_ AVEncVideoForceKeyFrame 屬性

強制編碼器將下一個畫面格編碼為主要畫面格。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoForceKeyFrame**

## <a name="property-value"></a>屬性值

如果此值為非零值，則編碼器會將下一個畫面格編碼為主要畫面格。 如果值為零，則編碼器會選取是否要將下一個框架編碼為主要畫面格。

這個屬性會套用至編碼器接收為輸入的下一個畫面格。 針對媒體基礎轉換 (MFT) ，這是傳遞至 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 方法的下一個畫面格。 在下一個畫面格之後，此設定會重設為零。

## <a name="remarks"></a>備註

這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](camera-encoder-h264-uvc-1-5.md)一起使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

