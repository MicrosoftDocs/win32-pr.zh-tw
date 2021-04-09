---
description: PKEY \_ AudioEndpoint \_ ControlPanelPageProvider 屬性會指定音訊端點裝置之裝置屬性延伸模組的已註冊提供者 CLSID。
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: 'PKEY_AudioEndpoint_ControlPanelPageProvider (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847308"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a>PKEY \_ AudioEndpoint \_ ControlPanelPageProvider

**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider** 屬性會指定音訊端點裝置之裝置屬性延伸模組的已註冊提供者 CLSID。 此延伸模組會提供在 [Windows 多媒體] 控制台的 [裝置內容] 頁面中顯示的音訊端點屬性，Mmsys.cpl。 如需 Mmsys.cpl 的詳細資訊，請參閱 Windows DDK 檔。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。

**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 結尾的寬字元字串，其中包含可識別控制台擴充功能提供者的 GUID。

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

 

 




