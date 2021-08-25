---
description: 指定拓撲載入器是否會變更媒體基礎轉換 (MFT) 的媒體類型。 應用程式通常不會使用此屬性。
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: 'MF_ACTI加值稅E_MFT_LOCKED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445447af46e1ce1da25aaa075dd4490d1210c1d01b2e7717829d2672dc74701f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060908"
---
# <a name="mf_activate_mft_locked-attribute"></a>MF \_ 啟動 \_ MFT \_ 鎖定屬性

指定拓撲載入器是否會變更媒體基礎轉換 (MFT) 的媒體類型。 應用程式通常不會使用此屬性。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

如果這個屬性的值為非零值，拓撲載入器不會變更 MFT 上的媒體類型。 拓撲載入器會在載入拓撲之後設定此屬性。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




