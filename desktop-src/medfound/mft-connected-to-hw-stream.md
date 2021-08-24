---
description: 指定以硬體為基礎的媒體基礎轉換 (MFT) 是否已連線到另一個以硬體為基礎的 MFT。
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: 'MFT_CONNECTED_TO_HW_STREAM 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ff2a2dea2fcb67cff776ba02c43193b571a382df57a5d0562f3f2cd1fb7248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602868"
---
# <a name="mft_connected_to_hw_stream-attribute"></a>\_連接 \_ 至 \_ HW \_ STREAM 屬性的 MFT

指定以硬體為基礎的媒體基礎轉換 (MFT) 是否已連線到另一個以硬體為基礎的 MFT。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

應用程式通常不會使用此屬性。

這個屬性會與以硬體為基礎的 MFTs 搭配使用。 當兩個硬體 MFTs 在拓撲內連接時，拓撲載入器會在下列物件上將此屬性設定為 **TRUE** ：

-   上游 MFT 的輸出資料流程
-   下游 MFT 的輸入資料流程

為了取得輸出資料流程的屬性存放區，拓撲載入器會呼叫上游 MFT 上的 [**IMFTransform：： GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) 。 為了取得輸入資料流程的屬性存放區，拓撲載入器會在下游 MFT 上呼叫 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) 。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[硬體 MFTs](hardware-mfts.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




