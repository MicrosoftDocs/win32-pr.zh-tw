---
title: EAPHost Registry 設定
description: 下列登錄機碼中的登錄值會控制 EAPHost 功能的各個層面。
ms.assetid: 2b954911-7c2e-4c86-b031-24632235a669
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec08a7428dac4c68044b0491e084574c6ff3d006fcf06f59912754c5a9f93833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482978"
---
# <a name="eaphost-registry-settings"></a>EAPHost Registry 設定

下列登錄機碼中的登錄值會控制 EAPHost 功能的各個層面。



| 子機碼                                                                 | 描述                                                                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BypassNegotiation](bypassnegotiation.md)                             | 判斷是否發生 RAS 伺服器和用戶端之間的功能協商。<br/>                                                                              |
| [AssumePhase2Fragmentation](assumephase2fragmentation.md)             | 判斷 RAS 伺服器和用戶端是否採用第2階段片段。<br/>                                                                                         |
| [OverrideEAPCertificateSelection](overrideeapcertificateselection.md) | 判斷用戶端是否會覆寫預設的智慧卡憑證選取行為，並為使用者提供更多憑證以供選擇。<br/> |
| [PeapServerUseAllPurposeCert](peapserveruseallpurposecert.md)         | 判斷是否使用所有用途的憑證進行 PEAP 驗證。<br/>                                                                                      |
| [PeapServerAcceptAllPurposeCert](peapserveracceptallpurposecert.md)   | 判斷是否接受 PEAP 驗證的所有用途憑證。<br/>                                                                                  |
| [TlsServerUseAllPurposeCert](tlsserveruseallpurposecert.md)           | 判斷是否使用所有用途的憑證進行 EAP-TLS 驗證。<br/>                                                                                   |
| [TlsServerAcceptAllPurposeCert](tlsserveracceptallpurposecert.md)     | 判斷是否接受 EAP-TLS 驗證的所有用途憑證。<br/>                                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost API 參考](eaphost-api-reference.md)
</dt> </dl>

 

 





