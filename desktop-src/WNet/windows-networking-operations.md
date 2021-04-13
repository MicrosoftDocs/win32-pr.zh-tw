---
title: Windows 網路作業
description: 應用程式可以使用 WNet 函式來流覽、新增或取消網路階層中任何位置的網路連接。
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315469"
---
# <a name="windows-networking-operations"></a>Windows 網路作業

應用程式可以使用 WNet 函式來流覽、新增或取消網路階層中任何位置的網路連接。

*持續* 連線是一種網路連線，系統會在使用者登入時自動還原該連接。 您可以呼叫 [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (或 [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) 和 [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) 函式，來控制網路連接是否會從某個會話持續到下一個會話。

若要尋找用來建立網路連線的預設使用者名稱或使用者名稱，請呼叫 [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) 函數。

除了呼叫 WNet 函式之外，處理常式也可以使用 mailslots 和具名管道來與另一個進程通訊。 如需詳細資訊，請參閱 [Mailslots](/windows/desktop/ipc/mailslots) 和 [管道](/windows/desktop/ipc/pipes)。

 

 