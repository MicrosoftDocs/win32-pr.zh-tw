---
description: 多個提供者路由器 (MPR) 在連線或中斷連線網路資源時呼叫連線通知函式。 若要接收這類通知，您可以在 DLL 中執行這些函數。
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: 連接通知 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352d5cb09923a666e3fe1474e9fd2ebe033f05be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114941"
---
# <a name="connection-notification-api"></a>連接通知 API

[*多個提供者路由器*](/windows/desktop/SecGloss/m-gly) (MPR) 在連線或中斷連線網路資源時呼叫連線通知函式。 若要接收這類通知，您可以在 DLL 中執行這些函數。

MPR 會在嘗試每個新增連接作業之前和之後呼叫 [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) 函式 ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona)、 [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)或 [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) 。 當 MPR 自動還原網路連線時，不會呼叫此函數。

MPR 會在嘗試 ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)或 [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)) 的每個取消連接作業之前和之後呼叫 [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify)函數。

如需 WNet 函式的詳細資訊，請參閱 [Windows 網路](/windows/desktop/WNet/windows-networking-wnet-)功能。

如需有關如何建立及註冊接收網路連線通知的應用程式的詳細資訊，請參閱 [接收連接通知](receiving-connection-notifications.md) 和 [註冊以接收連線通知](registering-to-receive-connection-notifications.md)。

 

 
