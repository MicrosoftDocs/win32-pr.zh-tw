---
description: 指定是否僅在應用程式處理常式中註冊媒體基礎轉換 (MFT) 。
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: 'MFT_PROCESS_LOCAL_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691648"
---
# <a name="mft_process_local_attribute-attribute"></a>MFT \_ 進程 \_ 區域 \_ 屬性屬性

指定是否只在應用程式的進程中註冊媒體基礎轉換 (MFT) 。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

這個屬性的使用方式如下：

1.  應用程式會藉由呼叫 [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) 或 [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) 函式來註冊本機 MFT。 這些函式會在應用程式的進程中註冊 MFT。
2.  呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數，以列舉符合一組特定準則的 MFTs。 應用程式可能會直接呼叫 **MFTEnumEx** 函式，但較常由拓撲載入器呼叫此函式。
3.  [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式會捕獲 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標的陣列，每個指標都代表一個 MFT 的啟用物件。 如果在本機註冊了 MFT，則 \_ 對應的啟用物件上的 [mft 進程 \_ 區域屬性] \_ 屬性會設定為 [ **TRUE** ]。

這個屬性的預設值為 **FALSE**。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




