---
title: BITS 結構和等位
description: 背景智慧型傳送服務 (位) 介面會使用下列結構。
ms.assetid: a1b8b4a1-77d6-46ac-96d5-6a0c99cfc643
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 199d5648ba8205d0417304350a104b2e16a607e4d7f1bdce4dfe9ecec34f98dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702028"
---
# <a name="bits-structures-and-unions"></a>BITS 結構和等位

背景智慧型傳送服務 (位) [介面](bits-interfaces.md) 會使用下列結構。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**BG_AUTH_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials) | 識別要用於使用者驗證要求的目標 (proxy 或伺服器) 、驗證配置和使用者的認證。 結構會傳遞至 [IBackgroundCopyJob2：： SetCredentials 方法](/windows/win32/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials)。 |
| [**BG_AUTH_CREDENTIALS_UNION**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials_union) | 識別要用於 [BG_AUTH_CREDENTIALS 結構](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials)中所指定之驗證配置的認證。 |
| [**BG_BASIC_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_basic_credentials) | 識別要驗證的使用者名稱和密碼。 |
| [**BG_FILE_INFO**](/windows/win32/api/bits/ns-bits-bg_file_info) | 提供要傳送之檔案的本機和遠端名稱。 |
| [**BG_FILE_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_file_progress) | 提供檔案相關的進度資訊，例如已傳送的位元組數目。 |
| [**BG_FILE_RANGE**](/windows/win32/api/bits2_0/ns-bits2_0-bg_file_range) | 識別要從檔案下載的位元組範圍。 |
| [**BG_JOB_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_job_progress) | 提供作業相關的進度資訊，例如已傳輸的位元組數和檔案數目。 針對上傳作業，進度會套用至上傳檔案，而不是回復檔。 若要查看回復檔案的進度，請參閱 [BG_JOB_REPLY_PROGRESS 結構](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress)。 |
| [**BG_JOB_REPLY_PROGRESS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress) | 提供與上傳-回復作業的回復部分相關的進度資訊。 |
| [**BG_JOB_TIMES**](/windows/win32/api/bits/ns-bits-bg_job_times) | 提供作業相關的時間戳記。 |
| [**BITS_FILE_PROPERTY_VALUE 聯集**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | 提供 BITS 檔案的屬性值。 |
| [**BITS_JOB_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | 根據 [BITS_JOB_PROPERTY_ID 列舉](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id)的值，提供 BITS 作業的屬性值。 |
