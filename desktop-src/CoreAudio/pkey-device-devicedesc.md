---
description: PKEY \_ Device \_ DeviceDesc 屬性包含端點裝置的裝置描述 (例如 &\# 0034;喇叭&\# 0034; ) 。
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: 'PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846960"
---
# <a name="pkey_device_devicedesc"></a>PKEY \_ 裝置 \_ DeviceDesc

**PKEY \_ Device \_ DeviceDesc** 屬性包含端點裝置的裝置描述 (例如「喇叭」 ) 。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。

**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 終止的寬字元字串，其中包含裝置描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Functiondiscoverykeys \_ devpkey。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[核心音訊屬性](core-audio-properties.md)
</dt> <dt>

[裝置內容](device-properties.md)
</dt> </dl>

 

 




