---
description: 元件物件模型 (COM) 是二進位標準，可在分散式運算環境中撰寫元件軟體。
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: 在 VSS 下備份和還原 COM + 類別註冊資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990469"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a><span data-ttu-id="d53c5-103">在 VSS 下備份和還原 COM + 類別註冊資料庫</span><span class="sxs-lookup"><span data-stu-id="d53c5-103">Backing Up and Restoring the COM+ Class Registration Database Under VSS</span></span>

<span data-ttu-id="d53c5-104">元件物件模型 (COM) 是二進位標準，可在分散式運算環境中撰寫元件軟體。</span><span class="sxs-lookup"><span data-stu-id="d53c5-104">The Component Object Model (COM) is a binary standard for writing component software in a distributed computing environment.</span></span>

<span data-ttu-id="d53c5-105">原始的 Win32 預存元件識別碼 (Guid) 以及登錄中 **HKEY \_ 類別 \_ 根目錄 \\ CLSID** 下的其他 COM 狀態。</span><span class="sxs-lookup"><span data-stu-id="d53c5-105">The original Win32 implementation stored component identifiers (GUIDs) and other COM state in the registry under **HKEY\_CLASSES\_ROOT\\CLSID**.</span></span>

<span data-ttu-id="d53c5-106">最新一代的元件物件模型（COM +）提供登錄獨立的資料庫來儲存元件註冊資訊： COM + 類別註冊資料庫。</span><span class="sxs-lookup"><span data-stu-id="d53c5-106">The current generation of the Component Object Model, COM+, offers a registry-independent database for storing component registration information: the COM+ Class Registration Database.</span></span>

<span data-ttu-id="d53c5-107">COM + 類別註冊資料庫支援 VSS 寫入器，可讓要求者使用儲存在陰影複製磁片區上的資料來備份註冊資料庫。</span><span class="sxs-lookup"><span data-stu-id="d53c5-107">The COM+ Class Registration Database supports a VSS writer, which allows requesters to back up the registration database using data stored on a shadow-copied volume.</span></span>

<span data-ttu-id="d53c5-108">若要還原 COM + 註冊資料庫，要求者必須呼叫 [ICOMAdminCatalog：： RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) 方法。</span><span class="sxs-lookup"><span data-stu-id="d53c5-108">To restore the COM+ Registration Database, a requester must call the [ICOMAdminCatalog::RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="d53c5-109">如需 COM + 註冊資料庫寫入器的詳細資訊，請參閱 [內建的 VSS 寫入](in-box-vss-writers.md)器。</span><span class="sxs-lookup"><span data-stu-id="d53c5-109">For more information about the COM+ Registration Database writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
