---
title: 週邊硬體指導方針
description: 如果其硬體裝置不是設計來透過遠端會話運作，廠商必須確保設備磁碟機軟體強制使用系統原則或群組原則來停用裝置的重新導向。
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372430"
---
# <a name="peripheral-hardware-guidelines"></a><span data-ttu-id="edbae-103">週邊硬體指導方針</span><span class="sxs-lookup"><span data-stu-id="edbae-103">Peripheral hardware guidelines</span></span>

<span data-ttu-id="edbae-104">在遠端桌面連線 (RDC) 用戶端上，遠端桌面工作階段主機 (RD 工作階段主機伺服器是本機電腦。</span><span class="sxs-lookup"><span data-stu-id="edbae-104">To a Remote Desktop Connection (RDC) client, the Remote Desktop Session Host (RD Session Host) server is the local computer.</span></span> <span data-ttu-id="edbae-105">因此，連接到伺服器的裝置（如磁片磁碟機和印表機）會顯示為用戶端的本機裝置。</span><span class="sxs-lookup"><span data-stu-id="edbae-105">Consequently, devices such as disk drives and printers attached to the server appear as local devices to a client.</span></span> <span data-ttu-id="edbae-106">相反地，連接至用戶端終端機的磁片磁碟機和印表機可能會顯示為遠端裝置，視針對連線選取的選項、使用的伺服器和使用的用戶端軟體版本而定。</span><span class="sxs-lookup"><span data-stu-id="edbae-106">In contrast, drives and printers attached to a client terminal can appear to be remote devices, depending on the options selected for the connection, the server used, and the version of the client software used.</span></span>

<span data-ttu-id="edbae-107">雖然初始版本的遠端桌面服務不支援將輸出直接傳送到連接至用戶端終端機的序列、平行和音效埠的應用程式，但目前的版本可讓這些裝置顯示為在遠端桌面服務會話中執行之應用程式的本機裝置。</span><span class="sxs-lookup"><span data-stu-id="edbae-107">While the initial release of Remote Desktop Services did not support applications that send output directly to serial, parallel, and sound ports attached to the client terminal, the current versions do allow these devices to appear as local devices to applications running in the Remote Desktop Services session.</span></span>

<span data-ttu-id="edbae-108">如果其硬體裝置不是設計來透過遠端會話運作，廠商必須確保設備磁碟機軟體強制使用系統原則或群組原則來停用裝置的重新導向。</span><span class="sxs-lookup"><span data-stu-id="edbae-108">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

 

 




