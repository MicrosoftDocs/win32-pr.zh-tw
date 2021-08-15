---
description: 列舉系統上符合指定準則的所有憑證，並傳回指紋清單。
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Win32_EncryptableVolume 類別的 FindValidCertificates 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: da642ff24fa01d27c74a30af7de6c7f91e33a712a28c47644a7044f43c40d586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892436"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 FindValidCertificates 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **FindValidCertificates** 方法會列舉系統上符合指定準則的所有憑證，並傳回指紋清單。 傳回的清單只包含具有有效 [*物件識別碼*](../secgloss/o-gly.md) (OID) 的憑證。 OID 可以是預設值，也可以在群組原則中指定。

## <a name="syntax"></a>語法


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CertificateThumbprint* \[擴展\]
</dt> <dd>

類型：**字串 \[ \]**

字串的陣列，其中包含有效憑證的清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                                           | Description                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                                           | 此方法成功。<br/>                |
| <dl> <dt>**FVE \_E \_ 不正確 \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl> | 可用的 BitLocker OID 無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 企業版， \[ 僅 Windows 7 旗艦版桌面應用程式\]<br/>                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
