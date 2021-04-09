---
description: 包含 IMFFieldOfUseMFTUnlock 指標，可用來解除鎖定 (MFT) 的媒體基礎轉換。 IMFFieldOfUseMFTUnlock 介面可用來解除鎖定具有使用規定限制的 MFT。
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: 'MFT_FIELDOFUSE_UNLOCK_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692312"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性屬性

包含 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 指標，可用來解除鎖定 (MFT) 的媒體基礎轉換。 **IMFFieldOfUseMFTUnlock** 介面可用來解除鎖定具有使用規定限制的 MFT。

## <a name="data-type"></a>資料類型

**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) IMFFieldOfUseMFTUnlock \** _ 儲存為 _*IUnknown \**_

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。

## <a name="remarks"></a>備註

如需此屬性的詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。

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

[使用限制領域](field-of-use-restrictions.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




