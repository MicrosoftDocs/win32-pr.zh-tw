---
description: 針對以範例為基礎的模式加密，指定明確 (未加密的) 位元組區塊大小。
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: 'MFSampleExtension_Encryption_SkipByteBlock 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c674a7f7762f97a1978bd827795733d01b1dea3053898c5ecd30308373449b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603128"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a>MFSampleExtension \_ Encryption \_ SkipByteBlock 屬性

針對以範例為基礎的模式加密，指定明確 (未加密的) 位元組區塊大小。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

Subsample 對應區塊中的加密位元組數目是在 [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) 屬性中指定。 如果其中一個屬性不存在或值為0，則表示範例資料不會加密。 這兩個值都必須為非零、正值或兩者都必須有零值。

如果來源是以值為基礎，則會根據 [資料軌加密] 方塊中的 [預設 skip 位元組區塊] 值來設定值， \_ \_ \_ ( [tenc] ) 在 [配置] 標頭中。 如需詳細資訊，請參閱 [MFSampleExtension \_ 加密 \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



 

 




