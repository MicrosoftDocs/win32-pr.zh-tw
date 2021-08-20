---
description: PKEY \_ AudioEndpoint \_ Disable \_ SysFx 屬性會指定是否在流入或流出音訊端點裝置的共用模式資料流程中啟用系統效果。
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: 'PKEY_AudioEndpoint_Disable_SysFx (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8f4e5b54773cc6fcdc14ed7788a8ce6c3da2bf28666109c1404095c0c5c12a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005227"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a>PKEY \_ AudioEndpoint \_ Disable \_ SysFx

**PKEY \_ AudioEndpoint \_ Disable \_ SysFx** 屬性會指定是否在流入或流出音訊端點裝置的共用模式資料流程中啟用系統效果。

系統效果會實作為音訊處理物件， (可以插入音訊串流中的) 。 是執行音訊處理功能的軟體模組，例如音量控制和格式轉換。 停用端點裝置的系統效果，可讓相關聯的串流通過未修改的。

如需有關 Windows Vista 中系統效果的詳細資訊，請參閱《 Windows 網站的[音訊裝置技術](https://www.microsoft.com/whdc/device/audio/default.mspx)》中標題為「Windows Vista 的自訂音訊效果」和「重複使用 Windows Vista 音訊系統效果」的白皮書。

這個屬性只適用于安裝了端點裝置所連接之音訊介面卡的 .inf 檔案所安裝的本機效果和全域效果。 此外，此屬性只會影響目標端點裝置，即使是連接到相同的介面卡，也不會影響任何其他端點裝置的系統效果。

**PROPVARIANT** 結構的 **vt** 成員會設定為 **vt \_ UI4**。

如果啟用了系統效果，或如果已停用 **端點 \_ \_ SYSFX** ，則 **PROPVARIANT** 結構的 **ulVal** 成員會設定為 **\_ \_ 已啟用的 endpoint SYSFX** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**音訊端點屬性**](audio-endpoint-properties.md)
</dt> <dt>

[核心音訊屬性](core-audio-properties.md)
</dt> </dl>

 

 




