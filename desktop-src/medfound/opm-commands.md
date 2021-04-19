---
description: OPM 命令
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: OPM 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976789"
---
# <a name="opm-commands"></a>OPM 命令

本節列出 [輸出保護管理員](output-protection-manager.md) (OPM) 可用的命令。

若要傳送 OPM 命令，請呼叫 [**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)。 針對每個命令，會列出下列資訊。



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 命令 GUID | 識別命令。 將 [**OPM 設定 \_ \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)結構的 **guidSetting** 成員設定為等於此值。 |
| 輸入資料   | 指定如何在 [**OPM \_ 設定 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)結構中解讀 **abParameters** 陣列。                      |



 

下列是已定義的命令：



| 命令                                                                                                       | 描述                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**OPM \_ 設定 \_ ACP \_ 和 \_ CGMSA \_ 信號**](opm-set-acp-and-cgmsa-signaling.md)                               | 指定除了保護層級以外的視訊訊號相關資訊。                      |
| [**OPM \_ 設定 \_ HDCP \_ SRM**](opm-set-hdcp-srm.md)                                                               | 更新 (SRM) 的系統 renewability 訊息，以 High-Bandwidth 數位內容保護 (HDCP) 。 |
| [**OPM \_ SET \_ 保護 \_ 等級**](opm-set-protection-level.md)                                               | 設定輸出保護機制的保護層級。                                       |
| [**\_ \_ \_ \_ 根據 \_ \_ CSS \_ DVD OPM 設定保護等級**](opm-set-protection-level-according-to-css-dvd.md) | 設定 DVD 播放的 HDCP 保護層級，並遵循 DVD 內容管理系統 (CSS) 規則。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[OPM 程式設計參考](opm-programming-reference.md)
</dt> <dt>

[輸出保護管理員](output-protection-manager.md)
</dt> </dl>

 

 



