---
description: 指定語音捕獲 DSP 是否執行雜訊抑制。
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: 'MFPKEY_WMAAECMA_FEATR_NS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969247"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ NS 屬性

指定語音捕獲 DSP 是否執行雜訊抑制。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

1

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

雜訊隱藏是 (DSP) 元件的數位信號處理，可抑制或減少音訊信號中的靜止背景雜音。 雜訊抑制會在聲場 echo 取消 (AEC) 和麥克風陣列處理之後套用。

這個屬性可以具有下列值。



| 值 | 描述                |
|-------|----------------------------|
| 0     | 停用雜訊抑制。 |
| 1     | 啟用雜訊抑制。  |



 

這個屬性的預設值為 1 (已啟用) 。 設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。

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

 

 
