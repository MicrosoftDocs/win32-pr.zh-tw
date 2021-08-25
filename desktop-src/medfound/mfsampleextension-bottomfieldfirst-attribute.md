---
description: 指定交錯式影片框架的欄位支配。
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: 'MFSampleExtension_BottomFieldFirst 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ab0a9847977ea25d93190911bbf2280629f0219eba3d4c4ddfb492e9fdcd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113068"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a>MFSampleExtension \_ BottomFieldFirst 屬性

指定交錯式影片框架的欄位支配。 這個屬性會套用至媒體範例。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

如果影片框架是交錯的，且此範例包含兩個交錯的欄位，這個屬性會指出先顯示哪個欄位。 若 **為 TRUE**，則底部欄位為第一個時間。 如果 **為 FALSE**，則表示頂端欄位是 first。

如果框架是交錯的，且範例包含單一欄位，則此屬性會指出此範例包含的欄位。 若 **為 TRUE**，則範例包含底部欄位。 如果 **為 FALSE**，則表示範例包含上方欄位。

如果框架是漸進式的，則此屬性會描述在輸出交錯時如何排序欄位。 若 **為 TRUE**，則應先輸出下一個欄位。 如果 **為 FALSE**，則應該先輸出最上層欄位。

如果未設定此屬性，則媒體類型會描述欄位支配。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> <dt>

[影片交錯](video-interlacing.md)
</dt> </dl>

 

 




