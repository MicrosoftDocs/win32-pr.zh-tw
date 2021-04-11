---
description: Net.exe 可以用來停止和啟動 IPv6 通訊協定。
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848008"
---
# <a name="netexe"></a>Net.exe

Net.exe 可以用來停止和啟動 IPv6 通訊協定。 重新開機 IPv6 會重新初始化通訊協定，就像電腦重新開機一樣，這可能會變更介面編號。 Net.exe 有許多子命令。 以下是與 IPv6 相關的命令：

<dl> <dt>

<span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop cpip6.sys**
</dt> <dd>

停止 IPv6 通訊協定，並將它從記憶體卸載。 如果有任何 IPv6 通訊端開啟，此命令會失敗。

</dd> <dt>

<span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start cpip6.sys**
</dt> <dd>

啟動 IPv6 通訊協定（如果已停止）。 如果% systemroot% System32 驅動程式目錄中有新的 Tcpip6.sys 驅動程式檔案 \\ \\ ，就會載入該驅動程式檔案。

</dd> </dl>

 

 



