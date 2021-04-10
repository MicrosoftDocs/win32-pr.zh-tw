---
title: WSAPROTOCOL_INFO 中的 Multipoint 屬性
description: WSAPROTOCOL 資訊結構中的 Multipoint 屬性 \_ 包括 XP1 \_ 支援 \_ multipoint、XP1 \_ MULTIPOINT \_ 控制 \_ 平面和 XP1 \_ MULTIPOINT \_ 資料 \_ 平面。
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baedcd07f53db462eb090217b53d93a1a4aa8c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690396"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a><span data-ttu-id="54ec2-103">WSAPROTOCOL_INFO 中的 Multipoint 屬性</span><span class="sxs-lookup"><span data-stu-id="54ec2-103">Multipoint attributes in WSAPROTOCOL_INFO</span></span>

<span data-ttu-id="54ec2-104">[**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中定義了三個屬性參數，以區分用於控制項和資料平面的不同配置：</span><span class="sxs-lookup"><span data-stu-id="54ec2-104">Three attribute parameters are defined in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure in order to distinguish the different schemes used in the control and data planes, respectively:</span></span>

-   <span data-ttu-id="54ec2-105">XP1 \_ 支援 \_ multipoint 值為1的 multipoint 表示此通訊協定專案支援 multipoint 通訊，且下列兩個參數有意義。</span><span class="sxs-lookup"><span data-stu-id="54ec2-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="54ec2-106">XP1 \_ MULTIPOINT \_ 控制 \_ 平面會指出控制平面的根目錄 (值 = 1) 或 nonrooted (值 = 0) 。</span><span class="sxs-lookup"><span data-stu-id="54ec2-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="54ec2-107">XP1 \_ MULTIPOINT \_ 資料 \_ 平面會指出資料平面是否為 root (value = 1) 或 nonrooted (value = 0) 。</span><span class="sxs-lookup"><span data-stu-id="54ec2-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="54ec2-108">如果 multipoint 通訊協定支援 root 和 nonrooted 資料平面（每個都有一個專案），則會出現兩個 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 專案。</span><span class="sxs-lookup"><span data-stu-id="54ec2-108">Two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

 

 
