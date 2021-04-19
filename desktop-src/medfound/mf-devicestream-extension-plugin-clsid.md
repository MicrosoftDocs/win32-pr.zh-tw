---
description: 指定影片捕獲裝置的後置處理外掛程式 CLSID。
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: 'MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970217"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a>MF \_ DEVICESTREAM \_ 延伸模組 \_ 外掛程式 \_ CLSID 屬性

指定影片捕獲裝置的後置處理外掛程式 CLSID。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

後置處理外掛程式是一種在捕獲影片映射後進行處理的 MFT。 硬體廠商可在安裝套件中包含後置處理外掛程式。 如果是，影片捕獲來源會將 MF \_ DEVICESTREAM \_ 延伸模組 \_ 外掛程式 \_ clsid 屬性設定為外掛程式的 clsid。

若要取得這個屬性，請執行下列動作：

1.  查詢 [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) 介面的媒體來源。
2.  呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 來取得資料流程的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。
3.  呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) 以取得屬性。

若要建立外掛程式，請呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
