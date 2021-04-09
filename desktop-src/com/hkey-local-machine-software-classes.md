---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: 與 HKEY \_ 本機電腦軟體類別機碼相關聯的子機碼與登錄值， \_ \\ \\ 包含支援 COM 功能所需之應用程式的相關資訊。
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c16fdbc97b32d01af9c96b5670cb5a19c09c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675599"
---
# <a name="hkey_local_machinesoftwareclasses"></a><span data-ttu-id="cd783-103">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別</span><span class="sxs-lookup"><span data-stu-id="cd783-103">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes</span></span>

<span data-ttu-id="cd783-104">與 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別機** 碼相關聯的子機碼與登錄值，包含支援 COM 功能所需之應用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cd783-104">The subkeys and registry values associated with the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key contain information about an application that is needed to support COM functionality.</span></span> <span data-ttu-id="cd783-105">此資訊包括支援的資料格式、相容性資訊、程式設計識別碼、DCOM 和控制項等主題。</span><span class="sxs-lookup"><span data-stu-id="cd783-105">This information includes such topics as supported data formats, compatibility information, programmatic identifiers, DCOM, and controls.</span></span>



| <span data-ttu-id="cd783-106">子機碼</span><span class="sxs-lookup"><span data-stu-id="cd783-106">Subkey</span></span>                                                                         | <span data-ttu-id="cd783-107">Description</span><span class="sxs-lookup"><span data-stu-id="cd783-107">Description</span></span>                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd783-108">**AppID**</span><span class="sxs-lookup"><span data-stu-id="cd783-108">**AppID**</span></span>](appid-key.md)                                                     | <span data-ttu-id="cd783-109">以 COM 為基礎之應用程式的設定選項。</span><span class="sxs-lookup"><span data-stu-id="cd783-109">Configuration options for COM-based applications.</span></span>                                                                 |
| [<span data-ttu-id="cd783-110">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="cd783-110">**CLSID**</span></span>](clsid-key-hklm.md)                                                | <span data-ttu-id="cd783-111">COM 類別的設定選項。</span><span class="sxs-lookup"><span data-stu-id="cd783-111">Configuration options for COM classes.</span></span>                                                                            |
| [<span data-ttu-id="cd783-112">**<\_ 副檔名>**</span><span class="sxs-lookup"><span data-stu-id="cd783-112">**<file\_extension>**</span></span>](-file-extension--key.md)                        | <span data-ttu-id="cd783-113">將副檔名與 ProgID 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="cd783-113">Associates a file name extension with a ProgID.</span></span>                                                                   |
| [<span data-ttu-id="cd783-114">**FileType**</span><span class="sxs-lookup"><span data-stu-id="cd783-114">**FileType**</span></span>](filetype-key.md)                                               | <span data-ttu-id="cd783-115">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)用來比對非複合檔案中各種檔案位元組的模式。</span><span class="sxs-lookup"><span data-stu-id="cd783-115">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span> |
| [<span data-ttu-id="cd783-116">**介面**</span><span class="sxs-lookup"><span data-stu-id="cd783-116">**Interface**</span></span>](interface-key.md)                                             | <span data-ttu-id="cd783-117">將介面名稱與介面識別碼 (IID) 相關聯。</span><span class="sxs-lookup"><span data-stu-id="cd783-117">Associates an interface name with an interface ID (IID).</span></span>                                                          |
| [**<ProgID>**](-progid--key.md)                                         | <span data-ttu-id="cd783-118">識別類別。</span><span class="sxs-lookup"><span data-stu-id="cd783-118">Identifies a class.</span></span> <span data-ttu-id="cd783-119">請注意，ProgID 不保證是全域唯一的，與 CLSID 不同。</span><span class="sxs-lookup"><span data-stu-id="cd783-119">Note that the ProgID is not guaranteed to be globally unique, unlike a CLSID.</span></span>                 |
| [<span data-ttu-id="cd783-120">**<與版本無關的 ProgID>**</span><span class="sxs-lookup"><span data-stu-id="cd783-120">**<version-independent ProgID>**</span></span>](-version-independent-progid--key.md) | <span data-ttu-id="cd783-121">用來判斷物件應用程式的最新版本。</span><span class="sxs-lookup"><span data-stu-id="cd783-121">Used to determine the latest version of an object application.</span></span>                                                    |



 

 

 




