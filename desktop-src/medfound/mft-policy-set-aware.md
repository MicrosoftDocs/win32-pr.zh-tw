---
description: 指定 IMFTransform 是否要接收 MEPolicySet 完成通知。
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977255"
---
# <a name="mft_policy_set_aware-attribute"></a>MFT \_ 原則 \_ 集 \_ 感知屬性

如果非零，則表示 **IMFTransform** 想要接收 [MEPolicySet](./mepolicyset.md) 完成通知。

## <a name="data-type"></a>資料類型

**UINT32** (視為 **BOOL**) 

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFInputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a>備註

此 attributet 可供 **IMFInputTrustAuthority** decrypter 使用。  (CDM) 的內容解密模組的執行可能包括 **IMFInputTrustAuthority** 的執行。 **IMFInputTrustAuthority** 物件是透過 [IMFContentDecryptionModule：： CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput)存取。


這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 2020 年4月更新   <br/>                                        |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 
