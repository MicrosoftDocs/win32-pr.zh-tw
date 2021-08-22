---
title: BITS 列舉
description: 背景智慧型傳送服務 (位) 介面會使用下列列舉。
ms.assetid: e43337c8-0c41-41e9-88fd-f2a46f666157
ms.topic: article
ms.date: 02/20/2019
ms.openlocfilehash: 4ced67a469ae5fb35e8098fdcfe3edcdbeafa08c55416f65f55635a7d3f5e948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323548"
---
# <a name="bits-enumerations"></a>BITS 列舉

[背景智慧型傳送服務 (位) 介面](bits-interfaces.md)會使用下列列舉。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**BG_AUTH_SCHEME**](/windows/win32/api/bits1_5/ne-bits1_5-bg_auth_scheme) | 定義常數，指定 proxy 或伺服器要求使用者驗證時要使用的驗證配置。 |
| [**BG_AUTH_TARGET**](/windows/win32/api/bits1_5/ne-bits1_5-bg_auth_target) | 定義常數，指定認證是否用於 proxy 或伺服器使用者驗證要求。 |
| [**BG_CERT_STORE_LOCATION**](/windows/win32/api/bits2_5/ne-bits2_5-bg_cert_store_location) | 定義常數，指定憑證存放區的位置。 |
| [**BG_ERROR_CONTEXT**](/windows/win32/api/bits/ne-bits-bg_error_context) | 定義常數，指定發生錯誤的內容。 |
| [**BG_JOB_PRIORITY**](/windows/win32/api/bits/ne-bits-bg_job_priority) | 定義常數，指定作業的優先權層級。  |
| [**BG_JOB_PROXY_USAGE**](/windows/win32/api/bits/ne-bits-bg_job_proxy_usage) | 定義常數，以指定要用於檔案傳輸的 proxy。 您可以為每個作業定義不同的 proxy 設定。 |
| [**BG_JOB_STATE**](/windows/win32/api/bits/ne-bits-bg_job_state) | 定義常數，指定作業的不同狀態。 |
| [**BG_JOB_TYPE**](/windows/win32/api/bits/ne-bits-bg_job_type) | 定義常數，指定傳送作業的類型，例如 [下載]。 |
| [**BITS_COST_STATE**](./bits-cost-state.md) | 定義指定 BITS 成本狀態的常數。 |
| [**BITS_FILE_PROPERTY_ID**](/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id) | 定義常數，指定對應于背景複製檔案屬性的識別碼值。 請參閱 [IBackgroundCopyFile5：： GetProperty](../delivery_optimization/ibackgroundcopyfile5-getproperty.md) 和 [SetProperty](../delivery_optimization/ibackgroundcopyfile5-setproperty.md)。 |
| [**BITS_JOB_PROPERTY_ID**](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id) | 定義常數，指定 BITS 作業的屬性識別碼。 |
| [**BITS_JOB_TRANSFER_POLICY**](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy) | 定義常數，指定對應于 BITS 屬性的識別碼值。 |