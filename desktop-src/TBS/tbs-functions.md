---
title: TB 函數
description: TBS 提供下列功能。
ms.assetid: df2d3e36-0a27-4cc0-bcb2-709eb6bedeac
keywords:
- TPM 基礎服務 TB、函數
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1b34f2dfbe18ef2230838ff4ba9ec2241d3cc2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376048"
---
# <a name="tbs-functions"></a>TB 函數

TBS 提供下列功能。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                       | 描述                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Tbsi \_ 內容 \_ 建立**](/windows/desktop/api/Tbs/nf-tbs-tbsi_context_create)<br/>                            | 建立可以用來將命令傳遞至 TBS 的內容控制碼。<br/>                                                                               |
| [**Tbsi \_ \_ \_ 從記錄檔建立證明 \_**](/previous-versions/windows/desktop/legacy/dn455155(v=vs.85))<br/> | 從 TCG 記錄檔中解壓縮 TrustPoint 來建立證明。<br/>                                                                                |
| [**Tbsi \_ GetDeviceInfo**](/windows/desktop/api/Tbs/nf-tbs-tbsi_getdeviceinfo)<br/>                                | 取得電腦上的 TPM 版本。<br/>                                                                                                  |
| [**Tbsi \_ Get \_ OwnerAuth**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_ownerauth)<br/>                               | 如果本機登錄中有可用的資訊，則抓取 TPM 的擁有者授權。 <br/>                                             |
| [**Tbsi \_ 取得 \_ TCG \_ 記錄檔**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log)<br/>                                  | 抓取最新的 Windows 開機設定記錄 (WBCL) ，也稱為 TCG 記錄檔。<br/>                                                  |
| [**Tbsi \_ 取得 \_ TCG \_ 記錄檔 \_ Ex**](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log_ex)<br/>                           | 取得指定類型的 Windows 開機設定記錄 (WBCL) ，也稱為 TCG 記錄檔。<br/>                                          |
| [**Tbsi \_ 取得 \_ TCG \_ 記錄**](/previous-versions/windows/desktop/legacy/dn455156(v=vs.85))<br/>                                | 取得一或多個 Windows 開機設定記錄 (WBCL) ，也稱為 TCG 記錄檔。<br/>                                                        |
| [**Tbsi \_ 實體 \_ 存在性 \_ 命令**](/windows/desktop/api/Tbs/nf-tbs-tbsi_physical_presence_command)<br/>     | 透過 TB 傳遞實體存在性 ACPI 命令至驅動程式。<br/>                                                                               |
| [**Tbsi \_ Revoke \_ 證明**](/windows/desktop/api/Tbs/nf-tbs-tbsi_revoke_attestation)<br/>                     | 如果 ELAM 驅動程式偵測到原則違規 (rootkit，例如) ，則會使 PCRs 失效。<br/>                                                     |
| [**Tbsip \_ Cancel \_ 命令**](/windows/desktop/api/Tbs/nf-tbs-tbsip_cancel_commands)<br/>                        | 取消指定內容的所有未完成命令。<br/>                                                                                      |
| [**Tbsip \_ 內容 \_ 關閉**](/windows/desktop/api/Tbs/nf-tbs-tbsip_context_close)<br/>                            | 關閉內容控制碼，此控制碼會釋放與內容（以 TB 為）相關聯的資源，並關閉用來與 TBS 通訊的系結控制碼。<br/> |
| [**Tbsip \_ Submit \_ 命令**](/windows/desktop/api/Tbs/nf-tbs-tbsip_submit_command)<br/>                          | 將可信賴平臺模組 (TPM) 命令提交至 TPM 基底服務， (TB) 進行處理。<br/>                                                       |



 

 

