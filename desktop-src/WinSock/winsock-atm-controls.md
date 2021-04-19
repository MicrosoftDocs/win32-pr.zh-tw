---
description: 「Windows 通訊端2」規格原本就支援「ATM 點對點」和「點對點」連接設定和卸載。
ms.assetid: 07e4fcb8-f7b5-450d-a2f4-ba81267ef8ca
title: Winsock ATM 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3eb0fc798878066f6e3a4fa04af688eee28ea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971206"
---
# <a name="winsock-atm-controls"></a><span data-ttu-id="576cb-103">Winsock ATM 控制項</span><span class="sxs-lookup"><span data-stu-id="576cb-103">Winsock ATM Controls</span></span>

<span data-ttu-id="576cb-104">「Windows 通訊端2」規格原本就支援「ATM 點對點」和「點對點」連接設定和卸載。</span><span class="sxs-lookup"><span data-stu-id="576cb-104">ATM point-to-point and point-to-multipoint connection setup and teardown are natively supported by the Windows Sockets 2 specification.</span></span> <span data-ttu-id="576cb-105">事實上，Windows 通訊端 2 QoS 規格和通訊協定獨立的 multipoint/多播機制的設計，與其他通訊協定搭配使用。</span><span class="sxs-lookup"><span data-stu-id="576cb-105">In fact, Windows Sockets 2 QoS specification and protocol-independent multipoint/multicast mechanisms were designed with ATM in mind, along with other protocols.</span></span> <span data-ttu-id="576cb-106">請參閱 windows 通訊端 2 API 規格的第2.7 節和附錄 D，分別適用于 Windows 通訊端2、服務品質和 Multipoint 支援。</span><span class="sxs-lookup"><span data-stu-id="576cb-106">See Section 2.7 and Appendix D of the Windows Sockets 2 API specification for Windows Sockets 2, Quality of Service, and Multipoint Support, respectively.</span></span> <span data-ttu-id="576cb-107">因此，本檔中不需要引進任何 ATM 特定 Ioctls。</span><span class="sxs-lookup"><span data-stu-id="576cb-107">Therefore, no ATM-specific Ioctls need to be introduced in this document.</span></span>

 

 



