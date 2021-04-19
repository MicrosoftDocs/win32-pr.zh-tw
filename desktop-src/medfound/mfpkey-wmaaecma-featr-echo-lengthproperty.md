---
description: 指定聲場 echo 取消 (AEC) 演算法可以處理的回應持續時間（以毫秒為單位）。
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: 'MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974570"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH 屬性

指定聲場 echo 取消 (AEC) 演算法可以處理的回應持續時間（以毫秒為單位）。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

256

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

AEC 演算法會使用彈性篩選，其長度取決於回應的持續時間。 建議應用程式使用下列其中一個值：

-   128
-   256
-   512
-   1024

預設值為256毫秒，這對大部分的辦公室和家用環境都已足夠。 設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。

只有在啟用 AEC 處理時，DSP 才會使用這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[語音捕獲 DSP](voicecapturedmo.md)
</dt> </dl>

 

 
