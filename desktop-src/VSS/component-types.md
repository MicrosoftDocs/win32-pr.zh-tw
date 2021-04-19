---
description: 元件表示透過型別所代表的資料。
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: 元件類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994560"
---
# <a name="component-types"></a><span data-ttu-id="c5497-103">元件類型</span><span class="sxs-lookup"><span data-stu-id="c5497-103">Component Types</span></span>

<span data-ttu-id="c5497-104">元件表示透過型別所代表的資料。</span><span class="sxs-lookup"><span data-stu-id="c5497-104">Components indicate the sort of data they represent through a type.</span></span>

<span data-ttu-id="c5497-105">目前，元件類型 (請參閱 [**VSS \_ 元件 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) 僅限於下列各項：</span><span class="sxs-lookup"><span data-stu-id="c5497-105">Currently, component types (see [**VSS\_COMPONENT\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) are limited to the following:</span></span>

-   <span data-ttu-id="c5497-106">資料庫元件</span><span class="sxs-lookup"><span data-stu-id="c5497-106">Database components</span></span>
-   <span data-ttu-id="c5497-107">檔案群組</span><span class="sxs-lookup"><span data-stu-id="c5497-107">File groups</span></span>

<span data-ttu-id="c5497-108">如需設定元件類型的相關資訊，請參閱 [依寫入器的元件定義](definition-of-components-by-writers.md)。</span><span class="sxs-lookup"><span data-stu-id="c5497-108">For implementation information about setting component types, see [Definition of Components by Writers](definition-of-components-by-writers.md).</span></span>

<span data-ttu-id="c5497-109">寫入器具有指出其使用方式的資料類型 (請參閱 [**VSS \_ 來源 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)) ，其如下所示：</span><span class="sxs-lookup"><span data-stu-id="c5497-109">Writers have a data typing that indicates their usage (see [**VSS\_SOURCE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), which can be the following:</span></span>

-   <span data-ttu-id="c5497-110">交易式資料庫 (例如 SQL server) </span><span class="sxs-lookup"><span data-stu-id="c5497-110">A transactional database (such as an SQL server)</span></span>
-   <span data-ttu-id="c5497-111">非交易式資料庫 (例如試算表用戶端) </span><span class="sxs-lookup"><span data-stu-id="c5497-111">A nontransactional database (such as a spreadsheet client)</span></span>
-   <span data-ttu-id="c5497-112">檔案群組 (其他) </span><span class="sxs-lookup"><span data-stu-id="c5497-112">File group (other)</span></span>

<span data-ttu-id="c5497-113">將元件類型指定為資料庫，可讓您更輕鬆地識別其內容、允許個別處理記錄檔和資料檔案 (如需詳細) 資訊，請參閱 [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) 和 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) ，並藉由不允許遞迴檔案選取或使用 [*替代路徑*](vssgloss-a.md) 來強制較大的檔案選取， (請參閱 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) 和 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)) 。</span><span class="sxs-lookup"><span data-stu-id="c5497-113">Specifying a component type as database allows for easier identification of its content, allows for separate handling of log and data files (see [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) and [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) for details), and enforces greater rigor in file selection by not allowing either recursive file selection or using an [*alternate path*](vssgloss-a.md) (see [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) and [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span></span>

<span data-ttu-id="c5497-114">另一方面，檔案群組元件的價格不知道它所包含的資料，因為您可以使用遞迴規格和替代路徑，所以您可以更自由地處理檔案的插入方式。</span><span class="sxs-lookup"><span data-stu-id="c5497-114">With a file group component, on the other hand, at the price of not knowing what data it contains, you have greater freedom about how files are inserted, because you can use recursive specification and alternate paths.</span></span>

<span data-ttu-id="c5497-115">未來可能會加入其他元件類型。</span><span class="sxs-lookup"><span data-stu-id="c5497-115">Additional component types may be added in the future.</span></span>

 

 



