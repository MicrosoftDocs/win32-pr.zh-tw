---
description: 描述在 Windows 下進行網路 i/o 作業的進程。
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: 網路 i/o 操作的描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319296"
---
# <a name="description-of-a-network-io-operation"></a>網路 i/o 操作的描述

下圖說明 Windows 上的網路 i/o 作業的處理常式。

![windows 下的網路 i/o 操作](images/fig4.png)

當應用程式呼叫檔案 i/o 函數來存取遠端電腦上的檔案時，會發生下列事件：

-   本機電腦上的 [網路](network-redirectors.md)重新導向器（也稱為重新導向程式）會攔截 i/o 要求。 在上圖中，這是由應用程式和用戶端重新導向器之間的實心箭號所描述。
-   重新導向器會建立包含所有要求資訊的資料封包，並將其傳送至檔案所在的伺服器。 在上圖中，這是由用戶端重新導向器和伺服器重新導向器之間的實心箭號所描述。
-   伺服器上的重新導向器會接收來自用戶端的封包、驗證 i/o 要求所需之檔案的存取權，而且如果經過驗證，則會代表用戶端執行要求。 如果沒有，則會將錯誤碼傳回至用戶端上的重新導向器。 在上圖中，是由伺服器重新導向程式和檔案之間的彎曲實心箭號所描述。
-   當要求執行時，伺服器上的重新導向器會將 i/o 要求所產生的任何資料，連同成功通知傳送至用戶端上的重新導向器。 在上圖中，這是由伺服器和用戶端重新導向器之間的點箭號所描述。
-   用戶端上的重新導向器會接收來自伺服器的封包，並將封包中的資料連同成功通知傳遞給應用程式。 在上圖中，這是由用戶端重新導向器和應用程式之間的虛線箭號所描述。

Windows 可以使用各種網路通訊協定來執行網路 i/o 操作，包括 [MICROSOFT SMB 通訊協定和 CIFS 通訊協定總覽](microsoft-smb-protocol-and-cifs-protocol-overview.md) 和 NFS。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                       | 描述                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [本機和網路 i/o 的差異](differences-in-local-and-network-i-o.md)<br/> | Windows 上的本機 i/o 和網路 i/o 之間的差異。<br/> |
| [網路重定向器](network-redirectors.md)<br/>                                   | 描述網路重新導向程式的功能。<br/>      |



 

 

 




