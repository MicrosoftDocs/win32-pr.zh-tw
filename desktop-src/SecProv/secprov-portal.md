---
description: 安全性 WMI 提供者可用於 wmi 腳本，以及建立受管理的安全性提供者。
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: 安全性 WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0206e337e5fa23470f015a0264bd77d53e8c4e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973823"
---
# <a name="security-wmi-providers"></a>安全性 WMI 提供者

## <a name="purpose"></a>目的

安全性 WMI 提供者可讓系統管理員和程式設計人員使用) Windows Management Instrumentation WMI (，設定 BitLocker 磁碟機加密 (的) 和可信賴平臺模組 (TPM) 。

## <a name="developer-audience"></a>開發人員對象

本檔指定的 WMI 提供者介面可用於管理和設定 BitLocker 磁碟機加密 (的) 以及 Windows Server 2008 2008 R2 上的信賴平臺模組 (TPM) ，以及 windows 7 和 windows Vista 的用戶端電腦。 它的目的是要讓撰寫腳本、使用者介面專案或其他的系統管理工具或 TPM 進行讀取。

## <a name="run-time-requirements"></a>執行階段需求求

安全性 WMI 提供者需要使用每個提供者和支援的作業系統指定的 mof 檔案。 最低作業系統是 Windows Server 2008 或 Windows Vista。 BitLocker 磁碟機加密僅適用于 windows vista Enterprise 和 Windows vista 旗艦版的 windows Vista。 如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。

## <a name="in-this-section"></a>本節內容



| 主題                                                                               | 描述                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [關於安全性 WMI 提供者](about-security-wmi-providers.md)<br/>         | 安全性 WMI 提供者的簡短總覽。<br/>           |
| [安全性 WMI 提供者參考](security-wmi-providers-reference.md)<br/> | 安全性 WMI 提供者的參考檔。<br/> |



 

## <a name="additional-resources"></a>其他資源

以下是其他資源。



|                    |                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類別<br/> | 如需有關安全性 WMI 提供者的詳細資訊，請參閱 [**win32 \_ EncryptableVolume**](win32-encryptablevolume.md) 和 [**win32 \_ Tpm**](win32-tpm.md)。<br/> |



 

 

 




