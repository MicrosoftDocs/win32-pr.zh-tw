---
description: 使用用來建立信任執行環境的記憶體保護區時，會使用下列結構：
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: 信任的執行結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d934ec26f9973697b987bf3a816e95d94ea591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971757"
---
# <a name="trusted-execution-structures"></a>信任的執行結構

使用用來建立信任執行環境的記憶體保護區時，會使用下列結構：

## <a name="in-this-section"></a>本節內容



| 主題                                                                                         | 描述                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**記憶體保護區 \_ 建立 \_ 資訊 \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | 包含用來建立記憶體保護區的架構專屬資訊。當記憶體保護區類型為 **記憶體保護區 \_ 類型 \_ SGX** 時，會指定 Intel Software Guard Extensions 的記憶體保護區， (SGX) 架構延伸模組。<br/>     |
| [**記憶體保護區 \_ 建立 \_ 資訊 \_ VBS**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | 包含用來建立記憶體保護區的架構專屬資訊。當記憶體保護區類型為 **記憶體保護區 \_ 類型 \_ vbs** 時，它會指定以虛擬化為基礎的安全性， (VBS) 記憶體保護區。<br/>                                       |
| [**記憶體保護區身分 \_ 識別**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | 描述記憶體保護區主要模組的身分識別。 <br/>                                                                                                                                                                 |
| [**記憶體保護區 \_ 資訊**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | 包含目前執行之記憶體保護區的相關資訊。<br/>                                                                                                                                                                  |
| [**記憶體保護區 \_ INIT \_ INFO \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | 包含用來初始化記憶體保護區的架構專屬資訊（當記憶體保護區類型是 **記憶體保護區 \_ 類型 \_ SGX**）時，它會指定 Intel Software Guard Extensions 的記憶體保護區， (SGX) 架構延伸模組。<br/> |
| [**記憶體保護區 \_ INIT \_ INFO \_ VBS**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | 包含用來初始化記憶體保護區的架構專屬資訊。當記憶體保護區類型為 **記憶體保護區 \_ 類型 \_ vbs** 時，它會指定以虛擬化為基礎的安全性， (VBS) 記憶體保護區。<br/>                                   |
| [**映射 \_ 記憶體保護區 \_ CONFIG32**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | 定義執行32位 Windows 之系統的記憶體保護區設定格式。<br/>                                                                                                                                          |
| [**映射 \_ 記憶體保護區 \_ CONFIG64**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | 定義執行64位 Windows 之系統的記憶體保護區設定格式。<br/>                                                                                                                                          |
| [**影像 \_ 記憶體保護區匯 \_ 入**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | 在記憶體保護區可以匯入的影像陣列中定義專案。<br/>                                                                                                                                                           |
| [**VBS \_ 記憶體保護區 \_ 報表**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | 描述在呼叫 [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) 函式所產生的報表中所包含的帶正負號語句的格式。<br/>                                                     |
| [**VBS \_ 記憶體保護區 \_ 報表 \_ 模組**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | 描述針對記憶體保護區載入的模組。<br/>                                                                                                                                                                                   |
| [**VBS \_ 記憶體保護區 \_ 報表 \_ PKG \_ 標頭**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | 描述透過呼叫 [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) 函式所產生之報表的內容。<br/>                                                                                     |
| [**VBS \_ 記憶體保護區 \_ 報表 \_ VARDATA \_ 標頭**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | 描述 [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) 函數所產生的報表中所包含之變數資料區塊的格式。<br/>                                                          |



 

 

 
