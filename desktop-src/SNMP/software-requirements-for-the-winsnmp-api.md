---
title: WinSNMP API 的軟體需求
description: WinSNMP 應用程式必須透過動態連結程式庫 WSNMP32.DLL 來存取 WinSNMP API。
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182978"
---
# <a name="software-requirements-for-the-winsnmp-api"></a><span data-ttu-id="2e4e6-103">WinSNMP API 的軟體需求</span><span class="sxs-lookup"><span data-stu-id="2e4e6-103">Software Requirements for the WinSNMP API</span></span>

<span data-ttu-id="2e4e6-104">WinSNMP 應用程式必須透過動態連結程式庫 WSNMP32.DLL 來存取 WinSNMP API。</span><span class="sxs-lookup"><span data-stu-id="2e4e6-104">A WinSNMP application must access the WinSNMP API through the dynamic-link library WSNMP32.DLL.</span></span>

<span data-ttu-id="2e4e6-105">以下是支援 WinSNMP API 功能所需的檔案。</span><span class="sxs-lookup"><span data-stu-id="2e4e6-105">The following files are required to support the functionality of the WinSNMP API.</span></span>



| <span data-ttu-id="2e4e6-106">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="2e4e6-106">Filename</span></span>     | <span data-ttu-id="2e4e6-107">描述</span><span class="sxs-lookup"><span data-stu-id="2e4e6-107">Description</span></span>                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4e6-108">WSNMP32.DLL.自由</span><span class="sxs-lookup"><span data-stu-id="2e4e6-108">WSNMP32.LIB</span></span>  | <span data-ttu-id="2e4e6-109">WinSNMP 程式庫</span><span class="sxs-lookup"><span data-stu-id="2e4e6-109">WinSNMP Library</span></span>                                                                              |
| <span data-ttu-id="2e4e6-110">WSNMP32.DLL</span><span class="sxs-lookup"><span data-stu-id="2e4e6-110">WSNMP32.DLL</span></span>  | <span data-ttu-id="2e4e6-111">提供 WinSNMP 介面</span><span class="sxs-lookup"><span data-stu-id="2e4e6-111">Provides WinSNMP interface</span></span>                                                                   |
| <span data-ttu-id="2e4e6-112">WINSNMP.H</span><span class="sxs-lookup"><span data-stu-id="2e4e6-112">WINSNMP.H</span></span>    | <span data-ttu-id="2e4e6-113">WinSNMP 標頭檔</span><span class="sxs-lookup"><span data-stu-id="2e4e6-113">WinSNMP header file</span></span>                                                                          |
| <span data-ttu-id="2e4e6-114">SNMPTRAP.EXE</span><span class="sxs-lookup"><span data-stu-id="2e4e6-114">SNMPTRAP.EXE</span></span> | <span data-ttu-id="2e4e6-115">接收 SNMP 陷阱，並將其轉送至 MGMTAPI.DLL，也就是 Microsoft SNMP 管理員 API 程式庫</span><span class="sxs-lookup"><span data-stu-id="2e4e6-115">Receives SNMP traps and forwards them to MGMTAPI.DLL, the Microsoft SNMP Manager API library</span></span> |
| <span data-ttu-id="2e4e6-116">SNMPAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="2e4e6-116">SNMPAPI.DLL</span></span>  | <span data-ttu-id="2e4e6-117">提供 SNMP 公用程式</span><span class="sxs-lookup"><span data-stu-id="2e4e6-117">Provides SNMP utilities</span></span>                                                                      |



 

 

 




