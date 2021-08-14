---
description: 所有的安全通道通訊協定都需要伺服器提供信任憑證授權單位單位的憑證 (CA) 作為其身分識別的證明。
ms.assetid: 060981e0-b52a-4cc2-bfd2-4cf24f921f16
title: 使用 Schannel 執行驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c2a5099dd29d6b3b342b583e37e2dc98187f5011c7cc75b75432924fba9ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921017"
---
# <a name="performing-authentication-using-schannel"></a>使用 Schannel 執行驗證

所有的安全通道通訊協定都需要伺服器提供信任 [*憑證授權單位*](../secgloss/c-gly.md)[*單位的憑證*](../secgloss/c-gly.md) (CA) 作為其身分識別的證明。 此進程稱為伺服器驗證。 用戶端驗證（用戶端會提供其身分識別的證明）是選擇性的，而且可能隨時由伺服器要求。

## <a name="authenticating-the-server"></a>驗證服務器

Schannel 的預設行為是使用 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)函數來驗證 [*伺服器憑證*](../secgloss/s-gly.md)的 [*完整性*](../secgloss/i-gly.md)和擁有權。 若要停用此功能， \_ 請 \_ \_ \_ 在呼叫 [**InitializeSecurityCoNtext (Schannel)**](./initializesecuritycontext--schannel.md) 函式時，指定 ISC 要求手動認證驗證。 如需詳細資訊，請參閱 [手動驗證 Schannel 認證](manually-validating-schannel-credentials.md)。

## <a name="authenticating-the-client"></a>驗證用戶端

Schannel 不會驗證用戶端的憑證;伺服器必須手動執行此驗證。 一般來說，伺服器會在包含使用者帳戶資訊的資料庫中檢查用戶端的身分識別。 對於需要使用憑證取得用戶端帳戶的伺服器，請參閱 [對應憑證](mapping-certificates.md)。

當伺服器要求用戶端驗證時，用戶端必須將其中一個憑證傳送至伺服器。 根據預設，安全通道不會通知用戶端，而是嘗試找出 [*用戶端憑證*](../secgloss/c-gly.md) ，並將它傳送至伺服器。 若要停用此功能，用戶端會 \_ \_ \_ \_ 在呼叫 [**InitializeSecurityCoNtext (Schannel)**](./initializesecuritycontext--schannel.md) 函式時，指定 ISC 需求使用提供的認證。 當指定這個旗標時， \_ \_ \_ 當伺服器要求驗證，且用戶端先前未提供憑證時，Schannel 會將每秒未完成的認證傳回給用戶端。

 

 
