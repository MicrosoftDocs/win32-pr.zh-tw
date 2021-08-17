---
description: 本附錄說明 Simplec 和 Simples 範例應用程式的重寫版本，可正常處理 IPv4 或 IPv6。已啟用 IPv6 的用戶端 CodeIPv6-Enabled Server 程式碼
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 附錄 B： IP 版本中立的原始程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37daf34b4a7d46a2fb8fc3cbaf5aed6cf7e054a3fb0147de8d86a643a9e4f59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741605"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a>附錄 B： IP 版本中立的原始程式碼

本附錄說明 Simplec 和 Simples 範例應用程式的重寫版本，可正常地處理 IPv4 或 IPv6。

-   [啟用 IPv6 的用戶端程式代碼](ipv6-enabled-client-code-2.md)
-   [啟用 IPv6 的伺服器程式碼](ipv6-enabled-server-code-2.md)

這段程式碼會」舉例說明此 IPv6 指南中所述的指導方針，並納入其中以提供已成功修改的原始程式碼，以新增 IPv6 支援。 這個範例是刻意簡單的，但提供流覽和審查的實際操作範例。 [附錄 A：僅限 ipv4 的原始程式碼](appendix-a-ipv4-only-source-code-2.md)中提供此原始程式碼的 IPv4 版本。

藉由比較附錄 A 中的原始程式碼 (僅限 IPv4) 和附錄 B (與 IP 版本無關) ，您可以瞭解修改 Windows 通訊端應用程式以新增 IPv6 支援所需的變更。

 

 



