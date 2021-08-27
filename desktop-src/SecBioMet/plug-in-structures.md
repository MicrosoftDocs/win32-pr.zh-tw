---
title: 外掛程式結構
description: Windows 生物特徵辨識架構 API 開發用戶端應用程式的結構。
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- Windows生物特徵辨識架構 api Windows 生物特徵辨識架構 API、外掛程式結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e150dd043a8c95e91d0f9095e23584544f43a503a709ae54c9180e06aa40bdaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101238"
---
# <a name="plug-in-structures"></a>外掛程式結構

Windows 生物特徵辨識架構 API 開發用戶端應用程式時，支援下列結構。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                | 描述                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**WINBIO \_ 帳戶 \_ 原則**](winbio-account-policy.md)<br/>                                  | 包含預設或帳戶特定的 lnk-antispoofing 原則。<br/>                                                         |
| [**WINBIO \_ 介面卡 \_ 介面 \_ 版本**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | 包含引擎、感應器和儲存介面卡介面資料表中所使用的主要和次要版本號碼。<br/>                |
| [**WINBIO \_ 引擎 \_ 介面**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | 包含自訂引擎介面卡函式的指標。<br/>                                                                 |
| [**WINBIO \_ 延伸 \_ 註冊 \_ 參數**](winbio-extended-enrollment-parameters.md)<br/> | 包含引擎介面卡建立註冊範本時所需的其他資訊。 <br/>                            |
| [**WINBIO \_ 管線**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | 包含在單一生物特徵辨識裝置中，感應器、引擎和存放裝置介面卡元件所使用的共用內容資訊。<br/> |
| [**WINBIO \_ 感應器 \_ 介面**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | 包含自訂感應器介面卡函式的指標。<br/>                                                                 |
| [**WINBIO \_ 儲存體 \_ 介面**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | 包含您自訂存放裝置介面卡函式的指標。<br/>                                                                |
| [**WINBIO \_ 儲存體 \_ 記錄**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | 包含標準格式的生物特徵辨識範本和相關聯的資料。<br/>                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[外掛程式參考](plug-in-reference.md)
</dt> <dt>

[外掛程式函數](plug-in-functions.md)
</dt> <dt>

[**WbioQueryEngineInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





