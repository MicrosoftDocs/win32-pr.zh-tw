---
description: 指定語音捕獲 DSP 所使用的音訊框架大小。
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: 'MFPKEY_WMAAECMA_FEATR_FRAME_SIZE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812a9c7b85a36b730caffe7679cc742a3bc029546a12839afd95a8c8ab58bfeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973287"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ FRAME \_ SIZE 屬性

指定語音捕獲 DSP 所使用的音訊框架大小。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

聲場 echo 取消 (AEC) 演算法一次處理一個畫面格的 PCM 音訊範例。 這個屬性的值是音訊框架的大小（在範例中）。 設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。

語音捕獲 DSP 支援下列畫面格大小：

-   80
-   128
-   160
-   240
-   256
-   320

如果這個屬性的值為零，則 DSP 會根據系統模式和輸出格式來選取框架大小。

但為了達到最佳效能，建議應用程式使用預設值。 如果處理模式僅為麥克風陣列，則預設值為320範例。 針對所有其他處理模式，預設值為160範例。 如需語音捕獲 DSP 處理模式的詳細資訊，請參閱 [MFPKEY \_ WMAAECMA \_ 系統 \_ 模式](mfpkey-wmaaecma-system-modeproperty.md)。

第一次呼叫 [**IMediaObject：： AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) 或 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)之後，您就可以讀取此屬性來取得實際使用的框架大小，即使 [**MFPKEY \_ WMAAECMA \_ 功能 \_ 模式**](mfpkey-wmaaecma-feature-modeproperty.md) 為 false 也是如此。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[語音捕獲 DSP](voicecapturedmo.md)
</dt> </dl>

 

 
