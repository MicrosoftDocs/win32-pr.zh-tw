---
title: 尋找應用程式目錄分割主機伺服器
description: 本主題說明如何尋找應用程式目錄分割主機伺服器。
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- 尋找應用程式目錄分割主機伺服器 AD
- 應用程式目錄分割 AD，尋找主機伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3cef9442d694b80893f67d5530b83aa188df4d172028271117492ed221bd239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186789"
---
# <a name="locating-an-application-directory-partition-host-server"></a>尋找應用程式目錄分割主機伺服器

NetLogon 服務會註冊應用程式目錄分割的下列 SRV 記錄清單：

-   \_ldap。 \_Tcp。<partition name>
-   \_ldap。 \_tcp ... <site name> \_網站。<partition name>

若要找出裝載指定的應用程式目錄分割複本的網域控制站，請呼叫具有 DomainName 參數的 [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)函式，並將 *DomainName* 參數設定為應用程式目錄分割的 DNS 名稱，以及在 *旗標* 參數中設定 **\_ 僅限 DS \_ LDAP \_ 所需** 的旗標。 如需詳細資訊和示範的程式碼範例，使用 **DsGetDcName** 函式，如何找出裝載應用程式目錄分割複本的網域控制站，請參閱 [尋找應用程式目錄分割主機伺服器的範例程式碼](example-code-for-locating-an-application-directory-partition-host-server.md)。

 

 




