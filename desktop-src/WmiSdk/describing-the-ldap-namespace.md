---
description: 從遠端連線到目前網域以外的 Active Directory server 時，您必須指定已屬於您所要 Active Directory 之網域成員的電腦名稱稱。
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: 描述 LDAP 命名空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027234"
---
# <a name="describing-the-ldap-namespace"></a><span data-ttu-id="b5211-103">描述 LDAP 命名空間</span><span class="sxs-lookup"><span data-stu-id="b5211-103">Describing the LDAP Namespace</span></span>

<span data-ttu-id="b5211-104">從遠端連線到目前網域以外的 Active Directory server 時，您必須指定已屬於您所要 Active Directory 之網域成員的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b5211-104">When connecting remotely to an Active Directory server other than the one in your current domain, you must specify the name of a computer that is already a member of the domain belonging to the Active Directory you want.</span></span>

<span data-ttu-id="b5211-105">若要從遠端連線到屬於 Active Directory 伺服器之網域成員的電腦，請輸入下列命令。</span><span class="sxs-lookup"><span data-stu-id="b5211-105">To remotely connect to a computer that is already a member of the domain belonging to the Active Directory server, type the following command.</span></span>

<span data-ttu-id="b5211-106">**\\\\RemoteComputer \\ 根目錄 \\ \\ LDAP**</span><span class="sxs-lookup"><span data-stu-id="b5211-106">**\\\\RemoteComputer\\root\\directory\\LDAP**</span></span>

<span data-ttu-id="b5211-107">此範例顯示組成完整命名空間名稱的兩個部分。</span><span class="sxs-lookup"><span data-stu-id="b5211-107">This example shows that there are two parts that make up a fully qualified namespace name.</span></span> <span data-ttu-id="b5211-108">第一個部分 (\\ \\ RemoteComputer) 代表已屬於您所需 Active Directory 伺服器之網域成員的電腦。</span><span class="sxs-lookup"><span data-stu-id="b5211-108">The first part (\\\\RemoteComputer) represents the computer that is already a member of the domain belonging to the Active Directory server you want.</span></span> <span data-ttu-id="b5211-109">第二個部分 \\ (\\ 根目錄 \\ LDAP) 代表目錄服務提供者中的 Active Directory 架構。</span><span class="sxs-lookup"><span data-stu-id="b5211-109">The second part (\\root\\directory\\LDAP) represents the Active Directory schema in the Directory Services Provider.</span></span>

> [!Note]  
> <span data-ttu-id="b5211-110">如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。</span><span class="sxs-lookup"><span data-stu-id="b5211-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



