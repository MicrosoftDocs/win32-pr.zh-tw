---
description: 本節說明 (VDS) 之虛擬磁碟服務的應用程式設計介面。
ms.assetid: d00fc772-331f-4d71-a418-e34acdfb6652
title: VDS 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369111add0b3f4b7e2742c764a6cbf8b1d8bfdd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979195"
---
# <a name="vds-reference"></a><span data-ttu-id="f595c-103">VDS 參考</span><span class="sxs-lookup"><span data-stu-id="f595c-103">VDS Reference</span></span>

<span data-ttu-id="f595c-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="f595c-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="f595c-105">本節說明 (VDS) 之虛擬磁碟服務的應用程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="f595c-105">This section describes the application programming interface to the Virtual Disk Service (VDS).</span></span>

<span data-ttu-id="f595c-106">應用程式開發人員會使用此 API 中的介面、結構、列舉和符號常數來查詢和設定儲存體（從磁片到存放裝置陣列）。</span><span class="sxs-lookup"><span data-stu-id="f595c-106">Application developers use the interfaces, structures, enumerations, and symbolic constants in this API to query and configure storage—from disks to storage arrays.</span></span> <span data-ttu-id="f595c-107">如需瞭解 VDS 型別之間的關聯性詳細資訊，請參閱 [Vds 物件模型](vds-object-model.md)。</span><span class="sxs-lookup"><span data-stu-id="f595c-107">For a detailed look at the relationship among VDS types, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="f595c-108">儲存體製造商會執行本節中定義的許多介面。</span><span class="sxs-lookup"><span data-stu-id="f595c-108">Storage manufacturers implement many of the interfaces defined in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f595c-109">本章節內容</span><span class="sxs-lookup"><span data-stu-id="f595c-109">In this Section</span></span>

<dl> <dt>

[<span data-ttu-id="f595c-110">VDS 常數</span><span class="sxs-lookup"><span data-stu-id="f595c-110">VDS Constants</span></span>](vds-constants.md)
</dt> <dd>

<span data-ttu-id="f595c-111">列出 VDS API 中的符號常數。</span><span class="sxs-lookup"><span data-stu-id="f595c-111">Lists the symbolic constants in the VDS API.</span></span>

</dd> <dt>

[<span data-ttu-id="f595c-112">VDS 資料類型</span><span class="sxs-lookup"><span data-stu-id="f595c-112">VDS Data Types</span></span>](vds-data-types.md)
</dt> <dd>

<span data-ttu-id="f595c-113">列出與 VDS 搭配使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="f595c-113">Lists the data types used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="f595c-114">VDS 列舉</span><span class="sxs-lookup"><span data-stu-id="f595c-114">VDS Enumerations</span></span>](vds-enumerations.md)
</dt> <dd>

<span data-ttu-id="f595c-115">描述與 VDS 搭配使用的列舉。</span><span class="sxs-lookup"><span data-stu-id="f595c-115">Describes the enumerations used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="f595c-116">VDS 介面</span><span class="sxs-lookup"><span data-stu-id="f595c-116">VDS Interfaces</span></span>](vds-interfaces.md)
</dt> <dd>

<span data-ttu-id="f595c-117">描述 VDS 介面及其公開的方法。</span><span class="sxs-lookup"><span data-stu-id="f595c-117">Describes VDS interfaces and the methods they expose.</span></span>

</dd> <dt>

[<span data-ttu-id="f595c-118">VDS 結構</span><span class="sxs-lookup"><span data-stu-id="f595c-118">VDS Structures</span></span>](vds-structures.md)
</dt> <dd>

<span data-ttu-id="f595c-119">描述以參數形式傳遞至 VDS 方法的結構。</span><span class="sxs-lookup"><span data-stu-id="f595c-119">Describes the structures passed as parameters to VDS methods.</span></span>

</dd> <dt>

[<span data-ttu-id="f595c-120">虛擬磁碟服務常見的傳回碼</span><span class="sxs-lookup"><span data-stu-id="f595c-120">Virtual Disk Service Common Return Codes</span></span>](virtual-disk-service-common-return-codes.md)
</dt> <dd>

<span data-ttu-id="f595c-121">描述 VDS 特定的最常見錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f595c-121">Describes the most common error codes that are specific to VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="f595c-122">虛擬磁碟服務詞彙</span><span class="sxs-lookup"><span data-stu-id="f595c-122">Virtual Disk Service Glossary</span></span>](virtual-disk-service-glossary-all.md)
</dt> <dd>

<span data-ttu-id="f595c-123">VDS 檔中所使用的技術術語詞彙。</span><span class="sxs-lookup"><span data-stu-id="f595c-123">Glossary of technical terms used in VDS documentation.</span></span>

</dd> </dl>

 

 
