---
description: PKEY \_ Device \_ FriendlyName 屬性包含端點裝置的易記名稱 (例如，&\# 0034; (XYZ 音訊介面卡) &\# 0034; ) 的喇叭。
ms.assetid: 3ccd6a78-8bc3-4a46-8f11-7c2ae8a23c63
title: 'PKEY_Device_FriendlyName (Functiondiscoverykeys \_ devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab8b8f30e04ae66356fb0910e3767d74b7b697a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846952"
---
# <a name="pkey_device_friendlyname"></a>PKEY \_ 裝置 \_ FriendlyName

**PKEY \_ Device \_ FriendlyName** 屬性包含端點裝置的易記名稱 (例如「喇叭 (XYZ 音訊介面卡) 」 ) 。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。

**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 結尾的寬字元字串，其中包含端點裝置的易記名稱。

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

 

 




