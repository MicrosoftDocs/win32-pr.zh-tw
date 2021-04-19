---
description: PKEY \_ AudioEndpoint \_ Association 屬性會將核心串流 (KS) 釘選類別與音訊端點裝置產生關聯。
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: 'PKEY_AudioEndpoint_Association (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001323"
---
# <a name="pkey_audioendpoint_association"></a>PKEY \_ AudioEndpoint \_ 關聯

**PKEY \_ AudioEndpoint \_ Association** 屬性會將核心串流 (KS) 釘選類別與音訊端點裝置產生關聯。 安裝音訊介面卡的 .inf 檔案會將釘選類別指派給介面卡中的每個 KS pin。 介面卡裝置上的 KS pin 代表音訊串流進入或離開裝置的時間點。 Pin 類別是 GUID，可指定由 KS 釘選執行的函式類型。 例如，標頭檔 Ksmedia 會定義釘選類別 GUID KSNODETYPE 麥克風， \_ 以表示連接至麥克風的 ks pin，以及 KSNODETYPE \_ 耳機以表示連接到耳機的 ks pin。 如需詳細資訊，請參閱 Windows DDK 檔中的 pin 分類屬性說明。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。

**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 結尾的寬字元字串，其中包含一個 KS 釘選類別 GUID。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**音訊端點屬性**](audio-endpoint-properties.md)
</dt> <dt>

[核心音訊屬性](core-audio-properties.md)
</dt> </dl>

 

 




