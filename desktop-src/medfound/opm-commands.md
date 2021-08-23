---
description: OPM 命令
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: OPM 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6d21119f86ab8f51392df248498681f8fe5dc1aa8218a0232b9f3bd1c7cb02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722238"
---
# <a name="opm-commands"></a>OPM 命令

本節列出 [輸出保護管理員](output-protection-manager.md) (OPM) 可用的命令。

若要傳送 OPM 命令，請呼叫 [**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)。 針對每個命令，會列出下列資訊。



| 值             | 描述                                                                                                                                                            |
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

 

 



