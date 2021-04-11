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
# <a name="netexe"></a><span data-ttu-id="26e1f-103">Net.exe</span><span class="sxs-lookup"><span data-stu-id="26e1f-103">Net.exe</span></span>

<span data-ttu-id="26e1f-104">Net.exe 可以用來停止和啟動 IPv6 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="26e1f-104">Net.exe can be used to stop and start the IPv6 protocol.</span></span> <span data-ttu-id="26e1f-105">重新開機 IPv6 會重新初始化通訊協定，就像電腦重新開機一樣，這可能會變更介面編號。</span><span class="sxs-lookup"><span data-stu-id="26e1f-105">Restarting IPv6 reinitializes the protocol as if the computer were restarting, which may change interface numbers.</span></span> <span data-ttu-id="26e1f-106">Net.exe 有許多子命令。</span><span class="sxs-lookup"><span data-stu-id="26e1f-106">Net.exe has many subcommands.</span></span> <span data-ttu-id="26e1f-107">以下是與 IPv6 相關的命令：</span><span class="sxs-lookup"><span data-stu-id="26e1f-107">The following commands are relevant to IPv6:</span></span>

<dl> <dt>

<span data-ttu-id="26e1f-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop cpip6.sys**</span><span class="sxs-lookup"><span data-stu-id="26e1f-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="26e1f-109">停止 IPv6 通訊協定，並將它從記憶體卸載。</span><span class="sxs-lookup"><span data-stu-id="26e1f-109">Stops the IPv6 protocol and unloads it from memory.</span></span> <span data-ttu-id="26e1f-110">如果有任何 IPv6 通訊端開啟，此命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="26e1f-110">This command fails if any IPv6 sockets are open.</span></span>

</dd> <dt>

<span data-ttu-id="26e1f-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start cpip6.sys**</span><span class="sxs-lookup"><span data-stu-id="26e1f-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="26e1f-112">啟動 IPv6 通訊協定（如果已停止）。</span><span class="sxs-lookup"><span data-stu-id="26e1f-112">Starts the IPv6 protocol if it was stopped.</span></span> <span data-ttu-id="26e1f-113">如果% systemroot% System32 驅動程式目錄中有新的 Tcpip6.sys 驅動程式檔案 \\ \\ ，就會載入該驅動程式檔案。</span><span class="sxs-lookup"><span data-stu-id="26e1f-113">If a new Tcpip6.sys driver file is present in the %systemroot%\\System32\\Drivers directory, that driver file is loaded.</span></span>

</dd> </dl>

 

 



