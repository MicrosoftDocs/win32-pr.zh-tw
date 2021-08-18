---
description: 安全通道 SSP 會實行 TLS、DTLS 和 SSL 通訊協定的版本。 不同的 Windows 版本支援不同的通訊協定版本。
ms.assetid: FF716A4E-ABF2-4773-9588-9D200945A866
title: TLS/SSL (Schannel SSP) 的通訊協定
ms.topic: article
ms.date: 01/20/2021
ms.custom: contperf-fy21q3
ms.openlocfilehash: a03264a40ab6d632165fe4cf75aa0dfd7ee85ac0474ef391c36a2b1980010422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920656"
---
# <a name="protocols-in-tlsssl-schannel-ssp"></a>TLS/SSL (Schannel SSP) 的通訊協定

安全通道 SSP 會實行 TLS、DTLS 和 SSL 通訊協定的版本。 不同的 Windows 版本支援不同的通訊協定版本。

## <a name="tls-protocol-version-support"></a>TLS 通訊協定版本支援

下表顯示 Microsoft Schannel 提供者的 TLS 通訊協定版本支援。

> [!TIP]
> 您可能需要水準滾動，才能查看資料表中的所有資料行。

| Windows 作業系統 | TLS 1.0 用戶端 | TLS 1.0 伺服器 | TLS 1.1 用戶端 | TLS 1.1 伺服器 | TLS 1.2 用戶端 | TLS 1.2 伺服器 | TLS 1.3 用戶端 | TLS 1.3 伺服器 |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| WindowsVista/Windows Server 2008                     | 啟用        | 啟用        | 不支援  | 不支援  | 不支援  | 不支援  | 不支援  | 不支援  |
| Windows Server 2008 Service Pack 2 (SP2)         | 啟用        | 啟用        | 已停用       | 已停用       | 已停用       | 已停用       | 不支援  | 不支援  |
| Windows 7/Windows Server 2008 R2                      | 啟用        | 啟用        | 已停用       | 已停用       | 已停用       | 已停用       | 不支援  | 不支援  |
| Windows 8/Windows Server 2012                         | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 8.1/Windows Server 2012 R2                    | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10 (版本 1507)                              | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10 (版本 1511)                              | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10，版本 1607/Windows Server 2016 標準 | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10 (版本 1703)                              | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10 (版本 1709)                              | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10 (版本 1803)                              | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10 版本 1809//Windows Server 2019         | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10 (版本 1903)                              | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10 (版本 1909)                              | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10 (版本 2004)                              | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10 版本 20H2                              | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows 10，版本21H1                              | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 不支援  | 不支援  |
| Windows伺服器2022                                   | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        | 啟用        |


## <a name="dtls-protocol-version-support"></a>DTLS 通訊協定版本支援

以下列出 Microsoft Schannel 提供者對 DTLS 通訊協定版本的支援。

*提示：您可能需要水準滾動，才能查看此資料表中的所有資料行：*

| Windows 作業系統                                            | DTLS 1.0 用戶端 | DTLS 1.0 伺服器 | DTLS 1.2 用戶端 | DTLS 1.2 伺服器 |
|-------------------------------------------------------|-----------------|-----------------|-----------------|-----------------|
| WindowsVista/Windows Server 2008                     | 不支援   | 不支援   | 不支援   | 不支援   |
| Windows Server 2008 SP2                          | 不支援   | 不支援   | 不支援   | 不支援   |
| Windows 7/Windows Server 2008 R2                      | 啟用         | 啟用         | 不支援   | 不支援   |
| Windows 8/Windows Server 2012                         | 啟用         | 啟用         | 不支援   | 不支援   |
| Windows 8.1/Windows Server 2012 R2                    | 啟用         | 啟用         | 不支援   | 不支援   |
| Windows 10 (版本 1507)                              | 啟用         | 啟用         | 不支援   | 不支援   |
| Windows 10 (版本 1511)                              | 啟用         | 啟用         | 不支援   | 不支援   |
| Windows 10，版本 1607/Windows Server 2016 標準 | 啟用         | 啟用         | 啟用         | 啟用         |
| Windows 10 (版本 1703)                              | 啟用         | 啟用         | 啟用         | 啟用         |
| Windows 10 (版本 1803)                              | 啟用         | 啟用         | 啟用         | 啟用         |
| Windows 10 版本 1809                              | 啟用         | 啟用         | 啟用         | 啟用         |
| Windows 10 (版本 1903)                              | 啟用         | 啟用         | 啟用         | 啟用         |
| Windows 10 (版本 1909)                              | 啟用         | 啟用         | 啟用         | 啟用         |
| Windows 10 (版本 2004)                              | 啟用         | 啟用         | 啟用         | 啟用         |
| Windows 10 版本 20H2                              | 啟用         | 啟用         | 啟用         | 啟用         |
| Windows 10，版本21H1                              | 啟用         | 啟用         | 啟用         | 啟用         |

## <a name="pre-tls-standard-protocols-support"></a>預先 TLS 標準通訊協定支援

以下列出 Microsoft Schannel 提供者對 TLS 標準通訊協定的支援：

*提示：您可能需要水準滾動，才能查看此資料表中的所有資料行：*

| Windows 作業系統                                            | PCT 1.0       | SSL2 用戶端   | SSL2 伺服器   | SSL3 用戶端 | SSL3 伺服器 |
|-------------------------------------------------------|---------------|---------------|---------------|-------------|-------------|
| WindowsVista/Windows Server 2008                     | 不支援 | 已停用      | 啟用       | 啟用     | 啟用     |
| Windows Server 2008 SP2                          | 不支援 | 已停用      | 啟用       | 啟用     | 啟用     |
| Windows 7/Windows Server 2008 R2                      | 不支援 | 已停用      | 啟用       | 啟用     | 啟用     |
| Windows 8/Windows Server 2012                         | 不支援 | 已停用      | 已停用      | 啟用     | 啟用     |
| Windows 8.1/Windows Server 2012 R2                    | 不支援 | 已停用      | 已停用      | 啟用     | 啟用     |
| Windows 10 (版本 1507)                              | 不支援 | 已停用      | 已停用      | 啟用     | 啟用     |
| Windows 10 (版本 1511)                              | 不支援 | 已停用      | 已停用      | 啟用     | 啟用     |
| Windows 10，版本 1607/Windows Server 2016 標準 | 不支援 | 不支援 | 不支援 | 已停用    | 已停用    |
| Windows 10 (版本 1703)                              | 不支援 | 不支援 | 不支援 | 已停用    | 已停用    |
| Windows 10 (版本 1803)                              | 不支援 | 不支援 | 不支援 | 已停用    | 已停用    |
| Windows 10 版本 1809                              | 不支援 | 不支援 | 不支援 | 已停用    | 已停用    |
| Windows 10 (版本 1903)                              | 不支援 | 不支援 | 不支援 | 已停用    | 已停用    |
| Windows 10 (版本 1909)                              | 不支援 | 不支援 | 不支援 | 已停用    | 已停用    |
| Windows 10 (版本 2004)                              | 不支援 | 不支援 | 不支援 | 已停用    | 已停用    |
| Windows 10 版本 20H2                              | 不支援 | 不支援 | 不支援 | 已停用    | 已停用    |
| Windows 10，版本21H1                              | 不支援 | 不支援 | 不支援 | 已停用    | 已停用    |


> [!IMPORTANT]
> 從 Windows 10 開始，版本1607和 Windows Server 2016，已移除 SSL 2.0，且已不再支援。

> [!TIP]  
> 所有版本的 Windows 都會接受統一的格式 "ClientHello" 訊息，即使 SSL 版本2已停用或不再受支援也一樣。
