---
description: 下列系統管理功能可讓網路提供者採取網路特定的動作，以顯示和操作網路特定目錄，換句話說，對應至非 Windows 通訊協定的目錄。
ms.assetid: df2f1bd6-5257-46e4-a4d4-ad2f5c0a1517
title: 系統管理功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83cb5b7c515fe8e22dc5542a4d29e54e8b01329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990379"
---
# <a name="administrative-functions"></a><span data-ttu-id="2f9c0-103">系統管理功能</span><span class="sxs-lookup"><span data-stu-id="2f9c0-103">Administrative Functions</span></span>

<span data-ttu-id="2f9c0-104">下列系統管理功能可讓網路提供者採取網路特定的動作，以顯示和操作網路特定目錄，換句話說，對應至非 Windows 通訊協定的目錄。</span><span class="sxs-lookup"><span data-stu-id="2f9c0-104">The following administrative functions enable a network provider to take network-specific action to display and manipulate network-specific directories, in other words, directories mapped to non-Windows protocols.</span></span>



| <span data-ttu-id="2f9c0-105">函式</span><span class="sxs-lookup"><span data-stu-id="2f9c0-105">Function</span></span>                                         | <span data-ttu-id="2f9c0-106">描述</span><span class="sxs-lookup"><span data-stu-id="2f9c0-106">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f9c0-107">**NPGetDirectoryType**</span><span class="sxs-lookup"><span data-stu-id="2f9c0-107">**NPGetDirectoryType**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) | <span data-ttu-id="2f9c0-108">由檔案管理員呼叫以判斷網路目錄的類型。</span><span class="sxs-lookup"><span data-stu-id="2f9c0-108">Called by File Manager to determine the type of a network directory.</span></span>                                                                                          |
| [<span data-ttu-id="2f9c0-109">**NPDirectoryNotify**</span><span class="sxs-lookup"><span data-stu-id="2f9c0-109">**NPDirectoryNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npdirectorynotify)   | <span data-ttu-id="2f9c0-110">由檔管理程式呼叫，以通知網路提供者目錄作業。</span><span class="sxs-lookup"><span data-stu-id="2f9c0-110">Called by File Manager to notify the network provider of directory operations.</span></span> <span data-ttu-id="2f9c0-111">您可以使用此函式來執行特定目錄的特殊行為。</span><span class="sxs-lookup"><span data-stu-id="2f9c0-111">This function can be used to perform special behavior for certain directories.</span></span> |



 

 

 



