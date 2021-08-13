---
description: 使用探索磁片區的指定檔案系統類型建立 BitLocker 磁片區。
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Win32_EncryptableVolume 類別的 PrepareVolume 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 67b36703883825d4144037c54ffb55c00308ed1cfb8ee3e4b074d75d63bf7390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891544"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a>Win32 EncryptableVolume 類別的 PrepareVolume 方法 \_

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **PrepareVolume** 方法會使用探索磁片區的指定檔案系統類型來建立 BitLocker 磁片區。 必須先呼叫這個方法，才能使用任何 **ProtectKeyWith \*** 方法來保護磁片區。

## <a name="syntax"></a>語法

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*DiscoveryVolumeType* \[在\]
</dt> <dd>

類型： **字串**

指定探索磁片區類型的字串。

| 值               | 意義                                                            |
|---------------------|--------------------------------------------------------------------|
| **&lt;沒有&gt;**    | 無探索磁片區。 此值會建立原生 BitLocker 磁片區。 |
| **&lt;預設&gt;** | 此值為預設行為。                                |
| **FAT32**           | 此值會建立 FAT32 探索磁片區。                       |

</dd> <dt>

*ForceEncryptionType* \[在\]
</dt> <dd>

類型： **uint32**

指定加密類型的整數。 這可以是下列其中一個值。

| 值                                                                                                                                                                                                                                       | 意義                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**未指定**</dt> <dt>0</dt> </dl> | 未指定加密類型。<br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <dt>**軟體**</dt> <dt>1</dt> </dl>             | 軟體加密。<br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <dt>**硬體**</dt> <dt>2</dt> </dl>             | 硬體加密。<br/>                  |

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。

| 傳回碼/值      | 描述                     |
|------------------------|---------------------------------|
| **S_OK** <br/> 0 (0x0)  | 此方法成功。<br/> |

## <a name="remarks"></a>備註

如果您在啟用 BitLocker 磁片區時未呼叫這個方法，就如同在 *DiscoveryVolumeType* 參數中使用預設值呼叫此方法一樣。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 企業版， \[ 僅 Windows 7 旗艦版桌面應用程式\]<br/>                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume mof</dt> </dl> |

## <a name="see-also"></a>另請參閱

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
